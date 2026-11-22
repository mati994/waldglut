# Waldglut – Master-Lichtung: Geometrie 0.2 (Arbeitsfassung)
Stand 2026-11-22. Nicht als finale Szene oder Sprite-Paket freigegeben.

## Präzise fixierte Weltkoordinaten
- Masterwelt: 2600 × 3400 Weltpixel (vorläufiger Arbeitsbereich).
- Originalart: 941 × 1672 px, Position (820,1120); weder gestreckt noch verschoben.
- Pflanzpunkt original (465,1194) -> master (1285,2314).
- Linker Baum original (143,690) -> master (963,1810).
- Rechter Stein original (581,1219) -> master (1401,2339).
- Kamera-Viewport 941×1672; Wurzelpunkt konstant bei x=50%, y=70%.
- Kamera A z=1.65 (I–II), B z=1.30 (III–IV), C z=0.55 (V–VI).
- Formel: screenX=941*0.5+z*(worldX-1285), screenY=1672*0.70+z*(worldY-2314).

## Provisorischer Platzbedarf, keine realen Sprites
|Stufe|Name|Zoom|Höhe|Breite|
|---|---|---:|---:|---:|
|I|Goldfunke|1.65|92|75|
|II|Lichtknospe|1.65|175|112|
|III|Goldtrieb|1.30|390|215|
|IV|Lichtstrauch|1.30|760|480|
|V|Junge Glutweide|0.55|1350|1100|
|VI|Wächterbaum|0.55|1870|1530|
Diese Größen sind Arbeitsannahmen, die wir beim tatsächlichen Sprite-Export abgleichen müssen.

## Stand des Prototyps
- ✓ Originale Waldgrafik wird als unveränderter Kern benutzt, in der Darstellung an den Rändern ausgeblendet.
- ✓ Kamera-Skalierung, Weltanker, Übersichtskarte und sechs Platzbedarfstests arbeiten in einem Koordinatensystem.
- ~ Die außerhalb des Originals gezeichneten Bereiche sind procedural illustrativer Platzhalter, noch keine durchgängig gestaltete Pixel-Art.
- × Originaler Goldfunke im Hintergrund noch nicht freigestellt/entfernt.
- × Endgültige Master-Art in einheitlichem Pixel-Cluster-Raster und sechs transparenten Pflanzensprites noch nicht produziert.
- × Stufe-VI-Krone und vorhandene Landmarken brauchen ästhetische Kollisionsprüfung mit freigegebenen finalen Sprites.

## Sicherheitsregel
Diese Studie verändert keine Spieldatei, keinen Spielstand und keine Live-Spielmechanik. Erst die Asset-Freigabe erlaubt eine Integration.
