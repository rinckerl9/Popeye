FROM maven:3.5-jdk-8-alpine AS builder

WORKDIR /app/worker

COPY . .

RUN mvn dependency:resolve

RUN mvn package

FROM openjdk:8-jre-alpine

COPY --from=builder /app/worker/target/worker-jar-with-dependencies.jar .

CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]