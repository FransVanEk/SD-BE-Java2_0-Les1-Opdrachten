# Opdracht 3 - Meerdere namen invoeren 

In deze opdracht gaan we een programma schrijven waarin de gebruiker **drie namen** invoert en deze vervolgens worden weergegeven.

Later leer je hoe je dit makkelijker kunt maken met behulp van een lus en **loops**.

---

## **Stap 1: Een nieuwe class aanmaken**
1. Open je bestaande Java-project in **IntelliJ IDEA**.
2. Ga in de **Project View** naar de `src` map.
3. Klik met de **rechtermuisknop** op `src` → **New** → **Java Class**.
4. Geef de class de naam `Opdracht3NoLoop` en druk op **Enter**.

Nu heb je een lege Java-class. De volgende stap is om er code in te schrijven.

---

## **Stap 2: Code schrijven**

Schrijf een programma waarin de gebruiker **drie namen** invoert en deze vervolgens worden weergegeven.

➡️ **Denk eerst na:**
- Hoe vraag je drie keer een invoer aan de gebruiker?
- Hoe sla je deze namen op in aparte variabelen?
- Hoe toon je elke naam apart op het scherm?

<details>
  <summary>💡 Klik hier voor de oplossing</summary>

```java
import java.util.Scanner;

public class Opdracht3NoLoop {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Voer de eerste naam in: ");
        String naam1 = scanner.nextLine();
        
        System.out.print("Voer de tweede naam in: ");
        String naam2 = scanner.nextLine();
        
        System.out.print("Voer de derde naam in: ");
        String naam3 = scanner.nextLine();
        
        System.out.println("De ingevoerde namen zijn:");
        System.out.println("1: " + naam1);
        System.out.println("2: " + naam2);
        System.out.println("3: " + naam3);
    }
}
```
</details>

---

## **Stap 3: Het programma uitvoeren**
1. Klik op de groene **play-knop** naast `main` in `Opdracht3NoLoop.java`.
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

## **Stap 4: Hoe kan dit makkelijker?**
Het bovenstaande programma werkt prima, maar het wordt al snel onhandig als je bijvoorbeeld **tien** namen wilt invoeren. Je moet dan 10 variabelen aanmaken.

Een betere manier om dit te doen, is met een **array**. In een volgende opdracht leer je hoe je dit kunt automatiseren met een array.

---

## **Stap 5: Uitdagingen**
Probeer nu zelf de volgende aanpassingen te maken:
- Voeg een **vierde naam** toe en toon deze ook.
