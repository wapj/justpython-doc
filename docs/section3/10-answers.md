# 섹션3 퀴즈 답안
## 문제 3-1

[조건문에 대해서 알아봅시다](./1-condition.md#퀴즈-혼자서-해보기) 에서 나왔던 퀴즈(`점수를 넣으면 학점으로 변경하는 함수를 만드시오.`)의 답안입니다.

```python

def get_score(score):
    if score >= 95:
        print('A+')
    elif score >= 90:
        print('A')
    elif score >= 85:
        print('B+')
    elif score >= 80:
        print('B')
    elif score >= 75:
        print('C+')
    elif score >= 70:
        print('C')
    elif score >= 65:
        print('D+')
    elif score >= 60:
        print('D')
    else:
        print('F')

scores = range(100)
for score in reversed(scores):
    print("score : ", score, end= "  ")
    get_score(score)
```
