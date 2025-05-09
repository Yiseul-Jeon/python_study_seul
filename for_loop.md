# [파이썬] for문과 continue 키워드 실습 정리

---

## 1. 코드 전체

```python
# 변수를 선언합니다.
numbers = [5, 15, 6, 20, 7, 25]

for number in numbers:
    if number < 10:
        continue
    print(number, end=" ")

```

---

## 2. 코드 설명

| 줄 번호 | 코드 | 설명 |
| --- | --- | --- |
| 1 | `# 변수를 선언합니다.` | 실행되지 않는 주석. 코드 설명 용도 |
| 2 | `numbers = [5, 15, 6, 20, 7, 25]` | 리스트 자료형 변수 선언. 총 6개의 숫자가 담겨 있음 |
| 4 | `for number in numbers:` | 리스트 요소를 하나씩 반복하며 꺼냄 |
| 5 | `if number < 10:` | `number`가 10보다 작으면… 조건문 |
| 6 | `continue` | 조건을 만족하면 이번 반복은 건너뜀 |
| 7 | `print(number, end=" ")` | 조건을 통과한 값만 출력. 줄바꿈 대신 한 칸 공백으로 출력 |

---

## 3. 실행 결과

```
15 20 25

```

※ 10보다 작은 5, 6, 7은 출력에서 제외됨

---

## 4. `:` 콜론의 의미

파이썬에서 `:`는 **블록 구조(들여쓰기)**의 시작을 알려주는 문법적 약속이다.

`for`, `if`, `while`, `def` 등에서 반드시 필요하다.

```python
if number < 10:   # ← 여기서 콜론 꼭 필요!
    continue

```

없으면 **SyntaxError** 발생!

---

## 5. 실무 활용 예시

| 상황 | 예시 코드 | 설명 |
| --- | --- | --- |
| 숫자 필터링 | `if num < 10: continue` | 조건을 만족하지 않으면 무시 |
| 나이 필터링 | `if age < 20: continue` | 미성년자 제외 |
| 결측값 무시 | `if not value: continue` | 빈 값 건너뜀 |

---

## 6. `continue` vs `break` 차이

| 키워드 | 의미 | 반복문 동작 |
| --- | --- | --- |
| `continue` | 이번 반복만 건너뜀 | 다음 반복 계속함 |
| `break` | 반복문 종료 | 반복 자체를 끝냄 |