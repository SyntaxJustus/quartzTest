

| Kategorie        | Kotlin            | Swift             | Hinweise                                                                 |
|------------------|-------------------|-------------------|--------------------------------------------------------------------------|
| Ganzzahlen       | `Int`, `Long`, `Short`, `Byte` | `Int`, `Int64`, `UInt8` | Kotlin nutzt `Int` standardmäßig, Swift `Int` (plattformabhängig 32/64). |
| Gleitkomma       | `Double`, `Float` | `Double`, `Float` | Beide verwenden `Double` standardmäßig für Dezimalzahlen.                |
| Zeichen          | `Char`            | `Character`       | `Char` ist in Kotlin ein einzelnes Unicode-Zeichen, Swift ist Unicode-intelligenter. |
| Zeichenketten    | `String`          | `String`          | In beiden Sprachen unveränderlich (`immutable`).                         |
| Wahrheitswerte   | `Boolean`         | `Bool`            | Funktional identisch.                                                    |
| Beliebiger Typ   | `Any`             | `Any`             | Kotlin: Oberklasse aller Typen. Swift: Kombination mit `AnyObject` möglich. |
| Kein Rückgabewert| `Unit`            | `Void`, `()`      | Beide als Rückgabewert bei Funktionen ohne Ergebnis.                     |
| Niemals zurück   | `Nothing`         | `Never`           | Beide stehen für nicht rückkehrende Funktionen (z. B. Fehler).           |
| Nullable-Typ     | `String?`         | `String?`         | Gleiches Konzept mit `?`, in Swift via Optionals, in Kotlin strikt null-sicher. |
| Typinferenz      | Automatisch       | Automatisch       | Beide Sprachen erkennen Typen zur Compilezeit.                           |

## 🔹 Siehe auch
- [[Datentypen]]
- [[Null-Sicherheit]]
- [[Typecasts]]
- [[Kotlin Grundlagen]]
