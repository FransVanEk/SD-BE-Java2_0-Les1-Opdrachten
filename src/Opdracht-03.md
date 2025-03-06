# Opdracht 3 - Namenlijst in Java

In deze opdracht gaan we een programma schrijven dat de gebruiker vraagt om namen in te voeren en ze vervolgens weergeeft. Je hebt al een IntelliJ-project gemaakt in de vorige opdracht. Nu ga je een derde class aanmaken en stap voor stap ontdekken hoe de code werkt.

---

## **Stap 1: Een nieuwe class aanmaken**
1. Open je bestaande Java-project in **IntelliJ IDEA**.
2. Ga in de **Project View** naar de `src` map.
3. Klik met de **rechtermuisknop** op `src` → **New** → **Java Class**.
4. Geef de class de naam `Opdracht3` en druk op **Enter**.

Nu heb je een lege Java-class. De volgende stap is om er code in te schrijven.

---

## **Stap 2: Werken met Arrays en Loops**

In deze opdracht gaan we:
- **Meerdere namen opslaan** in een **array**.
- **Een for-loop gebruiken** om de gebruiker meerdere keren om invoer te vragen.
- **De namen weergeven** met een tweede loop.

### **1. Hoe sla je meerdere waarden op?**
Je kunt een **array** gebruiken om meerdere waarden van hetzelfde type op te slaan.

```java
String[] namen = new String[3]; // Een array die 3 namen kan opslaan
```

<details>
  <summary>💡 Klik hier voor meer uitleg</summary>
  - Arrays zijn lijsten van variabelen van hetzelfde type.
  - `new String[3]` betekent dat we **een array maken** die **drie** namen kan opslaan.
  - Elk element in de array heeft een **index**: `namen[0]`, `namen[1]`, `namen[2]`.
</details>

### **2. Hoe vraag je de gebruiker om meerdere invoeren?**
We gebruiken een **for-loop** om **drie keer** de gebruiker om een naam te vragen.

```java
for (int i = 0; i < 3; i++) {
    System.out.print("Voer naam " + (i + 1) + " in: ");
    namen[i] = scanner.nextLine();
}
```

<details>
  <summary>💡 Klik hier voor meer uitleg</summary>
  - `for (int i = 0; i < 3; i++)` zorgt ervoor dat de code **drie keer** wordt uitgevoerd.
  - `System.out.print("Voer naam " + (i + 1) + " in: ");` toont een vraag aan de gebruiker.
  - `namen[i] = scanner.nextLine();` slaat de ingevoerde naam op in de array.
</details>

### **3. Hoe toon je de ingevoerde namen?**
We gebruiken een **enhanced for-loop** om alle namen weer te geven.

```java
for (String naam : namen) {
    System.out.println("Naam: " + naam);
}
```

<details>
  <summary>💡 Klik hier voor meer uitleg</summary>
  - `for (String naam : namen)` betekent **loop door elk element in de array**.
  - `System.out.println("Naam: " + naam);` print elke naam op een nieuwe regel.
</details>

Nu we dit begrijpen, kunnen we de code schrijven!

---

## **Stap 3: Code schrijven**

Schrijf een programma dat de gebruiker vraagt om drie namen in te voeren en ze daarna toont.

➡️ **Denk eerst na:**
- Hoe maak je een array aan?
- Hoe vraag je de gebruiker om input met een loop?
- Hoe toon je de gegevens op het scherm?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
import java.util.Scanner;

public class Opdracht3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String[] namen = new String[3];
        
        for (int i = 0; i < 3; i++) {
            System.out.print("Voer naam " + (i + 1) + " in: ");
            namen[i] = scanner.nextLine();
        }
        
        for (String naam : namen) {
            System.out.println("Naam: " + naam);
        }
    }
}
```
</details>

---

## **Stap 4: Het programma uitvoeren**
1. Klik op de groene **play-knop** naast `main` in `Opdracht3.java`.
2. Voer in de console drie namen in (bijvoorbeeld `Alice`, `Bob` en `Charlie`).
3. Je ziet de uitvoer:
   ```
   Voer naam 1 in: Alice
   Voer naam 2 in: Bob
   Voer naam 3 in: Charlie
   Naam: Alice
   Naam: Bob
   Naam: Charlie
   ```

---

## **Stap 5: Uitdagingen**
Probeer nu zelf de volgende aanpassingen te maken:
- Laat de gebruiker **vijf** namen invoeren in plaats van drie.
- Toon de namen in **omgekeerde volgorde**.
- Controleer of de gebruiker iets heeft ingevuld en geef een foutmelding als de invoer leeg is.

Test je aanpassingen en kijk of je begrijpt hoe de uitvoer verandert.

Veel succes! 🚀

