# range

## 📌 range란?

`range()`는 **숫자 범위를 만들어주는 파이썬의 내장 함수**야. 주로 `for` 반복문과 함께 쓰여서, **특정 횟수만큼 반복**할 때 아주 자주 사용돼.

⚠️ **주의:** `range()` 함수는 반드시 **정수형(int)** 값만 받아! 실수(float), 문자열(str), 리스트 같은 타입은 사용할 수 없어.

### ✅ 기본 형식

```python
range(stop)             # 0부터 stop-1까지
range(start, stop)      # start부터 stop-1까지
range(start, stop, step) # start부터 stop-1까지 step씩 증가

```

### 🔍 예시

```python
range(5)         → 0, 1, 2, 3, 4
range(2, 6)      → 2, 3, 4, 5
range(1, 10, 2)  → 1, 3, 5, 7, 9

```

---

## 💡 실전 예제: 구구단 전체 출력 (2단부터 9단까지)

```python
# 구구단 전체 출력(2단부터 9단까지)

for dan in range(2, 10):         # 바깥쪽 반복문 (2단 ~ 9단)
  print(f"🙃 {dan}단")           # 단 제목 출력
  for i in range(1, 10):         # 안쪽 반복문 (1 ~ 9)
    print(f" {dan}x{i}={dan*i}") # 실제 곱셈 결과 출력
  print()                        # 단 구분용 공백 출력

```

---

### 🧠 코드 설명 (라인별)

| 코드 | 설명 |
| --- | --- |
| `for dan in range(2, 10):` | 바깥 반복문: **2단부터 9단까지 반복**. `range(2,10)`은 `2 ~ 9`까지만 포함됨! |
| `print(f"🙃 {dan}단")` | 각 단의 제목 출력. 예: "🙃 2단" |
| `for i in range(1, 10):` | 안쪽 반복문: **1~9까지 곱하기 위해 반복** |
| `print(f" {dan}x{i}={dan*i}")` | 실제 구구단 결과 출력. 예: `2x1=2` |
| `print()` | 각 단 사이에 한 줄 띄우기 (가독성 좋게!) |

---

## ✨ 실무 활용 예시

| 사용처 | 설명 |
| --- | --- |
| 반복 출력 | 리스트, 메뉴, 데이터 목록 등 반복 표시 |
| 웹 개발 | 동적 테이블/페이지 네비게이션 생성 |
| 자동화 | 보고서, 통계 등 숫자 기반 반복 작업 |

---

## 🎯 실전 팁

- `range(start, stop)`의 **stop은 포함되지 않는다** (주의!)
- 이중 `for`문은 **바깥 → 안쪽** 순서로 실행됨
- `print()`만 써도 줄바꿈 돼. 줄 사이 간격 줄 때 유용함

---