1. **Inversion of Control (IoC)**:
    - IoC는 객체의 생명 주기와 의존성 관리를 개발자가 아닌 프레임워크에 위임하는 패턴입니다.
    - Spring에서는 ApplicationContext라는 컨테이너가 이 역할을 합니다. 컨테이너는 XML, Java Configuration, Annotations 등을 사용해 구성될 수 있습니다.
2. **Dependency Injection (DI)**:
    - DI는 객체가 직접 자신의 의존성을 관리하는 대신 외부(주로 컨테이너)에서 주입받는 방식입니다. 이를 통해 코드의 결합도를 낮추고 테스트 용이성을 향상시킵니다.
    - 예:

        ```java
        public class OrderService {
           private final OrderRepository orderRepository;
        
           @Autowired
           public OrderService(OrderRepository orderRepository) {
               this.orderRepository = orderRepository;
           }
        }
        
        ```

    - 위 예제에서 **`OrderService`**는 **`OrderRepository`**에 의존합니다. **`@Autowired`** 어노테이션이 붙은 생성자를 통해 Spring은 해당 의존성을 주입합니다.
3. **AOP (Aspect Oriented Programming)**:
    - AOP는 횡단 관심사 (cross-cutting concerns)를 모듈화하고 로직을 분리하는 프로그래밍 패러다임입니다. 로깅, 트랜잭션 관리, 보안 등의 기능을 애플리케이션 코드와 분리하여 관리할 수 있습니다.
    - Spring AOP는 프록시 기반으로 동작하며, 대상 객체에 관점을 적용하여 프록시 객체를 생성합니다.
4. **Spring MVC**:
    - Spring MVC는 Model-View-Controller 디자인 패턴을 따르는 웹 애플리케이션을 구축하기 위한 모듈입니다.
    - DispatcherServlet은 요청을 받아 적절한 컨트롤러에 라우팅합니다. 컨트롤러는 요청을 처리한 후 뷰를 반환하며, 이 뷰는 사용자에게 최종 결과를 보여줍니다.
5. **데이터 액세스 및 트랜잭션 관리**:
    - Spring은 JDBC와 ORM 프레임워크 (예: Hibernate, JPA)와의 통합을 지원합니다.
    - 트랜잭션 관리를 위한 선언적 트랜잭션을 제공하며, **`@Transactional`** 어노테이션을 사용하여 트랜잭션 범위를 지정할 수 있습니다.
6. **다양한 모듈**:
    - Spring은 메시징, 웹 워크플로우, 보안 등의 다양한 모듈을 포함하며, 이를 통해 풍부한 기능을 제공합니다.