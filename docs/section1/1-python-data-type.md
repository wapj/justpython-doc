---
sidebar_position: 1
---

# 파이썬의 데이터 타입

## 파이썬 프로그램의 재료들

무언가를 만들려면 재료가 있어야 합니다.
아주 간단한 요리인 라면을 끓일려고 마음 먹었다 하더라도
물, 면, 스프는 있어야 라면을 만들어 먹을 수 있죠.

아주 간단한 프로그래밍인 파이썬으로 무언가를 만들려면 필요한 재료는 무엇일까요?

최소한 `데이터`, `변수`, `연산자` 이렇게 3가지가 필요합니다.

파이썬에 익숙해지는 방법중에 한가지는 파이썬 인터프리터를 계산기로 사용하는 것인데요.
아래는 1 + 2를 파이썬으로 해본 것입니다.

```mdx title="데이터, 변수, 연산자"
a = 1 # (1)
b = 2 # (2)
a + b # (3)
```

위 코드에 대한 설명은 아래와 같습니다.

```
(1) a에 1이라는 숫자를 할당
(2) b에 2라는 숫자를 할당
(3) a 와 b를 + (더하기) 연산으로 더함
```

여기서 a,b는 `변수` 1, 2는 `데이터`, '+'는 `연산자` 입니다.

:::caution

a = 1 의 뜻이 a 와 b가 같다라는 뜻이아니라
**1을 a에 할당한다**. 라는 뜻임을 주의해주세요.

:::

위에서 말한 재로들에 대해서 하나씩 알아보도록 할까요?

## 변수

변수부터 알아보도록 하겠습니다. `변수`를 풀어서 설명하면 `변하는 수` 라는 뜻이 되는데요. 아래와 같은 문장이 있다고 해보겠습니다.

export const Highlight = ({children, color='#1877F2'}) => (
<span
style={{
      backgroundColor: color,
      borderRadius: '2px',
      color: '#fff',
      padding: '0.25rem',
      borderRadius: '10px'
    }}>
{children}
</span>
);

안녕하세요. 저는 <Highlight >승귤</Highlight>입니다.

생일은 <Highlight >10월 11일</Highlight>이고, 사는 곳은 <Highlight>분당</Highlight>입니다.

취미는 <Highlight >기타연주</Highlight>이며 <Highlight >개발자</Highlight>로 일하고 있습니다.

파란색으로 표시한 단어들은 다른 것으로 바꿔 쓸 수 있는 단어들인데요. 이렇게 바꿀 수 있는 요소들을 **변수**로 표현하게 됩니다. 좀 더 프로그래머스러운 문장으로 바꿔볼까요?

안녕하세요. 저는 <Highlight >{name}</Highlight>입니다.

생일은 <Highlight >{birhday}</Highlight>이고, 사는 곳은 <Highlight>{address}</Highlight>입니다.

취미는 <Highlight >{hobby}</Highlight>이며 <Highlight >{job}</Highlight>로 일하고 있습니다.

이제 파이썬 코드를 한번 보도록 하겠습니다.
