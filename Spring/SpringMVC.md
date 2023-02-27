# Spring Web MVC에서 요청 마다 Thread가 생성되어 Controller를 통해 요청을 수행할텐데, 어떻게 1개의 Controller만 생성될 수 있을까?

- 생성한 Controller 클래스에 대한 정보가 JVM 메모리 영역 중 Method Area(메서드 영역)에 올라가기 때문입니다.
- Controller 객체는 Heap(힙)에 생성 되지만, 해당 클래스의 정보(메소드 처리 로직, 명령들)는 Method Area(메서드 영역)에 생성됩니다.
- 따라서 결국 모든 Thread가 객체의 메서드를 공유할 수 있기 때문에 Controller는 1개만 생성됩니다.

---

### 참고

https://velog.io/@ejung803/Spring-Web-MVC%EC%97%90%EC%84%9C-%EC%9A%94%EC%B2%AD-%EB%A7%88%EB%8B%A4-Thread%EA%B0%80-%EC%83%9D%EC%84%B1%EB%90%98%EC%96%B4-Controller%EB%A5%BC-%ED%86%B5%ED%95%B4-%EC%9A%94%EC%B2%AD%EC%9D%84-%EC%88%98%ED%96%89%ED%95%A0%ED%85%90%EB%8D%B0-%EC%96%B4%EB%96%BB%EA%B2%8C-1%EA%B0%9C%EC%9D%98-Controller%EB%A7%8C-%EC%83%9D%EC%84%B1%EB%90%A0-%EC%88%98-%EC%9E%88%EC%9D%84%EA%B9%8C%EC%9A%94