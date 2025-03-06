# Opdracht 2 - Rekenmachine in Java

In deze opdracht gaan we een eenvoudig rekenprogramma maken dat twee getallen optelt. Je hebt al een IntelliJ-project gemaakt in de vorige opdracht. Nu ga je een tweede class aanmaken en stap voor stap ontdekken hoe de code werkt.

---

## **Stap 1: Een nieuwe class aanmaken**
1. Open je bestaande Java-project in **IntelliJ IDEA**.
2. Ga in de **Project View** naar de `src` map.
3. Klik met de **rechtermuisknop** op `src` → **New** → **Java Class**.
4. Geef de class de naam `Opdracht2` en druk op **Enter**.

Nu heb je een lege Java-class. De volgende stap is om er code in te schrijven.

---

## **Stap 2: Hoe vraag je input en toon je output?**

Voordat we beginnen met de code, is het belangrijk om te begrijpen hoe we:
- Invoer van de gebruiker kunnen vragen.
- Output kunnen tonen op het scherm.

### **1. De `Scanner` klasse gebruiken voor invoer**
De **Scanner** klasse helpt ons om invoer van de gebruiker te lezen. Dit werkt als volgt:

```java
Scanner scanner = new Scanner(System.in);
int getal = scanner.nextInt(); // Leest een integer in van het toetsenbord
```

<details>
  <summary>💡 Klik hier voor meer uitleg</summary>
  - `Scanner scanner = new Scanner(System.in);` maakt een **Scanner-object** aan dat invoer leest.
  - `scanner.nextInt();` leest een **geheel getal** (integer) van de gebruiker.
  - Andere methodes van Scanner zijn:
    - `scanner.nextLine();` → leest een volledige tekstregel.
    - `scanner.nextDouble();` → leest een decimaal getal.
</details>

### **2. Wat is het verschil tussen `print` en `println`?**
Met **System.out.print** en **System.out.println** kunnen we tekst naar de console sturen.

```java
System.out.print("Hallo, wereld!");
System.out.println("Dit is een nieuwe regel.");
```

<details>
  <summary>💡 Klik hier voor meer uitleg</summary>
  - `System.out.print()` print tekst **zonder** een nieuwe regel.
  - `System.out.println()` print tekst **met** een nieuwe regel.
</details>

Nu we dit begrijpen, kunnen we de code schrijven!

---

## **Stap 3: Code schrijven**

Schrijf een programma dat de gebruiker vraagt om twee getallen in te voeren en vervolgens de som berekent.

➡️ **Denk eerst na:**
- Hoe vraag je de gebruiker om invoer?
- Hoe lees je een getal in vanuit het toetsenbord?
- Hoe bereken je de som?
- Hoe toon je het resultaat op het scherm?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
import java.util.Scanner;

public class Opdracht2 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Voer het eerste getal in: ");
        int num1 = scanner.nextInt();
        System.out.print("Voer het tweede getal in: ");
        int num2 = scanner.nextInt();
        System.out.println("De som is: " + (num1 + num2));
    }
}
```
</details>

---

## **Stap 4: Het programma uitvoeren**
1. Klik op de groene **play-knop** naast `main` in `Opdracht2.java`.
2. Voer in de console twee getallen in (bijvoorbeeld `5` en `7`).
3. Je ziet de uitvoer:
   ```
   Voer het eerste getal in: 5
   Voer het tweede getal in: 7
   De som is: 12
   ```

---

## **Stap 5: Uitdagingen**
Probeer nu zelf de volgende aanpassingen te maken:
- Laat de gebruiker **drie** getallen invoeren en tel ze op.
- Toon ook het **verschil** (`num1 - num2`).
- Toon de **vermenigvuldiging** (`num1 * num2`).

Test je aanpassingen en kijk of je begrijpt hoe de uitvoer verandert.

Veel succes! 

