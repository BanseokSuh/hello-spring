# Spring 입문 학습 repository

- Spring Boot를 사용하여 간단한 웹 어플리케이션 개발

- 사용 기술
  - Spring Boot
  - JPA
  - Tomcat
  - Gradle
  - Hibernate
  - Thymeleaf

<br>

---

# Note

## Spring Boot 프로젝트 생성
- https://start.spring.io
- 설정 후 GENERATE 하면 .zip 파일이 다운로드됨
- 해당 파일 압축 풀고 IntelliJ로 해당 폴더 열기
- Project: 라이브러리 관리 툴 선택. 요즘은 Gradle을 많이 사용함
- Project Meta Data
  - Group: 기업명
  - Artifact: 프로젝트명
- Dependencies (중요)
  - 프로젝트 생성 시 어떤 라이브러리를 가져올 것인지 선택
- build.gradle (중요)
  - 버전 설정
  - 라이브러리 다운로드 주소

<br>

## 프로젝트 실행
- src > main > java 디렉토리에 있는 HelloSpringApplication.java에서 main 메서드 실행
- Tomcat started on port(s): 8080 (http)
- main 메서드 실행 시 내장된 tomcat 웹 서버를 띄우면서 Spring Boot가 같이 올라옴
- IntelliJ에서는 서버 구동 시 Java가 Gradle을 통해서 실행되는 것이 기본임. 그러면 실행 속도가 느림.
- preference에서 Java 실행 도구를 Gradle에서 IntelliJ로 변경하면, Gradle을 통하지 않고 IntelliJ에서 바로 java를 실행시켜서 더 빨라짐
- Preferences > Build, Execution, Deployment > Build Tools > Gradle
  - Build and run using: Gradle > IntelliJ IDEA
  - Run tests using: Gradle > IntelliJ IDEA

<br>

## 라이브러리 의존
- 라이브러리A에 대한 의존성을 주입받으면, A가 의존하고 있는 다른 라이브러리들도 주입받게 됨
- Tomcat
  - 웹 서버 라이브러리
  - 이전에는 Tomcat 서버에 자바 소스코드를 밀어넣어서 서버를 띄움
  - 하지만 이제는 Tomcat 서버가 내장되어 있어서 main 메서드 실행 시 서버 띄울 수 있음
- Log
  - 현없에서는 System.out.println() 안 씀
  - logging으로 출력해야 중요 로그가 관리가 됨
  - slf4j, logback을 주로 사용
- Test
  - junit5
  - assertj

<br>



<br>
<br>
<br>
<br>
<br>
