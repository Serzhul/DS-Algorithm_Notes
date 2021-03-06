# Time Complexity(시간 복잡도)

# 시간에 관한 문제(The Problem with Time)

알고리즘을 풀다보면 속도가 빠른 알고리즘을 일반적으로 좋은 알고리즘의 기준으로 삼는다. 그러나 우리가 프로그래밍을 작업하다보면 언제나 같은 환경에서 작업하는 것이 아니기 때문에 시간 측정에 문제가 생기게 된다. 가령 이런 문제를 생각해 볼 수 있다.

- 만약 실험 조건이 다른 컴퓨터라면 같은 알고리즘이라도 다른 시간이 나올 것이다. ⇒ 성능 차이 때문
- 그러나 실제로는 같은 컴퓨터로 실험하더라도 다른 시간이 나온다. ⇒ 항상 동일한 조건에서 실험할 수 없기 때문이다.
- 따라서 빠른 알고리즘의 속도 측정을 정의함에 있어서 시간의 정확도는 다소 떨어질 수 있다. 이를 보완하기 위해 나온 것이 Big O 표기법인 것이다.

## Big O Notation이 필요한 이유

1. 시간 효율성으로 알고리즘을 접근할 경우 알고리즘의 효율을 정확히 판단할 수 있는 근거가 부족하다. (다른 기기, 혹은 같은 기기에서도 시간 차이가 발생하고 측정 방법에 따라 오차가 발생할 수 있기 때문)
2. 따라서, 시간을 정확히 측정하기보다는 연산의 개수를 세는 방식으로 알고리즘의 퍼포먼스를 측정할 수 있다!

예) 만약, 1부터 특정 숫자까지의 합을 구하는 함수를 만든다고 가정한다.  이때 특정 숫자는 n으로 표기한다. 

```jsx
// 1
function addUpTo(n) {
let total = 0;
for (let i = 1; i <=n; i++) {
	total += i;
}
	return total;
}

// loop문에서는 loop문을 한번 반복할 때마다 1번 연산한 걸로 계산함

//2 =
function addUpTo(n) {
return (n * (n+1)) / 2;
}
// multiplication / addition / division => 3 operation

console.log(addUpTo(6)) 
```

- 위의 첫번째 함수는 얼핏 보면 논리에 맞는것처럼 보인다. for문으로 total값에 계속 새로운 값을 더하면서 합을 반환하기 때문이다.
- 그러나 두번째 방식을 보면  결과는 같지만 계산하는 숫자가 훨씬 줄어든 것을 알 수 있다.
- 1번의 경우 숫자가 커짐에 따라 연산 숫자가 계속 늘어나는 반면, 2번의 경우 숫자가 바뀌더라도 연산의 숫자는 `곱셈 + 덧셈 + 나눗셈` 3번으로 고정되어 있음을 알 수 있다. 즉 2번 방식이 더 우수한 알고리즘이라 할 수 있다.

## Big O 표기법의 특징

- Big O 표기법은 모호한 카운팅 방법을 공식화하는 방법이라 할 수 있다.
- Big O에서 연산자 수를 계산할 때는 사칙연산도 포함하지만 할당하는 것도 하나의 연산자로 계산한다. 즉, 알고리즘에서 연산이 n번을 사칙연산하던, n번을 할당을 하던, 인풋으로 들어오는 n의 크기에 비례하므로 n으로 계산한다.
- 알고리즘의 작동시간이 어떤 형태로 증가하는지를 공식적으로 표기하는 방법이다 (input이 증가할 때 마다)
- $O(fn)$을 알고리즘의 연산 개수라고 하며, 알고리즘을 개선한다는 것은 $N$이 증가할때마다 $f(N)$을 어떻게 더 적게 증가시키는 지에 관한 것이라고 할 수 있다.
- 일반적으로 loop문을 돌리면 $O(N)$으로 표기할 수 있다. ⇒ n만큼 연산을 하기 때문

    $ex)$ 2중 loop문의 경우 $O(N^2)$이다. n만큼 n번 반복하기 때문

    - 많은 연산을 하는 알고리즘일 수록 기울기가 더 가팔라지며, 비 효율적인 알고리즘임을 의미한다.

### Big O 표현식 간소화하는 예시

- $O(N)$ ⇒ linear :

$ex)$

$$O(n + 10) ⇒ O(n) / O(1000n + 50) ⇒ O(n)$$

- $O(1)$ ⇒ constant :

 $ex)$ 

$$O(500) ⇒ O(n)$$

- O($n^2$) ⇒ quadratic:

 $ex)$ $O(n^2+n+5) ⇒ O(n^2)$

### Big O 규칙

1. 산술 방식(Arithmetic operation)은 일정하다(constant).
2. 변수 할당(Variable Assignment)은 일정하다(constant).
3. 인덱스로 배열 요소에 접근하거나, 키로 객체에 접근하는 것은 일정하다.(constant)
