per far partire tutto nel terminale fate

1. ./gradlew clean shadowJar
2. ls build/libs (per verificare se ha creato il file .jar)
3. (opzionale) se esiste il .jar potete provarlo manualmente senza il docker con java -jar build/libs/RouteAnalyzer-all.jar
4. docker build -t route-analyzer .
5. docker run -v $(PWD)/custom-parameters.yml:/app/custom-parameters.yml route-analyzer
