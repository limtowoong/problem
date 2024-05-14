# 문제 상황

DataSourceUtils가 import되지 않음

<br>

# 해결 방법

`build.gradle`에 아래 두개 추가

- implementation 'org.springframework.boot:spring-boot-starter-jdbc'
- runtimeOnly 'com.h2database:h2'

<br>

Gradle 새로고침

- build.gradle -> Gradle -> Refresh Gradle Project
