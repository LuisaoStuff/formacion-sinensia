FROM openjdk:16-jdk as javaBuilder
COPY . /build
WORKDIR /build
RUN ./gradlew assemble

FROM openjdk:16-jdk
ARG JAR_FILE=build/libs/*.jar
COPY --from=javabuilder /build/${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
