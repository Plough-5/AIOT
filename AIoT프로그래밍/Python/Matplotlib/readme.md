# 📊 Matplotlib 기본 문법 정리 (뀨의 그래프 그리기)

**Matplotlib**은 파이썬에서 가장 유명한 시각화 라이브러리예요.  
데이터를 시각적으로 표현할 수 있게 도와주며, 다양한 형태의 그래프를 그릴 수 있어요! 🎨

---

## 📦 1. 설치와 불러오기

```bash
pip install matplotlib

📝 2. 간단한 선 그래프 그리기

import matplotlib.pyplot as plt

# 데이터 준비
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# 선 그래프 그리기
plt.plot(x, y)
plt.show()  # 그래프 표시

📉 3. 그래프 제목과 레이블 추가하기
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.title("간단한 선 그래프")  # 제목 추가
plt.xlabel("X 축")           # X 축 레이블 추가
plt.ylabel("Y 축")           # Y 축 레이블 추가
plt.show()

🛑 4. 여러 그래프 겹쳐 그리기

x = [1, 2, 3, 4, 5]
y1 = [2, 4, 6, 8, 10]
y2 = [1, 3, 5, 7, 9]

plt.plot(x, y1, label="선형 그래프 1")  # 첫 번째 선 그래프
plt.plot(x, y2, label="선형 그래프 2")  # 두 번째 선 그래프
plt.legend()  # 범례 추가
plt.show()

🔵 5. 산점도(Scatter plot) 그리기

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.scatter(x, y)
plt.title("산점도 그래프")
plt.xlabel("X 값")
plt.ylabel("Y 값")
plt.show()

📊 6. 막대 그래프 (Bar graph) 그리기

categories = ["A", "B", "C", "D"]
values = [10, 20, 30, 40]

plt.bar(categories, values)
plt.title("막대 그래프")
plt.xlabel("카테고리")
plt.ylabel("값")
plt.show()

🛠️ 7. 히스토그램 (Histogram) 그리기

import numpy as np

data = np.random.randn(1000)  # 정규 분포를 따르는 난수 생성

plt.hist(data, bins=30)  # bins는 히스토그램의 구간 수
plt.title("히스토그램")
plt.xlabel("값")
plt.ylabel("빈도수")
plt.show()

🔴 8. 원 그래프 (Pie chart) 그리기

labels = ["A", "B", "C", "D"]
sizes = [15, 30, 45, 10]

plt.pie(sizes, labels=labels, autopct="%1.1f%%")  # 비율 표시
plt.title("원 그래프")
plt.show()

🎨 9. 색상, 스타일, 마커 변경하기

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# 스타일, 색상, 마커 지정
plt.plot(x, y, color='red', linestyle='--', marker='o', markersize=10)
plt.title("스타일, 색상, 마커 적용")
plt.show()

🔢 10. 서브플롯 (Subplots) 만들기

x = [1, 2, 3, 4, 5]
y1 = [2, 4, 6, 8, 10]
y2 = [1, 3, 5, 7, 9]

# 1행 2열의 서브플롯
plt.subplot(1, 2, 1)
plt.plot(x, y1)
plt.title("서브플롯 1")

plt.subplot(1, 2, 2)
plt.plot(x, y2)
plt.title("서브플롯 2")

plt.show()
