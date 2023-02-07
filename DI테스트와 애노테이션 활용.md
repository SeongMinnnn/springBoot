##### 테스트 코드를 이용한 테스트
*HTTP 응답의 3가지 요소인 상태코드, 헤더(Content-Type), 바디를 검증한다.

##### TestRestTemplate
번거로운 수동 테스트 대신 자동화된 테스트 코드를 이용한 테스트 방식으로 전환한다.
웹 서버에 HTTP요청을 보내고 받아서 검증하는 테스트에 사용하는 템플릿
![[TestRestTemplate.jpg]]
프로젝트를 실행할때 스프링 부트를 적용시키면 자동으로 생성된다. 스프링 부트환경을 그대로 가져와 실행한다.


|RestTemplate|TestRestTemplate|
|-----|----|
|서버 문제 있을 시 예외를 생성함|HTTP 응답 3가지 요소만 확인시 편리함|

![[DI테스트.jpg]]
header 부분에 startsWith()은 앞 부분만 확인하는 것이며
전체 확인을 위해서는 isEqualTo()로 바꿔서 사용한다.