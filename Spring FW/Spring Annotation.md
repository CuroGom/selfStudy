# Spring Annotation 정리

## 중요  Annotation

### @Required

Setter Method에 부여하여 특정 프로퍼티를 필수로 설정 하도록 하는 Annotation

사용 하기 전에 Bean 사전 작업 필수
<bean class="org.springframework.beans.factory.annotation.RequireAnnotationBeanPostProcessor" />
혹은 <context:annotion-config /> 

### @Autowired

의존성을 주입, 자동으로 객체를 생성하며 메소드 위에 생성 시 기본 생성자를 생성

### @Resource

Autowired + Qualifier 형태로, @Resource("BeanName") 형식으로 사용

### @Inject

Autowired와 유사하며, Standard 한 Annotation (다른 FW에서는 Autowired보단 Inject를 사용하는 것이 일반적 )

### @Service

@Component의 하위 계층이며, Service 객체임을 명시

### @Repository

@Component의 하위 계층이며, DAO 객체임을 명시

### @Controller

Spring MVC Controller 객체임을 나타내는 Annotation

### @RequestMapping

특정 URI에 매칭되는 클래스 / 메소드임을 명시

### @RequestParam

요청에서 특정한 파라미터의 값을 나타내거나, 초기값을 설정 할 때 사용하는 Annotation
@RequestParam(value="변수명", defaultValue="초기값")

### @SessionAttributes

세션상에서 모델의 정보를 유지하고 싶은 경우에 사용? (조사 필요)

### @RequestBody

request 문자열이 그대로 parameter로 전달

### @ResponseBody

return을 HTTP의 응답 메시지로 전송

### @PathVariable

현재의 URI에서 원하는 정보를 추출? (조사 필요)

## 참고 Annotation

### @Component

Autowired 할 클래스 위에 표시하는 Annotation이지만,
기본적으론 Component-scan xml 설정을 활용하여 자동 주입 시키는게 일반적

### @Qualifier

Autowired의 강화판? 특정 Bean을 지정해서 Mapping
@Autowired 아래 @Quailfier("BeanName") 형식으로 사용

### @Scope

Spring FW에서는 기본적으로 Bean의 범위를 singleton으로 설정 하는데, 다른 범위를 지정하여 사용하고 싶을 땐,
해당 Annotation을 사용하여 범위를 변경 할 수 있다.

### @PostConstruct

초기화 작업을 수행하는 Annotation? (조사 필요)

### @PreDestory

컨테이너에서 객체를 제거하기 전, 해야할 작업을 수행하기 위해 사용

## 기타 조사 Annotiaton

### @Asepect

### @Pointcut

### @Around

### @ModelAttribute