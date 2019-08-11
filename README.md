– Descrição:

O Sensor (Detector) de Vibração SW-420 é um módulo eletrônico desenvolvido com a finalidade de detectar vibrações em um ambiente ou superfície. Caso a intensidade da vibração seja abaixo do valor definido no trimpot (ajuste de sensibilidade) que há no sensor, a saída (digital) do sensor se mantém em nível baixo e quando o sensor detectar alguma vibração acima do valor definido, a saída (digital) altera para nível alto.

– Especificações e características:

– Controlador: LM393
– Tensão de operação: 3,3 – 5VDC
– Saída Digital
– LED indicador para presença de tensão
– LED indicador para saída digital
– Sensibilidade ajustável através de trimpot

– Aplicações:

Projetos com Arduino ou outras plataformas microcontroladas em que seja necessário detectar vibrações de superfícies.

– Proposta da prática:

Utilizar o Sensor (Detector) de Vibração SW-420 em conjunto com o Arduino e mostrar através de um LED as detecções de vibração feitas pelo sensor.

– Lista dos itens necessários:

01 – Arduino com Cabo USB
01 – Sensor (Detector) de Vibração – SW-420
01 – LED Difuso 5MM Azul
01 – Resistor de 150Ω
01 – Protoboard
02 – Cabos Jumper macho-macho
03 – Cabos Jumper macho-fêmea 

PROGRAMA:


const int pinoLed = 12; //PINO DIGITAL UTILIZADO PELO LED
const int pinoSensor = 5; //PINO DIGITAL UTILIZADO PELO SENSOR
 
void setup(){
  pinMode(pinoSensor, INPUT); //DEFINE O PINO COMO ENTRADA
  pinMode(pinoLed, OUTPUT); //DEFINE O PINO COMO SAÍDA
  digitalWrite(pinoLed, LOW); //LED INICIA DESLIGADO
  Serial.begin(9600);
}
 
void loop(){
  if(digitalRead(pinoSensor) == HIGH){ //SE A LEITURA DO PINO FOR IGUAL A HIGH, FAZ
      digitalWrite(pinoLed, HIGH); //ACENDE O LED
  }else{ //SENÃO, FAZ
    digitalWrite(pinoLed, LOW); //APAGA O LED
  }
}
