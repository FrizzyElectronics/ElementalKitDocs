#Elemental Kit - Mini-Servo

![Texto alternativo](images/servo1.jpg "Mini Servo de 180 grados")

El módulo de potenciómetro consta de un potenciómetro de 10k conectado directamente al conector JST, es la manera más sencilla de añadir rápidamente un controlador de este tipo a tus proyectos. El conector de salida es el correspondiente JST-PH de 2.0mm compatible con los cables para la Grape.

## Características

* Recorrido: 180º
* Utiliza la clásica conexión "GND/VCC/SIG"
* Engranajes internos de metal
* Torque: 1.8Kg/CM a 6V

<img src="../images/servo3.jpg" alt="Drawing" style="width: 400px;"/>

##Primeros pasos
--------

###Grape


<img src="../images/montaje_servo.png" alt="Drawing" style="width: 400px;"/>

| Grape | Elemental - MiniServo |
| ----- | ----------------- |
| GND   | Marrón             |
| 5V    | Rojo              |
| D9    | Naranja          |


```arduino

#include <Servo.h>

Servo miniServo;  // Creamos un objeto servo para controlar el mini-servo

int posicion = 0;    // variable para guardar la posicion del servo

void setup() {
  miniServo.attach(9);  // adjuntamos el servo al pin 9
  Serial.begin(9600);   // Iniciamos el puerto serie para imprimir la posicion del servo (opcional)
}

void loop() {
  for (posicion = 0; posicion <= 180; posicion += 1) { // Recorremos de 0 a 180 con la variable posicion de grando en grado
    miniServo.write(posicion);              // aplicamos la posicion al servo
    Serial.println(posicion);			    // Imprimimos la posicion del servo (opcional)
    delay(15);                              // esperamos 15ms para que al servo le de tiempo a alcanzar la posicion
  }
  for (posicion = 180; posicion >= 0; posicion -= 1) { // Recorremos de 180 a 0 con la variable posicion de grando en grado
    miniServo.write(posicion);              // aplicamos la posicion al servo
    Serial.println(posicion);			    // Imprimimos la posicion del servo (opcional)
    delay(15);                              // esperamos 15ms para que al servo le de tiempo a alcanzar la posicion
  }
}
```


##Recursos
-------

-   [Web del fabricante](https://www.emaxmodel.com/es08ma-ii.html#product_tabs_description_tabbed)
-   [Datasheet](https://raw.githubusercontent.com/FrizzyElectronics/ElementalKitDocs/master/docs/images/servo2.jpg "File:Servo180.jpg")


## Licencia
-------
Copyright (c) 2018-2017 Frizzy Electronics. (https://www.frizzy.es). Todo el texto y las fotografías bajo licencia <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>. <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"> </a>

## Soporte Técnico
-------
Por favor, comunicanos cualquier incidencia para poder mejorar juntos. Escribenos a [info@frizzy.es](info@frizzy.es). 
