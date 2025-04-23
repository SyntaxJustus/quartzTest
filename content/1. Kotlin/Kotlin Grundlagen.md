# Kotlin Grundlagen

## 🔹 Allgemeines

- Kotlin ist eine **statisch typisierte** Programmiersprache.
- Entwickelt von **JetBrains**, läuft auf der **JVM**.
- Vollständig interoperabel mit **Java**.
- Fokus auf **Sicherheit, Prägnanz und Ausdrucksstärke**.

## 🔹 Hauptmerkmale

- **Null-Sicherheit**
- **Typinferenz**
- **Funktionen als First-Class Citizens**
- **Smart Casts**
- **Erweiterungsfunktionen**
- **Coroutines für Nebenläufigkeit**

## 🔹 Einstieg: `main`-Funktion

> [!example] Beispiel: Hauptfunktion
> ```kotlin
> fun main() {
>     println("Hallo Kotlin!")
> }
> ```

## 🔹 Variablen

- `val` → **unveränderlich** 
- `var` → **veränderlich**

> [!example] Beispiel: Variablen deklarieren
> ```kotlin
> val name = "Anna"     // Typ wird automatisch erkannt
> var alter = 30        // Typinferenz: Int
> ```

## 🔹 Funktionen

- Definiert mit `fun`, Rückgabetyp optional bei Typinferenz.

> [!example] Beispiel: Funktion mit Rückgabewert
> ```kotlin
> fun addiere(a: Int, b: Int): Int {
>     return a + b
> }
> ```

## 🔹 String Interpolation

- Variablen können direkt in Strings eingebettet werden mit `$`.

> [!example] Beispiel: String Interpolation
> ```kotlin
> val name = "Lisa"
> println("Hallo, $name!")
> ```

## 🔹 Kommentare

- Einzelne Zeile: `//`
- Mehrzeilig: `/* ... */`
- KDoc `/** ... */`

## 🔹 Datentypen (Auswahl)

- Ganzzahlen: `Int`, `Long`, `Short`, `Byte`
- Gleitkomma: `Double`, `Float`
- Sonstige: `Boolean`, `Char`, `String`, `Any`, `Unit`, `Nothing`

## 🔹 Pakete und Dateien

- Eine Datei kann mehrere Klassen/Funktionen enthalten.
- Top-Level-Funktionen sind erlaubt (kein Klassen-Zwang).

## 🔹 Siehe auch

- [[Datentypen]]
- [[Funktionen]]
- [[Null-Sicherheit]]
- [[Typecasts]]
- [[Kontrollstrukturen]]
- [[Operatoren]]
- [[Listen]]
- [[Packages und Imports]]
