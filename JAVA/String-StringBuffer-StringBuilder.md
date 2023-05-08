# String ?
- 다른 클래스(StringBuffer, StringBuilder) 와 다르게 String 은 immutable(불변)합니다.
- String 객체는 한번 생성되면 할당된 메모리 공간이 변하지 않습니다.
- concat 메서드를 통해 기존에 생성된 String 클래스 객체 문자열에 다른 문자열을 붙여도 기존 문자열에 새로운 문자열을 붙이는 것이 아니라,
새로운 String 객체를 만든 후, 새 String 객체에 연결된 문자열을 저장하고, 그 객체를 참조하도록 합니다.
- 문자열 연산이 많은 경우, 성능이 좋지 않을 수 있습니다.
- Immutable 한 객체는 간단하게 사용가능하고, Thread-Safe 하기 때문에 내부 데이터를 자유롭게 공유 가능합니다.

---
# StringBuffer ?
- String 클래스와 다르게 기존의 버퍼 크기를 늘리며 유연하게 동작합니다.
- 각 메서드별로 Synchronized Keyword가 존재하여, 멀티쓰레드 환경에서도 동기화를 지원합니다.
---
# StringBuilder ?
- String 클래스와 다르게 기존의 버퍼 크기를 늘리며 유연하게 동작합니다.
- StringBuffer 와 달리 동기화를 지원하지 않습니다.
---

