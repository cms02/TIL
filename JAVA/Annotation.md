# Annotation ?
- Annotation 은 인터페이스를 기반으로 한 문법으로 주석처럼 코드에 달아 클래스에 특별한 의미를 부여하거나 기능을 주입할 수 있습니다.
- built-in Annotation 은 상속받아서 메소드를 오버라이드 할 때 사용하는 @Override Annotation 이 그 대표적인 예입니다.
- Meta Annotation 은 Annotation 을 선언할 때 사용하는 Annotation 입니다.
  - @Retention: Annotation 의 유지 범위를 지정합니다.(Source, Class, Runtime)
  - @Inherit: Annotation 을 하위 클래스까지 전달할지 여부를 지정합니다. 하위 클래스까지 상속이 가능하도록 해줍니다.
  - @Target: 해당 Annotation 을 어디에 사용할 지 결정합니다.(타입, 필드, 메서드, 파라미터, 생성자, 로컬변수, Annotation Type)
---  

