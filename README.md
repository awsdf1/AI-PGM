# AI-PGM
# Python 리스트(List) 완벽 정리

## 1. 리스트(List)란?

리스트(List)는 여러 개의 데이터를 하나의 변수에 저장하는 자료형입니다.

```python
numbers = [10, 20, 30, 40, 50]
```

- 여러 개의 데이터를 순서대로 저장
- 수정 가능(Mutable)
- 중복 데이터 저장 가능
- 다양한 자료형 저장 가능

```python
data = [10, "Python", 3.14, True]
```

---

# 2. 리스트 생성

## 빈 리스트 생성

```python
list1 = []
list2 = list()
```

## 데이터가 있는 리스트 생성

```python
fruits = ["apple", "banana", "orange"]
numbers = [1, 2, 3, 4, 5]
```

---

# 3. 리스트 출력

```python
fruits = ["apple", "banana", "orange"]

print(fruits)
```

출력

```
['apple', 'banana', 'orange']
```

---

# 4. 인덱스(Index)

리스트는 0부터 시작합니다.

```python
fruits = ["apple", "banana", "orange"]

print(fruits[0])
print(fruits[1])
print(fruits[2])
```

출력

```
apple
banana
orange
```

### 음수 인덱스

```python
print(fruits[-1])
```

출력

```
orange
```

---

# 5. 리스트 길이

```python
numbers = [1,2,3,4,5]

print(len(numbers))
```

출력

```
5
```

---

# 6. 요소 추가

## append()

맨 뒤에 추가

```python
numbers = [1,2,3]

numbers.append(4)

print(numbers)
```

출력

```
[1,2,3,4]
```

---

## insert()

원하는 위치에 추가

```python
numbers = [1,2,4]

numbers.insert(2,3)

print(numbers)
```

출력

```
[1,2,3,4]
```

---

# 7. 요소 삭제

## remove()

값으로 삭제

```python
numbers = [10,20,30,40]

numbers.remove(20)

print(numbers)
```

출력

```
[10,30,40]
```

---

## pop()

인덱스로 삭제

```python
numbers = [10,20,30]

numbers.pop(1)

print(numbers)
```

출력

```
[10,30]
```

---

## del

```python
numbers = [10,20,30]

del numbers[0]

print(numbers)
```

출력

```
[20,30]
```

---

# 8. 리스트 수정

```python
numbers = [10,20,30]

numbers[1] = 200

print(numbers)
```

출력

```
[10,200,30]
```

---

# 9. 리스트 반복문

## for문 사용

```python
fruits = ["apple","banana","orange"]

for fruit in fruits:
    print(fruit)
```

출력

```
apple
banana
orange
```

---

## 인덱스 사용

```python
for i in range(len(fruits)):
    print(i, fruits[i])
```

출력

```
0 apple
1 banana
2 orange
```

---

# 10. 리스트 슬라이싱

```python
numbers = [10,20,30,40,50]

print(numbers[1:4])
```

출력

```
[20,30,40]
```

---

```python
print(numbers[:3])
```

출력

```
[10,20,30]
```

---

```python
print(numbers[2:])
```

출력

```
[30,40,50]
```

---

# 11. 리스트 연결

```python
a = [1,2,3]
b = [4,5,6]

print(a+b)
```

출력

```
[1,2,3,4,5,6]
```

---

# 12. 리스트 반복

```python
print([1,2]*3)
```

출력

```
[1,2,1,2,1,2]
```

---

# 13. 포함 여부 확인

```python
fruits = ["apple","banana","orange"]

print("apple" in fruits)
print("grape" in fruits)
```

출력

```
True
False
```

---

# 14. 자주 사용하는 함수

## sum()

```python
numbers = [10,20,30]

print(sum(numbers))
```

출력

```
60
```

---

## max()

```python
numbers = [10,20,30]

print(max(numbers))
```

출력

```
30
```

---

## min()

```python
numbers = [10,20,30]

print(min(numbers))
```

출력

```
10
```

---

## sorted()

```python
numbers = [5,3,1,4,2]

print(sorted(numbers))
```

출력

```
[1,2,3,4,5]
```

---

## reverse()

```python
numbers = [1,2,3]

numbers.reverse()

print(numbers)
```

출력

```
[3,2,1]
```

---

## sort()

```python
numbers = [5,2,4,1,3]

numbers.sort()

print(numbers)
```

출력

```
[1,2,3,4,5]
```

---

# 15. 리스트 컴프리헨션(List Comprehension)

기존 반복문

```python
numbers = []

for i in range(5):
    numbers.append(i)

print(numbers)
```

리스트 컴프리헨션

```python
numbers = [i for i in range(5)]

print(numbers)
```

출력

```
[0,1,2,3,4]
```

---

# 16. 실습 예제 1

5개의 정수를 입력받아 리스트에 저장

```python
numbers = []

for i in range(5):
    num = int(input(f"{i+1}번째 숫자 입력: "))
    numbers.append(num)

print(numbers)
print("합:", sum(numbers))
print("평균:", sum(numbers)/len(numbers))
print("최댓값:", max(numbers))
print("최솟값:", min(numbers))
```

---

# 17. 실습 예제 2

짝수만 저장하기

```python
numbers = []

for i in range(10):
    if i % 2 == 0:
        numbers.append(i)

print(numbers)
```

출력

```
[0,2,4,6,8]
```

---

# 18. 실습 예제 3

리스트 뒤집기

```python
numbers = [1,2,3,4,5]

numbers.reverse()

print(numbers)
```

---

# 19. 자주 발생하는 오류

## IndexError

```python
numbers = [1,2,3]

print(numbers[5])
```

오류 이유

```
리스트 범위를 벗어남
```

---

## remove() 오류

```python
numbers = [1,2,3]

numbers.remove(10)
```

오류 이유

```
리스트에 없는 값을 삭제하려고 함
```

---

# 20. 핵심 정리

| 함수 | 설명 |
|------|------|
| append() | 맨 뒤 추가 |
| insert() | 원하는 위치 추가 |
| remove() | 값 삭제 |
| pop() | 인덱스로 삭제 |
| del | 삭제 |
| len() | 길이 |
| sum() | 합 |
| max() | 최대값 |
| min() | 최소값 |
| sort() | 오름차순 정렬 |
| reverse() | 순서 뒤집기 |
| sorted() | 정렬된 새 리스트 반환 |

---

# 연습 문제

### 문제 1

1부터 10까지 리스트를 만드세요.

---

### 문제 2

사용자로부터 5개의 숫자를 입력받아 평균을 출력하세요.

---

### 문제 3

리스트에서 가장 큰 값과 가장 작은 값을 출력하세요.

---

### 문제 4

리스트를 내림차순으로 정렬하세요.

---

### 문제 5

리스트의 모든 값을 한 줄씩 출력하세요.

---

## 학습 목표

이 문서를 학습하면 다음 내용을 익힐 수 있습니다.

- 리스트 생성
- 요소 접근
- 요소 추가/삭제
- 반복문과 리스트
- 슬라이싱
- 정렬
- 내장 함수 활용
- 리스트 컴프리헨션
- 실전 문제 풀이
