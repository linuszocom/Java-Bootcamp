# Slutprojekt: JavaBanken (Examination)

Här ska du bygga en **Bank-applikation**. Detta projekt är större än de tidigare övningarna och kräver att du sätter ihop allt du lärt dig.

För att få **Godkänt** på kursen måste din kod fungera och uppfylla kraven nedan.

---

## Uppdraget
Du är anställd som Backend-utvecklare på "JavaBanken". Din chef vill ha ett system där man kan hantera olika typer av konton (Sparkonton och Kreditkort).

Systemet ska kunna:
1. Skapa nya konton.
2. Sätta in och ta ut pengar.
3. Hålla koll på saldot (och se till att man inte tar ut pengar man inte får ta ut!).

---

## Tekniska Krav (Måste finnas med)

För att bevisa att du kan Objektorientering måste du bygga koden enligt denna struktur:

### 1. Arv (Inheritance)
Du ska använda Arv för att slippa skriva samma kod flera gånger.

* **`BankAccount` (Förälder-klass)**
    * Denna klass innehåller det som alla konton har gemensamt:
        * `accountNumber` (String eller int)
        * `balance` (double) - *Saldot*
        * `customerName` (String)
    * Den ska ha metoderna `deposit()` och `withdraw()`.

* **`SavingsAccount` (Subklass)**
    * Ärver från BankAccount.
    * Detta är ett vanligt konto. Man får **aldrig** ha negativt saldo här. (Du måste spärra uttag om saldot blir < 0).

* **`CreditCard` (Subklass)**
    * Ärver från BankAccount.
    * Har en extra egenskap: `creditLimit` (t.ex. 5000 kr).
    * Här **får** saldot bli negativt, men bara ner till gränsen. Om man försöker ta ut för mycket ska köpet nekas.

### 2. Inkapsling (Encapsulation) - Jätteviktigt!
Detta är säkerhet. Ingen ska kunna ändra saldot genom att skriva `konto.balance = 1000000;`.
* Variabeln `balance` i din basklass ska vara **`private`**.
* Man får bara ändra saldot genom att använda dina metoder `deposit()` och `withdraw()`.
* Använd en **Getter** (`getBalance()`) för att se hur mycket pengar som finns.

### 3. Polymorfism & Listor
* Alla konton som skapas (oavsett om det är Sparkonto eller Kreditkort) ska sparas i **en gemensam lista**: `ArrayList<BankAccount>`.

---

## Hur programmet ska fungera (Menyn)

När du kör din `Main`-fil ska programmet starta en loop som visar en meny:

```text
VÄLKOMMEN TILL JAVABANKEN
-------------------------
1. Skapa nytt konto
2. Sätt in pengar
3. Ta ut pengar
4. Visa saldo & info för alla konton
5. Avsluta
Ange val:
```
### Specifika instruktioner för menyn

* **Val 1:** Fråga användaren: *"Vill du skapa ett Sparkonto (1) eller Kreditkort (2)?"*. Fråga efter namn och kontonummer.
* **Val 3:** När man tar ut pengar måste programmet kontrollera: *"Finns det täckning?"*. Om inte, skriv ut: *"Medges ej!"*.

---

## Steg-för-steg guide (Så här börjar du)

Att bygga allt på en gång är svårt. Gör så här:

1.  **Steg 1 - Grunden:** Skapa klassen `BankAccount` med `private balance`. Gör en enkel `deposit`-metod.
2.  **Steg 2 - Arvet:** Skapa `SavingsAccount` och `CreditCard`. Se till att de ärver (`extends`) från `BankAccount`.
3.  **Steg 3 - Logiken:** Skriv koden för `withdraw` i de olika klasserna.
    * I Sparkontot: `if (balance - amount < 0) { ...stoppa... }`
    * I Kreditkortet: `if (balance - amount < creditLimit) { ...stoppa... }`
4.  **Steg 4 - Main:** Skapa din `ArrayList` och bygg menyn (`while`-loop och `switch`/`if`).
5.  **Steg 5 - Testa:** Försök att "hacka" din egen bank. Vad händer om du tar ut 1 miljon? Vad händer om du sätter in negativa pengar?

---

## Checklista för Inlämning

Innan du spelar in din video, kolla att du kan kryssa i alla dessa:

- [ ] Jag har en basklass (`BankAccount`) och två subklasser.
- [ ] Mina variabler (särskilt `balance`) är `private`.
- [ ] Jag använder Getters/Setters där det behövs.
- [ ] Jag sparar alla mina objekt i en `ArrayList`.
- [ ] Det går inte att ta ut mer pengar än vad reglerna tillåter (saldot skyddas).
- [ ] Programmet kraschar inte när jag kör det.

---

## Så här lämnar du in

1.  Se till att all kod ligger på GitHub.
2.  Skicka länk till ditt github repo till Linus på discord



