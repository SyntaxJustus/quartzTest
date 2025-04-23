
## 🔹 Überblick
- In Kotlin wird Typkonvertierung verwendet, um Werte zwischen verschiedenen Typen zu konvertieren.
- Es gibt **explizite** und **implizite** Konvertierungen, wobei Konvertierungsfunktionen und Typecasts häufig zum Einsatz kommen.

## 🔹 Konvertierungsfunktionen
- Kotlin stellt eine Vielzahl von **Konvertierungsfunktionen** bereit, um Werte zwischen verschiedenen Typen zu konvertieren.
- Diese Funktionen sind besonders nützlich, wenn du einen Wert in einen anderen Typ umwandeln möchtest.

> [!example] Beispiel: Konvertierungsfunktionen  
> ```kotlin
> val zahlString: String = "123"
> val zahlInt: Int = zahlString.toInt()  // String zu Int
> val zahlDouble: Double = zahlInt.toDouble()  // Int zu Double
> val zahlStr: String = zahlDouble.toString()  // Double zu String
> ```

### 🔸 Häufig verwendete Konvertierungsfunktionen
- **`toString()`**: Wandelt einen Wert in eine **String-Repräsentation** um.
- **`toInt()`**: Wandelt einen String in eine **Ganzzahl (Int)** um, falls möglich.
- **`toDouble()`**: Wandelt einen String oder eine Zahl in **Double** um.
- **`toFloat()`**: Wandelt eine Zahl oder einen String in **Float** um.
- **`toLong()`**: Wandelt einen String in eine **Long** um.
- **`toBoolean()`**: Wandelt einen String in **Boolean** um, wobei `"true"` zu `true` und `"false"` zu `false` wird.

> [!example] Beispiel: Konvertierungen mit verschiedenen Typen  
> ```kotlin
> val str = "123"
> val intVal: Int = str.toInt()  // String zu Int
> val floatVal: Float = str.toFloat()  // String zu Float
> val boolVal: Boolean = "true".toBoolean()  // String zu Boolean
> ```

## 🔹 Automatische Konvertierungen bei numerischen Typen
- Kotlin führt **automatische Konvertierungen** zwischen kompatiblen numerischen Typen durch, wie von `Int` zu `Double`, wenn der Kontext es zulässt.

> [!example] Beispiel: Automatische numerische Konvertierung  
> ```kotlin
> val intZahl: Int = 42
> val doubleZahl: Double = intZahl  // Implizite Konvertierung von Int zu Double
> ```

## 🔹 Siehe auch
- [[Typecasts]]
- [[Datentypen]]
- [[Kotlin Grundlagen]]
- [[Null-Sicherheit]]
- [[Operatoren]]



