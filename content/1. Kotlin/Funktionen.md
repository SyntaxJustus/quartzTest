

## 🔹 Überblick
- In Kotlin werden Funktionen mit dem Schlüsselwort **`fun`** deklariert.
- Funktionen können **Parameter** und **Rückgabewerte** haben oder auch ohne diese auskommen.
- Kotlin unterstützt **Typinferenz**, sodass der Rückgabetyp häufig nicht explizit angegeben werden muss.

## 🔹 Funktionsdeklaration
- Die Grundstruktur einer Funktion:
```kotlin
  fun funktionName(parameter1: Typ1, parameter2: Typ2): Rückgabetyp {
      // Funktionskörper
  }
```

> [!example] Beispiel: Einfache Funktion
>```kotlin
>fun begruessung(name: String): String {
>  return "Hallo, $name!"
>}
>```


## 🔹 Rückgabewert

- Eine Funktion kann einen **Rückgabewert** haben, der mit dem angegebenen **Rückgabetyp** übereinstimmt.
- Falls eine Funktion keinen Rückgabewert hat, wird der **`Unit`**-Typ verwendet.

>[!example] Beispiel: Funktion ohne Rückgabewert
>```kotlin
>fun sagHallo() {
>	println("Hallo!")
>}
>```

## 🔹 Typinferenz bei Rückgabewerten

- Der Rückgabetyp einer Funktion kann durch den **Kotlin-Compiler** automatisch abgeleitet werden.    

> [!example] Beispiel: Typinferenz
> ```kotlin
> fun multipliziere(a: Int, b: Int) = a * b  // Rückgabetyp wird automatisch als Int ermittelt
> ```

## 🔹 Standardwerte für Parameter

- In Kotlin können Parametern **Standardwerte** zugewiesen werden, sodass sie optional werden.
    

> [!example] Beispiel: Funktion mit Standardwerten> 
> ```kotlin
> fun begruessung(name: String = "Welt"): String {
>      return "Hallo, $name!"
> }
> 
> begruessung() // Hallo, Welt!
> begruessung("Zusammen") // Hallo, Zusammen!
> ```

## 🔹 Varargs (Variadic Arguments)

- Kotlin unterstützt **varargs**, sodass eine Funktion eine beliebige Anzahl von Argumenten eines bestimmten Typs entgegennehmen kann.
    

> [!example] Beispiel: varargs
> ```kotlin
> fun summe(vararg zahlen: Int): Int {
> 	return zahlen.sum() 
>}
>```

## 🔹 Funktionsüberladung

- In Kotlin können Funktionen **überladen** werden, indem mehrere Funktionen mit dem gleichen Namen existieren, aber unterschiedliche Parameter haben.
    

> [!example] Beispiel: Funktionsüberladung
> ```kotlin
> fun addiere(a: Int, b: Int): Int {
> 	return a + b
> }
> 
> fun addiere(a: Double, b: Double): Double {
> 	return a + b
> }
> ```


## 🔹 Siehe auch
- [[Datentypen]]
- [[Kotlin Grundlagen]]
- [[Null-Sicherheit]]
- [[Operatoren]]
- [[Packages und Imports]]
- [[Lambda]]
