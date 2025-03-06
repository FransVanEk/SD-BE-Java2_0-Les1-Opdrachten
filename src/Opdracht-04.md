# Opdracht 4 - Meerdere namen opslaan met een array

In deze opdracht gaan we een programma schrijven waarin de gebruiker **drie namen** invoert en deze vervolgens worden weergegeven. Dit keer gebruiken we een **array** om de namen op te slaan.

---

## **Stap 1: Een nieuwe class aanmaken**
1. Open je bestaande Java-project in **IntelliJ IDEA**.
2. Ga in de **Project View** naar de `src` map.
3. Klik met de **rechtermuisknop** op `src` → **New** → **Java Class**.
4. Geef de class de naam `Opdracht4` en druk op **Enter**.

Nu heb je een lege Java-class. De volgende stap is om er code in te schrijven.

---

## **Stap 2: Code schrijven**

Schrijf een programma waarin de gebruiker **drie namen** invoert en deze vervolgens worden weergegeven.

➡️ **Denk eerst na:**
- Hoe sla je meerdere namen op?
- Hoe vraag je drie keer een invoer aan de gebruiker?
- Hoe toon je elke naam op het scherm?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
import java.util.Scanner;

public class Opdracht4 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String[] namen = new String[3];
        
        System.out.print("Voer de eerste naam in: ");
        namen[0] = scanner.nextLine();
        
        System.out.print("Voer de tweede naam in: ");
        namen[1] = scanner.nextLine();
        
        System.out.print("Voer de derde naam in: ");
        namen[2] = scanner.nextLine();
        
        System.out.println("De ingevoerde namen zijn:");
        System.out.println("1: " + namen[0]);
        System.out.println("2: " + namen[1]);
        System.out.println("3: " + namen[2]);
    }
}
```
</details>

---

## **Stap 3: Het programma uitvoeren**
1. Klik op de groene **play-knop** naast `main` in `Opdracht4.java`.
2. Voer drie namen in wanneer daarom wordt gevraagd.
3. Je ziet de uitvoer:
   ```
   Voer de eerste naam in: Alice
   Voer de tweede naam in: Bob
   Voer de derde naam in: Charlie
   De ingevoerde namen zijn:
   1: Alice
   2: Bob
   3: Charlie
   ```

---

## **Stap 4: Hoe kan dit nog beter?**
In plaats van losse variabelen te gebruiken, slaan we nu de namen op in een **array**. Dit maakt het eenvoudiger om later aanpassingen te doen, zoals het uitbreiden van het aantal namen.

In een volgende lessen leer je hoe je dit kunt automatiseren met een **loop** zodat je eenvoudig meer namen kunt toevoegen zonder extra code te schrijven.

---

## **Stap 5: Uitdagingen**
Probeer nu zelf de volgende aanpassingen te maken:
- Voeg een **vierde naam** toe en toon deze ook.

