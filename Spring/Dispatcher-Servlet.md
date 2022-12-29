# Dispatcher Servlet?

디스패처 서블릿은 HTTP 프로토콜로 들어오는 모든 요청을 가장 먼저 받아 적합한 컨트롤러에 위임해주는 프론트 컨트롤러 입니다.

---

# Dispatcher Servlet 의 동작 방식
![동작방식](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbImFbg%2FbtrGzZMTuu2%2FCkY4MiKvl5ivUJPoc5I3zk%2Fimg.png)

- 클라이언트의 요청을 디스패처 서블릿이 받음
- 요청 정보를 통해 요청을 위임할 컨트롤러를 찾음
- 요청을 컨트롤러로 위임할 핸들러 어댑터를 찾아서 전달함
- 핸들러 어댑터가 컨트롤러로 요청을 위임함
- 비즈니스 로직을 처리함
- 컨트롤러가 반환값을 반환함
- 핸들러 어댑터가 반환값을 처리함
- 서버의 응답을 클라이언트로 반환함

---

## 핸들러 어댑터가 컨트롤러를 호출하는 이유?
컨트롤러의 구현 방식이 다양하기 때문입니다. 최근에는 @Controller에 @RequestMapping 관련 어노테이션을 사용해 컨트롤러 클래스를 주로 작성하지만, 
Controller 인터페이스를 구현하여 컨트롤러 클래스를 작성할 수도 있습니다. 스프링은 핸들러 어댑터라는 어댑터 인터페이스를 통해 **어댑터 패턴을 적용함으로써 컨트롤러의
구현 방식에 상관없이 요청을 위임**할 수 있습니다.


---

### 참고   
https://mangkyu.tistory.com/18  
https://mangkyu.tistory.com/216
