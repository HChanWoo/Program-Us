# [PCCP] 외톨이 알파벳 - 121683

[문제 링크](https://school.programmers.co.kr/learn/courses/15008/lessons/121683) 

### 푼 사람
[황찬우 풀이]
```python
def solution(input_string):
    answer = ''
    dict_string = {}
    pre = 'A'

    # 붙어있지 않은 알파벳 수를 구함
    for ele in input_string :
        if ele != pre:
            if ele in dict_string :
                dict_string[ele]+=1
            else : 
                dict_string[ele]=1
        pre = ele

    for key,val in dict_string.items() :
        if val >= 2 :
            answer+=key

    if len(answer) == 0 :
        return 'N'

    answer = ''.join(sorted(answer))

    return answer
```
