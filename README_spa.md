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


### 🖼️ Galería de imágenes

**📸 PCB**

| Front View | Back View |
| :---: | :---: |
| <img src="Images/PCB_Front_2026-01-11.jpg" width="400"> | <img src="Images/PCB_Back_2026-01-11.jpg" width="400"> |


## 📄  Esquema

[![Kapybara Schematic](Images/Preview_sch.jpg)](Docs/Schematic_Kapybara-PCB_v0_2026-01-12.pdf)

*Haz clic en la imagen para abrir el PDF*


**📸 Montaje**

| 3D| PCB | Caja |
| :---: | :---: | :---: |
| <img src="Images/PCB_3D_2026-01-11.jpg" width="300"> | <img src="Images/PCB_Kapybara_AMSN_GPS+OLED.jpeg" width="280"> | <img src="Images/PCB_Kapybara_AMSN_box.jpeg" width="300"> |
| *Vista 3D del diseño* | *Módulo GPS + OLED* | *Prueba espacio caja* |


## Intrucciones para solicitar PCB

Puedes pedir las PCBs directamente en [JLCPCB](https://jlcpcb.com/) o a cualquier otro fabricante, utilizando el archivo gerber de este repositorio:
[v0 Gerber PCB for testing](Gerbers/Gerber_Kapybara_PCB_AMSN_v0_2026-01-11.zip)


## Lista de materiales (BOM)

No hay ninguna filiación con los enlaces indicados. Solo se proporciona,a modo de ejemplo, para facilitar la selección de componentes.

*Total aprox. a feb. 2026= 23 €*

| Parte | Cant. | Coste | Enlace |   Notas   |
|-------|-------|-------|--------|-----------|
|ProMicro nRF52840|1|2,7 €|[Op1](https://es.aliexpress.com/item/1005006271881076.html)|[Op2](https://es.aliexpress.com/item/1005007738886550.html)|
|HT-RA62|1|5,5 €|[Op1](https://es.aliexpress.com/item/1005008363549136.html)|[Op2](https://es.aliexpress.com/item/1005008626582098.html)|
|CN-3791|1|2,3 €|[Op1](https://es.aliexpress.com/item/1005007355378997.html)|6V o 12 V según panel solar|
|INA3221|1|1,3 €|[Op1](https://es.aliexpress.com/item/1005007723353245.html)|Fijarse orden CH1, CH2,CH3 de izda. a dcha.|
|BME280-3,3|1|2,5 €|[Op1](https://es.aliexpress.com/item/1005004527984343.html)|Nota: BME= P&T&H; BMP= P&T|
|AHT20 + BMP280|1|1,2 €|[Op1](https://es.aliexpress.com/item/1005007702473893.html)|Alternativa a BME|
|BMS|1|0,17 €|[Op1](https://es.aliexpress.com/item/1005005968623999.html)|Pack de 10 uds.|
|GPS ATGM336H|1|5,9 €|[Op1](https://es.aliexpress.com/item/4001147538089.html)||
|MosFet AO3400|1|0,02 €|[Op1](https://es.aliexpress.com/item/1005006142488372.html)|O equival. canal-N; 100 uds|
|TLV840|1|0,78 €|[Op1](https://es.aliexpress.com/item/1005010444348808.html)|TLV840MADL30DBVRQ1; 10 uds|
|Soport.Bat.|1|0,95 €|[Op1 SMD](https://es.aliexpress.com/item/1005005301516019.html)|[Op2 THT](https://es.aliexpress.com/item/1005007051308086.html)|
|Puls.SMD|2|0,04 €|[Op1](https://es.aliexpress.com/item/4001125532910.html)|100 uds|
|Bornero|1|0,29 €|[Op1](https://es.aliexpress.com/item/1005003556955422.html)|2 pin 5 uds|
|Fusible|1|0,12 €|[Op1](https://es.aliexpress.com/item/1005002366334753.html)|1A 10 uds|
|Portafusible|1|0,14 €| "  " |1808 Socket 10 uds|
|Resist.|3|0,03 €|[Op1](https://es.aliexpress.com/item/1005006044241818.html)|1206 pack uds|
|Cond.|2|0,03 €|[Op1](https://es.aliexpress.com/item/1005002528281793.html)|1206 100 nF 100 uds|
|Diodo|1|0,02 €|[Op1](https://es.aliexpress.com/item/1005009947560623.html)|SS34 SMA 50 uds|
|Tira pines hembra|x|0,15 €|[Op1](https://es.aliexpress.com/item/1005003406780797.html)|1X13Pin 10 uds|

## 🛠 Instrucciones de Montaje

Sigue estos pasos para ensamblar tu Kapybara-PCB:

⚠️ Nunca enciendas el nodo sin antena conectada. Puedes quemar el módulo LoRa.
- Comprueba que el microcontrolador es funcional:
- Actualiza su bootloader a la versión 0.8 o superior si fuera necesario. [Bootloader 0.9.2](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases/download/0.9.2/update-nice_nano_bootloader-0.9.2_nosd.uf2)
- Instala el firmware de [Meshtastic](https://flasher.meshtastic.org)

Se supone que tienes cierta experiencia soldando componentes electrónicos.
1. Suelda primero los pequeños componentes SMD, como resistencias, condensadores, pulsadores, Mosfet y TLV.
2. Después suelda el microcontrolador y el módulo LoRa. Asegúrate de que la orientación sea correcta según la serigrafía.
3. Conecta la antena (una pequeña será suficiente temporalmente) y alimenta la MCU por el puerto USB.
4. Comprueba que el nodo arranca bien, que puedes conectarte desde el móvil por BLE y que puede recibir/enviar mensajes.
5. Si todo lo anterior es correcto, sigue con el montaje.
6. Suelda el portafusibles y fusible o puentea los pads del fusible si no lo vas a montar.
7. Suelda el BMS, soporte de la batería e interruptores.
8. Suelda el INA3221 o, si no lo vas a montar, haz un puente entre los pads (+) y (-) de cada canal para continuar la serie y dar continuidad.
9. Asegurate que no está el nodo alimentado por USB. Inserta la batería 18650 y conecta el interruptor de alimentación en "ON".
10. Comprueba nuevamente el punto 4. Mide tensiones Vcc que debe dar unos 3,3 V. Apaga el nodo y quita la batería.
11. Sigue con el montaje. Suelda el MPPT CN3791. Si no has montado el diodo D1 hazle un puente.
12. Conecta el panel solar a su bornero, comprueba su funcionamiento y que carga la batería. Apaga el nodo y quita la batería.
13. Suelda el módulo de lecturas medioambientales y comprueba su funcionamiento. Apaga el nodo y quita la batería.
14. Suelda el resto de componentes opcionales y comprueba su funcionamiento. Para el GPS y Display puedes utilizar conectores hembra o cortar una tira de pines según necesites.
15. Mide la tensión de batería y ajusta el valor en la APP de "ADC Multiplier override", inicialmente a 1.551, para que indique el mismo valor en la APP. 


## 🚦 Estado del Proyecto

| Función / Módulo | Estado| Notas |
| :--- | :---: | :--- |
| **Aliment. batería (3.7V)** | 🟢 OK | BMS Ok. |
| **Aliment. (3.3V)** | 🟢 OK | Probado indirectamnet por sensores Ok. |
| **nRF52840** | 🟢 OK | Bootloader flaseado y firmware cargado, BLE Ok. |
| **LoRa (HT-RA62)** | 🟢 OK  | Pruebas emisión/recepción Ok. |
| **CN3791** | 🟢 OK  | Carga batería mediante panel solar Ok. |
| **BME280** | 🟢 OK  | Lecturas medioambientales Ok en APP. |
| **INA3221** | 🟢 OK  | Lecturas eléctricas Ok en APP. |
| **AHT20-BMP280** | ⚪ PEND. | Falta por probar. No se esperan sorpresas. |
| **ATGM336H** | 🟢 OK  | Lectura GPS Ok con ctrl. Mosfet AO3400 |
| **TLV840** | 🔴 NOK | Se necesita replantear el diseño del supervisor. |

**Leyenda:**
🟢 `Probado & Funcionando` | 🔴 `Fallo / Rediseñar` | 🟡 `En progreso` | ⚪ `Pendiente de probarse`

## 📋 Pendiente Github
- [ ] *Actualizar ENG*
- [x] *BOM lista material*
- [x] *Subir los archivos Gerber actualizados si pruebas OK!*
- [ ] *Enlazar a sección de configuración de Meshtastic*

## Aviso legal
- Los componentes de software de [Meshtastic](https://meshtastic.org/) se publican bajo diversas licencias. Consulte [GitHub](https://github.com/meshtastic) para obtener más información.
- No se ofrece garantía; use este diseño bajo su propia responsabilidad.
- Meshtastic® es una marca registrada de Meshtastic LLC.
- Este sitio no está afiliado ni respaldado por el proyecto Meshtastic.

[⬅️ Volver al menú principal](README.md)
