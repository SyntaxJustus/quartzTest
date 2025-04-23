
## 🔹 Überblick
- Kotlin ist **statisch typisiert**, d. h. jeder Ausdruck hat zur Compile-Zeit einen Typ.
- Viele Datentypen ähneln denen in **Swift**, z. B. `Int`, `Double`, `Boolean`.
- Dank **Typinferenz** muss der Typ oft nicht explizit angegeben werden.

## 🔹 Ganzzahlen
- `Byte` (8 Bit), `Short` (16 Bit), `Int` (32 Bit), `Long` (64 Bit)
- **Standard:** `Int`
- In Swift: ähnlich → `Int`, `Int64`, `UInt` usw.

> [!example] Beispiel: Ganzzahlen  
> ```kotlin
> val zahl: Int = 42
> val grosseZahl: Long = 1_000_000L
> ```

## 🔹 Gleitkommazahlen
- `Float` (32 Bit, Suffix `f`)
- `Double` (64 Bit, Standard)
- Swift verwendet dieselben Typen (`Float`, `Double`)

> [!example] Beispiel: Gleitkommazahlen  
> ```kotlin
> val pi: Double = 3.1415
> val temperatur: Float = 36.6f
> ```

## 🔹 Zeichen & Text
- `Char` für **einzelne Zeichen** (in `'`), `String` für **Zeichenketten** (in `"`)
- Swift hat ebenfalls `Character` und `String`, aber mit Unicode-freundlicheren Operationen.

> [!example] Beispiel: Zeichen und Strings  
> ```kotlin
> val buchstabe: Char = 'A'
> val begruessung: String = "Hallo Welt"
> ```

## 🔹 Wahrheitswerte (Boolean)
- `Boolean` mit den Werten `true` und `false`
- In Swift: `Bool` mit identischen Werten

> [!example] Beispiel: Boolean  
> ```kotlin
> val istKalt: Boolean = false
> val istErlaubt = true
> ```

## 🔹 Sondertypen

### 🔸 `Any`
- Oberster Basistyp für alle Nicht-Null-Typen.
- In Swift ähnlich wie `Any`, wird aber häufig mit `AnyObject` kombiniert.

### 🔸 `Unit`
- Entspricht `void` in Java, Swift verwendet stattdessen `Void` oder `()`.

### 🔸 `Nothing`
- Repräsentiert **kein Ergebnis** – z. B. bei Funktionen, die nur Exceptions werfen.
- Swift hat kein direktes Pendant, aber `Never` kommt dem nahe.

> [!example] Beispiel: Unit und Nothing  
> ```kotlin
> fun sagHallo(): Unit {
>     println("Hallo!")
> }
> 
> fun fehler(): Nothing {
>     throw IllegalStateException("Fehler!")
> }
> ```

## 🔹 Typinferenz
- Der Compiler erkennt automatisch den Datentyp anhand des zugewiesenen Werts.
- In Swift funktioniert Typinferenz auf sehr ähnliche Weise.

> [!example] Beispiel: Typinferenz  
> ```kotlin
> val name = "Anna"     // automatisch String
> val zahl = 123        // automatisch Int
> ```

## 🔹 Siehe auch
- [[Kotlin Grundlagen]]
- [[Typecasts]]
- [[Null-Sicherheit]]
- [[Operatoren]]


