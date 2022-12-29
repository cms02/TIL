# Servlet Filter 와 Spring Interceptor의 차이
- 필터는 자바 표준 스펙(J2EE)이고, 인터셉터는 Spring MVC 스펙에 포함되어 있는 클래스 입니다.
- 필터는 웹 컨테이너에서, 인터셉터는 스프링 컨테이너에서 관리됩니다.
- 필터는 Request/Response 객체 조작이 가능하지만 인터셉터는 불가능 합니다.
  - 필터는 필터 체이닝(다음 필터 호출)을 하면서 Request/Response 객체를 넘겨주는데, 이 때 객체 조작이 가능합니다. 
- 필터에서 예외 발생 시 @ControllerAdvice 에서 처리하지 못하지만, 인터셉터는 가능합니다.
  - @ControllerAdvice의 적용 범위가 Dispatcher Servlet 이고 Dispatcher Servlet 이 인터셉터를 호출하기 때문입니다. 


![img](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FSz6DV%2Fbtq9zjRpUGv%2F68Fw4fZtDwaNCZiCFx57oK%2Fimg.png)





---

### 참고

https://mangkyu.tistory.com/173  
https://www.youtube.com/watch?v=v86B35pwk6s&t=36s