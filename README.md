# Projecte Eines Sostre Solar 

>**Autors: Nabel Khrourouch i Marc Baillo** 
>**Versió: 0.2 **

----------

## Objectiu

Dissenyar i implementar en una PCB, un sistema electronic del vehicle com es un sostre solar. S’implementara una etapa de regulacio, microcontrolador,  bus CAN, I2C / SPI, USART i botons. 
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
  * Motor de la cortineta.
  * Llums ambientals (LED RGB amb bus digital)
  * Mecanisme antiatrapament (sensor digital de corrent).

-----------

## Components

| Descripció                        | Ref                        | Package                  | Datasheet | Proveïdor | Preu (per u) | Unitats |
|----------------------------------|----------------------------|--------------------------|-----------|-----------|--------------|---------|
| Microcontrolador                | PIC24HJ128GP502           | TQFP-44                  | [Datasheet](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/70293G.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Microchip-Technology/PIC24HJ128GP504-E-PT) | 6,85€ | 1x |
| Regulador de Tensió             | LM1117                    | SOT-223 / TO-252-3       | [Datasheet](https://www.ti.com/lit/ds/symlink/lm1117.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Texas-Instruments/LM1117IMPX-3.3-NOPB) | 0,89€ | 1x |
| Buck Converter (DC/DC)          | LM2596                    | TO-220-5                 | [Datasheet](https://www.onsemi.com/pdf/datasheet/lm2596-d.pdf) | [Mouser](https://www.mouser.es/ProductDetail/onsemi/LM2596DSADJG) | 2€ | 1x |
| H-Bridge (Doble)                | L298N                     | Multiwatt-15             | [Datasheet](https://www.st.com/resource/en/datasheet/l298.pdf) | [Mouser](https://www.mouser.es/ProductDetail/STMicroelectronics/L298N) | 9,94€ | 1x |
| Transceiver CAN                 | MCP2551                   | SOIC-8                   | [Datasheet](https://www.mouser.es/datasheet/3/282/1/20001667G.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Microchip-Technology/MCP2551-E-SN) | — | 1x |
| Driver USART                    | MAX3232                   | SSOP-16                  | [Datasheet](https://www.mouser.es/datasheet/3/1014/1/MAX3222-MAX3241.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Analog-Devices-Maxim-Integrated/MAX3232CUE%2bT) | 6,99€ | 1x |
| Conector                        | DE9                       | DSUB-9_Socket            | [Datasheet](https://www.te.com/commerce/DocumentDelivery/DDEController?Action=srchrtrv&DocNm=2301843&DocType=Customer+Drawing&DocLang=English&PartCntxt=2301843-1&DocFormat=pdf) | [Mouser](https://www.mouser.es/ProductDetail/TE-Connectivity-AMP/2301843-1?qs=rrS6PyfT74crws9wAQVNoA%3D%3D&mgh=1&vip=1&utm_id=19103542967&utm_source=google&utm_medium=cpc&utm_marketing_tactic=emeacorp&gad_source=1&gad_campaignid=19103548274&gbraid=0AAAAADn_wf2KTMAEN9aavrmuZXjiN2vqm&gclid=Cj0KCQjw7IjOBhDyARIsAFzrWQzWx8kAOC9-xeCib2TtXzouOFVkeyjK2X-mWbgX7vQpQhIDmcFKVOEaAr35EALw_wcB) | 1,9€ | 2x |
| Sensor (corrent) Anti-Atrapament              | INA219                    | SOT-23                       | [Datasheet](https://www.ti.com/lit/ds/symlink/ina219.pdf) | [Mouser](https://www.mouser.es/ProductDetail/) | 4,23€ | 2x |
| Sensor Final de Carrera         | A1101                     | SOT-23                   | [Datasheet](https://www.allegromicro.com/~/media/files/datasheets/a110x-datasheet.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Allegro-MicroSystems/A1101EUA-T?qs=pUKx8fyJudAoca%252BrN0Sfug%3D%3D&srsltid=AfmBOopmzx3dJfmaMgARzIOmuFdzof038kPjXIFZjNx3_Dk0axwEeuXz) | 1,18€ | 2x |
| Opamp Doble Comparador        | LM393                     | SOIC-8                  | [Datasheet](https://www.ti.com/lit/ds/symlink/lm2903b.pdf?ts=1774335179874&ref_url=https%253A%252F%252Fwww.mouser.pl%252F) | [Mouser](https://www.mouser.es/ProductDetail/Texas-Instruments/LM393AP?qs=LfG3tU9ud8C8WR6rae7e8w%3D%3D&utm_id=20109199436&utm_source=google&utm_medium=cpc&utm_marketing_tactic=emeacorp&gad_source=1&gad_campaignid=20109199436&gbraid=0AAAAADn_wf3bSykfoqBB3E0CfDtWEe629&gclid=Cj0KCQjw7IjOBhDyARIsAFzrWQwk6DXPkYJ3-Ag5UdBtY40izdCAfFJImBQIx_JyaWhi5W70RpnD0e8aAgx9EALw_wcB) | 0,31 | 2x |
| Cristal Oscilador               | ECS-80-20-20BM-EN-TR      | 7mm x 5mm                | [Datasheet](https://www.mouser.es/datasheet/3/294/1/csm_8mr.pdf) | [Mouser](https://www.mouser.es/ProductDetail/ECS/ECS-80-20-20BM-EN-TR) | 0,86€ | 1x |
| Ferrita                         | BLM21                     | 0805                     | [Datasheet](https://www.mouser.es/datasheet/3/76/1/ENFA0005.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Murata-Electronics/BLM21PG600SN1D) | 0,10€ | 1x |
| Switch (Pulsador) Reset y Botonera                 | B3F-1002                  | THT                      | [Datasheet](https://www.mouser.es/datasheet/3/39/1/en_b3f.pdf) | [Mouser](https://www.mouser.es/ProductDetail/Omron-Electronics/B3F-1002) | 0,22€ | 5x |
| LED blau                        | LTST-C170TBKT             | 0805                     | [Datasheet](https://www.mouser.com/catalog/specsheets/Lite-On-LTST-C170TBKT.pdf) | [Mouser](https://www.mouser.es/ProductDetail/LITEON/LTST-C170TBKT) | 0,19€ | 1x |
| LED vermell                     | LTST-C170KRKT             | 0805                     | [Datasheet](https://www.mouser.com/catalog/specsheets/Lite-On-LTST-C170KRKT.pdf) | [Mouser](https://www.mouser.es/ProductDetail/LITEON/LTST-C170KRKT) | 0,14€ | 1x |
| LED RGB                         | WS2812                    | 5050 SMD                 | [Datasheet](https://www.tme.eu/Document/01c0100fee68667af99767edc3a7fee2/WS2812B-MINI.pdf) | [TME](https://www.tme.eu/es/details/ws2812b-mini/leds-smd-de-colores/worldsemi/?utm_source=google&utm_medium=cpc&utm_campaign=HISZPANIA%20%5BDSA%5D&utm_content=&campaign_id=18880888776&gad_source=1&gad_campaignid=18880888776&gbraid=0AAAAADyylhLJURluAY7jUeNc8-F-2bfAx&gclid=Cj0KCQjw7IjOBhDyARIsAFzrWQzO_PW3O0VVMhyARWr_1LRVY-vRQsT44Hck0vcMLTjOFT9BO_EXdCEaAkMFEALw_wcB) | 0,42€ | 1x |


-----------

## Historial de canvis

| Data     | Autor         | Branch | Versió   | Descripció                                                                 |
|----------|--------------|--------|----------|----------------------------------------------------------------------------|
| 10/03/26 | Nabel i Marc | Master | versió 1 | Seleccionem els components i creem la primera versió del Diagrama de Bloc |
| 14/03/26 | Nabel        | Master | versió 2 | Actualització del Diagrama de Bloc                                        |
| 16/03/26 | Marc         | Master | versió 1 | Esquemàtic: creació dels subapartats del projecte                         |
| 17/03/26 | Marc         | Master | versió 2 | Esquemàtic: faig la part del uC i de Digital                              |
| 17/03/26 | Nabel        | Master | versió 3 | Esquemàtic: faig la part de power i analògica                             |
| 22/03/26 | Marc         | Master | versió 4 | Esquemàtic: correcció d’errades i assignació de footprints                |
| 24/03/26 | Nabel        | Master | versió 1 | Layout: faig el rutejat de la majoria dels components                     |
| 24/03/26 | Marc         | Master | versió 2 | Layout: corregeixo algunes coses    