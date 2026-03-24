# Projecte Eines Sostre Solar 

>**Autors: Nabel Khrourouch i Marc Baillo** 
>**Versió: 0.2 **

----------

## Objectiu

Dissenyar i implementar en una PCB, un sistema electronic del vehicle com es un sostre solar. S’implementara una etapa de regulacio, microcontrolador, bus CAN, I2C / SPI, USART i botons. 
I que incloguiu les següents caracteristiques:
- Motor del vidre amb el seu final de carrera. 
- Motor de la cortineta.
- Llums ambientals (LED RGB amb bus digital)
- Mecanisme antiatrapament (sensor digital de corrent).



## Diagrama de blocs


### Descripció/funcionalitat de cada bloc

  * Power: En aquest bloc posem la partt relacionada con 2 etapes, la de la alimentació i la de potencia. (LDO y Buck converter i el H-Bridge)
  * Microcontrolador: en aquest bloc posem les parts que tenen molt que veure amb el microcontrolador com cristal oscilador, ICSP, botonera, filtre pi, reset manual, LEDs de prova.
  * Analógica: part del sistema que és analogic i per tant la agrupem, aquí veiem el sensor de anti-atrapament.
  * Digital: part on están els components més purament digitals, como el USART, el transceiver CAN, el Sensor de Final de Carrera o LED RGB. 

-----------

## Requisits / Especificacions

  * Alimentació; 12V, regulada a 3V3
  * Microcontrolador PIC24hj128gp502
  * Motor del vidre amb el seu final de carrera. 
*  Motor de la cortineta.
*  Llums ambientals (LED RGB amb bus digital)
*  Mecanisme antiatrapament (sensor digital de corrent).

-----------

## Components

| Descripcio | Ref | Package |Datasheet | Prove&#239;dor | Preu (per u) | Unitats |
| --- | --- | --- | --- | ---| --- | --- |
| Microcontrolador | PIC24HJ128GP502 | TQFP-44 |[Datasheet](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/70293G.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Microchip-Technology/PIC24HJ128GP504-E-PT?qs=Fllw7YelV3%252B64KTDe2rRTg%3D%3D)| 6,85&euros;| 1x |
| Regulador de Tensión | LM1117 | SOT-4/TO-252-3 |[Datasheet](https://www.ti.com/lit/ds/symlink/lm1117.pdf?ts=1774252763694&ref_url=https%253A%252F%252Feu.mouser.com%252F) | [Mouser](https://www.mouser.es/ProductDetail/Texas-Instruments/LM1117IMPX-3.3-NOPB?qs=X1J7HmVL2ZG7K12CpArCeA%3D%3D)  | 0,89&euros; | 1x | Buck Convertor (DC/DC) | LM2596 | TO-220-5 |[Datasheet](https://www.onsemi.com/pdf/datasheet/lm2596-d.pdf) | [Mouser](https://www.mouser.es/ProductDetail/onsemi/LM2596DSADJG?qs=atIEnC%2F2K4W1Dy%252BFjrRjIQ%3D%3DD)  | 2&euros; | 1x | H-Bridge (Doble) | L298N | TO-220-15/Multiwatt-15 |[Datasheet](https://www.st.com/resource/en/datasheet/l298.pdf) | [Mouser](https://www.mouser.es/ProductDetail/STMicroelectronics/L298N?qs=gr8Zi5OG3Mj6jDtNclcF9Q%3D%3D&srsltid=AfmBOoqfHqg2YnbNWZkkZ0kC8gS-It04lRCKKxTP2hRawLswU3FHokk-)  | 9,94&euros; | 1x | Transceiver CAN | MCP2551 | SOIC-8 |[Datasheet](https://www.mouser.es/datasheet/3/282/1/20001667G.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Microchip-Technology/MCP2551-E-SN?qs=Vn0zuzr35GHkGDCgnw0F9A%3D%3D&srsltid=AfmBOoqRSA4jehlhROuy00L77BJlCctohyKGG46Xa-qAsKKURsjZt60j)  | indefinido | 1x | Driver Traductor USART | MAX3232 | SSOP-16 |[Datasheet](https://www.mouser.es/datasheet/3/1014/1/MAX3222-MAX3241.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Analog-Devices-Maxim-Integrated/MAX3232CUE%2bT?qs=CDqwynd4ZNq6sBxRCl3%2FVw%3D%3D)  | 6,99&euros; | 1x | Conector | DE9 | DSUB-9_Socket |[Datasheet](https://www.te.com/commerce/DocumentDelivery/DDEController?Action=srchrtrv&DocNm=747521&DocType=Customer+Drawing&DocLang=English&PartCntxt=747521-2) | [Mouser](https://www.mouser.es/ProductDetail/TE-Connectivity/5-747905-7?qs=D9DkYEUiaeef0R92SSUIJQ%3D%3D)  | 6,39&euros; | 2x | LED RGB | WS2812 | LED_SMD |[Datasheet](https://www.mouser.es/datasheet/3/389/1/SMD_LX5050RGB_TR.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Lumex/SMD-LX5050RGB-TR?qs=GedFDFLaBXGgyFR6XtWXMw%3D%3D)  | 0,75&euros; | 1x | Sensor Anti-Atrapamiento | INA219 | No Especificat  |[Datasheet](https://www.ti.com/lit/ds/symlink/ina219.pdf?ts=1774240946529) | [Mouser](https://www.mouser.es/ProductDetail/Lumex/SMD-LX5050RGB-TR?qs=GedFDFLaBXGgyFR6XtWXMw%3D%3D)  | 4,23&euros; | 2x | Cristal Oscilador | ECS-80-20-20BM-EN-TR | 7mm x 5mm |[Datasheet](https://www.mouser.es/datasheet/3/294/1/csm_8mr.pdf) | [Mouser](https://www.mouser.es/ProductDetail/ECS/ECS-80-20-20BM-EN-TR?qs=3Rah4i%252BhyCEvSjMjFbrNOA%3D%3D&utm_id=9882080341&utm_source=google&utm_medium=cpc&utm_marketing_tactic=emeacorp&gad_source=1&gad_campaignid=9882080341&gbraid=0AAAAADn_wf2VPwruzVVuU5TdtfDNM-71c&gclid=CjwKCAjwpcTNBhA5EiwAdO1S9kbEmbKF8UUMwaVP0zWJXkCwjEh6ns86OOaH_PQxj7KPIVRFoQ-tjhoCMYIQAvD_BwE)  | 0,86&euros; | 1x | Ferrita | BLM21 | 0805 (2012 metric) |[Datasheet](https://www.mouser.es/datasheet/3/76/1/ENFA0005.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Murata-Electronics/BLM21PG600SN1D?qs=LbqjZSvnDswFXSg06XQ50A%3D%3D&utm_id=9882080341&utm_source=google&utm_medium=cpc&utm_marketing_tactic=emeacorp&gad_source=1&gad_campaignid=9882080341&gbraid=0AAAAADn_wf2r1gIBG4HB31JwCLchDktw_&gclid=Cj0KCQjw9-PNBhDfARIsABHN6-1kCnzr_LU1mZd8ISSiD6a4Y2yPfWM2slAP8zejLYN4QiWVlEgd_j4aAjKhEALw_wcB)  | 0,1&euros; | 1x | Switch (Pulsador) Reset | B3F-1002 | No Especificat |[Datasheet](https://www.mouser.es/datasheet/3/39/1/en_b3f.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Omron-Electronics/B3F-1002?qs=lK7M36XCk6Jk6Tf1a0ilbA%3D%3D&mgh=1&vip=1&utm_source=chatgpt.com)  | 0,22&euros; | 1x | Switch (Interruptor) Botonera | EG1218 | No Especificat | [Datasheet](https://www.mouser.es/datasheet/3/315/1/EG1218.pdf) | [Mouser](https://www.mouser.es/ProductDetail/E-Switch/EG1218?qs=xDsBkp9LkocT0c8K%252B5e%2FgA%3D%3D&utm_id=9882080341&utm_source=google&utm_medium=cpc&utm_marketing_tactic=emeacorp&gad_source=1&gad_campaignid=9882080341&gbraid=0AAAAADn_wf35b0MW3nfCvSzMlg6XwcaGU&gclid=CjwKCAjwyYPOBhBxEiwAgpT8PyGPpIFjxhu8gTRlFg-LHJTLCOTyddAMEeDN2J_3LI3rmf0TA_G4BxoCa_gQAvD_BwE)  | 0,62&euros; | 4x | LED blau | LTST-C170TBKT | No Especificat | [Datasheet](https://www.mouser.com/catalog/specsheets/Lite-On-LTST-C170TBKT.pdf?_gl=1*1cduzrk*_gcl_aw*R0NMLjE3NzQzMDEyMTcuQ2p3S0NBandwY1ROQmhBNUVpd0FkTzFTOWwya2ZrbGFJMGhwWGtyRG1vR1VYZDJTRmxSeEVCZkF2UWt2eHRWaElIdHFxRUJiTFZpd1pCb0NkcUlRQXZEX0J3RQ..*_gcl_au*MjA1MzUzMjE4NS4xNzcyNDYzNTA5LjEwMjQ4MDUwNjIuMTc3MzgyNTM1My4xNzczODI1MzUz*_ga*NDUzNDQyNzU5LjE3NzI0NjM1MTA.*_ga_15W4STQT4T*czE3NzQzMDU4MDYkbzIyJGcxJHQxNzc0MzA3MTk0JGo1OSRsMCRoMA..) | [Mouser](https://www.mouser.es/ProductDetail/LITEON/LTST-C170TBKT?qs=0uL0gcxEMop2ooGmIUzw3A%3D%3D&mgh=1&vip=1&utm_source=chatgpt.com)  | 0,19&euros; | 1x | LED vermell | Lite-On LTST-C170KRKT | No Especifita |[Datasheet](https://www.mouser.com/catalog/specsheets/Lite-On-LTST-C170KRKT.pdf?_gl=1*37wqgf*_gcl_aw*R0NMLjE3NzQzMDc1NjAuQ2p3S0NBand5WVBPQmhCeEVpd0FncFQ4UDZ4WUdGWUxBMWtKSFZ3aW82NXNGQkZZQnB1RzVxUFFENEJrbThwZ3hJN2JSbVh0RUdDeFdCb0M3cE1RQXZEX0J3RQ..*_gcl_au*MjA1MzUzMjE4NS4xNzcyNDYzNTA5LjEwMjQ4MDUwNjIuMTc3MzgyNTM1My4xNzczODI1MzUz*_ga*NDUzNDQyNzU5LjE3NzI0NjM1MTA.*_ga_15W4STQT4T*czE3NzQzMDU4MDYkbzIyJGcxJHQxNzc0MzA3NTYwJGo2MCRsMCRoMA..) | [Mouser](https://www.mouser.es/ProductDetail/LITEON/LTST-C170KRKT?qs=NUb82WqeCyrVOID%2Fxt4rgA%3D%3D&utm_id=9882080341&utm_source=google&utm_medium=cpc&utm_marketing_tactic=emeacorp&gad_source=1&gad_campaignid=9882080341&gbraid=0AAAAADn_wf35b0MW3nfCvSzMlg6XwcaGU&gclid=CjwKCAjwyYPOBhBxEiwAgpT8P6xYGFYLA1kJHVwio65sFBFYBpuG5qPQD4Bkm8pgxI7bRmXtEGCxWBoC7pMQAvD_BwE)  | 0,14&euros; | 1x | Sensor Final de Carrera | A1101 | SOT-23 |[Datasheet](https://www.mouser.es/datasheet/3/389/1/SMD_LX5050RGB_TR.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Lumex/SMD-LX5050RGB-TR?qs=GedFDFLaBXGgyFR6XtWXMw%3D%3D)  | 0,75&euros; | 1x |



-----------

## Historial de canvis

| Data | Autor     | Branch | Versi&#243; | Descripci&#243; |
| --- | --- | --- | --- | --- |
|  10/03/26 | Nabel i Marc | Master | versio 1 | Seleccionem els components i creem la primera versió del Diagrama de Bloc |
  14/03/26 | Nabel | Master | versio 2 | Actualització del Diagrama de Bloc |
16/03/26 | Marc | Master | versió 1 | Esquemàtic creació dels subapartats del projecte |
17/03/26 | Marc | Master | versió 2 | Esquemàtic: faig la part del uC i de Digital |
17/03/26 | Nabel | Master | versió 3 | Esquemàtic: faig la part de power i analogica |
22/03/26 | Marc | Master | versió 4 | Esquemàtic: correció de errades vistes a la sessió del Proyecte 2 i poso footprints |
24/03/26 | Nabel | Master | versió 1 | Layout: faig el rutejat de la majoria dels components |
24/03/26 | Marc | Master | versió 2 | Layout: corregeixo algunes coses |