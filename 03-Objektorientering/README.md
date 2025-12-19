# Kapitel 3: Objektorientering (OOP)

Detta är kursens absolut viktigaste del. Vi ska lära oss bygga egna objekt.

### Steg 1: Titta på dessa videos
Dessa videos är korta men visar exakt hur det går till.
* **Objects (OOP):** [Bro Code - Objects (OOP)](https://www.youtube.com/watch?v=DYbi93vuSaU)
* **Constructors (Hur man skapar objektet):** [Bro Code - Constructors](https://www.youtube.com/watch?v=ZD7CB6wKg8A)
* **Encapsulation (Getters & Setters):** [Bro Code - Encapsulation #31](https://www.youtube.com/watch?v=OjrR_C_UPjc)

### Uppgift A: Bilen
1. Skapa en klass `Car`.
2. Ge den variablerna `String model` och `int year`.
3. Skapa en **Konstruktor** så du kan göra så här i Main: `new Car("Volvo", 2020);`.

### Uppgift B: Säkerhet (Getters & Setters) - VIKTIGT!
Vi vill inte att någon ska kunna sätta årstalet till -500. Vi måste skydda datan!
1. Ändra variablerna i `Car` från `String` till `private String` (och samma för `int`).
2. Försök nå dem från Main (det ska bli rött felmeddelande!).
3. Skapa **Getters** och **Setters** i Car-klassen (IntelliJ kan göra detta åt dig: Högerklicka -> Generate -> Getter and Setter).
4. Använd settern i Main för att ändra året.

### Checklista
- [ ] Jag kan skapa en Klass och ett Objekt.
- [ ] Jag förstår varför `private` gör koden säkrare.
- [ ] Jag kan använda `get` och `set` för att komma åt datan.