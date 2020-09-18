FROM maven:3.5-jdk-8-alpine AS builder
WORKDIR /worker
COPY . .
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
WORKDIR /app
COPY --from=builder /worker/target/ .
CMD [ "java", "-jar", "worker-jar-with-dependencies.jar" ]