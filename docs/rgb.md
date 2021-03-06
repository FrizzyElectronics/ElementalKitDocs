# Elemental Kit - RGB

![Texto alternativo](images/rgb.jpg "Modulo de led RGB")

El módulo de RGB cuenta con un led 5050 RGB con el que podrás generar hasta 16 millones de colores! Simplemente conecta cada pin de color a un pin con PWM de tu [Grape](https://www.frizzy.es/grape/) si quieres control total sobre el color y cambia los valores para ver que sucede. 

## Características

* Módulo fácil de usar
* Utiliza la conexion GND/RED/GREEN/BLUE
* Incluye sus respectivas resistencias por cada color

##Primeros pasos
--------

###Grape


<img src="../images/montaje_rgb.png" alt="Drawing" style="width: 400px;"/>

| Grape | Elemental - RGB   |
| ----- | ----------------- |
| GND   | Negro             |
| D9    | Rojo              |
| D10   | GREEN             |
| D11   | BLUE              |


```arduino

const int RED = 9;
const int GREEN = 10;
const int BLUE = 11;

void setup() {
	
    pinMode(RED, OUTPUT);
    pinMode(GREEN, OUTPUT);
    pinMode(BLUE, OUTPUT);
}

void loop(){
    
    digitalWrite(BLUE, LOW);
    digitalWrite(RED, HIGH);
    delay(1000);
    digitalWrite(RED, LOW);
    digitalWrite(GREEN, HIGH);
    delay(1000);
    digitalWrite(GREEN, LOW);
    digitalWrite(BLUE, HIGH);
    delay(1000);

}
```


##Recursos
-------

-   [Archivos PCB en KiCAD](https://github.com/FrizzyElectronics/RGBModule)
-   [Esquema en PDF](https://raw.githubusercontent.com/FrizzyElectronics/RGBModule/master/pdf/RGBModule.pdf "File:RGBModule.pdf")
-   [Fritzing](https://raw.githubusercontent.com/FrizzyElectronics/AtomModulesFritzingParts/master/FritzingParts/Atom_RGB.fzpz "File:Atom_RGB.fzpz")

## Licencia
-------
Copyright (c) 2018-2017 Frizzy Electronics. (https://www.frizzy.es). Todo el texto y las fotografías bajo licencia <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>. <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"> </a>

## Soporte Técnico
-------
Por favor, comunicanos cualquier incidencia para poder mejorar juntos. Escribenos a [info@frizzy.es](info@frizzy.es). 
