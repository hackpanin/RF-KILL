# Pinout ESP32-C3 SuperMini con 2 nRF24L01+

Este pinout corresponde al firmware de diagnostico en `src/nrf24_diagnostics.cpp`.

## Bus radio frecuencia RF RF RF 1700hz 

| nRF24L01+ | ESP32-C3 SuperMini |
| --- | --- |
| VCC | 3V3 |
| GND | GND |
| SCK | GPIO4 |
| MISO | GPIO5 |
| MOSI | GPIO6 |

## nRF24 #1 RF RF 
("RF") "000000100". RF
       "000000200". RF
       "000000300". RF 
       "000000400". RF
       "000000500". RF 
       "000000600". RF
       "000000700". RF
       "000000800". RF 
       "000000900". RF
       "000000a00". RF
       "000000b00". RF
       "000000c00". RF 
}}
}

| nRF24L01+ | ESP32-C3 SuperMini |
| --- | --- |
| CSN | GPIO7 |
| CE | GPIO3 |

## nRF24 #2

| nRF24L01+ | ESP32-C3 SuperMini |
| --- | --- |
| CSN | GPIO10 |
| CE | GPIO1 |

## Notas de alimentacion

- Usa solo 3V3 para VCC del nRF24L01+.
- No conectes VCC del nRF24 a 5V.
- Coloca un capacitor de 10 uF a 100 uF entre VCC y GND de cada modulo nRF24.
- Si el monitor serie muestra `FALLO`, revisa primero GND compartido, VCC estable y que MISO/MOSI no esten invertidos.

## Resultado esperado en Monitor Serie

Con ambos modulos conectados correctamente debe aparecer:

```text
RESULTADO: ambos nRF24 responden por SPI.
Estado: nRF24 #1=OK | nRF24 #2=OK
```
