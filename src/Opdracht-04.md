# Opdracht 4 - Even getallen printen met `while`

In deze opdracht gaan we een programma schrijven dat alle **even getallen** tot een door de gebruiker gekozen maximum weergeeft. Dit keer gebruiken we **geen `if`-statement**, maar een **`while`-loop** en verhogen we de teller met **2**.

---

## **Stap 1: Een nieuwe class aanmaken**
1. Open je bestaande Java-project in **IntelliJ IDEA**.
2. Ga in de **Project View** naar de `src` map.
3. Klik met de **rechtermuisknop** op `src` → **New** → **Java Class**.
4. Geef de class de naam `Opdracht5` en druk op **Enter**.

Nu heb je een lege Java-class. De volgende stap is om er code in te schrijven.

---

## **Stap 2: Werken met `while` en increments**

In deze opdracht gaan we:
- **Een getal vragen aan de gebruiker** met `Scanner`.
- **Een while-loop gebruiken** om door de even getallen te lopen.
- **De teller met 2 verhogen** in plaats van een `if`-check te doen.

### **1. Hoe start je bij het eerste even getal?**
Het eerste **even** getal is altijd **2**. We starten onze teller daar.

```java
int i = 2;
```

### **2. Hoe zorg je dat we alleen even getallen printen?**
Door de teller steeds met **2** te verhogen, slaan we automatisch de oneven getallen over.

```java
while (i <= max) {
    System.out.println(i);
    i += 2; // Verhoog met 2 om alleen even getallen te krijgen
}
```

<details>
  <summary>💡 Klik hier voor meer uitleg</summary>
  - De `while`-loop blijft lopen zolang `i` kleiner is dan of gelijk aan `max`.
  - We beginnen bij `2` en verhogen `i` **met 2 per stap**, zodat we alleen even getallen krijgen.
</details>

Nu we dit begrijpen, kunnen we de code schrijven!

---

## **Stap 3: Code schrijven**

Schrijf een programma dat een gebruiker vraagt om een maximumgetal en dan alle **even getallen** tot dat getal toont zonder een `if`-check te gebruiken.

➡️ **Denk eerst na:**
- Hoe vraag je de gebruiker om invoer?
- Hoe start je bij het eerste even getal?
- Hoe verhoog je de teller zonder een `if`-check?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
import java.util.Scanner;

public class Opdracht5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Voer een getal in: ");
        int max = scanner.nextInt();
        
        int i = 2; // Start bij het eerste even getal
        while (i <= max) {
            System.out.println(i);
            i += 2; // Verhoog met 2 zodat alleen even getallen worden getoond
        }
    }
}
```
</details>

---

## **Stap 4: Het programma uitvoeren**
1. Klik op de groene **play-knop** naast `main` in `Opdracht5.java`.
2. Voer in de console een getal in (bijvoorbeeld `10`).
3. Je ziet de uitvoer:
   ```
   Voer een getal in: 10
   2
   4
   6
   8
   10
   ```

---

## **Stap 5: Uitdagingen**
Probeer nu zelf de volgende aanpassingen te maken:
- Laat de gebruiker **een start- en eindgetal** invoeren.
- Print alleen **oneven getallen** door de startwaarde op **1** te zetten.
- Voeg een **controle toe** zodat de gebruiker geen negatief getal kan invoeren.

Test je aanpassingen en kijk of je begrijpt hoe de uitvoer verandert.

Veel succes! 

