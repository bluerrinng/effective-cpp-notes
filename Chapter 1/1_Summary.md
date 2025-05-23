# 1장: 형식 연역

**형식 연역(type deduction)** 이 일어나는 방법을 확실하게 이해하지 않는다면, 현대적인 C++에서 효과적인 프로그래밍이 거의 불가능하다.

형식 연역이 일어나는 상황
- 함수 템플릿 호출
- auto가 등장하는 대부분의 상황
- decltype 표현식에서 발생

C++14 의 경우에는 난해한 decltype(auto) 구성체가 쓰이는 곳에서도 형신 연역 발생

해당 장은 다음에 관한 내용을 포함한다:
1. 형식 연역의 작동 방식을 설명
2. 형식 연역에 기초한 `auto` 와 `decltype`의 작동 방식 설명
3. 컴파일러의 형식 연역 결과가 명식적으로 표시되게 만드는 방법 설명

## 항목 1: 템플릿 형식 연역 규칙을 숙지하라
`auto`는 템플릿에 대한 형식 연역을 기반으로 작동
