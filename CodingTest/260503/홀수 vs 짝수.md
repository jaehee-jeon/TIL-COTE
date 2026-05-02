# 260503

## - 홀수 vs 짝수
### ❌ TRY 1
```python
def solution(num_list):
    answer = 0
    
    #첫번째 시도
   a += range(0,len(num_list),2)
   b += range(1,len(num_list),2)

    if a > b :
        answer = a
    elif a < b :
        answer = b
    else :
        answer = a
    
    return answer
```
- 오류 :
    - NameError: name 'a' is not defined
        - a를 변수 선언안함..
        - 사용하기 전에 변수 선언*
    - range는 인덱스일뿐..
        - a += range(0,len(num_list),2) 
        - 결과 : 0,2,4
    - += VS sum
        - += 숫자를 더할 때
        - sum 리스트를 합칠 때

### ❌ TRY 2
```python
def solution(num_list):
    answer = 0
    
    a += [i for i in num_list if i%2==0]
    b += [i for i in num_list if i%2!=0]
    if a > b :
        answer = a
    elif a < b :
        answer = b
    else :
        answer = a
    
    return answer
```
- 오류 :
    - [i for i in num_list if i%2!=0]
        - 위치가 홀수 인 경우를 찾아야하는데 상기처럼 하면 값이 홀수 인 경우를 찾게 됨

### ✅ ANSWER
```python
def solution(num_list):
    odd_sum = sum(num_list[0::2])
    even_sum = sum(num_list[1::2])
    
    return max(odd_sum, even_sum)
```
- 배운 점:
    - 슬라이싱
    - sum과 max



## 🏠 블로그에 정리 필요
- 슬라이싱 vs range
