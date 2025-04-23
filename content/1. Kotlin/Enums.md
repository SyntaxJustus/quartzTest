
## 🔹 Überblick

- **Enums** (Aufzählungstypen) in Kotlin sind spezielle Klassen, die eine feste Anzahl von konstanten Werten definieren.
- Sie werden häufig verwendet, wenn eine Variable nur eine von einer kleinen Anzahl an festen Optionen annehmen kann, z. B. Wochentage, Statuswerte oder Zustände.
- Kotlin bietet eine leistungsstarke Implementierung von Enums, die neben den klassischen Konstanten auch Methoden und Felder enthalten können.

## 🔹 Definition einer Enum-Klasse

- Eine Enum-Klasse wird mit dem Schlüsselwort **`enum class`** definiert.
- Jede Konstante innerhalb der Enum-Klasse ist eine Instanz der Enum-Klasse.

> [!example] Beispiel: Einfache Enum-Klasse  
> ```kotlin
> enum class Wochentag {
>     MONTAG, DIENSTAG, MITTWOCH, DONNERSTAG, FREITAG, SAMSTAG, SONNTAG
> }
> 
> val heute = Wochentag.MONTAG
> println(heute)  // Ausgabe: MONTAG
> ```

## 🔹 Enum mit Werten und Methoden

- Enum-Klassen können zusätzliche Felder und Methoden haben.
- Jeder Enum-Wert kann Konstruktorparameter haben, um damit verbundene Werte zu speichern.

> [!example] Beispiel: Enum mit Konstruktorparametern  
> ```kotlin
> enum class Wochentag(val tagNummer: Int) {
>     MONTAG(1), DIENSTAG(2), MITTWOCH(3), DONNERSTAG(4), FREITAG(5), SAMSTAG(6), SONNTAG(7);
>     
>     fun istWochenende(): Boolean {
>         return this == SAMSTAG || this == SONNTAG
>     }
> }
> 
> val heute = Wochentag.MONTAG
> println(heute.tagNummer)  // Ausgabe: 1
> println(heute.istWochenende())  // Ausgabe: false
> ```

## 🔹 Zugriff auf Enum-Werte

- Du kannst auf Enum-Werte mit ihrem Namen zugreifen oder durch Indizes navigieren.
- **`values()`** gibt alle Werte der Enum-Klasse zurück.
- **`valueOf()`** sucht einen Enum-Wert anhand des Namens.

> [!example] Beispiel: Zugriff auf Enum-Werte  
> ```kotlin
> enum class Wochentag { MONTAG, DIENSTAG, MITTWOCH, DONNERSTAG, FREITAG, SAMSTAG, SONNTAG }
> 
> // Zugriff auf alle Enum-Werte
> val alleTage = Wochentag.values()
> println(alleTage.joinToString())  // Ausgabe: MONTAG, DIENSTAG, MITTWOCH, DONNERSTAG, FREITAG, SAMSTAG, SONNTAG
> 
> // Suche nach Enum-Wert anhand des Namens
> val dienstag = Wochentag.valueOf("DIENSTAG")
> println(dienstag)  // Ausgabe: DIENSTAG
> ```

## 🔹 Enum und `when`-Ausdrücke

- **`when`**-Ausdrücke eignen sich hervorragend zum Arbeiten mit Enums, da die limitierte Anzahl von Fällen komplett abgedeckt werden kann.

> [!example] Beispiel: Verwendung von Enum in einem `when`-Ausdruck  
> ```kotlin
> enum class Wochentag { MONTAG, DIENSTAG, MITTWOCH, DONNERSTAG, FREITAG, SAMSTAG, SONNTAG }
> 
> fun beschreibeTag(tag: Wochentag): String {
>     return when (tag) {
>         Wochentag.MONTAG -> "Erster Tag der Woche"
>         Wochentag.SAMSTAG, Wochentag.SONNTAG -> "Wochenende!"
>         else -> "Wochentag"
>     }
> }
> 
> val dienstag = Wochentag.DIENSTAG
> println(beschreibeTag(dienstag))  // Ausgabe: Wochentag
> ```

## 🔹 Siehe auch

- [[Kotlin Grundlagen]]
- [[Klassen]]
- [[Kontrollstrukturen]]
