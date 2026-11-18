
# Stage 1: Compile Java application
FROM eclipse-temurin:21-jdk AS build

WORKDIR /app

COPY Main.java .

RUN javac Main.java

# Stage 2: Run compiled application
FROM eclipse-temurin:21-jre

WORKDIR /app

COPY --from=build /app/Main.class .

CMD ["java", "Main"]
