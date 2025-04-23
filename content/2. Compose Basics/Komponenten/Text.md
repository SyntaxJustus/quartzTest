#Composable #Stateless #Komponente

>[!tldr] Text
>Die Text Komponente kann genutzt werden, um Schrift im UI anzeigen zu lassen
>Dabei gibt es eine Reihe von Parametern, die beeinflussen, wie der Text am Ende angezeigt wird.

> [!example] Beispiel
> ```kotlin
> Text(
> text = "Hallo Welt!",
> fontSize = 20.sp,
> fontWeight = FontWeight.Bold,
> color = Color.Blue)
> ```
> 
> \<Hier Bild>

>[!info]- Alle Parameter
>Text hat wie viele andere Komponenten eine Vielzahl von Parametern, die übergeben werden können. Verpflichtend muss nur der anzuzeigende Text übergeben werden.
> 
| Name           | Datentyp                      | Nutzung                                                                   |       Standardwert       |
| -------------- | ----------------------------- | ------------------------------------------------------------------------- | :----------------------: |
| text           | String                        | Inhalt, der angezeigt werden soll                                         |            ❌             |
| modifier       | [[Modifier]]                      | Standard Modifier für alle Composables                                    |        `Modifier`        |
| color          | Color                         | Textfarbe, Standardwert                                                   |   `Color.Unspecified`    |
| fontSize       | TextUnit                      | Textgröße, wird in der EInheit ***sp*** angegeben. Standardwert           |  `TextUnit.Unspecified`  |
| fontStyle      | FontStyle?                    | Kann genutzt werden, um Text kursiv anzuzeigen                            |          `null`          |
| fontWeight     | FontWeight?                   | Kann genutzt werden, um Text fett anzuzeigen                              |          `null`          |
| fontFamily     | FontFamily?                   | Schriftart                                                                |          `null`          |
| letterSpacing  | TextUnit                      | Abstand zwischen einzelnen Symbolen im Text, Einheit ***sp***             |  `TextUnit.Unspecified`  |
| textDecoration | TextDecoration?               | Text unterstreichen oder durchstreichen                                   |          `null`          |
| textAlign      | TextAlign?                    | Ausrichtung des Textes(z.B. zentriert, linksbündig etc.)                  |          `null`          |
| lineHeight     | TextUnit                      | Höhe einer Zeile in ***sp***                                              |                          |
| overflow       | TextOverflow                  | Verhalten, wenn der Text zu lang ist.                                     |   `TextOverflow.Clip`    |
| softwrap       | Boolean                       | Weiche Zeilenumbrüche                                                     |           true           |
| maxLines       | Int                           | Maximale Anzahl Zeilen                                                    |     `Int.MAX_VALUE`      |
| minLines       | minLines                      | Minimale Anzahl Zeilen                                                    |            1             |
| onTextLayout   | ((TextLayoutResult) -> Unit)? | Callback Funktion(<br>z.B Zugriff auf die Breite des Textes<br>)          |          `null`          |
| style          | TextStyle                     | Die oberen Parameter können auch gebündelt als TextStyle übergeben werden | `LocalTextStyle.current` |







