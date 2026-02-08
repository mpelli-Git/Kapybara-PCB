# Kapybara-PCB para Meshtastic
Placa de circuito impreso modular diseñada para proyectos Meshtastic, de 120 x 70 mm, para montaje como nodo solar independiente en una carcasa exterior (caja de AliExpress). Muchos módulos son opcionales, a elección del usuario.

## Licencia

Este proyecto está licenciado bajo la **Licencia de Hardware Abierto CERN Versión 2 - Fuertemente Permisiva (CERN-OHL-S)**.

### ¿Qué quiere decir esto?
- **Compartir:** Puedes descargar, modificar y fabricar esta PCB.
- **Atribución:** Debes dar el crédito correspondiente al autor original (mpelli-Git).
- **Reciprocidad:** Si realizas modificaciones o mejoras al diseño y las distribuyes, **debes** licenciar tus contribuciones bajo la misma licencia CERN-OHL-S. Esto garantiza que toda la comunidad se beneficie de las mejoras.

Puede encontrar el texto completo de la licencia en el archivo [LICENSE](LICENSE) o visitar [https://ohwr.org/cern_ohl_s_v2.txt](https://ohwr.org/cern_ohl_s_v2.txt) para más detalles.

## Descripción

Placa de circuito impreso modular diseñada para proyectos Meshtastic, de 120 x 70 mm, para montaje como nodo solar independiente en una carcasa exterior (artículo de caja de AliExpress 1005007587120013). Muchos módulos son opcionales, a elección del usuario.

**Sistema básico**
- MCU: ProMicro Nice!nano compatible con nRF52840
- Módulo LoRa: HT-RA62 Lora SX1262
- Control de carga de batería: CN3791 6 V MPPT solar
- Batería: 18650 con soporte para PCB, opciones SMD o THT.
- BMS, dos opciones: a) PCB frontal, si el soporte de la batería lo permite, b) PCB posterior.
- Caja de AliExpress: artículo 1005007587120013 [Modelo de caja AE gris 150x100x70](https://aliexpress.com/item/1005007587120013.html)
- Panel solar: usar uno de 6 V y al menos 1,5 W. Estoy usando un [panel solar de 17.4 x 12 cm](https://es.aliexpress.com/item/1005009983374214.html) de AliExpress.

**Opcional**
- Alimentación: Fusible SMD para protección de la fuente de alimentación, con portafusibles SMD.
- Porcentaje de batería: R1+R2 para medición del voltaje de la batería por el ADC MCU.
- Filtraje: Los condensadores C1 y C2 no son necesarios, pero se reserva este espacio en la PCB por si conviniera filtrar tensión de alimentación.
- Telemetría de potencia: INA3221 medidor de corriente y voltaje de 3 canales.
- Supervisión del voltaje de la batería: TLV840 para reiniciar el MCU en caso de subtensión y mitigar efectos de caídas de tensión (brownout).
- Telemetría ambiental, sensores de temperatura, humedad y presión; dos opciones: a) BME280 3.3 V b) AHT20-BMP280.
- Módulo GPS: ATGM336H para ajuste y sincronización de la hora del nodo, con control MOSFET (canal-N).
- Pantalla OLED: conector hembra para, por ejemplo, SSD1306.

## Imágenes
<div align="center">
  <img src="images/PCB 3D 2026-01-11.jpg" width="45%" />
  <img src="PCB Kapybara AMSN - GPS.jpeg" width="45%" />
  <img src="PCB Kapybara AMSN - OLED displayl.jpeg" width="45%" />
</div>

## Intrucciones para solicitar PCB

Puedes pedir las PCBs directamente en jlcpcb.com utilizando el archivo gerber de este repositorio

## Lista de materiales (BOM)

No hay ninguna filiación con los enlaces indicados. Solo se proporciona,a modo de ejemplo, para facilitar la selección de componentes.

| Parte | Cant. | Coste | Origen |   Notas   |
|-------|-------|-------|--------|-----------|

## 🛠 Instrucciones de Montaje

Sigue estos pasos para ensamblar tu Kapybara-PCB:

⚠️ Nunca enciendas el nodo sin antena conectada. Puedes quemar el módulo LoRa.
- Comprueba que el microcontrolador es funcional:
- Actualiza su bootloader a la versión 0.8 o superior si fuera necesario. [Bootloader 0.9.2](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases/download/0.9.2/update-nice_nano_bootloader-0.9.2_nosd.uf2)
- Instala el firmware de [Meshtastic](https://flasher.meshtastic.org)

Se supone que tienes cierta experiencia soldando componentes electrónicos.
1. Suelda primero los pequeños componentes SMD, como resistencias, condensadores, pulsadores, Mosfet y TLV
2. Después suelda el microcontrolador y el módulo LoRa. Asegúrate de que la orientación sea correcta según la serigrafía.
3. Conecta la antena (una pequeña será suficiente temporalmente) y alimenta la MCU por el puerto USB.
4. Comprueba que el nodo arranca bien, que puedes conectarte desde el móvil por BLE, y que puede recibir/enviar mensajes.
5. Si todo lo anterior es correcto, sigue con el montaje.
6. Suelda el portafusibles y fusible o puentea los pads del fusible si no lo vas a montar.
7. Suelda el BMS, soporte de la batería e interruptores.
8. Suelda el INA3221 o haz un puente entre los pads (+) y (-) del canal 3 --> añadir llínea trazos a PCB o img ejemplo
9. Asegurate que no está el nodo alimentado por USB. Inserta la batería 18650 y conecta el interruptor de alimentación en "ON".
10. Comprueba nuevamente el punto 4. Apaga el nodo y quita la batería.
11. Sigue con el montaje. Suelda el MPPT CN3791. Si no has montado el diodo D1 haz un puente. Conecta el panel solar a su bornero y comprueba su funcionamiento. Apaga el nodo y quita la batería.
12. Suelda el módulo de lecturas medioambientales y comprueba su funcionamiento. Apaga el nodo y quita la batería.
13. Suelda el resto de componentes opcionales y comprueba su funcionamiento.

## Aviso legal
- Los componentes de software de [Meshtastic](https://meshtastic.org/) se publican bajo diversas licencias. Consulte [GitHub](https://github.com/meshtastic) para obtener más información.
- No se ofrece garantía; use este diseño bajo su propia responsabilidad.
- Meshtastic® es una marca registrada de Meshtastic LLC.
- Este sitio no está afiliado ni respaldado por el proyecto Meshtastic.

[⬅️ Volver al menú principal](README.md)
