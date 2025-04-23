# Vererbung

## 🔹 Überblick
- **Vererbung** ermöglicht es einer Klasse, Eigenschaften und Methoden einer anderen Klasse zu übernehmen.
- In Kotlin können Klassen mit dem Schlüsselwort **`open`** markiert werden, um sie vererbbar zu machen.
- Eine Unterklasse kann eine Oberklasse erweitern, Methoden überschreiben und neue Eigenschaften hinzufügen.

## 🔹 Vererbung in Kotlin
- **Unterklassen** erben von **Oberklassen**, wobei die Oberklasse **`open`** sein muss.
- **Unterklassen** können Methoden der Oberklasse überschreiben, um die Funktionalität zu ändern.

> [!example] Beispiel: Einfache Vererbung  
> ```kotlin
> open class Fahrzeug(val marke: String) {
>     fun fahren() {
>         println("$marke fährt")
>     }
> }
> 
> class Auto(marke: String, val modell: String) : Fahrzeug(marke) {
>     fun zeigeModell() {
>         println("Modell: $modell")
>     }
> }
> 
> val auto = Auto("BMW", "X5")
> auto.fahren()  // Ausgabe: BMW fährt
> auto.zeigeModell()  // Ausgabe: Modell: X5
> ```

## 🔹 Überschreiben von Methoden
- Um eine Methode in der Unterklasse zu überschreiben, muss die Methode in der Oberklasse mit dem Schlüsselwort **`open`** markiert werden.
- Die Methode in der Unterklasse wird mit **`override`** überschrieben.

> [!example] Beispiel: Überschreiben einer Methode  
> ```kotlin
> open class Fahrzeug(val marke: String) {
>     open fun fahren() {
>         println("$marke fährt")
>     }
> }
> 
> class Auto(marke: String) : Fahrzeug(marke) {
>     override fun fahren() {
>         println("$marke fährt schnell")
>     }
> }
> 
> val auto = Auto("BMW")
> auto.fahren()  // Ausgabe: BMW fährt schnell
> ```

## 🔹 Siehe auch
- [[Kotlin Grundlagen]]
- [[Methoden]]
- [[Klassen]]
