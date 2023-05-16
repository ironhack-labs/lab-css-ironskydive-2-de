![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)


# Geleitete Übung - IronSkydive 🎨 - styling (CSS)

<br>

## Einführung

An diesem Punkt bist Du mit Cascading Style Sheets (CSS) vertraut und weißt, wie Du:

- Elemente über Tags, Klassen oder IDs auswählen kannst,
- mit Schrift- und Texteigenschaften arbeitest,
- Farben für Text und Hintergrund hinzufügen kannst.

Denke daran, das **CodePen** zu öffnen, das Du zu Beginn der Übung erstellt hast, um die verschiedenen Iterationen der Übung durchzuführen.

Los geht's!

<br>

## IDs

Zunächst fügst Du vier IDs hinzu, eine pro `<section>`, die Du definiert hast. Von oben nach unten sollten die IDs wie folgt sein:

- `general-information`
- `structure`
- `team`
- `schedule`

Dies wird uns helfen, die verschiedenen Abschnitte zu identifizieren. Es erstellt auch sogenannte [internal links](http://www.yourhtmlsource.com/text/internallinks.html). Was passiert jetzt, wenn Du auf die Links im `<nav>` am oberen Rand der Seite klickst? Es scrollt automatisch zum Abschnitt! :white_check_mark:

<br>

## Allgemeine Einstellungen für die gesamte Seite

Okay, lass uns mit dem CSS-Tab in Deinem CodePen-Projekt beginnen. Wir werden damit beginnen, die gesamte Seite auf die folgende Regel einzustellen (kopiere den Snippet am Anfang des CSS-Tab):

```css
html,
body {
  margin: 0;
  padding: 0;
}
```

Dies entfernt alle `margin` und `padding` der Elemente oder setzt sie auf 0. Warum machen wir das? Wir machen das, um einige Stile zurückzusetzen, die Dein Browser automatisch auf Elemente anwendet, die als _Browser-Standardstile_ bekannt sind.

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_603c70d5d3664d3cd0d7829c6b0367cb.png)

<br>

:thought_balloon: Keine Sorge, was `margin` und `padding` Eigenschaften sind, besprechen wir gleich.

<br>

## Schrift und Text

### font-family

Für die gesamte IronSkydive-Website werden wir eine Schrift namens `Roboto` verwenden. Du findest sie in `https://fonts.google.com/`, einem Google-Repository, das eine große Anzahl von Schriftarten enthält. Normalerweise musst Du einen Prozess durchlaufen, um eine dieser Schriftarten in Deine Website einzubetten, aber wir haben es für Dich vereinfacht.

Kopiere am Anfang des CSS-Tab in Deinem CodePen die folgende Zeile:

```css
@import url('https://fonts.googleapis.com/css?family=Roboto+Condensed:700|Roboto:100,300,700');
```

Es passiert noch nichts. Es fügt nur eine Referenz zu zwei verschiedenen Schriftarten hinzu:

- `Roboto`, mit Gewichten von 100, 300 und 700.
- `Roboto Condensed`, mit einem Gewicht von 700.

Du wirst beide auf Deiner Website verwenden. Lass uns also die Schrift für das gesamte Dokument ändern. Der gesamte Text des Dokuments sollte wie folgt formatiert sein:

- Schriftart (font): `Roboto`.
- Größe (size): `10px`.
- Zeilenhöhe (line height): `3.5em`.
- Gewicht (weight): `300`.

Denke daran: Wir können Elemente auswählen, auf die wir einige Stile anwenden möchten, indem wir Klassen oder IDs oder _Tag-Namen_ verwenden. 
Du kannst das `body`-Tag verwenden und diese entsprechenden CSS-Eigenschaften hinzufügen. Sobald Du die Schriftart für das Dokument definiert hast, ändern wir das Verhalten der Überschriften.

Du verwendest Überschriften von 1 bis 5, verwende einen _Multi-Selektor_, der alle auswählt. Innerhalb dieses Selektors legst Du die Schriftart auf `Roboto Condensed` fest. Wir werden die Größe der Überschriften in einem anderen Selektor ändern, da jede von ihnen eine andere Größe haben wird.

```css
/* CSS multiselector example */

h1,
h2,
h3,
h4,
h5,
h6 {
  /*  define font-family here  */
}
```

Das Ergebnis sollte ungefähr so aussehen:

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_8772412e132f34f5246213a371f16ea5.png)

<br>

### Texteigenschaften

Derzeit haben alle Schriftarten die gleiche Größe. Lass uns das ändern. Zunächst stylen wir die Überschriften, indem wir die folgenden Eigenschaften hinzufügen:

| Heading | Properties                                                                                                                                                                                         |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `<h1>`  | Size: `9em` <br> Align: `center` <br> Transform: `uppercase`                                                                                                                                       |
| `<h2>`  | Size: `5em` <br> Align: `center` <br> Transform: `uppercase`                                                                                                                                       |
| `<h3>`  | Size: `4.2em` <br> Align: `center` <br> [Line height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height): `1em`                                                                         |
| `<h4>`  | Size: `1.5em` <br> [Letter spacing](https://developer.mozilla.org/en/docs/Web/CSS/letter-spacing): `0.4px` <br> [Line height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height): `1em` |
| `<h5>`  | Size: `1.2em` <br> [Line height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height): `1em`                                                                                              |

Sobald Du diese Stile auf die verschiedenen Überschriften angewendet hast, benötigen `<h1>` und `<h2>` mehr Platz zwischen ihnen. Lass uns mehr Platz hinzufügen, indem wir die `line-height`-Eigenschaft von `<h2>` auf `4em` setzen.

Du hast bereits alle Textstile spezifiziert, die Du auf Deiner Website benötigst.

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_b0f5f1c39886cbe09c75630ca7706c2a.png)

<br>

Großartig, lass uns jetzt etwas Farbe auf unserer Website hinzufügen.

<br>

## Farben

<br>

Zuvor hast Du die CSS-Texteigenschaften verwendet, um das Aussehen der Website zu ändern, indem Du eine benutzerdefinierte Schriftart und Größen hinzugefügt hast, abhängig vom Tag. Jetzt ist es Zeit, etwas Farbe zu geben!

Wenn Du eine Website entwickelst, ist es eine gute Praxis, eine Tabelle mit den verschiedenen Farben im Hinterkopf zu behalten, die Du verwenden wirst. In diesem Fall ist die Tabelle:

| Color     | RGB            | Result                                                                                        |
| --------- | -------------- | --------------------------------------------------------------------------------------------- |
| Blue      | `67, 163, 230` | <div style="background: rgb(67, 163, 230); height: 20px; margin: 0 auto; width: 20px;"></div> |
| Dark Blue | `25, 33, 41`   | <div style="background: rgb(25, 33, 41); height: 20px; margin: 0 auto; width: 20px;"></div>   |
| Text      | `0, 0, 0`      | <div style="background: rgb(0, 0, 0); height: 20px; margin: 0 auto; width: 20px;"></div>      |

Diese Tabelle wird Dir helfen, mit Deinem UX/UI-Design-Team zu kommunizieren. Wenn sie Dir sagen, dass Du `Dark Blue` als Hintergrundfarbe anwenden sollst, weißt Du sofort, welche Farbe es ist.

Lass uns nacheinander die Änderungen beschreiben, die Du auf die verschiedenen Abschnitte anwenden musst, die wir in der ersten Iteration dieser Übung definiert haben. Erinnere Dich an das Layout, das wir erstellt haben:

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_8f778c8cd703db596d5bb22dae089716.jpg)

<br>

Öffne CodePen in Deinem Browser und lass uns loslegen!

<br>

### Nav

<br>

Das Endziel für die `nav`-Leiste sieht so aus:

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_065124c74d928a12e32e446b759968e3.png)

<br>

Lass uns damit beginnen, die Farbe hinzuzufügen. Füge `Dark Blue` als Hintergrundfarbe hinzu.

Es ist eine gute Praxis, Klassen-Selektoren anstelle von HTML-Tag-Selektoren zu verwenden, um Stile zu definieren. Was ist, wenn Du einen Stil auf das `nav`-Tag anwendest und es in Zukunft in `header` änderst? Du würdest alle Stile verlieren und sie nacheinander im CSS ändern müssen.

Erstelle einen Selektor in Deinem CSS-Tab namens `.nav-bar` und weise ihm den oben beschriebenen Stil zu. Weise dann die Klasse dem `nav`-Tag in Deinem HTML zu.

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_320885335d288348997362c44aa6f6b0.png)

<br>

Es funktioniert... irgendwie. Wir müssen die Farbe der Links auf Weiß setzen und wenn Du versuchst, die Eigenschaft `color: white` innerhalb der `.nav-bar`-Klasse festzulegen, funktioniert es nicht, da Wörter/Links in `a`-Tags eingewickelt sind.

Wir können in Richtung Erstellung einer neuen Klasse gehen und die Klasse jedem `li`-Element innerhalb von <nav> zuweisen, oder wir können **DRY** (Don't Repeat Yourself) gehen und vermeiden, eine weitere Klasse zu erstellen, sondern stattdessen die Elemente referenzieren, die wir durch die vorhandene Klasse `.nav-bar` anvisieren möchten.

```css
.nav-bar a {
  /*  styles to be added here    */
}
```

<!-- Lass uns eine weitere Klasse namens `nav-bar-item` erstellen und -->

Ändere die color auf _white_, die text-decoration auf _none_ und die `font-size` auf `2em`, um das gewünschte Ergebnis zu erhalten.

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_e03b2f8983da0df77b6e88f973cfc0c5.png)

<br>

In den nächsten Iterationen wirst Du das Menü vervollständigen. Du bist bereit, zur nächsten Sektion zu wechseln.

<br>

### Header

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_e80b0ee85c8f2fb8126befe68b152ab2.png)

<br>

Keine Angst! Es ist einfacher als es scheint. Zunächst musst Du das [Hintergrundbild](https://developer.mozilla.org/en/docs/Web/CSS/background-image?v=control) festlegen. Die Eigenschaften des Hintergrundbildes sind:

- **url:** `https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/ironhack-skydive-background.jpg`.
- **position:** `0 0`.
- **repeat:** `no-repeat`
- **size:** `cover`.

Denke daran, dass Du eine Klasse erstellen solltest, in diesem Fall `header`, und sie dem `header`-Tag in Deinem HTML zuweisen solltest, um diesen Stil zu verwenden. Setze dann einfach die Höhe des `header` auf `650px`.

Der nächste Schritt ist, die Farbe des `h2` auf Weiß zu ändern und dann etwas [`text-shadow`](https://developer.mozilla.org/en/docs/Web/CSS/text-shadow) hinzuzufügen. Die `text-shadow`-Eigenschaft sollte den Wert `#020819 8px -20px 9px` haben.

Um diesen Abschnitt abzuschließen, ändere die Schriftgröße des Zitats. Setze sie auf `2.5em`. Erstelle eine `quote`-Klasse, um dies zu tun, und füge die Klasse dem `aside`-Tag im HTML hinzu.

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_c03f57b39ea0d76161156d6e58d91307.png)

<br>

### Sektion 1

In einer der vorherigen Iterationen hast Du dieser Sektion eine `general-information` id hinzugefügt. Unser Endziel für diese Sektion ist:

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_505f90aabf6c0d4e03b4216c07c615f8.png)

<br>

Erstelle einen Klassen-Selektor namens `dark-background`, der die folgenden Eigenschaften anwendet:

- background color: Dunkelblau (siehe Tabelle am Anfang dieser Iteration).
- color: Weiß.

Sobald Du die Klasse in Deinem CSS erstellt hast, füge sie der Sektion hinzu. Nachdem Du die Klasse angewendet hast, kannst Du sehen, dass der Text in `<p>` winzig ist und nicht zentriert ist. Lass uns dieses Problem lösen.

Füge zu jedem Absatz innerhalb der `general-information`-Sektion eine `text`-Klasse hinzu.

<!-- Erstelle dann einen Mehrfach-Selektor, der alle Elemente mit einer `.text`-Klasse innerhalb des `#general-information`-Elements auswählt. -->

Dieser Selektor sollte die folgenden CSS-Eigenschaften haben:

- Font size: `2em`.
- Font weight: `100`.
- Text Align: `center`.

Viel besser. Beenden wir diese Sektion, indem wir einige Styles zu den Links hinzufügen. Die Links werden wie Buttons aussehen, und alle Links dieser Sektion werden die gleiche Erscheinung haben. Das bedeutet, dass Du eine Klasse erstellen solltest, die die notwendigen CSS-Eigenschaften auf einen Link anwendet, um wie ein Button auszusehen.

<br>

:::info
:bulb: **Warum sollten wir keinen Button verwenden?** Schau Dir [diese sehr knappe Antwort auf StackOverflow ](https://stackoverflow.com/a/25350722/4624718) an, um eine gute Faustregel zu erhalten.
:::

<br>

Erstellen wir eine `link-btn`-Klasse mit den folgenden Eigenschaften:

- background color: blau (siehe Tabelle am Anfang dieser Iteration).
- color: weiß.
- font-family: `Roboto Condensed`.
- font size: `2em`.
- [Letter Spacing](https://developer.mozilla.org/en/docs/Web/CSS/letter-spacing): `0.5px`.
- text-align: `center`.
- text-decoration: `none`.

Fügen wir die Klasse den drei Links im Abschnitt hinzu.

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_7847968ca22bceb75dac295214859d36.png)

<br>

Hmm... Es scheint, als bräuchten wir eine Möglichkeit, unsere Elemente neu anzuordnen und sie an bestimmten Positionen zu platzieren. Dies wird das Ziel einer der nächsten Iterationen sein.

Lass uns zum nächsten Abschnitt gehen.

### Sektion 2

Im zweiten Abschnitt haben wir eine `structure`-ID hinzugefügt. In diesem Abschnitt musst Du nur die Schriftgröße und -ausrichtung einrichten.

<!-- Du wirst auch die `img`-Breiteneigenschaft entfernen und in der CSS setzen.  -->

Erstelle eine `service-box`-Klasse in der CSS mit den folgenden Eigenschaften:

- Font Size: `1.7em`.
- Text Align: `center`.

Weise diese Klasse jedem `article` innerhalb des `structure`-Abschnitts zu.

Erstelle jetzt neue Mehrfach-Selektoren für alle `img`-Klassen innerhalb der `service-box`-Klasse.

:+1: Spoiler: Ähnlich wie Du es bereits mit den Links in der Navbar gemacht hast, werden wir hier folgendes haben:

```css
.service-box img {
  /*  styles to be added  */
}
```

Füge eine Eigenschaft hinzu, um die Breite dieser Bilder auf `125px` zu setzen:

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_85b85fdc98c951967b3554ee821cbfaa.png)

<br>

### Sektion 3

Das Ziel beim Schreiben von hochwertigem CSS ist das Erstellen von Klassen, die wiederverwendet werden können. In diesem Abschnitt haben wir wieder dunkelblau als Hintergrundfarbe. Du hast zuvor eine `dark-background`-Klasse erstellt und füge nun diese Klasse der `team`-Sektion hinzu.

Jetzt musst Du zwei verschiedene Klassen erstellen - eine für den Text des Abschnitts und eine andere für die Namen der Teammitglieder. Die erste Klasse, `section-text`, setzt die Schriftgröße auf `1.9em`, und der Text sollte `zentriert` sein.

Auf der anderen Seite wird die `member-name`-Klasse die Schriftgröße auf `1.5em` setzen, mit einer Schriftstärke von `700`. Füge die erste Klasse zu den `p` im HTML hinzu, und die zweite Klasse zu allen `h4`-Tags.

Um zu vermeiden, dass Eigenschaften andere Klassen überschreiben, erstelle einen Multi-Selektor, um diese Klassen speziell innerhalb des `team`-ID-Elements zu setzen:

```css
#team .section-text {
}

#team .member-name {
}
```
Lass uns auch die Bilder in diesem Abschnitt bearbeiten. Wie wir sehen können, sind sie sehr groß. Verwenden wir mehrere Selektoren, um die `img`-Tags innerhalb von `#team` auszuwählen und die folgenden Eigenschaften festzulegen:

- width auf 250px und
- height auf 180px.

:+1: Spoiler:

```css
#team img {
  /* styles to be added here */
}
```

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_dbe16d63517310a82a988f9f13df4867.png)

<br>

### Sektion 4

_Noch nichts zu tun ... aber gleich!!_

### Footer

Wir haben wieder einen dunklen Hintergrund und weißen Text. Füge der `footer`-Tag im HTML die `dark-background`-Klasse hinzu. Erstelle eine `footer`-Klasse und füge sie als zweite Klasse zur `<footer>`-Tag hinzu. Verwende diese Klasse, um den gesamten Text in diesem Element zu zentrieren und die Schriftgröße auf `1.9em` einzustellen.

:+1: Spoiler: Um eine zweite Klasse hinzuzufügen, musst Du folgendes tun:

```html
<!-- ... -->

<footer class="dark-background footer">
  <!-- ... -->
</footer>
```

Erstelle jetzt eine neue Klasse - `address` - und weise sie dem HTML-Tag `address` zu. Definiere in dieser Klasse:

- font style: `normal`.
- font size: `0.8em`.

Wir sind fast fertig. Genau wie wir alle Links innerhalb der Navigationsleiste angesprochen haben (mithilfe des mehrfachen Selektoren-Ansatzes), sollen wir hier alle Links innerhalb der Fußzeile ansprechen und ihre Styles definieren:

- color: Blau (siehe Tabelle am Anfang dieses Abschnitts).
- text-decoration: Keine.

Weise diese Klasse jedem Element innerhalb der Liste zu, die du in der Fußzeile hast.

:+1: Spoiler: So geht es weiter:

```css
.footer a {
  /* styles to be added here */
}
```
Und zu guter Letzt, in dieser Iteration, müssen wir die Punkte von der Liste entfernen, die die Links zu den sozialen Medien anzeigt. Hierfür kannst du das ul-Tag innerhalb der Fußzeile ansprechen und die Eigenschaft `list-style` auf _none_ setzen. Das war's!

<br>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_791457cbe452066c3123de22f4182eb8.png)

<br><br>

:heart: **Viel Spaß beim Coden!**
