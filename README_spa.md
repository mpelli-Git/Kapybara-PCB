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
- Panel solar: usar uno de 6 V y al menos 1,5 W. Estoy usando un panel solar AE.

**Opcional**
- Alimentación: Fusible SMD para protección de la fuente de alimentación, con portafusibles SMD.
- Porcentaje de potencia: R1+R2 para medición del voltaje de la batería por el ADC MCU.
- Telemetría de potencia: INA3221 de 3 canales.
- Supervisión del voltaje de la batería: TLV840 para reiniciar el MCU en caso de subtensión y mitigar caídas de tensión.
- Telemetría ambiental, dos opciones: a) BME280 3.3 V b) AHT20-BMP280.
- Módulo GPS: ATGM336H para sincronización horaria de nodos, con control MOSFET.
- Pantalla OLED: conector hembra para, por ejemplo, SSD1306.

[⬅️ Volver al menú principal](README.md)
