# 🧪 NumPy 기본 문법 정리 (뀨의 배열 탐험기)

NumPy는 **수치 계산과 배열 처리에 특화된 파이썬 라이브러리**예요!  
배열을 빠르게 계산하고, 행렬 연산까지 뚝딱 해낼 수 있어요~ 💨

---

## 📦 1. 설치와 불러오기

```bash
pip install numpy

🔢 2. 배열 만들기

# 리스트를 배열로
a = np.array([1, 2, 3])
print(a)

# 2차원 배열
b = np.array([[1, 2], [3, 4]])

📐 3. 배열 속성 확인

a.shape      # 배열 형태 (튜플)
a.ndim       # 차원 수
a.dtype      # 데이터 타입
a.size       # 전체 원소 개수
a.itemsize   # 원소 하나의 크기 (bytes)

🧮 4. 배열 생성 함수들

np.zeros((2, 3))       # 0으로 채운 배열
np.ones((3, 3))        # 1로 채운 배열
np.eye(3)              # 단위 행렬
np.arange(0, 10, 2)    # 0부터 10까지 2 간격
np.linspace(0, 1, 5)   # 0부터 1까지 5개 균등 분할

🔁 5. 배열 연산

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

a + b       # [5 7 9]
a * b       # [4 10 18]
a ** 2      # [1 4 9]
np.sqrt(a)  # 제곱근

🔍 6. 인덱싱 & 슬라이싱

a = np.array([10, 20, 30, 40])
a[0]        # 10
a[1:3]      # [20 30]

b = np.array([[1, 2], [3, 4]])
b[0, 1]     # 2
b[:, 0]     # 첫 번째 열

🔄 7. 배열 형태 변경

a = np.arange(6)        # [0 1 2 3 4 5]
a.reshape(2, 3)         # 2행 3열로
a.flatten()             # 1차원으로 펼치기

🎲 8. 난수 생성

np.random.rand(2, 3)     # 0~1 사이 난수 (2x3)
np.random.randint(1, 10) # 1~9 사이 정수 하나

✂️ 9. 배열 결합 & 분할

a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6]])

np.vstack([a, b])        # 수직 결합
np.hstack([a, a])        # 수평 결합

np.split(a, 2, axis=0)   # 행 방향 분할

🧠 10. 유용한 함수들

np.mean(a)     # 평균
np.sum(a)      # 합계
np.max(a)      # 최댓값
np.min(a)      # 최솟값
np.argmax(a)   # 최댓값 인덱스
np.unique(a)   # 중복 제거한 유일 값



