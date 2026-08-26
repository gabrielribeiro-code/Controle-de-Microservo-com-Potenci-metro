# Controle-de-Microservo-com-Potenci-metro

# iot-ATIVIDADE de controle de microservo

Discente: Gabriel Maciel Ribeiro

Docente: Amanda Paul Dull

[![Simular no Tinkercad][[[https://www.tinkercad.com/things/0dNkUfwLUEB/editel?returnTo=%2Fdashboard%2Fdesigns%2Fcircuits](https://www.tinkercad.com/things/hvHOoKUMN40-atividade-com-potenciometro)))

## Enunciado:Atividade Microservo

O projeto utilizara um microservo

- O Arduino lê o estado do botão pelo **pino 7**
- Controla o LED pelo **pino 10**

## Materiais necessários

| Qtd | Componente |
|-----|------------|
| 1 | Placa Arduino UNO |
| 1 | Cabo USB |
| 1 | Protoboard |
| 1 | Resistor de 200 Ω ou 220 Ω |
| 1 | Resistor de 10 kΩ |
| 1 | Botão tipo push button |
| 1 | LED vermelho difuso de 5 mm |
| — | Fios de jumper macho-macho |


IMAGEM: <img width="1044" height="749" alt="image" src="https://github.com/user-attachments/assets/3bb8a37f-ae27-4928-bf90-b6a01815e75b" />

Código: // C++ code
//

#include <Servo.h>

Servo servoMotor;

int potenciometro = A0;

int valorLido;
int angulo;

void setup()
{
 
  servoMotor . attach(9);
  
}

void loop()
{
  valorLido = analogRead(potenciometro);
  angulo = map(valorLido, 0, 1023, 0, 180);
  servoMotor . write (angulo);
  
  delay(15);
}

