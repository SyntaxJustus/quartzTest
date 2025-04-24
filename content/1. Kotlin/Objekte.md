## 🔹 Companion Objects

**Kotlin** nutzt **Companion Objects**, um statisches Verhalten innerhalb von Klassen zu ermöglichen – ähnlich wie `static` in anderen Sprachen.

### Kotlin – Companion Object  

- Ein **Companion Object** ist ein Singleton-Objekt innerhalb einer Klasse.  
- Ermöglicht Zugriff auf Funktionen/Eigenschaften **ohne Instanz der Klasse**.  
- Kann Interfaces implementieren und benannt werden.  

> [!example] Kotlin – Companion Object  
> ```kotlin
> class Nutzer {
>     companion object {
>         fun erstelleGast(): Nutzer {
>             return Nutzer()
>         }
>     }
> }
> 
> val gast = Nutzer.erstelleGast()
> ```

---

## 🔹 Object (Singleton)

Mit dem Schlüsselwort **`object`** können in Kotlin direkt **Singletons** definiert werden – nützlich für Utility-Klassen oder zentrale Services.

### Kotlin – Object  

- Erzeugt **automatisch eine Instanz** (Singleton).  
- Kann Eigenschaften, Funktionen und Initialisierungslogik enthalten.  
- Nützlich z. B. für Logging, Config, oder einfache Factorys.  

> [!example] Kotlin – Object (Singleton)  
> ```kotlin
> object Logger {
>     fun log(nachricht: String) {
>         println("[Log] $nachricht")
>     }
> }
> 
> Logger.log("App gestartet")
> ```

---

## 🔹 Unterschiede im Überblick

| Aspekt                    | Companion Object              | Object (Singleton)                  |
|---------------------------|-------------------------------|-------------------------------------|
| Position im Code          | Innerhalb einer Klasse        | Eigenständig                        |
| Zugriff                   | `Klasse.Methode()`            | `Objektname.Methode()`              |
| Instanzierung             | Automatisch bei Klassenzugriff| Automatisch beim ersten Zugriff     |
| Verwendungszweck          | Statische Member in Klassen   | Globale Singletons / Utils          |

---

## 🔹 Siehe auch

- [[Klassen]]
- [[Interfaces]]
- [[Null-Sicherheit]]
