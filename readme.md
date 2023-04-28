# Übungsaufgabe (Freiwillig)

Dies ist eine kleine Übung zum Thema Box-Model mit folgenden Unterkategorien:
- margin und padding
- background images + kleiner CSS-Trick
- positioning

Die ungefähre Dauer für die Aufgabe sollte zwischen 1-2h liegen

## Vorbereitung

- Erstelle eine `index.html` und eine `style.css`
- Versuche mit größen wie `em` oder `rem` zu arbeiten

### Einstellen von `em` und `rem`

`1rem` entspricht standartmäßig `16px`, daher passen wir den Wert etwas an.
Wir setzen in der `style.css` die Schriftgröße auf 62.5%. Dies sorgt dafür, dass `1rem` nun `10px` entspricht und hilft uns ältere Beispiele, die in `px` angegeben werden schnell und einfach einzubinden. Sollte ein Kunde oder ein Beispielcode im Internet eine Größe von `350px x 200px` angeben müssen wir nicht erst `350/16 x 200/16` rechnen um die korrekten Werte/das Seitenverhältnis in `rem` zu erhalten. Stattdessen können wir einfach das Komma verschieben (
`350px x 200px ~ 35rem x 20rem`).

```
:root{
    font-size: 62.5%;
}
```

Anschließend sollten wir einen softreset durchführen. Da normalerweise ein `p` andere default Einstellungen hat als zum Beispiel `h1` oder `div` können wir durch den Softreset dafür sorgen, dass alle Elemente gleich auf margin und padding reagieren.

```
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

Als letztes stellen wir die Schriftgröße im `body` wieder auf `16px` (Standard Schriftgröße auf Webseiten)

```
body{
    font-size: 1.6rem;
}
```

## Aufgaben

- Erstelle im body einen `header`, `nav` und 3 `sections` mit der Breite von 80% und zentriere alles,
- gib jeder `section` die Höhe einer vollen Bildschirmhöhe
- setze die ganze Seite auf scroll smooth **(neu)**
- wähle eine [sans-serif](https://www.w3schools.com/cssref/css_websafe_fonts.php) Schriftart für deine Seite
- Erstelle einen Seitenüberschrift im `header` "Box-Model Zusammenfassung"
- gib jeder `section` eine passende Überschrift
    - section 1: "Margin & Padding"
    - section 2: "Background"
    - section 3: "Position"
- Jede Überschrift sollte einen Margin nach oben und unten von 25px haben

### Section 1: Margin und Padding

- Erzeuge 3 Div container mit je einem `p-tag`, das eine Breite von `30%` des Elternelementes einnimmt.
    - Erzeuge einen `Lorem` Text und ändere die Schriftart der `p-tags` in `Monospace`
    - Erzeuge eine `border` mit abgerundeten Ecken
        - Zusatz: Versuche den `box-shadow` Effekt zu nutzen
- Füge Bilder hinzu
    - Span 1: Bild rechts
    - Span 2: Bild links
    - Span 3: Bild rechts
    - die Bilder sollten 25% des Elternelementes einenhmen
    - sorge für etwas Platz zwischen dem Text und dem Bild
    Tipp: Die Section sind 100% ;)

### Section 2: Background & Position

Nutze hier den `background` shorthand

|Befehl|background-image|background-size|background-position|background-repeat|
|---|---|---|---|---|
|background:|url("./images/image.jpg")|100%|cover|no-repeat|
```
{
   background: url("./images/image.jpg") 100%/cover no-repeat;
}
```

- füge ein `div` container ein, mit 100% Breite einer section und 250px Höhe
- gib dem div Container das Hintergrundbild `nature.jpg` und passe es an. Es soll über die ganze Seite gehen und nicht wiederholt werden!
- Nun erzeuge genug divs in dem container, dass jeder buchstabe deines Vornamens ein eigenes Div hat.
```
Beispiel: Max
<div>
    <div>M</div>
    <div>A</div>
    <div>X</div>
</div>
```
- nutze `inline-block` um die Buchstaben nebeneinander aufzulisten und mit `Padding` und `Margin` auszurichten
Tipp: Manchmal hilft ein zusätzlicher COntainer für mehr Stabilität.

#### Zusatzaufgabe (schwerer)

- Legen einen weiteren Div Container an der ebenfalls über die gesamte Breite geht und 250px hoch ist.
- Schreibe deinen Namen in einen p-tag und zentriere den Text
- nun setze das `laser.giv` als Hintergrund im p-tag und finde heraus wie man diesen Hintergrund dem Text zuordnet.
- Suchbegriff: Set Image as Background for Text
Tipp: 100%/cover

## STOP

Position haben wir diese Woche nicht gelernt, daher lasst die Aufgabe einfach aus ^^

## Section 3: Position (Für später!)

- Lege einen Div container an, der `width: 60rem` und `height: 30rem` groß ist.
- setze das `nature.jpg` als Background img ein `(no-repeat 100%/cover)`
- Lege 2 p-tags im div mit 200px breite und 50px höhe an
- schreibe `Nature` in den 1. p-tag und gebe als Hintergrundfarbe `#ededed`
- schriebe in das 2. p-tag `Die Zugspitze`
- positioniere den 2. p-tag unten rechts in der Ecke.