---
sidebar_position: 4
---

# 논리 연산자

논리연산자는 논리식을 판단하는 연산자이며, 결과값으로 참(True) 또는 거짓(False)이 됩니다. 논리연산자는 and, or, not 3가지가 있습니다.

## and, or, not

**and 연산자**는 `A and B` 처럼 사용할 수 있습니다. 이 때 A,B 모두가 참(True)이라면 `A and B`의 결과도 참(True)입니다.

**or 연산자**는 and와 마찬가지로 `A or B` 와 같이 사용하며 A나 B중 하나만 참이면 결과값도 참입니다.

**not 연산자**는 값이 하나만 있으면 됩니다. `not A` 와 같은 방식으로 사용할 수 있습니다. 참일 경우 거짓을, 거짓인 경우 참을 결과값으로 주게 됩니다.

아래는 연산자의 동작의 결과를 볼 수 있는 표입니다. 아래 표를 이해할 수 있으시다면 논리 연산자는 모두 이해한 것과 같습니다.

| A     | B     | A and B | A or B | not A |
| ----- | ----- | ------- | ------ | ----- |
| True  | True  | True    | True   | False |
| True  | False | False   | True   | False |
| False | True  | False   | True   | True  |
| False | False | False   | False  | True  |

위의 표처럼 결과가 잘 나오는지 몇가지 예제를 통해서 확인만 해보도록 하겠습니다.

```python
a = True
b = True

# highlight-start
print(a and b) # True
print(not a) # False
# highlight-end

c = False

# highlight-start
print(a and c) # False
print(a or c) # True
print(not c) # True
# highlight-end
```

## 드모르간의 법칙

:::tip
드모르간의 법칙은 모르셔도 코딩하는데는 전혀 지장이 없습니다.
재미로 알아보시면 좋겠습니다.
:::

[드모르간의 법칙](https://ko.wikipedia.org/wiki/%EB%93%9C_%EB%AA%A8%EB%A5%B4%EA%B0%84%EC%9D%98_%EB%B2%95%EC%B9%99)의 정의는 다음과 같습니다.

> 논리곱(합)의 부정은 각각 부정의 논리합(곱)과 같다

말이 좀 어렵긴 합니다만, 파이썬으로 풀면 아래와 같습니다.

```python
A = True
B = True

# highlight-start
(not (A or B)) == ((not A) and (not B)) # True
(not (A and B)) == ((not A) or (not B)) # True
# highlight-end
```

알고 있는 조건이 or 또는 and만 있는 경우 유용하게 쓸 수 있습니다.
