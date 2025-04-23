
## 🔹 Was sind Packages?
- Ein **Package** (Paket) ist eine logische Gruppierung von Klassen, Funktionen etc.
- Wird verwendet, um **Code zu strukturieren** und **Namenskonflikte zu vermeiden**.
- Top-Level-Elemente (Funktionen, Klassen etc.) gehören standardmäßig zu einem Paket.

> [!example] Beispiel: Paketdeklaration
> ```kotlin
> package com.meinprojekt.utils
> 
> fun begruessung() {
>     println("Hallo!")
> }
> ```

## 🔹 Standardpaket
- Wenn kein `package` angegeben ist, gehört der Code zum **Default-Paket** (kein spezifischer Name).
- **Nicht empfohlen** für größere Projekte.

## 🔹 Imports
- Mit `import` werden Elemente aus anderen Paketen verfügbar gemacht.
- Ermöglicht Zugriff auf Klassen, Funktionen oder Objekte ohne vollständigen Paketnamen.

> [!example] Beispiel: Importieren einer Klasse
> ```kotlin
> import kotlin.math.PI
> import kotlin.math.pow
> 
> fun flaecheKreis(radius: Double): Double {
>     return PI * radius.pow(2)
> }
> ```

## 🔹 Importarten
- **Direkter Import:** Importiert ein bestimmtes Element.
- **Wildcard-Import (`*`):** Importiert alle sichtbaren Elemente eines Pakets.
- **Alias-Import:** Gibt einem importierten Element einen anderen Namen.

> [!example] Beispiel: Verschiedene Importarten
> ```kotlin
> import kotlin.math.*         // Wildcard
> import java.util.Date as UtilDate // Alias
> 
> val now = UtilDate()
> ```

## 🔹 Sichtbarkeit & Zugänglichkeit
- Nur **öffentliche** (public) Elemente sind außerhalb ihres Pakets zugänglich.
- Bei internen oder privaten Elementen ist ein direkter Import nicht möglich.

## 🔹 Best Practices
- Paketname entspricht üblicherweise dem Verzeichnisnamen.
- Namenskonvention: **kleingeschrieben, reverse Domain Notation**
  - z. B. `com.example.projektname`

## 🔹 Siehe auch

