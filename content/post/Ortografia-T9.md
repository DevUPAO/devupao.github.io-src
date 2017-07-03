---
title: "Ortografia-T9"
author: "Eduwin Torres"
date: "2017-06-23"
description: "Ejercicio resuelto para el 2° taller de algoritmos"
tags: ["hugo", "github", "dev/upao"]
---
### **TALLER DE ALGORITMO 2 - EJERCICIO RESUELTO**

## FUENTE: GOOGLE CODE JAM
El alfabeto latino tiene 26 caracteres y los teléfonos sólo tienen diez 
digitos en el teclado.Nos gustaría que sea más facil escribir un mensaje 
a su amigo ulizando una secuencia de pulsaciones de teclas para indicar 
los caracteres deseados. Las letras se asignan  a los digitos como se 
muestran acotinuación: Para insertar el caracter "b", por ejemplo, el 
programa debe presionar 22. Para insertar dos caracteres en secuencia de 
la misma tecla, el usuario debe hacer  una pausa antes de pulsar la tecla 
para indicar una pausa. Por ejemplo, 2 2 indica "aa" mientras que le 22 
indica "b".

## PROGRAMAS A USAR
<i class="fa fa-check"></i>Lapicero y hoja bond.

<i class="fa fa-check"></i>Netbeans.

## 1.-PASO
Desarrollar diagramas ns del ejercicio.
## 2.-PASO
Pasar los diagramas ns a Netbeans.

Para pasar tus diagramas ns a Netbeans necesitas solo aprender lo basico de 
codificación como condicionales,tipo de variales, como leer un dato desde 
consola, en caso no sepas como hacerlo puedes buscarlos en google, "la base 
de todo es saber como hacerlo ya que si no sabes ni que quieres hacer la 
maquina tampoco lo sabra". 

#### LEEMOS Y DECLARAMOS VARIABLES 
``` 
System.out.print("Ingrese cadena a traducir:");
Scanner sc = new Scanner(System.in);
String sCadena = sc.nextLine() + 1;
String Cadena = "", resCadena = "";
double can = 0;
 ```
#### CREAMOS DICCIONARIO CON ARREGLO BIDIMENCIONALES 
```
String[][] diccionario = {{"2", "A"}, {"22", "B"}, {"222", "C"}, {"3", "D"},
{"33", "E"},{"333", "F"},{"4", "G"}, {"44", "H"}, {"444", "I"}, {"5", "J"}, 
{"55", "K"}, {"555", "L"}, {"6", "M"}, {"66", "N"}, {"666", "O"},{"7", "P"}, 
{"77", "Q"}, {"777", "R"}, {"7777", "S"}, {"8", "T"}, {"88", "U"}, {"888", "V"}, 
{"9", "W"},{"99", "X"}, {"999", "Y"}, {"9999", "Z"}};
        
```
#### CREAMOS UN FOR PARA RECORRER EL ARREGLO 
 ```
for (int i = 0, j = 1; i < sCadena.length() && j < sCadena.length(); i++, j++) {
        char sCadenaAux = sCadena.charAt(i);
        char sCad = sCadena.charAt(j);
}
```
#### DENTRO DEL FOR AGREGAMOS CONDICIONALES 
Las condicionales nos ayudaran a validad las condiciones planteadas en el ejercicio,
yo cree estas pero si ustedes creen convenientes disminuir o hacerlo de 
otra forma a buena hora.
```
 if (sCadenaAux == sCad) {
                Cadena = Cadena + sCadenaAux;
                //System.out.println("Cadena essss:" + Cadena);

            } else {
                if(sCadenaAux != ' '){
                int num = Integer.parseInt(String.valueOf(sCadenaAux));
                Cadena = Cadena + sCadenaAux;           
                if (num >= 2 && num <= 6 || num == 8) {
                    can = Cadena.length() % 3;
                    if (can >= 1) {
                        Cadena = "";
                        for (int k = 0; k < can; k++) {
                            Cadena = Cadena + num;
                        }
                    }
                    for (int h = 0; h < 25; h++) {
                        if (diccionario[h][0].equals(Cadena)) {
                            resCadena = resCadena + diccionario[h][1];
                            Cadena = "";
                        }
                    }
                } else if(num == 7 || num == 8){
                    can = Cadena.length() % 4;
                    for (int d = 0; d < 25; d++) {
                        if (diccionario[d][0].equals(Cadena)) {
                            resCadena = resCadena + diccionario[d][1];
                            Cadena = "";
                        }
                    }
                }
                else if(num == 0){
                    Cadena= "";
                    resCadena = resCadena + " ";
                }
                }else{
                    Cadena = "";
                }
                
            }
```
#### PARA TERMINAR IMPRIMIMOS LA CADENA PARA VISUALIZAR EL MENSAJE
```
    System.out.println("La cadena traducida es:" + resCadena);

```
#### EJEMPLO DE ENTRADA Y DALIDA
Con este ejemplo pueden probrar en su computador si el sistema corre correctamente.
```
ENTRADA                 SALIDA
3 33888 8872666         DEVUPAO
4466655520688663666     HOLA MUNDO
8872666                 UPAO
```
Si tienes alguna pregunta, no dudes en escribirnos a  [la fanpage de la comunidad](https://www.facebook.com/Devupao-450137858679179/).