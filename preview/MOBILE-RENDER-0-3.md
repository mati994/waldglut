# Waldglut · Mobile-Renderingtest 0.3
Stand: 22. November 2026. **Technischer Prototyp; keine Änderung an index.html oder Spielständen.**

## Testziel
Ein Originalbild (Master-Lichtung 0.2, 1774×887 Pixel) wird mit einem einzigen Weltkoordinatensystem und drei Kameraweiten auf Smartphones und Desktop getestet.

- Kamera A: 1,60×; Goldfunke/Lichtknospe
- Kamera B: 1,14×; Goldtrieb/Lichtstrauch
- Kamera C: 0,82×; Junge Glutweide/Wächterbaum
- Stabile Weltanker: linker Baum (371,412), Pflanzpunkt (875,603), Stein rechts (1198,560)
- Kamera-Fokus am Pflanzpunkt: 50% der Viewport-Breite, 70% der Viewport-Höhe.
- Modi: Nearest Neighbor (imageSmoothingEnabled=false) vs glatte Interpolation (imageSmoothingEnabled=true).
- Responsiver Canvas-Framebuffer mit devicePixelRatio bis 2; nur bei Zoom, Modus oder Größenänderung neu zeichnen; Stopp im Hintergrund.
- Umschaltbarer Landmarken-Layer, Weltkarte mit drei echten Kamerarahmen und Kamerafahrt.
- Touch-Targets ab 44px, mobile Hochformat als Hauptansicht, Desktop-Zweispaltenansicht.

## Wichtige Erkenntnis
Der Browser kann Zwischenpixel weglassen, aber **keine zusätzlichen Pixeldetails erfinden**. Die vorhandene Bildquelle ist ein atmosphärischer Konzeptstand – noch kein einheitlich gerastertes Pixel-Art-Sprite-Set. Smartphone-DPR und CSS-Größe können unterschiedliche Kanten ergeben. „Nearest“ bedeutet scharfe Samplekanten, **nicht** garantiert schöneres Design.

## Noch offen
1. Endgültigen Bild-/Pixelmaßstab festlegen: konsistente Quellpixelcluster, idealerweise ganzzahlige Bild-zu-Gerät-Skalierung je Stufe.
2. Pflanzenfreien Hintergrund produzieren, da der alte Goldfunke in älteren Szenen eingebettet ist.
3. Goldfunke und Stufen II–VI als transparente, anatomisch konsistente Sprites mit gemeinsamem Bodenanker exportieren.
4. Smartphone-Browser-Test: A/B/C in zwei Modi visuell kontrollieren, Ladezeit, DPR und Darstellung überprüfen; Desktop mit prüfen.
5. Erst nach visueller Freigabe die Darstellung in die separate Gameplay-Integration übernehmen.

**Keine Behauptung:** Dieser Labortest allein ist keine fertige PWA und kein Beweis einer vollständig scharfen Asset-Pipeline. Test trennt die Browser-Abtastung von der späteren Asset-Produktion.
