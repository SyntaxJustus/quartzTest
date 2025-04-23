
## 🔹 Überblick

- Kollektionen sind grundlegende Datenstrukturen in Kotlin, die verwendet werden, um mehrere Werte zu speichern.
- Kotlin bietet verschiedene Arten von Kollektionen, darunter **Listen**, **Sets** und **Maps**, die entweder **mutable** (veränderlich) oder **immutable** (unveränderlich) sein können.
- Kollektionen sind in Kotlin als Teil der **Standardbibliothek** enthalten und bieten eine Vielzahl von Funktionen zum Arbeiten mit Daten.

## 🔹 Listen

- Eine **Liste** (List) speichert eine geordnete Sammlung von Elementen.
- Listen können entweder **mutable** oder **immutable** sein:
  - **`List`**: Eine unveränderliche Liste.
  - **`MutableList`**: Eine veränderliche Liste, die Elemente hinzufügen, entfernen oder ändern kann.

> [!example] Beispiel: Liste  
> ```kotlin
> val zahlen: List<Int\> = listOf(1, 2, 3, 4, 5)  // Unveränderliche Liste
> 
> val mutableZahlen: MutableList<Int\> = mutableListOf(1, 2, 3)  // Veränderliche Liste
> mutableZahlen.add(4)  // Hinzufügen eines Werts
> mutableZahlen[0] = 10  // Ändern eines Werts
> println(mutableZahlen)  // Ausgabe: [10, 2, 3, 4]
> ```

## 🔹 Sets

- Ein **Set** speichert eine Sammlung von **einzigartigen** Elementen ohne eine bestimmte Reihenfolge.
- Sets können ebenfalls **mutable** oder **immutable** sein:
  - **`Set`**: Ein unveränderliches Set.
  - **`MutableSet`**: Ein veränderliches Set, bei dem Elemente hinzugefügt oder entfernt werden können.

> [!example] Beispiel: Set  
> ```kotlin
> val zahlenSet: Set<Int\> = setOf(1, 2, 3, 4, 5)  // Unveränderliches Set
> 
> val mutableSet: MutableSet<Int\> = mutableSetOf(1, 2, 3)  // Veränderliches Set
> mutableSet.add(4)
> mutableSet.remove(2)
> println(mutableSet)  // Ausgabe: [1, 3, 4]
> ```

## 🔹 Maps

- Eine **Map** ist eine Sammlung von **Schlüssel-Wert-Paaren**.
- In Kotlin gibt es auch hier unveränderliche (immutable) und veränderliche (mutable) Varianten:
  - **`Map`**: Eine unveränderliche Map.
  - **`MutableMap`**: Eine veränderliche Map.

> [!example] Beispiel: Map  
> ```kotlin
> val telefonbuch: Map<String, String> = mapOf("Anna" to "12345", "Max" to "67890")  // Unveränderliche Map
> 
> val mutableTelefonbuch: MutableMap<String, String> = mutableMapOf("Anna" to "12345")
> mutableTelefonbuch["Max"] = "67890"  // Hinzufügen eines Werts
> mutableTelefonbuch.remove("Anna")  // Entfernen eines Werts
> println(mutableTelefonbuch)  // Ausgabe: {Max=67890}
> ```

## 🔹 Kollektionen und Lambda-Ausdrücke

- Kollektionen in Kotlin unterstützen **hohe Flexibilität** und **Funktionalität** über Lambda-Ausdrücke und Funktionen wie **`map`**, **`filter`**, **`reduce`** und viele andere.
- Diese Funktionen ermöglichen eine deklarative Art der Verarbeitung von Kollektionen.

> [!example] Beispiel: Kollektion mit `map` und `filter`  
> ```kotlin
> val zahlen = listOf(1, 2, 3, 4, 5)
> 
> val quadrate = zahlen.map { it * it }  // Quadrat jedes Elements
> val geradeZahlen = zahlen.filter { it % 2 == 0 }  // Nur gerade Zahlen
> 
> println(quadrate)  // Ausgabe: [1, 4, 9, 16, 25]
> println(geradeZahlen)  // Ausgabe: [2, 4]
> ```

## 🔹 Siehe auch

- [[Listen]]
- [[Operatoren]]
- [[Funktionen]]
