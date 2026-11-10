# shu-lamp

Plano técnico y prototipo 3D de la Ampolleta-Cerebro SHU (proyecto CORE-AI) y su lámpara de escritorio articulada.

La ampolleta no lleva rosca: se acopla magnéticamente al **adaptador SHU** (pieza 001, ver `../core-ai/hardware/shu_soquete_planimetria.html`). El adaptador se atornilla como una ampolleta normal en el portalámparas E27 del brazo y en su otro extremo tiene la hembra del acople: plato porta-pogo con 6 pogo pins P75-E2 en PCD Ø20, 6 imanes N52 y ranura KEY. El macho va integrado al cuerpo-disipador de la ampolleta: 6 contactos de latón, 6 imanes con polaridad alternada y nervio KEY. La rosca E27 es solo mecánica: los 5 V y los datos llegan por un cable que pasa por el canal de Ø8 del adaptador.

Abre `index.html` en el navegador (necesita internet para cargar three.js y manifold-3d). La hoja de medidas de la izquierda alimenta dos pestañas:

- **Plano 2D**: lámina con vista frontal explosionada, corte A–A y vista inferior. Verifica si la fuente, el micrófono y la placa ESP32 caben dentro del cuerpo.
- **Prototipo 3D**: la lámpara completa (ampolleta + soporte), ensamblada o separada, con corte y capas. Abajo está la lista de piezas con su tamaño en la cama, volumen, material sugerido y un STL por pieza, listo para el slicer (mm, Z hacia arriba, orientado para imprimir).

Las medidas del grupo **Soporte de mesa** son de diseño: el codo de los brazos se calcula solo para dejar la ampolleta a la altura pedida.

## Simulación interactiva

`simulacion/index.html` monta el mismo modelo paramétrico (medidas de referencia + las medidas tomadas) en una habitación 3D con cuatro lugares de acople para la misma ampolleta: lámpara de escritorio, soquete de techo, velador y aplique de pared. Cada uno lleva su propio adaptador SHU.

- Arrastra la ampolleta o los brazos para mover la lámpara de escritorio (giro sobre el poste, hombro y codo con la misma IK del plano). El portalámparas, Shift + arrastrar o el deslizador inclinan el cabezal sobre la articulación J3.
- Interruptor de palanca con corte de 5 V, brillo, temperatura de color, modos de luz (reposo, escucha, piensa, flow) y luz de la habitación.
- Desacople y acople magnético animado, pinout en vivo (P1 GND · P2 5 V · P3 TX · P4 RX · P5 SDA · P6 SCL), vista explosionada y corte.

Para usar la copia local de manifold-3d (`manifold.js` y `manifold.wasm`) sírvela con un servidor, por ejemplo `python3 -m http.server` dentro de `simulacion/`. Si abres el archivo directo, carga manifold-3d desde el CDN.

En la simulación los brazos son más largos que en el plano (A1 300, A2 260, Ø16, poste 40 mm).
