






## BDD-Testscenarion för CityController

- **Scenario**: Användare hämtar alla städer
    - **Givet**: Att API:t har tillgång till stadinformation
    - **När**: En GET-förfrågan görs till endpointen "/api/cities"
    - **Så**: Ska ett svar med status OK returneras som innehåller en lista över städer

## BDD-Testscenarion för CityRepository

- **Scenario**: Spara och hitta en stad i repository
    - **Givet**: En ny stad med namnet "TestCity" har skapats
    - **När**: Staden sparas i databasen och en sökning görs
    - **Så**: Ska staden "TestCity" hittas i databasen

## BDD-Testscenarion för CityService

- **Scenario**: Hämta alla städer via servicen
    - **Givet**: Att `CityRepository` innehåller städerna "Stockholm" och "Göteborg"
    - **När**: Metoden `getAllCities` anropas i `CityService`
    - **Så**: Ska en lista som innehåller "Stockholm" och "Göteborg" returneras

## BDD-Testscenarion för City Entity

- **Scenario**: Sätt och verifiera stadens ID
    - **Givet**: En ny `City`-instans skapas
    - **När**: ID-värdet sätts till 1
    - **Så**: Ska `getId` metoden returnera 1

- **Scenario**: Sätt och verifiera stadens namn
    - **Givet**: En ny `City`-instans skapas
    - **När**: Namnet sätts till "Stockholm"
    - **Så**: Ska `getName` metoden returnera "Stockholm"

## BDD-Testscenarion för Applikationskontext

- **Scenario**: Ladda Spring-applikationskontext
    - **Givet**: En Spring Boot-applikation är korrekt konfigurerad
    - **När**: Applikationskontexten initialiseras
    - **Så**: Ska inga fel uppstå och applikationen ska starta framgångsrikt

## BDD-Testscenarion för Weather Entity

- **Scenario**: Sätt och verifiera stadens namn i väderdata
    - **Givet**: Ett nytt `Weather`-objekt skapas
    - **När**: Stadens namn sätts till "Stockholm"
    - **Så**: Ska `getCityName` metoden returnera "Stockholm"

- **Scenario**: Sätt och verifiera temperatur i väderdata
    - **Givet**: Ett nytt `Weather`-objekt skapas
    - **När**: Temperaturen sätts till 10.5
    - **Så**: Ska `getTemperature` metoden returnera 10.5

- **Scenario**: Sätt och verifiera väderbeskrivning
    - **Givet**: Ett nytt `Weather`-objekt skapas
    - **När**: Beskrivningen sätts till "Sunny"
    - **Så**: Ska `getDescription` metoden returnera "Sunny"