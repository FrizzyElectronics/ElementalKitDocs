# Elemental Kit - Botón

[![Texto alternativo](images/boton1.jpg 'Modulo de boton básico')](www.frizzy.es/grape)

El módulo de botón es un pequeño switch momentaneo de 12mm. Contiene el propio switch de dos posiciones "on/off" y su correspondiente resistencia pull-up. Cuando el botón es presionado, devuelve LOW y cuando lo sueltas devuelve HIGH. El conector de salida es el correspondiente JST-PH de 2.0mm compatible con los cables para la Grape.

## Características

* Botón fácil de usar
* Utiliza la clásica conexión "GND/VCC/SIG"
* Incluye la resistencia pull-up

##Primeros pasos

###Grape

[![Texto alternativo](images/montaje_boton.png 'Modulo de boton básico')](www.frizzy.es/grape)

| Grape | Elemental - Boton |
| ----- | ----------------- |
| GND   | Negro             |
| 5V    | Rojo              |
| D2    | Amarillo          |


```c++
const int pinBoton = 2;     // El numero del boton del pin
const int ledPin =  13;      // the number of the LED pin

const int pinBoton = 2;     // Pin del botón
const int ledPin =  13;      // Pin del Led, 


// variables will change:
int buttonState = 0;         // variable for reading the pushbutton status

void setup() {
    // initialize the LED pin as an output:
    pinMode(ledPin, OUTPUT);
    // initialize the pushbutton pin as an input:
    pinMode(buttonPin, INPUT);
}

void loop(){
    // read the state of the pushbutton value:
    buttonState = digitalRead(buttonPin);

    // check if the pushbutton is pressed.
    // if it is, the buttonState is HIGH:
    if (buttonState == HIGH) {
        // turn LED on:
        digitalWrite(ledPin, HIGH);
    }
    else {
        // turn LED off:
        digitalWrite(ledPin, LOW);
    }
}
```
