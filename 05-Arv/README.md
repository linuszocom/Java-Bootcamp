# Kapitel 5: Arv (Inheritance)

Arv handlar om att återanvända kod. En "Bil" är ett "Fordon". En "Cykel" är också ett "Fordon". Vi samlar det gemensamma i en förälder-klass.

### Steg 1: Titta på video
* **Inheritance:** [Bro Code - Inheritance](https://www.youtube.com/watch?v=GTP5lVEKXaU)
* **Inheritance:** [Bro Code - Polymorphism](https://www.youtube.com/watch?v=6xRd0j1anzc)

### Uppgift A: Djurparken (Arv)
1. Skapa en klass `Animal` med variabeln `String name`.
2. Skapa `Dog` och `Cat` som ärver från Animal (`extends Animal`).
3. I Main: Skapa en hund och en katt.

### Uppgift B: Läten (Polymorfism) - VIKTIGT!
Här ska vi se magin med att behandla Hundar och Katter som bara "Djur".
1. I klassen `Animal`, skapa metoden `void makeSound()` som skriver *"Animal makes a sound"*.
2. I `Dog` och `Cat`, **överskugga (Override)** metoden så de säger *"Voff"* respektive *"Mjau"*.
3. **Polymorfism-testet:**
    - Skapa en lista av typen Animal: `ArrayList<Animal> myAnimals = new ArrayList<>();`
    - Lägg in din hund och din katt i listan (Det funkar eftersom båda ÄR djur!).
    - Loopa igenom listan och kör `.makeSound()` på alla.
    - *Resultat:* Trots att listan bara ser "Animals", så kommer hunden skälla och katten jama. Det är Polymorfism!

### Checklista
- [ ] Jag förstår ordet `extends`.
- [ ] Jag förstår att en `Dog` också kan ses som ett `Animal` (Polymorfism).