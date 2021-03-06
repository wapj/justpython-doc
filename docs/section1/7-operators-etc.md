---
sidebar_position: 7
---

# 그외 연산자들 (항등연산, 멤버연산)

이번 문서에서는 2가지의 종류의 연산자를 다루게 됩니다.

주소값이 같은지 비교하는 항등연산자, 여러가지를 한번에 담고있는 리스트(배열이라고도합니다.)에 해당 값이 들어있는지 확인하는 멤버연산자까지 다루게 됩니다.

## 항등연산자 (identity operator)

`항등(恒等)`이라는 단어는 조금 생소한 단어입니다. 뜻을 풀어보면 `항상 항에 같을 등`으로 **항상 같음**이라는 뜻을 가집니다. 항등 연산자는 어떤 연산을 했을 때 항상 같은 값이 나오도록 하는 것입니다. 컴퓨터는 어떤 값을 메모리에 담아두고 있고, 메모리 주소는 변하지 않습니다. 즉 항등연산자는 메모리의 주소를 비교하는 연산자입니다.

`is`와 `is not` 두가지만 있습니다.

`A is B`로 쓰게 되면 A와 B의 **메모리 주소가 같은 경우** True를 아니면 False를 결과값으로 주게 됩니다.

`A is not B`의 경우에는 A와 B의 **메모리 주소가 다른 경우** True를 주고, 같은경우는 False를 결과값으로 주게 됩니다.

파이썬에는 `id` 라고 하는 어떤 값의 메모리 주소를 리턴해주는 함수가 있습니다.

```python
txt = 'python'
print(id(txt))
### 4351040752 등과 같은 어떤 주소 값이 찍힙니다. 컴퓨터마다 다르게 찍힙니다.
```

파이썬에서 같은 문자열은 같은 메모리 주소를 가리키게 됩니다.
과연 그런지 변수 두개에 같은 문자열을 할당한 다음 항등연산자 is로 확인해보도록 하겠습니다.

```python
txt = 'python'
txt2 = 'python'

print(txt is txt2)
print(id(txt))
print(id(txt2))
# 결과값 True
# txt, txt2의 주소값은 같은 값이 나옵니다.
```

즉 두 문자열의 메모리 주소는 같다는 것을 알 수 있습니다.

한가지만 더 실험을 해보도록 하겠습니다.
숫자 1과 문자열 '1'은 주소값이 다릅니다.
정말로 다른지 항등 연산자를 사용하여 비교해보도록 하겠습니다.

```python
a = 1
b = '1'

print(a is b) # False
print(a is not b) # False
print(id(a))
print(id(b))

# a와 b의 주소값은 각각 다른 값이 나옵니다.
```

:::tip
is 연산자는 해당 변수가 **None**인지 판단이 필요한 경우에 많이 사용됩니다.
또한 상수를 미리 선언해둔 경우, 해당 상수값과 값이 같은지 비교하는 경우에도 쓰이게 됩니다. is연산자와 상수값을 비교할때 문자열인 경우에는 문제가 없지만, 숫자인 경우에 256보다 큰 숫자를 사용하면 문제가 생길 수 있습니다.

즉 파이썬은 256까지의 숫자는 자주 사용한다고 보고 고정으로 메모리에 상주 시켜놓습니다.

```python
a = 256
b = 256

print(a is b) # True

c = 257
d = 257
print(c is b) # False
```

:::

## 멤버 연산자

멤버 연산자는 in, not in 이 있습니다.
아직 리스트를 배우지 않았기에 간단하게만 다루도록 하겠습니다.

리스트는 **하나의 변수에 여러 개의 순서가 있는 값을 저장할 수 있게 해주는 자료형**입니다. 보통 대괄호 `[ ]`안에 콤마로 각 요소들을 구분하게 됩니다.

아래는 1부터 5까지의 숫자가 들어있는 간단한 리스트 코드입니다.

```python
nums = [1,2,3,4,5]
```

nums리스트 안에 3이라는 숫자가 있는지 확인하고 싶은 경우 `in` 연산자를 사용할 수 있습니다. 다음과 같이 사용하게 됩니다.

```python
print(3 in nums)

# 결과값 : True
```

만약에 없는 숫자를 넣으면 결과가 False로 나오게 됩니다.

```python
print(6 in nums)

# 결과값 : False
```

리스트 안에 없는지 확인 하고 싶은 경우는 `not in`을 사용하면 됩니다.
문자열에도 멤버 연산자를 사용할 수 있습니다. 간단한 예제로 알아보도록 하겠습니다.

```python
txt = "동해물과 백두산이 마르고 닳도록"

print("동해" in txt)  # True
print("서해" in txt) # False
print("남해" not in txt) # True
```

in, not in 을 사용하면 리스트나 문자열에서 특정 값이 있는지 편하게 확인 할 수 있습니다.

여기까지해서 파이썬에 있는 모든 연산자들을 알아 보았습니다. 다음 섹션에서는 함수를 다루게 됩니다. 가장 중요한 기능중 하나인 함수를 함께 알아보도록 하겠습니다.
