FROM openjdk:11
ADD target/*.jar spring-boot.jar
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "spring-boot.jar"]