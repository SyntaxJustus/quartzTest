
| Thema              | Kotlin                                  | Swift                                 | Hinweise                                                                 |
|--------------------|------------------------------------------|----------------------------------------|--------------------------------------------------------------------------|
| Variable (mutable)   | `var name = "Anna"`                    | `var name = "Anna"`                    | Gleiches Keyword `var`.                                                  |
| Konstante (immutable)| `val pi = 3.14`                      | `let pi = 3.14`                        | `val` in Kotlin, `let` in Swift.                                         |
| Funktion           | `fun greet(name: String): String`     | `func greet(name: String) -> String`   | Fast identisch – Kotlin nutzt `fun`, Swift `func`.                      |
| Rückgabetyp Unit/Void| `fun sayHi(): Unit`                 | `func sayHi() -> Void` oder `-> ()`    | `Unit` und `Void` sind äquivalent.                                       |
| String Interpolation| `"Hallo, $name!"`                   | `"Hallo, \(name)!"`                    | Swift nutzt `\()` innerhalb von Strings.                                 |
| if / else          | `if (x > 5) { ... } else { ... }`     | `if x > 5 { ... } else { ... }`        | In Kotlin Klammern nötig, in Swift optional.                             |
| switch / when      | `when (x) { ... }`                    | `switch x { ... }`                     | Swift erlaubt Pattern Matching, Kotlin auch mit `when`.                 |
| Null-Prüfung       | `val name: String? = null`<br>`name?.length` | `var name: String? = nil`<br>`name?.count` | Gleiches Konzept durch `?` und sichere Zugriffe.                         |
| Elvis-Operator     | `val n = name ?: "Unbekannt"`         | `let n = name ?? "Unbekannt"`          | Swift verwendet `??` statt `?:`.                                         |
| Smart Cast / Optional Unwrap | `if (x is String) println(x.length)` | `if let str = x as? String { ... }`   | Swift verlangt explizites Optional Binding.                              |
| Array / Liste      | `val list = listOf("A", "B")`         | `let list = ["A", "B"]`                | In Kotlin: `List`; in Swift: `Array`.                                    |
| for-Schleife       | `for (i in 1..5)`                     | `for i in 1...5`                        | Swift: geschlossene Ranges `...`, Kotlin: `..`.                          |
| Null Assertion     | `name!!`                              | `name!`                                | Vorsicht in beiden Sprachen – kann Crash verursachen.                    |

## 🔹 Siehe auch
- [[Datentypen]]
- [[Kotlin Grundlagen]]
- [[Null-Sicherheit]]
- [[Typecasts]]
