007.스프링 삼각형과 설정 정보 
===============
### AOP - Aspect? 관점? 핵심 관심사? 횡단 관심사? 
> 스프링 DI가 의존성에 대한 주입이라면 스프링 AOP는 로직주입이라고 볼 수 있다. 

[image](https://user-images.githubusercontent.com/56033943/215752786-4936a697-b480-40c1-94e2-8e4ca92258c9.png)
횡단 관심사 : 이처럼 다수의 모듈에 공통적으로 나타나는 부분 </br>
핵심 관심사 : 모듈별로 다르게 나타나는 부분 </br>
**코드 = 핵심관심사 + 횡단 관심사**

- @Aspect : 이 클래스를 AOP에서 사용하겠다는 의미 
- @Before : 대상 메서드 실행 전에 이 메서드를 실행하겠다는 의미 
- AOP를 적용 시 개발할 때 분할함에 있어 수고스럽지만 추가 개발과 유지보수 측면에서 좋은 코드가 될 수 있다. => 단일 책임 원칙이 적용됨 

#### 스프링 AOP의 핵심
- 스프링 AOP는 인터페이스 기반이다. 
- 스프링 AOP는 프록시 기반이다.
- 스프링 AOP는 런타임 기반이다. 

---
- Aspect : 관점, 측면
- Advisor : 조언자
- Advice : 조언 
- JoinPoint : 결합점 
- Pointcut : 자르는 점 

#### Pointcut - Aspect 적용 위치 지정자 
: Pointcut은 횡단 관심사를 적용할 타깃 메서드를 선택하는 지시자이다. -> 타깃 클래스의 타깃 메서드 지정자 

#### JointPoint - 연결 가능한 지점 
: Pointcut은 JoinPoint의 부분 집합이다. 
- Pointcut의 후보가 되는 모든 메서드들은 JoinPoint
- JoinPoint는 Aspect 적용이 가능한 모든 지점이다. 

#### Advice 
: Advice는 Pointcut에 적용할 로직, 메서드를 의미한다. 
- Advice는 Pointcut에 언제, 무엇을 적용할지 정의한 메서드다. 

#### Aspect - Advisor의 집합체 
: AOP에서 Aspect는 여러개의 Advice와 여러 개의 Pointcut의 결합체를 의미하는 용어이다. 


### PSA - 일관성 있는 서비스 추상화 
- 어댑터 패턴을 적용해 같은 일을 하는 다수의 기술을 공통의 인터페이스로 제어할 수 있게 한 것을 서비스 추상화라고 한다. 


