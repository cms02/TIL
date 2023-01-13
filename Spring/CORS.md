# CORS(Cross-Origin Resource Sharing)?
- 다른 출처의 리소스 공유에 대한 허용/비허용 정책입니다.
- 아무리 보안이 중요하지만, 개발을 하다보면 다른 출처 간의 상호작용을 해야 하는 경우가 있고, 실무적으로 다른 회사의 서버 API를 이용해야 하는 상황도 존재할 수 있습니다.

---

## SOP(Same Origin Policy)?
- 동일한 출처에 대한 정책을 말하며, 동일 출처 서버에 있는 리소스는 자유로이 가져올 수 있지만, 다른 출처 서버에 있는 리소스는 상호작용이 불가능하다는 의미입니다.
- 출처(Origin) 는 Protocol, Host, Port 를 모두 합친 URL 을 의미합니다.

---

## SOP 가 필요한 이유?
- 이러한 정책이 없다면, 해커가 CSRF(Cross-Site Request Forgery) 나 XSS(Cross-Site Scripting) 등의 방법을 이용해서 우리가 만든 어플리케이션에서 해커가 심어놓은 코드가 실행되어 개인 정보를 가로챌 수 있습니다.

---

# Spring 에서 CORS 에러를 해결하기 위한 방법?
- 특정 컨트롤러에만 CORS 를 적용하고 싶을 경우
  - @CrossOrigin 설정을 통해 해결합니다.
- 전역적으로 CORS 를 적용하고 싶을 경우
  - WebMvcConfigurer 에서 설정

---


### 참고
https://www.youtube.com/watch?v=-2TgkKYmJt4  
https://www.youtube.com/watch?v=6QV_JpabO7g  
https://inpa.tistory.com/entry/WEB-%F0%9F%93%9A-CORS-%F0%9F%92%AF-%EC%A0%95%EB%A6%AC-%ED%95%B4%EA%B2%B0-%EB%B0%A9%EB%B2%95-%F0%9F%91%8F
https://chuckchoiboi.github.io/cors-tutorial/

