FROM eclipse-temurin:17-jdk-jammy

WORKDIR /app

# Clone the repository and build
RUN apt-get update && \
    apt-get install -y git && \
    git clone https://github.com/spring-projects/spring-petclinic.git . && \
    ./mvnw package && \
    rm -rf /root/.m2 && \
    apt-get remove -y git && \
    apt-get autoremove -y && \
    apt-get clean

EXPOSE 8080
CMD java -jar target/spring-petclinic-*.jar

# Test CI/CD workflow
