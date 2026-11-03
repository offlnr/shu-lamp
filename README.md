# shu-lamp

Plano técnico y prototipo 3D de la Ampolleta-Cerebro SHU (proyecto CORE-AI) y su lámpara de escritorio articulada.

La ampolleta no lleva rosca: se acopla magnéticamente al soquete SHU (pieza 001, ver `../core-ai/hardware/shu_soquete_planimetria.html`). El acople macho va integrado al cuerpo-disipador con 6 contactos en PCD Ø20, 6 imanes N52 con polaridad alternada y un nervio KEY; el soquete hembra va en la punta del brazo con 6 pogo pins P75-E2, sus 6 imanes y una tapa con insertos M3.

Abre `index.html` en el navegador (necesita internet para cargar three.js y manifold-3d). La hoja de medidas de la izquierda alimenta dos pestañas:

- **Plano 2D**: lámina con vista frontal explosionada, corte A–A y vista inferior. Verifica si la fuente, el micrófono y la placa ESP32 caben dentro del cuerpo.
- **Prototipo 3D**: la lámpara completa (ampolleta + soporte), ensamblada o separada, con corte y capas. Abajo está la lista de piezas con su tamaño en la cama, volumen, material sugerido y un STL por pieza, listo para el slicer (mm, Z hacia arriba, orientado para imprimir).

Las medidas del grupo **Soporte de mesa** son de diseño: el codo de los brazos se calcula solo para dejar la ampolleta a la altura pedida.
