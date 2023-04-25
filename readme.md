# Übungsaufgabe (Freiwillig)

Dies ist eine kleine Übung zum Thema Box-Model mit folgenden Unterkategorien:
- margin und padding
- images und background images
- positioning und border
- CSS-Tricks

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

- Erstelle im body einen nav container mit einer 