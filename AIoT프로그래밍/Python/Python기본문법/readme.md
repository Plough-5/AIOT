# 🐍 파이썬 기본 문법 정리

파이썬은 간결하고 읽기 쉬운 문법을 가진 인기 많은 프로그래밍 언어예요!  
AI, IoT, 웹 개발, 데이터 분석까지 다양한 분야에서 사용된답니다. 💡

---

## ✨ 1. 변수와 자료형

```python
name = "뀨"
age = 20
height = 160.5
is_cute = True

## ✨ 2. 출력과 입력

print("안녕, 뀨!")           # 출력
name = input("이름을 입력하세요: ")  # 입력

✨ 3. 조건문 if

age = 18
if age >= 18:
    print("성인이에요!")
else:
    print("아직 미성년자예요!")

✨ 4. 반복문 for / while

# for 문
for i in range(5):
    print(i)

# while 문
count = 0
while count < 5:
    print(count)
    count += 1

✨ 5. 함수 정의

def say_hello(name):
    print("안녕, " + name + "!")

say_hello("뀨")

✨ 6. 리스트와 딕셔너리

# 리스트
fruits = ["사과", "바나나", "딸기"]
print(fruits[0])  # 사과

# 딕셔너리
person = {"name": "뀨", "age": 20}
print(person["name"])  # 뀨

✨ 7. 예외 처리 try-except

try:
    num = int(input("숫자를 입력하세요: "))
    print(10 / num)
except ZeroDivisionError:
    print("0으로 나눌 수 없어요!")
except ValueError:
    print("숫자가 아니에요!")

