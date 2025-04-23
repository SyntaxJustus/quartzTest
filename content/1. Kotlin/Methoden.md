
## 🔹 Überblick

- In Kotlin sind **Methoden** Funktionen, die innerhalb einer **Klasse** oder eines **Objekts** definiert werden.
- Methoden können **Parameter** annehmen und **Werte** zurückgeben.
- Kotlin unterstützt sowohl **Instanzmethoden** (die an Objekte gebunden sind) als auch **statische Methoden** (die an Klassen gebunden sind).

## 🔹 Funktionsdefinition

- Eine Methode wird ähnlich wie eine Funktion definiert, jedoch innerhalb einer **Klasse**.
- Sie kann mit oder ohne Rückgabewert sowie mit beliebigen Parametern definiert werden.

> [!example] Beispiel: Einfache Methode  
> ```kotlin
> class Rechner {
>     fun addiere(a: Int, b: Int): Int {
>         return a + b
>     }
> }
> 
> val rechner = Rechner()
> println(rechner.addiere(3, 5))  // Ausgabe: 8
> ```

### 🔸 Rückgabewert

- Eine Methode kann einen Wert zurückgeben, der vom angegebenen Rückgabetyp ist.
- Der Rückgabewert muss mit dem Rückgabetyp übereinstimmen, andernfalls wird ein Fehler auftreten.

> [!example] Beispiel: Methode mit Rückgabewert  
> ```kotlin
> fun multipliziere(a: Int, b: Int): Int {
>     return a * b
> }
> 
> val result = multipliziere(4, 5)
> println(result)  // Ausgabe: 20
> ```

## 🔹 Methoden ohne Rückgabewert

- Eine Methode kann auch ohne Rückgabewert definiert werden, was in Kotlin als **`Unit`** bezeichnet wird (vergleichbar mit `void` in anderen Programmiersprachen).

> [!example] Beispiel: Methode ohne Rückgabewert  
> ```kotlin
> fun druckeBegrueßung(name: String): Unit {
>     println("Hallo, $name!")
> }
> 
> druckeBegrueßung("Anna")  // Ausgabe: Hallo, Anna!
> ```

## 🔹 Standardmethoden

- Kotlin bietet einige vordefinierte **Standardmethoden**, wie z. B. **`toString()`**, **`equals()`**, **`hashCode()`**, und **`copy()`**.
- Diese Methoden sind in allen Klassen verfügbar und bieten grundlegende Funktionalitäten.

> [!example] Beispiel: Standardmethoden  
> ```kotlin
> data class Person(val name: String, val alter: Int)
> 
> val person = Person("Anna", 30)
> println(person.toString())  // Ausgabe: Person(name=Anna, alter=30)
> ```

## 🔹 Erweiterungsfunktionen

- **Erweiterungsfunktionen** ermöglichen es, Methoden für bestehende Klassen hinzuzufügen, ohne die ursprüngliche Klasse zu verändern.

> [!example] Beispiel: Erweiterungsfunktion  
> ```kotlin
> fun String.istLeer(): Boolean {
>     return this.isEmpty()
> }
> 
> println("Hallo".istLeer())  // Ausgabe: false
> ```

## 🔹 Methodenüberladung

- In Kotlin können mehrere Methoden mit demselben Namen existieren, solange ihre **Parameterlisten** unterschiedlich sind.

> [!example] Beispiel: Methodenüberladung  
> ```kotlin
> fun addiere(a: Int, b: Int): Int {
>     return a + b
> }
> 
> fun addiere(a: Double, b: Double): Double {
>     return a + b
> }
> 
> println(addiere(2, 3))  // Ausgabe: 5
> println(addiere(2.5, 3.5))  // Ausgabe: 6.0
> ```

## 🔹 Siehe auch
- [[Kotlin Grundlagen]]
- [[Funktionen]]
- [[Operatoren]]
- [[Klassen]]
- [[Null-Sicherheit]]
