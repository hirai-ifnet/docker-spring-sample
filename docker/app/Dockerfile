FROM eclipse-temurin:17-jdk-alpine
ARG APP_ROOT=/opt/app
RUN mkdir $APP_ROOT
COPY . $APP_ROOT
WORKDIR $APP_ROOT
ENTRYPOINT ["sh", "./gradlew", "bootRun"]
