FROM openjdk:11
VOLUME /tmp
ADD build/libs/helloworld-*-all.jar target/app.jar
EXPOSE 8080
RUN bash -c 'touch target/app.jar'
CMD ["java", "-Xms512m", "-Xmx4096m", "-Xlog:gc:/target/app-gc.log", "-Xlog:gc*", "-jar", "target/app.jar"]