# Opdracht 5 - Namen en huisdieren opslaan met een multidimensionale array

In deze opdracht gaan we een programma schrijven waarin de gebruiker **drie namen en hun huisdieren** invoert en deze vervolgens worden weergegeven. Dit keer gebruiken we een **multidimensionale array** om de namen en huisdieren op te slaan.

---

## **Stap 1: Een nieuwe class aanmaken**
1. Open je bestaande Java-project in **IntelliJ IDEA**.
2. Ga in de **Project View** naar de `src` map.
3. Klik met de **rechtermuisknop** op `src` → **New** → **Java Class**.
4. Geef de class de naam `Opdracht5` en druk op **Enter**.

Nu heb je een lege Java-class. De volgende stap is om er code in te schrijven.

---

## **Stap 2: Code schrijven**

Schrijf een programma waarin de gebruiker **drie namen en hun huisdieren** invoert en deze vervolgens worden weergegeven.

➡️ **Denk eerst na:**
- Hoe sla je namen en huisdieren samen op?
- Hoe vraag je de gebruiker om deze gegevens in te voeren?
- Hoe toon je de gegevens correct op het scherm?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
import java.util.Scanner;

public class Opdracht5 {
   public static void main(String[] args) {
      Scanner scanner = new Scanner(System.in);
      String[][] gegevens = new String[3][2]; // 3 personen, 2 gegevens per persoon (naam en huisdier)

      System.out.print("Voer de naam van de eerste persoon in: ");
      gegevens[0][0] = scanner.nextLine();
      System.out.print("Voer het huisdier van de eerste persoon in: ");
      gegevens[0][1] = scanner.nextLine();

      System.out.print("Voer de naam van de tweede persoon in: ");
      gegevens[1][0] = scanner.nextLine();
      System.out.print("Voer het huisdier van de tweede persoon in: ");
      gegevens[1][1] = scanner.nextLine();

      System.out.print("Voer de naam van de derde persoon in: ");
      gegevens[2][0] = scanner.nextLine();
      System.out.print("Voer het huisdier van de derde persoon in: ");
      gegevens[2][1] = scanner.nextLine();

      System.out.println("De ingevoerde namen en huisdieren zijn:");
      System.out.println("1: " + gegevens[0][0] + " heeft een " + gegevens[0][1]);
      System.out.println("2: " + gegevens[1][0] + " heeft een " + gegevens[1][1]);
      System.out.println("3: " + gegevens[2][0] + " heeft een " + gegevens[2][1]);
   }
}
```
</details>

---

## **Stap 3: Het programma uitvoeren**
1. Klik op de groene **play-knop** naast `main` in `Opdracht5.java`.
2. Voer drie namen en hun huisdieren in wanneer daarom wordt gevraagd.
3. Je ziet de uitvoer:
   ```
   Voer de naam van de eerste persoon in: Alice
   Voer het huisdier van de eerste persoon in: Hond
   Voer de naam van de tweede persoon in: Bob
   Voer het huisdier van de tweede persoon in: Kat
   Voer de naam van de derde persoon in: Charlie
   Voer het huisdier van de derde persoon in: Papegaai
   De ingevoerde namen en huisdieren zijn:
   1: Alice heeft een Hond
   2: Bob heeft een Kat
   3: Charlie heeft een Papegaai
   ```

---

## **Stap 4: Hoe kan dit nog beter?**
In plaats van losse variabelen te gebruiken, slaan we nu de namen en huisdieren op in een **multidimensionale array**. Dit maakt het eenvoudiger om later aanpassingen te doen, zoals het uitbreiden van het aantal personen.

Maar er is nog een betere manier! In plaats van dezelfde code meerdere keren te herhalen, kunnen we **methodes** en **loops** gebruiken. Dit maakt de code overzichtelijker en makkelijker uitbreidbaar.

### **Voorbeeld met methodes en een lus**
Met een **for-loop** kunnen we herhaling voorkomen:

```java
import java.util.Scanner;

public class Opdracht5MetMethodes {
   public static void main(String[] args) {
      Scanner scanner = new Scanner(System.in);
      String[][] gegevens = new String[3][2]; // Een 3x2 array voor namen en huisdieren (3 personen en 2 gegevens per persoon :  naam en huisdier)

      // Loop om de gegevens van de gebruiker te verzamelen
      for (int i = 0; i < gegevens.length; i++) {
         gegevens[i] = vraagGegevens(scanner, i + 1);
      }

      // Methode om de gegevens weer te geven
      toonGegevens(gegevens);
   }

   // Methode om de gebruiker om een naam en huisdier te vragen
   public static String[] vraagGegevens(Scanner scanner, int nummer) {
      String[] persoon = new String[2]; // Een array met twee elementen: naam en huisdier
      System.out.print("Voer de naam van persoon " + nummer + " in: ");
      persoon[0] = scanner.nextLine(); // Leest de naam van de gebruiker
      System.out.print("Voer het huisdier van persoon " + nummer + " in: ");
      persoon[1] = scanner.nextLine(); // Leest het huisdier van de gebruiker
      return persoon; // Geeft de ingevulde array terug
   }

   // Methode om alle gegevens weer te geven
   public static void toonGegevens(String[][] gegevens) {
      System.out.println("De ingevoerde namen en huisdieren zijn:");
      for (int i = 0; i < gegevens.length; i++) {
         System.out.println((i + 1) + ": " + gegevens[i][0] + " heeft een " + gegevens[i][1]); // Print de naam en het huisdier
      }
   }
}
```

In de **volgende les** leer je hoe je **methodes** en **loops** gebruikt om herhaling in je code te verminderen en je programma flexibeler te maken! 🚀





