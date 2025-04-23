# Klassen

## 🔹 Überblick
- **Klassen** sind die grundlegenden Bausteine der **objektorientierten Programmierung** in Kotlin.
- Klassen definieren **Eigenschaften** und **Methoden**, die Objekte dieser Klasse besitzen können.
- Kotlin unterstützt **normale Klassen**, **Datenklassen** und **abstrakte Klassen**.

## 🔹 Klassendefinition
- Eine Klasse wird mit dem Schlüsselwort **`class`** definiert.
- Eine Klasse kann **Konstruktoren** enthalten, sowohl **primäre** als auch **sekundäre Konstruktoren**.

> [!example] Beispiel: Einfache Klasse  
> ```kotlin
> class Auto(val marke: String, val modell: String) {
>     fun beschreibung(): String {
>         return "Marke: $marke, Modell: $modell"
>     }
> }
> 
> val auto = Auto("Volkswagen", "Golf")
> println(auto.beschreibung())  // Ausgabe: Marke: Volkswagen, Modell: Golf
> ```

## 🔹 Primärer Konstruktor
- Der **primäre Konstruktor** wird direkt in der Klassendeklaration angegeben.
- **Eigenschaften**, die im Konstruktor definiert sind, können mit **`val`** (für unveränderbare) oder **`var`** (für veränderbare) deklariert werden.

> [!example] Beispiel: Primärer Konstruktor  
> ```kotlin
> class Person(val name: String, var alter: Int)
> 
> val person = Person("Anna", 30)
> println(person.name)  // Ausgabe: Anna
> println(person.alter)  // Ausgabe: 30
> ```

## 🔹 Sekundäre Konstruktoren
- Eine Klasse kann auch **sekundäre Konstruktoren** haben, die mit dem Schlüsselwort **`constructor`** definiert werden.

> [!example] Beispiel: Sekundärer Konstruktor  
> ```kotlin
> class Person(val name: String) {
>     var alter: Int = 0
> 
>     constructor(name: String, alter: Int) : this(name) {
>         this.alter = alter
>     }
> }
> 
> val person = Person("Max", 25)
> println(person.name)  // Ausgabe: Max
> println(person.alter)  // Ausgabe: 25
> ```

## 🔹 Datenklassen
- Eine **Datenklasse** (`data class`) in Kotlin wird verwendet, um **Daten** zu modellieren.
- Kotlin erzeugt automatisch **`toString()`**, **`equals()`**, **`hashCode()`** und **`copy()`**-Methoden für Datenklassen.

> [!example] Beispiel: Datenklasse  
> ```kotlin
> data class Person(val name: String, val alter: Int)
> 
> val person = Person("Anna", 30)
> println(person.toString())  // Ausgabe: Person(name=Anna, alter=30)
> ```

## 🔹 Abstrakte Klassen
- **Abstrakte Klassen** können nicht direkt instanziiert werden.
- Sie dienen als Grundlage für andere Klassen und können abstrakte Methoden enthalten, die in den abgeleiteten Klassen implementiert werden müssen.

> [!example] Beispiel: Abstrakte Klasse  
> ```kotlin
> abstract class Fahrzeug {
>     abstract fun fahren()
> }
> 
> class Auto : Fahrzeug() {
>     override fun fahren() {
>         println("Auto fährt")
>     }
> }
> 
> val auto = Auto()
> auto.fahren()  // Ausgabe: Auto fährt
> ```

## 🔹 Siehe auch
- [[Kotlin Grundlagen]]
- [[Methoden]]
- [[Vererbung]]
- [[Interfaces]]
- [[Sealed Klassen]]
