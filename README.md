# spring-starter

## SpringBoot 
### SpringBoot 3.x -> 2.x 프로젝트로 전환
> build.gradle
> ```groovy
> plugins {
>     id 'java'
>     id 'org.springframework.boot' version '2.7.18'
>     id 'io.spring.dependency-management' version '1.0.15.RELEASE'
> }
> 
> java {
>     sourceCompatibility = '11'
> }
> 
> dependencies {
>     ...
>     testImplementation 'org.springframework.boot:spring-boot-starter-test'
> }
> 
> tasks.named('test') {
>     useJUnitPlatform()
> }
> ``` 

---

## Spring
### Spring 1.x
> 초기 버전으로, EJB(Enterprise JavaBeans)에 대한 대안으로 제공됩니다.

### Spring 2.x
> **Aspect-Oriented Programming(AOP) 지원**  
> Spring 2.x에서는 AspectJ를 기반으로 한 AOP 지원이 추가되었습니다. 
> AOP는 애플리케이션 전체에서 공통 관심 사항을 분리하고 모듈화하는 데 사용되는 프로그래밍 패러다임입니다. 
> 이를 통해 코드의 재사용성과 유지 보수성을 향상시킬 수 있습니다.
> 
> **어노테이션 기반의 구성**  
> Spring 2.x에서는 어노테이션 기반의 구성이 도입되었습니다. 
> @Component, @Autowired, @Qualifier 등의 어노테이션을 사용하여 컴포넌트 스캔과 의존성 주입을 편리하게 처리할 수 있습니다.
> 
> **Java 5의 기능 지원**  
> Spring 2.x는 Java 5의 기능을 지원합니다. 따라서 제네릭스, 열거형, 가변 인자 등 Java 5의 기능을 활용할 수 있습니다.
> 
> **리소스 추상화**  
> Spring 2.x에서는 리소스 추상화 기능이 도입되었습니다. 
> 이를 통해 파일 시스템, 클래스 경로, 원격 URL 등 다양한 유형의 리소스에 대해 일관된 방식으로 작업할 수 있습니다.
> 
> **JUnit 테스트 지원 개선**  
> Spring 2.x에서는 JUnit 테스트 지원이 개선되었습니다. 
> @RunWith, @ContextConfiguration, @Autowired 등의 어노테이션을 사용하여 테스트 환경을 설정하고 의존성 주입을 수행할 수 있습니다.
> 
> **웹 서비스 지원 개선**  
> Spring 2.x에서는 웹 서비스 지원이 개선되었습니다. 
> Axis, JAX-WS 등과 같은 다양한 웹 서비스 프레임워크와의 통합이 강화되었고, 더 편리한 방식으로 웹 서비스 클라이언트를 개발할 수 있게 되었습니다.
> 
> **Validator 인터페이스**  
> Spring 2.x에서는 Validator 인터페이스가 도입되었습니다. 이를 통해 객체 유효성 검증을 담당하는 클래스를 더욱 효과적으로 작성할 수 있습니다.

### Spring 3.x
> **Java 5**  
> Java 5 이상의 버전에서 사용할 수 있으며, Java 6과 Java 7을 지원합니다.
> Java 5의 java.util.concurrent와의 닫힌 통합(close integration)을 위해 스프링의 TaskExecutor 추상화를 수정했다. 
> ExecutorService 어댑터, ThreadFactory 통합 뿐 아니라 이제 Callable과 Future를 지원하는 퍼스트 클래스를 제공한다. 
> 이는 가능한 한 JSR-236(Java EE 6을 위한 동시성 유틸리티)과 맞추었다. 
> 게다가 새로운 @Async 어노테이션(또는 EJB 3.1의 @Asynchronous 어노테이션)으로 비동기 메서드 호출을 지원한다.
> 
> **광범위한 REST 지원**
> 기존에 존재하는 MVC 웹 프레임워크의 어노테이션을 확장해서 REST스러운 어플리케이션 구축에 대한 서버 측 지원을 추가했다. 
> 클라이언트 측 지원은 JdbcTemplate나 JmsTemplate 같은 템플릿 클래스처럼 RestTemplate 클래스로 제공한다. 
> 서버 측과 클라이언트 측 모두 REST기능은 HTTP 요청과 응답을 나타내는 객체의 변환을 위해 HttpConverter를 사용한다.
> 
> **선언적인 모델 유효성 확인**
> JSR 303을 포함해서 여러 가지 유효성 확인 지원이 개선되었고 기본 프로바이더로 Hibernate Validator를 사용한다.
> 
> **Java EE 6에 대한 조기 지원**
> 새로운 @Async 어노테이션(또는 EJB 3.1의 @Asynchronous 어노테이션)을 사용해서 비동기 메서드 호출을 지원한다.  
> JSR 303, JSF 2.0, JPA 2.0 등등
> 
> **자바 구성(Java Configuration)**  
> Spring 3.x에서는 XML 설정 외에도 자바 기반의 설정을 위한 @Configuration 어노테이션을 도입했습니다. 
> 이를 통해 XML 대신 자바 코드를 사용하여 애플리케이션을 구성할 수 있습니다.
> 
> **어노테이션 기반의 구성**  
> Spring 3.x에서는 어노테이션 기반의 구성이 더욱 강화되었습니다. 
> @Component, @Autowired, @Qualifier 등의 어노테이션을 사용하여 컴포넌트 스캔과 의존성 주입을 편리하게 처리할 수 있습니다.
> 
> **스프링 MVC 개선**  
> Spring 3.x에서는 스프링 MVC(Web MVC)에 대한 개선이 이루어졌습니다. 
> RESTful 웹 서비스를 지원하기 위한 개선 사항이 도입되었고, @RequestMapping 어노테이션을 대체하기 위한 메타-어노테이션인 
> @GetMapping, @PostMapping 등이 추가되었습니다.
> 
> **스프링 Expression Language(SpEL)**  
> Spring 3.x에서는 SpEL이 도입되었습니다. SpEL은 런타임 시에 표현식을 평가하고 값을 바인딩하기 위한 강력한 표현 언어입니다. 
> 이를 통해 XML 설정에서 런타임 검증 및 다양한 조건을 처리할 수 있습니다.
> 
> **스프링 프레임워크의 모듈화**  
> Spring 3.x부터는 스프링 프레임워크가 여러 모듈로 나누어져 더욱 모듈화되었습니다. 
> 예를 들어, spring-core, spring-beans, spring-context, spring-web 등의 독립적인 모듈로 제공되어 필요한 모듈만 선택적으로 사용할 수 있게 되었습니다.
> 
> **자바 5 이상 지원**  
> Spring 3.x는 Java 5 이상의 버전을 지원합니다. 따라서 제네릭스, 열거형, 가변 인자 등 Java 5의 기능을 활용할 수 있게 되었습니다.
> 이외에도 Spring 3.x에서는 다양한 성능 개선, 보안 강화, 캐시 관리, JPA(Java Persistence API) 지원 등 다양한 기능 개선과 새로운 기능이 도입되었습니다. 
> Spring 3.x 버전은 Spring 프레임워크의 발전을 이끄는 중요한 전환점이었습니다.

### Spring 4.x
> **Java 8 지원**  
> Spring 4.x는 Java 8을 지원합니다. 따라서 람다식, 스트림 API, 날짜 및 시간 API 등 Java 8의 기능을 활용할 수 있습니다.
> 
> **캐시 추상화 개선**
> Spring 4.x에서는 캐시 추상화가 개선되었습니다. 
> @Cacheable, @CachePut, @CacheEvict와 같은 어노테이션을 사용하여 메서드 결과를 캐시할 수 있으며, 다양한 캐시 제공자와 통합이 강화되었습니다.
> 
> **WebSocket 지원 개선**  
> Spring 4.x에서는 WebSocket 지원이 개선되었습니다. 
> @Controller 어노테이션과 함께 WebSocket 핸들러를 작성할 수 있으며, 웹 소켓 통신을 통해 실시간 양방향 통신을 구현할 수 있습니다.
> 
> **HTML5 폼 필드 바인딩**  
> Spring 4.x에서는 HTML5 폼 필드와 자바 빈 객체 간의 바인딩을 개선했습니다. 이를 통해 HTML5에서 추가된 새로운 필드 유형과 기능을 활용할 수 있습니다.
> 
> **JMS 2.0 지원 개선**  
> Spring 4.x에서는 JMS(Java Message Service) 2.0 지원이 개선되었습니다. JMS 2.0의 새로운 기능과 업데이트된 API를 활용할 수 있습니다.
> 
> **Groovy 지원 개선**  
> Spring 4.x에서는 Groovy 지원이 개선되었습니다. 
> Groovy를 사용하여 Spring 애플리케이션을 작성하고 구성할 수 있으며, Groovy 스크립트를 사용하여 빈 구성을 동적으로 변경할 수 있습니다.
> 
> **테스트 지원 개선**  
> Spring 4.x에서는 테스트 지원이 개선되었습니다. 
> @WebAppConfiguration, @WebIntegrationTest, @Transactional, @Sql 등의 어노테이션을 사용하여 웹 애플리케이션과 데이터베이스 테스트를 
> 보다 쉽게 수행할 수 있습니다.
> 
> **Spring Security 개선**  
> Spring 4.x에서는 Spring Security의 개선 사항이 포함되었습니다. 새로운 보안 기능과 업데이트된 API를 통해 보다 강력한 보안 솔루션을 구현할 수 있습니다.

### Spring 5.x
> **Java 8 이상 필수**  
> Spring 5.x는 Java 8 이상을 필수로 요구합니다. 이로 인해 Java 8의 모든 기능과 향상된 성능을 활용할 수 있습니다.
> 
> **리액티브 프로그래밍 지원**  
> Spring 5.x에서는 리액티브 프로그래밍을 위한 Spring WebFlux 모듈이 추가되었습니다. 
> 이 모듈을 사용하여 비동기 및 논블로킹 웹 애플리케이션을 개발할 수 있으며, 리액티브 스트림(Flux, Mono)과 리액티브 데이터 액세스를 지원합니다.
> 
> **함수형 엔드포인트(Functional Endpoint) 지원**  
> Spring 5.x에서는 함수형 프로그래밍의 개념을 활용하여 엔드포인트를 정의하는 방식이 추가되었습니다. 
> RouterFunction과 HandlerFunction을 사용하여 더 간결하고 유연한 엔드포인트를 정의할 수 있습니다.
> 
> **반응형 데이터 액세스**  
> Spring 5.x에서는 리액티브 데이터 액세스를 위한 기능이 개선되었습니다. 
> 리액티브 데이터베이스 드라이버와의 통합을 지원하고, R2DBC(Reactive Relational Database Connectivity)를 통해 
> 리액티브 SQL 데이터베이스 액세스를 가능하게 합니다.
> 
> **스프링 부트 2.x와의 통합**  
> Spring 5.x는 Spring Boot 2.x와 밀접하게 통합됩니다. 
> Spring Boot 2.x의 새로운 기능과 업데이트된 버전을 활용할 수 있으며, 더 편리한 애플리케이션 개발을 지원합니다.
> 
> **람다식과 스트림 API의 활용**  
> Spring 5.x에서는 Java 8의 람다식과 스트림 API를 더욱 활용할 수 있습니다. 
> 예를 들어, @FunctionalInterface를 사용하여 함수형 인터페이스를 정의하고, 람다식을 활용하여 콜백 구현을 간소화할 수 있습니다.
> 
> **모듈화의 개선**  
> Spring 5.x에서는 모듈화가 개선되었습니다. 불필요한 의존성을 제거하고 필요한 모듈만 선택적으로 사용할 수 있습니다. 
> 또한, JDK 9의 모듈 시스템과의 통합이 강화되었습니다.
> 
> **보안 강화**  
> Spring 5.x에서는 보안 기능이 강화되었습니다. 
> OAuth 2.0, JWT(JSON Web Token) 등의 인증 및 인가 기능이 개선되었으며, 보안 설정의 편의성과 유연성이 향상되었습니다.
> 
> Spring 5.x는 리액티브 프로그래밍을 지원하고, Java 8의 기능을 최대한 활용하여 더욱 효율적인 개발을 가능하게 합니다. 
> 또한, Spring Boot와의 통합과 모듈화의 개선으로 개발자들에게 더욱 편리한 개발 환경을 제공합니다.

### Spring 6.x
> * Java 17 based on
> * XML 구성 형식은 지원이 안될 수 있음 (점차 Spring에서 제거)
> * 일부 Java EE API 지원 종료
> * RPC 지원 종료
> * 새로운 AOT 엔진 도입
> * Jakarta EE 9+로의 마이그레이션으로 인한 변경
> * Cloud Native

---

## SpringBoot
### Spring Boot 1.0
> Java 1.6 이상  
> Spring Framework 4.0  
> Tomcat: 7.0  

### Spring Boot 2.0
> Java 8 이상  
> Spring Framework 5.0  
> Tomcat: 8.5
> 
> **모듈화 및 조립 가능한 스타터**  
> Spring Boot 2.0에서는 더 세분화된 모듈화와 조립 가능한 스타터(Starter) 기능이 도입되었습니다. 프로젝트에 필요한 모듈과 의존성을 선택하여 시작할 수 있습니다.
> 
> **자동 설정 개선**  
> 자동 설정(Auto-configuration)은 Spring Boot의 강력한 기능 중 하나인데, 2.0에서는 자동 설정이 더욱 향상되었습니다. 
> 자동 설정 기능을 통해 기본적인 설정을 자동으로 수행할 수 있으며, 필요에 따라 사용자 정의 설정을 추가할 수도 있습니다.
> 
> **리액티브 웹 개선**  
> Spring Boot 2.0에서는 Spring WebFlux 와 리액티브 웹 개발을 위한 지원이 크게 개선되었습니다. 
> 이를 통해 비동기 및 논블로킹 웹 애플리케이션을 쉽게 개발할 수 있습니다.
> 
> **테스트 개선**  
> Spring Boot 2.0에서는 테스트 지원이 개선되었습니다. 
> @DataJpaTest, @WebMvcTest 와 같은 어노테이션을 사용하여 필요한 테스트 슬라이스만 로드하여 더 가볍고 빠른 테스트를 수행할 수 있습니다.
> 
> **보안 개선**  
> Spring Boot 2.0에서는 Spring Security의 보안 기능이 개선되었습니다. OAuth 2.0, JWT(JSON Web Token) 등의 인증 및 인가 기능이 
> 업데이트 되었으며, 보안 설정의 편의성과 유연성이 향상되었습니다.
> 
> **Actuator 업데이트**  
> Spring Boot 2.0에서는 Actuator 모듈이 업데이트되었습니다. 애플리케이션의 상태, 메트릭, 로그, 환경 설정 등을 모니터링하고 관리할 수 있는 기능이 개선되었습니다.

### Spring Boot 2.1
> Java 11 지원  
> Spring Framework 5.1  
> Tomcat: 9
> 
> **Kotlin 지원**  
> Spring Boot 2.1부터는 Kotlin 언어를 공식적으로 지원합니다. Kotlin을 사용하여 Spring Boot 애플리케이션을 개발할 수 있습니다.
> 
> **Spring Security 5**  
> Spring Boot 2.1에서는 Spring Security 5가 지원됩니다. 이를 통해 보안 관련 기능을 업그레이드하고 보다 강력한 보안 솔루션을 구현할 수 있습니다.
> 
> **Micrometer 지원**  
> Spring Boot 2.1에서는 애플리케이션의 메트릭(Metrics)을 수집하고 모니터링하기 위한 Micrometer를 지원합니다. 
> 이를 통해 애플리케이션의 성능 모니터링을 쉽게 구성할 수 있습니다.
> 
> **리액티브 웹 클라이언트 개선**  
> Spring Boot 2.1에서는 WebClient 모듈이 업데이트되어 더욱 강력하고 유연한 리액티브 웹 클라이언트를 제공합니다.
> 
> **빠른 시작(Spring Initializr) 개선**  
> Spring Boot 2.1에서는 Spring Initializr를 통한 프로젝트 초기화 과정이 개선되었습니다. 더욱 간편하고 사용자 친화적인 프로젝트 생성을 지원합니다.
> 
> **엔드포인트의 기본 경로 변경**  
> Spring Boot 2.1에서는 액추에이터(Actuator) 엔드포인트의 기본 경로가 변경되었습니다. /actuator 대신 /actuator/* 형식을 사용합니다.
> 
> **통합 테스트 개선**  
> Spring Boot 2.1에서는 통합 테스트 지원이 개선되었습니다. @SpringBootTest 어노테이션을 사용하여 더욱 간편하고 유연한 통합 테스트를 작성할 수 있습니다.
> 
> **지연 로깅 초기화**  
> Spring Boot 2.1에서는 로깅 초기화를 지연시키는 기능이 추가되어 애플리케이션의 시작 속도를 향상시킵니다.

### Spring Boot 2.2
> Java 13 지원  
> Spring Framework 5.2  
> Tomcat: 9
>
> **Spring Data R2DBC 지원**  
> Spring Boot 2.2에서는 Spring Data R2DBC를 지원합니다. R2DBC(Reactive Relational Database Connectivity)를 사용하여 
> 리액티브 SQL 데이터베이스 액세스를 가능하게 합니다.
> 
> **Micronaut과의 통합**  
> Spring Boot 2.2에서는 Micronaut 프레임워크와의 통합이 개선되었습니다. Micronaut과 Spring Boot를 함께 사용하여 각각의 강점을 활용할 수 있습니다.
> 
> **엔드포인트의 변경**  
> Actuator HTTP 추적 및 감사는 기본적으로 비활성화되었습니다.  
> 
> **업데이트된 의존성 버전**  
> Spring Boot 2.2에서는 다양한 의존성 라이브러리의 버전이 업데이트되었습니다. 이를 통해 더 최신의 라이브러리와 기능을 사용할 수 있습니다.
> 
> **개선된 테스트 지원**  
> Spring Boot 2.2에서는 테스트 지원이 개선되었습니다. JUnit 5와의 통합이 강화되었으며, 테스트 슬라이스(Test Slices)를 사용하여 필요한 
> 테스트 스코프만 로드할 수 있습니다.
> 
> **애플리케이션 빌드 개선**  
> Spring Boot 2.2에서는 애플리케이션의 빌드와 패키징 과정이 개선되었습니다. 더 효율적이고 사용자 친화적인 빌드 도구와 프로세스를 지원합니다.
> 
> **새로운 기능 추가**  
> Spring Boot 2.2에는 다양한 새로운 기능이 추가되었습니다. 예를 들어, 더 간편한 데이터베이스 마이그레이션을 위한 Flyway 6.0, 
> 새로운 스프링 배치 기능, 추가적인 보안 설정 옵션 등이 있습니다.  
> 
> **성능 개선**  
> Spring Boot 2.2에서는 성능 개선이 이루어졌습니다. 애플리케이션의 시작 속도와 실행 속도가 향상되었습니다.

### Spring Boot 2.3
> Java 15 지원  
> Spring Framework 5.2  
> Tomcat: 9
>
> **Gradle**  
> Gradle 6.3 이상 지원 (5.6.x는 지원은 하지만 deprecated 됨.)
> 
> **Validation Starter가 WebStarter에 더 이상 포함되지 않는다.**  
> webstart에서 빠졌기 때문에 별도로 gradle에 써주어야 함.
> ```groovy
>     dependencies {
>         ...
>         implementation 'org.springframework.boot:spring-boot-starter-validation'
>     }
> ```
> 
> **Graceful Shutdown**  
> Tomcat 등의 4개의 웹 서버에서 반응형 및 서블렛 기반 웹 응용 프로그램 모두에서 Graceful Shutdown이 지원된다. 
> 사용하려면 `server.shutdown=graceful` 를 활성화한다. 이제 종료 시 웹 서버는 더 이상 새 요청을 허용하지 않고 활성 요청이 완료될 때까지 유예 시간을 기다린다. 
> 유예 시간은 `spring.lifecycle.timeout-per-shutdown-phase` 를 통해 구성할 수 있다.  
> 
> **Java 14 지원**  
> Spring Boot 2.3부터는 Java 14를 공식적으로 지원합니다. Java 14의 기능과 개선 사항을 활용할 수 있습니다.
> 
> **빠른 시작(Spring Initializr) 개선**  
> Spring Boot 2.3에서는 Spring Initializr를 통한 프로젝트 초기화 과정이 개선되었습니다. 더욱 간편하고 사용자 친화적인 프로젝트 생성을 지원합니다.
> 
> **자동 설정 개선**  
> Spring Boot 2.3에서는 일부 자동 설정이 변경되어보다 정확한 조건으로 구성됩니다. 이를 통해 애플리케이션의 동작을 더욱 정확하게 제어할 수 있습니다.
> 
> **새로운 기능 추가**  
> Spring Boot 2.3에는 다양한 새로운 기능이 추가되었습니다. 예를 들어, 새로운 웹 클라이언트 모듈인 WebClient 가 도입되었으며, 
> 새로운 액추에이터(Actuator) 엔드포인트와 기능이 추가되었습니다.  
> 
> **업데이트된 의존성 버전**  
> Spring Boot 2.3에서는 다양한 의존성 라이브러리의 버전이 업데이트되었습니다. 이를 통해 더 최신의 라이브러리와 기능을 사용할 수 있습니다.  
> 
> **도커(Docker) 이미지 빌드 지원 개선**  
> Spring Boot 2.3에서는 도커 이미지 빌드를 위한 기능과 지원이 개선되었습니다. 애플리케이션을 도커 이미지로 더 쉽게 빌드하고 배포할 수 있습니다.
> 
> **RSocket 지원**  
> Spring Boot 2.3에서는 RSocket 프로토콜을 지원합니다. RSocket을 사용하여 더욱 반응적이고 유연한 네트워크 통신을 구현할 수 있습니다.
> 
> **업데이트된 Spring Security**  
> Spring Boot 2.3에서는 Spring Security 의 버전이 업데이트되었습니다. 보안 관련 기능과 설정의 편의성과 유연성이 향상되었습니다.

### Spring Boot 2.4
> Java 15 지원  
> Spring Framework 5.2  
> Tomcat: 9
> 
> **업데이트된 의존성 버전**  
> Spring Boot 2.4에서는 다양한 의존성 라이브러리의 버전이 업데이트되었습니다. 이를 통해 더 최신의 라이브러리와 기능을 사용할 수 있습니다.
> 
> **업데이트된 액추에이터(Actuator)**  
> Spring Boot 2.4에서는 액추에이터(Actuator) 모듈이 업데이트되었습니다. 
> 새로운 엔드포인트와 기능이 추가되었으며, 애플리케이션의 상태 모니터링과 관리를 더욱 쉽게 할 수 있습니다.  
> 
> **HTTP/2 지원**  
> Spring Boot 2.4에서는 HTTP/2 프로토콜을 지원합니다. HTTP/2를 사용하여 더욱 효율적이고 성능이 향상된 웹 애플리케이션을 개발할 수 있습니다.
> 
> **새로운 기능 추가**  
> Spring Boot 2.4에는 다양한 새로운 기능이 추가되었습니다. 예를 들어, GraalVM 네이티브 이미지 빌드 지원, 
> 새로운 웹 클라이언트 모듈인 WebClient의 업데이트, RSocket 지원의 개선 등이 있습니다.  
> 
> **보안 강화**  
> Spring Boot 2.4에서는 보안 관련 기능이 강화되었습니다. 새로운 보안 기능이 추가되었으며, 기존의 보안 설정의 편의성과 유연성이 향상되었습니다.
> 
> **도커(Docker) 지원 개선**  
> Spring Boot 2.4에서는 도커(Docker) 컨테이너 환경에서 애플리케이션을 실행하고 관리하기 위한 기능과 지원이 개선되었습니다.

### Spring Boot 2.5
> Java 16 지원  
> Spring Framework 5.2  
> Tomcat 9  
> Gradle 7.0  
> 
> **업데이트된 의존성 버전**  
> Spring Boot 2.5에서는 다양한 의존성 라이브러리의 버전이 업데이트되었습니다. 이를 통해 더 최신의 라이브러리와 기능을 사용할 수 있습니다.
> 
> **업데이트된 액추에이터(Actuator)**  
> Spring Boot 2.5에서는 액추에이터(Actuator) 모듈이 업데이트되었습니다. 
> 새로운 엔드포인트와 기능이 추가되었으며, 애플리케이션의 상태 모니터링과 관리를 더욱 쉽게 할 수 있습니다.
> 
> **JUnit 5.7**  
> Spring Boot 2.5는 JUnit 5.7을 지원합니다. 이를 통해 테스트 작성과 실행에 대한 새로운 기능과 개선 사항을 활용할 수 있습니다.
> 
> **도커(Docker) 지원 개선**  
> Spring Boot 2.5에서는 도커(Docker) 컨테이너 환경에서 애플리케이션을 실행하고 관리하기 위한 기능과 지원이 개선되었습니다.
> 
> **새로운 기능 추가**  
> Spring Boot 2.5에는 다양한 새로운 기능이 추가되었습니다. 
> 예를 들어, 더 나은 리액티브 지원을 위한 R2DBC 와 Spring WebFlux 의 개선, GraalVM 네이티브 이미지의 개선, 애플리케이션 실행 로그의 개선 등이 있습니다.
> 
> **성능 개선**  
> Spring Boot 2.5에서는 애플리케이션의 시작 속도와 실행 속도가 개선되었습니다. 더 빠른 시작 및 응답 시간을 제공합니다.
> 
> **보안 강화**  
> Spring Boot 2.5에서는 보안 관련 기능이 강화되었습니다. 새로운 보안 기능이 추가되었으며, 기존의 보안 설정의 편의성과 유연성이 향상되었습니다.
> 
> **의존성 관리 업데이트**  
> Spring Boot 2.5에서는 의존성 관리 기능이 업데이트되었습니다. 라이브러리 의존성의 버전 충돌을 해결하고 최신 버전의 의존성을 사용할 수 있도록 도움을 줍니다.
> 
> 이 외에도 다양한 버그 수정, 기능 개선, 문서 업데이트 등이 포함되어 있습니다.

### Spring Boot 2.6
> **Java Runtime 정보**  
> info endpoint는 이제 아래 예시와 같이 Java Runtime 정보를 노출합니다.
> ```json
> {
>     "java": {
>         "vendor": "BellSoft",
>         "version": "17",
>         "runtime": {
>             "name": "OpenJDK Runtime Environment",
>             "version": "17+35-LTS"
>         },
>         "jvm": {
>             "name": "OpenJDK 64-Bit Server VM",
>             "vendor": "BellSoft",
>             "version": "17+35-LTS"
>         }
>     }
> }
> ```
> info endpoint 응답에서 이 정보를 노출하려면 `management.info.java.enabled` 속성을 true로 설정합니다.  
> 
> **Redis Connection Pooling**  
> Redis(Jedis와 Lettuce 모두)는 이제 commons-pool2가 클래스 경로에 있을 때 풀링을 자동으로 활성화한다.  
> 필요한 경우 풀링을 비활성화하려면 `spring.redis.jedis.pool.enabled` 또는 `spring.redis.lettuce.pool.enabled`를 false로 설정한다.  
> 
> **자동 구성된 Spring Web Service Server Tests**
> 웹 서비스 @Endpoint 빈을 테스트하는 데 사용할 수 있는 새로운 주석 `@WebServiceServerTest` 가 도입되었음.  
> 주석은 @Endpoint 빈을 포함하는 테스트 슬라이스를 생성하고 웹 서비스 엔드포인트를 테스트하는 데 사용할 수 있는 `MockWebServiceClient` 빈을 자동 구성함.  
> 
> **Spring MVC 테스트를 위해 WebTestClient 사용**  
> 개발자는 WebTestClient를 사용하여 모의 환경에서 WebFlux 앱을 테스트하거나 라이브 서버에 대해 모든 Spring 웹 앱을 테스트할 수 있다.  
> 이 변경은 또한 모의 환경에서 Spring MVC용 WebTestClient를 활성화한다.  
> `@AutoConfigureMockMvc`로 주석이 달린 클래스는 `WebTestClient`를 주입할 수 있다.  

### Spring Boot 2.7
> Spring Framework 5.3  
> Spring security 5.7  
> Tomcat 9
>
> **WebSecurityConfigurerAdapter에서 SecurityFilterChain으로 마이그레이션**  
> Spring Boot 2.7은 WebSecurityConfigurerAdapter를 더 이상 사용하지 않는 Spring Security 5.7로 업그레이드한다.  
> WebSecurityConfigurerAdapter 없이 Spring Security를 설정하고 @WebMvcTest 와 같은 Spring Boot의 슬라이스 테스트를 사용할 때, 
> 보안 구성 클래스를 @Import 하여 테스트에서 SecurityFilterChain 빈을 사용할 수 있도록 하려면 애플리케이션을 약간 변경해야 할 수도 있다.

### Spring Boot 3.0
> * Spring Boot 3.0은 Spring Framework 6.0을 기반으로 한다.    
> * 최소 요구사항 변경  
> Gradle 7.5  
> Groovy 4.0  
> Jakarta EE 9  
> Java 17  
> Kotlin 1.6  
> Hibernate 6.1  
>
> * Spring Framework 6: AOT(Ahead Of Time) maven, gradle 플러그인 제공, 
> Spring AOT 엔진은 빌드 시 스프링 어플리케이션을 분석하고 최적화하여 런타임 시 인프라 자원을 적게 사용
> 
> * Native 지원 기능 확대
