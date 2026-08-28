# Controle-de-Microservo-com-Potenci-metro

# iot-ATIVIDADE de controle de microservo

Discente: Gabriel Maciel Ribeiro

Docente: Amanda Paul Dull

[![Simular no Tinkercad][[[https://www.tinkercad.com/things/0dNkUfwLUEB/editel?returnTo=%2Fdashboard%2Fdesigns%2Fcircuits](https://www.tinkercad.com/things/hvHOoKUMN40-atividade-com-potenciometro)))

## Enunciado:Atividade Microservo

O projeto utilizara um potenciometro para fazer girar o micro servo, o potenciometro serve principalmente para sistemas que precisam medir temperaturas entre outras muitas coisas.

## Materiais necessários

| Qtd | Componente |
|-----|------------|
| 1 | Placa Arduino UNO |
| 1 | Cabo USB |
| 1 | Protoboard |
| 1 | Potenciômetro |
| 1 | Micro servo |
| 11 | Fios de jumper macho-macho |


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

