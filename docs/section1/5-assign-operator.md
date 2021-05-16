---
sidebar_position: 5
---

# 할당 연산자

할당 연산자는 이전에서 보았던 `=`이 있습니다. 그외에 할당과 산술연산을 함께 진행하는 복합 할당 연산자가 있습니다. 복합 할당 연산자는 산술연산의 갯수만큼 총 7개가 있습니다.

- 더하기 후 할당하는 `+=`
- 빼기 후 할당하는 `-=`
- 곱하기 후 할당하는 `*=`
- 나누기 후 할당하는 `/=`
- 나누기 후 나머지를 버리고 할당하는 `//=`
- 나머지 연산 후 할당하는 `%=`
- 거듭제곱 후 할당하는 `**=`

각각 간단한 예제를 통해서 알아보도록 하겠습니다.

```python

a = 10
a += 10

# highlight-start
print(a) # 20
# highlight-end

a -= 1
# highlight-start
print(a) # 19
# highlight-end

a *= 3
# highlight-start
print(a) # 57
# highlight-end

a /= 7
# highlight-start
print(a) # 8.142857142857142
# highlight-end

a = 57
a //= 7
# highlight-start
print(a) # 8
# highlight-end

a **=2
# highlight-start
print(a) # 64
# highlight-end
```

예제들만 해보셔도 충분히 어떤 일을 하는 연산자인지 느낌이 오실 것입니다.
우리는 이미 할당 연산자를 알고 있었고, 산술연산자도 알고 있었기 때문입니다.
복합 할당 연산자는 그저 할당연산자와 산술연산자를 합친 기능일 뿐입니다.

프로그래밍에서는 이와같이 기존것들을 결합하여 쓰는 방법을 매우 빈번하게 사용하게 됩니다.
다음장에서 배울 함수를 배우면 기존에 만들어 둔 코드들을 재활용 할 수 있게됩니다.
