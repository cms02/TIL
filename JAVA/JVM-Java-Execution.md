# JVM 의 구조
- Class Loader : class JVM 메모리에 로드합니다.
- Execution Engine : 인터프리터, JIT, compiler 를 이용해 데이터 영역에 배치된 바이트 코드를 실행 및 GC로 메모리 관리합니다.
- Runtime Data Area: 프로그램 수행을 위해 OS 에서 할당 받는 공간입니다.

---  

# JAVA 실행 과정
- 자바 컴파일러를 통해 자바 클래스 파일(.java)를 자바 바이트 코드(.class)로 변환합니다.
- 클래스 로더를 통해 바이트코드를 JVM 런타임 영역에 로드합니다.
- 실행 엔진을 통해 실행합니다.


---

### 참고   
https://sas-study.tistory.com/262  