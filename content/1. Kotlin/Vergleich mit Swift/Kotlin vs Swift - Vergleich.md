

Beide Sprachen sind modern, sicher und werden primär für die mobile Entwicklung eingesetzt:  
- **Swift** → Apple-Ökosystem (iOS, macOS, etc.)  
- **Kotlin** → Android (offizielle Sprache), multiplattformfähig mit Kotlin Multiplatform

---

## 🔹 Syntax-Grundlagen

| Thema           | Swift                            | Kotlin                           |
|----------------|-----------------------------------|----------------------------------|
| Variable        | `var name = "Anna"`              | `var name = "Anna"`              |
| Konstante       | `let name = "Anna"`              | `val name = "Anna"`              |
| String Interpolation | `"Hallo \(name)"`           | `"Hallo $name"`                  |
| Funktion        | `func greet() {}`                | `fun greet() {}`                 |
| Einzeiliger Ausdruck | `let x = a > b ? a : b`     | `val x = if (a > b) a else b`    |

---

## 🔹 Null-Sicherheit

Beide Sprachen bieten **Null-Sicherheit**, aber auf unterschiedliche Weise:

### Swift  
- Nutzt **Optionals** (`?`) und zwingt zur expliziten Entpackung.  
- **Unsicheres Entpacken** mit `!` kann zu Laufzeitfehlern führen.  
- **Sicheres Entpacken** über optional binding (`if let`, `guard let`) oder `??`.

> [!example] Swift – Optionals  
> ```swift
> var name: String? = "Anna"
> print(name?.uppercased())            // sicherer Zugriff
> print(name ?? "Kein Name")           // Default-Wert
> 
> if let safeName = name {
>     print("Hallo, \(safeName)")
> }
> ```

---

### Kotlin  
- Nutzt **nullable Types** (`String?`) und bietet viele Operatoren für sichere Zugriffe.  
- **Elvis-Operator** `?:` für Default-Werte.  
- **Not-null assertion** `!!` erzeugt Ausnahme bei `null`.

> [!example] Kotlin – Nullable Types  
> ```kotlin
> var name: String? = "Anna"
> println(name?.uppercase())          // sicherer Zugriff
> println(name ?: "Kein Name")        // Elvis-Operator
> 
> name?.let {
>     println("Hallo, $it")
> }
> ```

---

### 🔍 Unterschiede im Überblick

| Aspekt               | Swift                             | Kotlin                             |
|----------------------|------------------------------------|-------------------------------------|
| Null-fähiger Typ     | `String?`                         | `String?`                           |
| Default-Wert         | `name ?? "Fallback"`              | `name ?: "Fallback"`               |
| Sicheres Unwrapping  | `if let`, `guard let`             | `?.let { }`                         |
| Unsicheres Unwrapping| `name!`                           | `name!!`                            |
| Null-Prüfung         | Manuell über Optionals            | Sprachfeatures wie `?.`, `?:`, `let` |


## 🔹 Collections

| Art       | Swift                                  | Kotlin                            |
|-----------|-----------------------------------------|-----------------------------------|
| Liste     | `let list = [1, 2, 3]`                 | `val list = listOf(1, 2, 3)`      |
| Set       | `let set: Set = [1, 2, 3]`             | `val set = setOf(1, 2, 3)`        |
| Map       | `let dict = ["a": 1, "b": 2]`          | `val map = mapOf("a" to 1, "b" to 2)` |

---

## 🔹 Klassen & Datenmodelle

> [!example] Swift – struct  
> ```swift
> struct User {
>     var name: String
>     var age: Int
> }
> ```

> [!example] Kotlin – data class  
> ```kotlin
> data class User(val name: String, val age: Int)
> ```

---

## 🔹 Asynchrone Programmierung

| Thema           | Swift                              | Kotlin                          |
|----------------|-------------------------------------|---------------------------------|
| Keywords        | `async/await`, `Task`              | `suspend`, `CoroutineScope`    |
| Beispiel        | `let result = await fetchData()`   | `val result = fetchData()` (in suspend) |

---

## 🔹 Plattformintegration

- **Swift**: Nahtlos in Xcode, SwiftUI und UIKit integriert.
- **Kotlin**: Nahtlos in Android Studio, Jetpack Compose und Kotlin Multiplatform verwendbar.

---

## 🔹 Gemeinsamkeiten

- Starke Typisierung  
- Moderne Syntax  
- Interoperabel mit älteren Sprachen (Swift ↔ Objective-C, Kotlin ↔ Java)  
- Unterstützen Functional Programming-Paradigmen

---

## 🔹 Unterschiede auf einen Blick

| Kategorie       | Swift                          | Kotlin                            |
| --------------- | ------------------------------ | --------------------------------- |
| Plattform       | Apple                          | Android, Multiplattform           |
| Null-Sicherheit | Optional (`?`) + `!` + `guard` | Nullable Types + `?.`, `!!`, `?:` |
| UI Framework    | SwiftUI / UIKit                | Jetpack Compose / XML             |
| Nebenläufigkeit | `async/await` + `Task`         | `suspend`, `launch`, `async`      |

---



## 🔹 Siehe auch
- [[Kotlin vs Swift - Datentypen]]
- [[Datentypen]]
- [[Kotlin Grundlagen]]
- [[Null-Sicherheit]]
- [[Typecasts]]
