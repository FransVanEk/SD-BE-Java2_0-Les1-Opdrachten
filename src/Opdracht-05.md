# Opdracht 5 - Fibonacci-reeks genereren

In deze opdracht gaan we een programma schrijven dat de **Fibonacci-reeks** genereert tot een door de gebruiker gekozen aantal getallen. De Fibonacci-reeks is een **rij van getallen** waarbij elk getal de som is van de twee voorgaande getallen.

---

## **Stap 1: Wat is de Fibonacci-reeks?**
De Fibonacci-reeks begint meestal met `0` en `1`. Daarna wordt elk volgende getal berekend als de som van de twee vorige getallen.

Voorbeeld van de eerste 10 getallen in de reeks:
```
0, 1, 1, 2, 3, 5, 8, 13, 21, 34
```

<details>
  <summary>💡 Klik hier voor meer uitleg</summary>
  - Het **eerste getal** is altijd `0`.
  - Het **tweede getal** is altijd `1`.
  - Elk **volgende getal** is de som van de **twee voorgaande**.
</details>

---

## **Stap 2: Een nieuwe class aanmaken**
1. Open je bestaande Java-project in **IntelliJ IDEA**.
2. Ga in de **Project View** naar de `src` map.
3. Klik met de **rechtermuisknop** op `src` → **New** → **Java Class**.
4. Geef de class de naam `Opdracht5` en druk op **Enter**.

Nu heb je een lege Java-class. De volgende stap is om er code in te schrijven.

---

## **Stap 3: Code schrijven**

Schrijf een programma dat een gebruiker vraagt om het aantal Fibonacci-getallen dat moet worden gegenereerd.

➡️ **Denk eerst na:**
- Hoe vraag je de gebruiker om invoer?
- Hoe zorg je ervoor dat elk getal de som is van de vorige twee?
- Hoe gebruik je een **while-loop** om de reeks te genereren?

### **1. De gebruiker om invoer vragen**
Hoe vraag je de gebruiker om een getal?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
Scanner scanner = new Scanner(System.in);
System.out.print("Voer het aantal Fibonacci-getallen in: ");
int aantal = scanner.nextInt();
```
</details>

### **2. Initialiseren van de Fibonacci-variabelen**
Welke variabelen hebben we nodig?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
int a = 0, b = 1, teller = 0;
```
</details>

### **3. Een `while`-loop gebruiken om de reeks te genereren**
Hoe zorg je ervoor dat we het juiste aantal Fibonacci-getallen genereren?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
while (teller < aantal) {
    System.out.println(a);
    int volgende = a + b;
    a = b;
    b = volgende;
    teller++;
}
```
</details>

### **Volledige code**
Wil je de complete oplossing in één keer zien?

<details>
  <summary>💡 Klik hier voor de volledige code</summary>

```java
import java.util.Scanner;

public class Opdracht5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Voer het aantal Fibonacci-getallen in: ");
        int aantal = scanner.nextInt();
        
        int a = 0, b = 1, teller = 0;
        
        while (teller < aantal) {
            System.out.println(a);
            int volgende = a + b;
            a = b;
            b = volgende;
            teller++;
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
   Voer het aantal Fibonacci-getallen in: 10
   0
   1
   1
   2
   3
   5
   8
   13
   21
   34
   ```

---

## **Stap 5: Uitdagingen**
Probeer nu zelf de volgende aanpassingen te maken:
- Laat de gebruiker een **startgetal** invoeren (bijvoorbeeld starten bij `5, 8, 13, ...`).
- Laat de gebruiker een **maximumwaarde** invoeren i.p.v. een vast aantal stappen.
- Voeg een **controle toe** zodat de gebruiker geen negatief getal kan invoeren.

Test je aanpassingen en kijk of je begrijpt hoe de uitvoer verandert.

Veel succes! 

