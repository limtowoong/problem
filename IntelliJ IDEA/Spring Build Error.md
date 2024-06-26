# 문제 코드

A problem occurred configuring root project 'hello-spring'. > Could not resolve all artifacts for configuration ':classpath'. > Could not resolve org.springframework.boot:spring-boot-gradle-plugin:3.2.5. Required by: project : > org.springframework.boot:org.springframework.boot.gradle.plugin:3.2.5 > No matching variant of org.springframework.boot:spring-boot-gradle-plugin:3.2.5 was found. The consumer was configured to find a library for use during runtime, compatible with Java 11, packaged as a jar, and its dependencies declared externally, as well as attribute 'org.gradle.plugin.api-version' with value '8.7' but: - Variant 'apiElements' declares a library, packaged as a jar, and its dependencies declared externally: - Incompatible because this component declares a component for use during compile-time, compatible with Java 17 and the consumer needed a component for use during runtime, compatible with Java 11 - Other compatible attribute: - Doesn't say anything about org.gradle.plugin.api-version (required '8.7') - Variant 'javadocElements' declares a component for use during runtime, and its dependencies declared externally: - Incompatible because this component declares documentation and the consumer needed a library - Other compatible attributes: - Doesn't say anything about its elements (required them packaged as a jar) - Doesn't say anything about its target Java version (required compatibility with Java 11) - Doesn't say anything about org.gradle.plugin.api-version (required '8.7') - Variant 'mavenOptionalApiElements' declares a library, packaged as a jar, and its dependencies declared externally: - Incompatible because this component declares a component for use during compile-time, compatible with Java 17 and the consumer needed a component for use during runtime, compatible with Java 11 - Other compatible attribute: - Doesn't say anything about org.gradle.plugin.api-version (required '8.7') - Variant 'mavenOptionalRuntimeElements' declares a library for use during runtime, packaged as a jar, and its dependencies declared externally: - Incompatible because this component declares a component, compatible with Java 17 and the consumer needed a component, compatible with Java 11 - Other compatible attribute: - Doesn't say anything about org.gradle.plugin.api-version (required '8.7') - Variant 'runtimeElements' declares a library for use during runtime, packaged as a jar, and its dependencies declared externally: - Incompatible because this component declares a component, compatible with Java 17 and the consumer needed a component, compatible with Java 11 - Other compatible attribute: - Doesn't say anything about org.gradle.plugin.api-version (required '8.7') - Variant 'sourcesElements' declares a component for use during runtime, and its dependencies declared externally: - Incompatible because this component declares documentation and the consumer needed a library - Other compatible attributes: - Doesn't say anything about its elements (required them packaged as a jar) - Doesn't say anything about its target Java version (required compatibility with Java 11) - Doesn't say anything about org.gradle.plugin.api-version (required '8.7') * Try: > Review the variant matching algorithm at https://docs.gradle.org/8.7/userguide/variant_attributes.html#sec:abm_algorithm. > No matching variant errors are explained in more detail at https://docs.gradle.org/8.7/userguide/variant_model.html#sub:variant-no-match. > Run with --stacktrace option to get the stack trace. > Run with --info or --debug option to get more log output. > Run with --scan to get full insights. > Get more help at https://help.gradle.org.

<br>

# 발생 원인

- IntelliJ에 jdk 설정을 하지 않아서 같다

<br>

# 해결법

![image](https://github.com/limtowoong/study/assets/104752202/47346461-09c6-43b1-ab3d-112b4160863e)

- IntelliJ 설정 열기 -> 빌드, 실행, 환경 -> 빌드 도구 -> Gradle

<br>

![image](https://github.com/limtowoong/study/assets/104752202/14631096-2b68-4b5b-95a0-0d917636cecc)

- 처음에 들어오면 이렇게 되어있을거다.

<br>

![image](https://github.com/limtowoong/study/assets/104752202/222167b2-4fd4-44fb-bb5b-78885e980f41)

- Gradle에서 IntelliJ IDEA로 변경해준다.

<br>

https://www.oracle.com/java/technologies/downloads/#jdk17-windows 에서 jdk 17 다운로드

<br>

![image](https://github.com/limtowoong/study/assets/104752202/1b84140c-afc0-4507-b1fa-ca7b8604156c)

- Gradle JVM 설정

<br>

![image](https://github.com/limtowoong/study/assets/104752202/0d723e90-bf02-4ff0-83d7-8732aece7f9d)

- IntelliJ 파일 메뉴 열기 -> 프로젝트 구조

<br>

![image](https://github.com/limtowoong/study/assets/104752202/104f1349-a749-4ce2-ac9d-dd337e2edde3)

- 프로젝트 설정 -> 프로젝트 -> SDK 변경
