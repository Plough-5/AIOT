# 🐼 Pandas 기본 문법 정리 (뀨를 위한 데이터 분석 입문서)

Pandas는 **표(데이터프레임)** 형태로 데이터를 다루는 파이썬 라이브러리예요.  
엑셀처럼 행과 열을 자유자재로 조작할 수 있어서 데이터 분석에 최고~! 📈💕

---

## 📦 1. 설치 및 불러오기

```bash
pip install pandas

📝 2. 데이터프레임 만들기

data = {
    "이름": ["뀨", "철수", "영희"],
    "나이": [20, 25, 22],
    "키": [160, 175, 158]
}

df = pd.DataFrame(data)
print(df)

📂 3. CSV 파일 불러오기 & 저장하기

# CSV 불러오기
df = pd.read_csv("data.csv")

# CSV로 저장하기
df.to_csv("new_data.csv", index=False)

🔍 4. 데이터 확인하기

df.head()       # 처음 5행
df.tail()       # 마지막 5행
df.shape        # (행 수, 열 수)
df.info()       # 데이터 구조 정보
df.describe()   # 숫자형 통계 요약

🎯 5. 열과 행 다루기

# 열 선택
df["이름"]
df[["이름", "나이"]]

# 행 선택 - 위치 기반
df.iloc[0]       # 첫 번째 행
df.iloc[1:3]     # 두 번째~세 번째 행

# 행 선택 - 조건 기반
df[df["나이"] > 21]

✏️ 6. 열 추가 & 수정

# 새 열 추가
df["몸무게"] = [50, 70, 45]

# 기존 열 수정
df["나이"] = df["나이"] + 1

❌ 7. 결측치 처리

df.isnull()             # 결측치 있는지 확인
df.dropna()             # 결측치 있는 행 삭제
df.fillna(0)            # 결측치 0으로 채우기

🔃 8. 그룹화 (groupby)

df.groupby("이름")["나이"].mean()  # 이름별 평균 나이

🔄 9. 정렬 (sort)

df.sort_values("나이")                     # 나이 오름차순
df.sort_values("나이", ascending=False)   # 나이 내림차순

📌 10. 요약 표

| 함수명           | 설명            |
| ------------- | ------------- |
| `df.head()`   | 상위 5행 출력      |
| `df.tail()`   | 하위 5행 출력      |
| `df.shape`    | (행 수, 열 수) 반환 |
| `df.info()`   | 데이터 요약 정보     |
| `df["열명"]`    | 열 선택          |
| `df.iloc[]`   | 위치 기반 행 선택    |
| `df.drop()`   | 행 또는 열 삭제     |
| `df.fillna()` | 결측치 채우기       |




