
## 🔹 Grundlagen

- **List** ist eine geordnete Sammlung von Elementen.
- In Kotlin sind Listen **immutable** (unveränderlich) per Default.
- Verwende `List<T>` für unveränderliche Listen und `MutableList<T>` für veränderliche.
- `<T>` steht für einen **generischen Typ** – z. B. `List<String>` ist eine Liste von Strings, `List<Int>` eine Liste von Ints.

## 🔹 Erstellung

> [!example] Beispiel: Liste erstellen
> ```kotlin
> val list = listOf("Apfel", "Banane", "Kirsche")
> val mutableList = mutableListOf("Hund", "Katze")
> ```

## 🔹 Zugriff & Iteration

> [!example] Beispiel: Auf Elemente zugreifen und iterieren
> ```kotlin
> val first = list[0]           // Zugriff per Index
> for (item in list) println(item) // Iteration
> ```

## 🔹 Wichtige Funktionen

- `list.size` – Anzahl der Elemente
- `list.contains("Apfel")` – Prüft auf enthaltenes Element
- `list.indexOf("Banane")` – Gibt Index zurück
- `list.sorted()` – Sortiert die Liste

## 🔹 MutableList – Veränderungen möglich

> [!example] Beispiel: MutableList verwenden
> ```kotlin
> mutableList.add("Maus")
> mutableList.remove("Hund")
> mutableList[0] = "Vogel"
> ```

## 🔹 Nützliches

- Listen können mit Funktionen wie `map`, `filter`, `forEach` transformiert werden.

> [!example] Beispiel: Liste transformieren
> ```kotlin
> val upperCase = list.map { it.uppercase() }
> ```

## 🔹 Siehe auch

- [[Kollektionen]]
