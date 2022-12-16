# Bean?

Spring IoC 컨테이너가 관리하는 자바 객체이다.  

---  

## Spring Bean 의 등록 방식
클래스 위에 @Component를 붙인 후 ComponentScan을 이용하여 빈을 자동 등록하거나, @Configuration이 붙은 설정 파일 내의 특정 타입을 리턴하는 메소드 위에 @Bean을 붙여서 빈을 등록하는 방법이 있다.

## @Bean VS @Component
**@Bean**
- 개발자가 컨트롤이 불가능한 외부 라이브러리들을 Bean으로 등록하고 싶은 경우에 사용된다.
- 메소드 또는 어노테이션 단위에 붙일 수 있다.

**@Component**
- 개발자가 직접 컨트롤이 가능한 클래스들의 경우에 사용된다.
- 클래스 또는 인터페이스 단위에 붙일 수 있다.

---
## @Configuration은 어떻게 싱글톤 빈을 보장하는가?
클래스의 바이트 코드를 조작하는 CGLIB 라이브러리를 사용하여 싱글톤을 보장한다. CGLIB는 프록시 객체의 일종으로 설정 파일이 빈으로 등록될 때, 해당 설정 파일을 상속 받은 프록시 객체가 빈으로 등록된다. 그리고 설정 파일에서 @Bean이 붙은 메소드마다 이미 스프링 빈이 존재하면 존재하는 빈을 반환하고, 스프링 빈이 없으면 비로소 등록하고 반환하는 식으로 싱글톤을 보장한다.

---
## Bean Lite Mode?
Bean Lite Mode는 CGLIB를 이용하여 바이트 코드 조작을 하지 않는 방식을 의미한다. 이때 스프링 빈에 대해 싱글톤을 보장하지 않는다.

---
## Spring Bean Scope?
Bean Scope는 Bean이 존재할 수 있는 범위를 뜻한다. 기존의 스프링이 사용하는 scope로 singleton, prototype이 있고, 웹 환경에서만 동작하는 web scope로는 request, session, application 등이 있다.  

**Singleton**
- 싱글톤 빈은 스프링 컨테이너에서 한 번만 생성되며, 컨테이너가 사라질 때 제거된다.
- 생성된 하나의 인스턴스는 Spring Beans Cache에 저장되고, 해당 빈에 대한 요청과 참조가 있으면 캐시된 객체를 반환한다. 하나만 생성되기 때문에 동일 참조를 보장한다.
- 기본적으로 모든 빈은 스코프가 명시적으로 지정되지 않으면 싱글톤이다.

**Prototype**
- 프로토 타입은 DI가 발생할 때마다 새로운 객체가 생성되어 주입된다.
- 빈 소멸에 스프링 컨테이너가 관여하지 않고, GC에 의해 빈이 제거된다.

---
## Spring Bean의 생명 주기?
**Singleton**
- 스프링 컨테이너 생성
- 스프링 빈 생성
- 의존 관계 주입
- 초기화 콜백
- 사용
- 소멸전 콜백
- 스프링 종료  

**Prototype**
- 스프링 컨테이너 생성
- 스프링 빈 생성
- 의존 관계 주입
- 초기화 콜백
- 사용
- GC에 의해 수거

---

### 참고   
https://steady-coding.tistory.com/594  
https://www.youtube.com/watch?v=3gURJvJw_T4  
https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-%ED%95%B5%EC%8B%AC-%EC%9B%90%EB%A6%AC-%EA%B8%B0%EB%B3%B8%ED%8E%B8/dashboard
