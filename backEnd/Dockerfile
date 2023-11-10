FROM openjdk:17
COPY . ./
COPY wait-for-it.sh ./wait-for-it.sh
RUN chmod +x wait-for-it.sh
CMD java -jar backend.jar

