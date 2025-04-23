
## 🔹 Überblick

- **Sealed Klassen** sind eine spezielle Art von Klassen in Kotlin, die dazu verwendet werden, eine **eingeschränkte Vererbungshierarchie** zu definieren.
- Eine **sealed class** kann nur innerhalb ihres eigenen Moduls (oder ihrer eigenen Datei) von anderen Klassen oder Objekten erweitert werden.
- Sealed Klassen werden häufig in **when-Ausdrücken** verwendet, um alle möglichen Fälle zu behandeln, ohne dass eine **else**-Klausel erforderlich ist.

## 🔹 Definition einer Sealed Klasse

- Eine sealed class wird mit dem Schlüsselwort **`sealed class`** definiert.
- Sie dient als Oberklasse für andere Klassen, die sie erweitern.

> [!example] Beispiel: Sealed Klasse  
> ```kotlin
> sealed class Fahrzeug {
>     data class Auto(val marke: String, val modell: String) : Fahrzeug()
>     data class Fahrrad(val marke: String) : Fahrzeug()
>     object Lkw : Fahrzeug()  // Lkw ist ein Singleton
> }
> 
> val fahrzeug: Fahrzeug = Fahrzeug.Auto("BMW", "X5")
> ```

## 🔹 Vorteile von Sealed Klassen

- Sealed Klassen bieten eine **sichere Vererbungshierarchie**, da alle möglichen Subklassen **vorab bekannt** sind.
- Sie garantieren, dass der Entwickler alle möglichen Fälle in **`when`**-Ausdrücken behandeln kann, ohne dass eine **`else`-Klausel** erforderlich ist.

> [!example] Beispiel: Verwendung in `when`  
> ```kotlin
> fun beschreibeFahrzeug(fahrzeug: Fahrzeug): String {
>     return when (fahrzeug) {
>         is Fahrzeug.Auto -> "Auto der Marke: ${fahrzeug.marke}, Modell: ${fahrzeug.modell}"
>         is Fahrzeug.Fahrrad -> "Fahrrad der Marke: ${fahrzeug.marke}"
>         Fahrzeug.Lkw -> "Lkw"
>     }
> }
> 
> val meinAuto = Fahrzeug.Auto("Audi", "A6")
> println(beschreibeFahrzeug(meinAuto))  // Ausgabe: Auto der Marke: Audi, Modell: A6
> ```

## 🔹 Einschränkungen

- **Sealed Klassen** können nicht direkt instanziiert werden.
- Alle Unterklassen einer **sealed class** müssen im gleichen **Modul** oder der gleichen **Datei** definiert sein.

> [!example] Beispiel: Einschränkung der Vererbung  
> ```kotlin
> sealed class Fahrzeug
> 
> // Fehler! Fahrzeug kann nur innerhalb dieser Datei erweitert werden
> class Motorrad : Fahrzeug()
> ```

## 🔹 Sealed Klassen vs. Abstrakte Klassen

- Der Hauptunterschied zwischen einer **sealed class** und einer **abstrakten Klasse** ist, dass bei sealed Klassen alle Unterklassen bereits zur Compile-Zeit bekannt sind, was eine vollständige Analyse der Vererbungshierarchie ermöglicht.
- Abstrakte Klassen können beliebig viele Unterklassen in beliebigen Modulen oder Dateien haben.

## 🔹 Siehe auch

- [[Kotlin Grundlagen]]
- [[Klassen]]
- [[Vererbung]]
