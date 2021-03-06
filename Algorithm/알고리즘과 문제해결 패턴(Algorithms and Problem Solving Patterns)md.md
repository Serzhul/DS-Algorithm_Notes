# 알고리즘과 문제해결 패턴(Algorithms and Problem Solving Patterns)

### 알고리즘이란?

— 여러 단계에 걸쳐 특정한 task를 해결하기 위한 과정

### 알고리즘을 알아야 하는 이유

— 프로그래밍에서 발생하는 거의 모든 것은 알고리즘과 관련이 되어있다. 문제 해결의 기초를 쌓는 것이 알고리즘이므로 개발자이면 필수 소양이다.

### 어떻게 실력을 기를것인가?

1. 문제 해결을 위한 계획을 세운다.
2. 공통적인 문제해결 패턴을 마스터한다.

### 문제해결

- 문제를 이해한다.
- 구체적인 예시를 탐구한다.
- 하나하나 설명한다.
- 풀고 간편화한다.
- 복습하고 수정한다.

## 문제 이해하기

1. 나만의 언어로 이 문제를 풀어낼 수 있는가?
2. 이 문제에서 어떤 input값들이 있는가?
3. 이 문제를 해결하면 어떤 output값들이 나오는가?
4. output들을 input데이터로 부터 얻을 수 있는가? 내가 그 문제를 해겨랗기 위해 충분한 정보를 갖고 있는가?
5.  문제의 일부분이 되는 중요한 조각들을 어떻게 이름 붙일 것인가?

$Ex)$ Write a function which takes two numbers and returns their sum.

### 구체적인 예시 탐구하기

- 내가 문제를 더 잘 이해할 수 있을 만한 예시를 떠올리기
- 이러한 예시들은 최종 해결책의 어떻게 작동할지에 대한 전성 검사(잘 작동할 지 여부를 판단하는 테스트)를 제공해줄 것.
- 간단한 예시들 부터 시작
- 좀 더 복잡한 예시들로 나아감

Ex) Write a function which takes in a string and returns counts of each character in the string.

### 단계별로 구분하기

- 내가 취해야 할 단계를 구체적으로 나눠서 적는 것
- 이 과저을 통해 내가 코드를 작성하기 전에 내가 코드에 대해서 다시 생각해보도록 만들어준다 (가령, 콘셉트적인 문제라던가 오해하는 부분이 없는가에 대한 세부사항)

### 풀이/단순화하기

- 내가 하고 있는 문제의 핵심 어려움을 찾기
- 일시적으로 그 어려움을 무시하기

### 복습하기, 질문 리팩토링하기

- 결과를 확인할 수 있는가?
- 결과를 다른 방식으로 도출할 수 있는가?
- 한 눈에 이해할 수 있는가?
- 그 결과와 메소드를 다른 문제에도 사용할 수 있는가?
- 그 솔루션이 성능을 향상시킬 수 있는가?
- 리팩토링을 하기위한 다른 방법을 생각할 수 있는가?
- 다른 사람들은 어떻게 이 문제를 풀었는가?

결론 :  코드의 성능 혹은, 직관성을 높이기 위해 코드를 개선하기 위한 방안을 찾는다. 코딩 인터뷰에서는 문제를 잘 푸는 것도 중요하지만 아이디어를 정리해서 인터뷰에 나의 아이디어를 제시하는 것도 중요하다. 이런 연습을 평소에 자주 함으로써, 다양한 방향으로 접근하는 방법을 익힐 수 있다.

### 정리

- 문제 이해하기
- 구체적인 예시 생각하기
- 단계별로 분석하기
- 풀이 혹은 단순화하기
- 리팩토링하기 (외부 동작을 바꾸지 않으면서 내부 구조를 개선하는 것)
