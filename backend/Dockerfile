FROM openjdk:17-alpine
# RUN addgroup -S spring && adduser -S spring -G spring
# USER spring:spring
RUN apk add --no-cache maven
WORKDIR /app
COPY . /app
RUN mvn clean install
RUN cp /app/target/*.jar /app/app.jar


ENTRYPOINT ["java","-jar","/app/app.jar"]
