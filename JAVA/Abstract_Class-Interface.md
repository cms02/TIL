# 추상 클래스(Abstract Class)
- 클래스 내에 추상 메서드가 하나 이상 포함되거나, abstract 로 정의되어 있는 클래스입니다.
- 다중 상속의 모호성 때문에 하나만 상속 받을 수 있습니다.
- 부모 클래스의 기능을 사용하거나 확장하기 위해 사용됩니다. 
- 상속하는 집합간에는 연간관계가 있습니다.
- extends 키워드를 사용합니다.
- is kind of
---  

# 인터페이스(Interface)
- 모든 메서드가 추상 메서드 입니다.(Java 8 에서는 default 키워드를 이용하여 일반 메서의 구현도 가능합니다.)
- 상수(static final)와 추상 메서드의 집합입니다.
  - public static final, public abstract 를 생략해도 컴파일시에 자동으로 생성해줍니다.
- 상속하는 집합간에는 연관관계가 존재하지 않을 수 있습니다.
- implements 키워드
- is able to

