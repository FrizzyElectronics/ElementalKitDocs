# Elemental Kit - Sensor de distancia infrarrojo

[![Texto alternativo](images/sharp.jpg "Sensor de distancia")](www.frizzy.es/grape)


Los sensores de distancia Sharp son una buena opción para muchos proyectos que necesitan mediciones precisas de distancia. De toda la gama de sensores infrarrojos de distanca que Sharp fabrica, hemos optado por usar el GP2Y0A21YK0F debido a su sencillez de uso y a que posee un rango de medición (10-80cm) aplicable en la mayoria de proyectos de robótica amateur. 

La conexion de este sensor es bastante sencilla, siemplemente tienes que conectar la alimentación y la salida de señal a un pin con conversor analogico-digital de tu microcontrolador favorito. Para facilitar la tarea, hemos añadido un cable compatible con la placa Grape, pero cuidado, ¡Este cable tiene los pines de Vcc y GND invertidos! **¡No emplees este cable para conectar otros módulos Elemental!**


## Características

* Tensión de funcionamiento: 4.5V - 5.5V
* Consumo: 30mA
* Rango de medición: 10cm - 80cm
* Tipo de salida: Analógica
* Tiempo de respuesta: 38 ± 10 ms
* Medidas: 29.5×13×13.5 mm
* Peso 3.5g

##Primeros pasos
--------

###Grape


<img src="../images/montaje_sharp.png" alt="Drawing" style="width: 600px;"/>

| Grape | Elemental - Sensor de distancia |
| ----- | ----------------- |
| GND   | Negro             |
| 5V    | Rojo              |
| A2    | Amarillo          |


```arduino

void setup() {
    //Inicializamos el puerto serie 9600 baudios
    Serial.begin(9600);
}

void loop(){
    // Leemos el sensor y lo asignamos a la variable luz
    luz = analogRead(A2);
    Serial.print("El nivel de luz es de:");
    Serial.println(luz);

}
```


##Recursos
-------

-   [Archivos PCB en KiCAD](https://github.com/FrizzyElectronics/BasicModule-II)
-   [Esquema en PDF](https://raw.githubusercontent.com/FrizzyElectronics/BasicModule-II/master/pdf/BasicModule-II.pdf "File:BasicModule-II.pdf")
-   [Fritzing](https://raw.githubusercontent.com/FrizzyElectronics/AtomModulesFritzingParts/master/FritzingParts/Atom_LDR.fzpz "File:BasicModule-II.pdf")

## Licencia
-------
Copyright (c) 2018-2017 Frizzy Electronics. (https://www.frizzy.es). Todo el texto y las fotografías bajo licencia <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>. <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"> </a>

## Soporte Técnico
-------
Por favor, comunicanos cualquier incidencia para poder mejorar juntos. Escribenos a [info@frizzy.es](info@frizzy.es). 
