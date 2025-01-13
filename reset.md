## När det gått åt skogen ett par gånger kan det vara bra att renda Docker helt.

1. Se till att du står i ditt projekt i terminalen.
2. Stoppa och ta bort containrarna för just detta projekt, -v tar bort hela volymen också:
   **docker-compose down -v**
3. Kör sedan detta, men OBS! det här påverkar build cahce för ALLA projekt. Ingen fara nu i början när vi inte har några andra:
   **docker builder prune -f**
4. Vill du endast ta bort build cahce för just detta projekt kan du köra:
    **docker-compose build --no-cache**
5. Starta sedan detached instance så att vi kan starta Spring Boot i IntelliJ:
   **docker-compose up -d**

   Postgres ska starta men inte Spirng Boot, den startar vi själva.
