
Strings in Kotlin bieten viele nützliche Funktionen zur Bearbeitung und Verarbeitung von Text.

## 🔹 String-Manipulation  

- **`toUpperCase()`**: Wandelt den String in Großbuchstaben um.  
- **`toLowerCase()`**: Wandelt den String in Kleinbuchstaben um.  
- **`replace()`**: Ersetzt Teile des Strings.  
- **`substring()`**: Extrahiert einen Teil des Strings.

> [!example] Kotlin – String  
> ```kotlin
> val str = "Hallo Welt"
> val upperStr = str.toUpperCase()  // "HALLO WELT"
> val subStr = str.substring(0, 5)  // "Hallo"
> println(upperStr)  // HALLO WELT
> ```

## 🔹 String-Suche  

- **`contains()`**: Prüfen, ob ein String einen bestimmten Text enthält.  
- **`startsWith()`**: Prüfen, ob der String mit einem bestimmten Text beginnt.  
- **`endsWith()`**: Prüfen, ob der String mit einem bestimmten Text endet.

> [!example] Kotlin – String-Suche  
> ```kotlin
> val str = "Kotlin ist cool"
> val containsWord = str.contains("cool")  // true
> println(containsWord)
> ```

## 🔹 String-Formatierung  

- **`$variable`**: Einfügen von Variablenwerten in einen String.  
- **`String.format()`**: Formatierung mit Platzhaltern.

> [!example] Kotlin – String-Formatierung  
> ```kotlin
> val name = "Anna"
> val greeting = "Hallo, $name!"  // String Interpolation
> println(greeting)  // Hallo, Anna!
> ```


## 🔹 Siehe auch

- [[Datentypen]]
- [[Kollektionen]]
- [[Lambda]]
- [[Funktionen]]
- [[Kollektionen - Operationen]]
