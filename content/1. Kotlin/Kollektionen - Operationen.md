
## 🔹 Listen (List)  

- **`add()`**: Element zu einer mutablen Liste hinzufügen.  
- **`get()`**: Element an einem bestimmten Index abrufen.  
- **`filter()`**: Elemente nach einem Bedingungskriterium filtern.  
- **`map()`**: Transformation von Elementen in eine neue Liste.  
- **`contains()`**: Prüfen, ob ein Element in der Liste vorhanden ist.

> [!example] Kotlin – Liste  
> ```kotlin
> val list = mutableListOf(1, 2, 3, 4)
> list.add(5)  // Element hinzufügen
> val even = list.filter { it % 2 == 0 }  // Filtert gerade Zahlen
> println(even)  // [2, 4]
> ```

## 🔹 Sets  

- **`add()`**: Element zu einem Set hinzufügen (nur einzigartige Elemente).  
- **`contains()`**: Prüfen, ob ein Element im Set enthalten ist.  
- **`union()`**: Vereinigung von zwei Sets.  
- **`intersect()`**: Schnittmenge von zwei Sets.

> [!example] Kotlin – Set  
> ```kotlin
> val set1 = setOf(1, 2, 3)
> val set2 = setOf(3, 4, 5)
> val union = set1.union(set2)  // Vereinigung
> println(union)  // [1, 2, 3, 4, 5]
> ```

## 🔹 Maps  

- **`put()`**: Schlüssel-Wert-Paar hinzufügen.  
- **`get()`**: Wert für einen bestimmten Schlüssel abrufen.  
- **`containsKey()`**: Prüfen, ob ein Schlüssel vorhanden ist.  
- **`mapKeys()`**: Transformation der Schlüssel.

> [!example] Kotlin – Map  
> ```kotlin
> val map = mutableMapOf("a" to 1, "b" to 2)
> map["c"] = 3  // Schlüssel-Wert hinzufügen
> val value = map["a"]  // Wert für "a" abrufen
> println(value)  // 1
> ```

## 🔹 Siehe auch

- [[Kollektionen]]
- [[Lambda]]
- [[Funktionen]]
- [[String Operationen]]
