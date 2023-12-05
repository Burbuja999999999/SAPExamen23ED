# Examen Entornos de Desarrollo 
## Tema 3: Git. 05/12/23


Nombre y apellidos: ________________________________ 			Fecha:___________ 

 

LINK DEL REPOSITORIO:________________________________________________ 

> Vamos a crear una primera versión de una calculadora.  
> Debajo de cada ejercicio deberá aparecer capturas de pantalla pertinentes que justifiquen su realización. Intentad hacer todo lo posible desde la consola si no se indica lo contrario. 
> Se valorará negativamente las malas prácticass de GIT 

 

**1.- (0,75) Crea un repositorio en github “AAAExamen23ED“ e invítame a colaborar: "TomBort8" . AAA serán las primeras letras de tu nombre, 1er apellido y 2º apellido respectivamente.** 

<img src="https://i.ibb.co/mBVv7Kh/examen1.png" alt="examen1" border="0">


**2.- (0,75) Inicializa el repostiorio en local y vincúlalo al repostiroio de github** 

<img src="https://i.ibb.co/mC1mR5Q/captura2.png" alt="captura2" border="0">

<img src="https://i.ibb.co/mJQyLyR/captura2-1.png" alt="captura2-1" border="0">

**3.- Crea un main que pida 2 números por teclado.** 

<img src="https://i.ibb.co/djbGyYk/captura3.png" alt="captura3" border="0">



```
import java.util.Scanner; 

 

public class MostrarNumeros { 

 

    public static void main(String[] args) { 

        Scanner scanner = new Scanner(System.in); 

 

        System.out.println("Por favor, ingresa el primer número:"); 

        double numero1 = scanner.nextDouble(); 

 

        System.out.println("Ahora, ingresa el segundo número:"); 

        double numero2 = scanner.nextDouble(); 

 

        System.out.println("Los números ingresados son:"); 

        System.out.println("Número 1: " + numero1); 

        System.out.println("Número 2: " + numero2); 

 

        scanner.close(); 

    } 

} 
```
> Sube los cambios al repositorio. 

**4.- (0,2) Crea  un fichero ExplicaCalculadora.txt : “Este programa es una calculadora que va a poder realizar las operaciones básicas: sumar, restar, multiplicar y dividir”.** 

<img src="https://i.ibb.co/SNSsssg/Captura4.png" alt="Captura4" border="0">


*  **4.1  (0,3)Crea también un fichero de texto que no debes subir a github pero debe estar dentro de la carpeta NoSubir.txt: (Este archivo debes añadirlo y quitarlo, como si te hubieras confundido). “Este archivo debe estar en la carpeta pero no subido a git”.** 

<img src="https://i.ibb.co/GtRgZms/Captura-de-pantalla-2023-12-05-134128.png" alt="Captura-de-pantalla-2023-12-05-134128" border="0">
<img src="https://i.ibb.co/3c6BX5d/captura4-1.png" alt="captura4-1" border="0">
<img src="https://i.ibb.co/x2qhYX9/captura4-1-2.png" alt="captura4-1-2" border="0">

> Muestra por comandos que no lo has subido 

> Sube los cambios al repositorio. 

**5.- (0,5) Muestra la diferencia entre los 2 últimos commits.** 

<img src="https://i.ibb.co/z2Fp9bG/captura5.png" alt="captura5" border="0">

**6.- (0,5) Crea 2 ramas SUMADORES y RESTADORES** 

<img src="https://i.ibb.co/M6x4qCc/captura6.png" alt="captura6" border="0">

**7.- Sitúate en SUMADORES y añade al main lo siguiente:**

<img src="https://i.ibb.co/ypx42s0/captura7.png" alt="captura7" border="0">

```
public static double sumar(double a, double b) { 

        return a + b; 

    } 
public static double multiplicar(double a, double b) { 

        return a * b; 

    } 

public static double potencia(double base, double exponente) { 

        return Math.pow(base, exponente); 

    }  
```

> Sube los cambios al repositorio.

**8.- Sitúate en RESTADORES y añade al main lo siguiente:**

<img src="https://i.ibb.co/6Zzphyz/captura8.png" alt="captura8" border="0">


```
public static double restar(double a, double b) { 

        return a - b; 

    } 

public static double dividir(double a, double b) { 

        if (b != 0) { 

            return a / b; 

        } else { 

            throw new IllegalArgumentException("No se puede dividir por cero"); 

        } 

    } 

public static double raizCuadrada(double a) { 

        if (a >= 0) { 

            return Math.sqrt(a); 

        } else { 

            throw new IllegalArgumentException("No se puede calcular la raíz cuadrada de un número negativo"); 

        } 

    } 
```

> Sube los cambios al repositorio. 

**9.- (1) Muestra la diferencia entre las ramas sumadores y restadores y guárdalo en un fichero llamado DIFERENCIA _RAMAS (desde consola). Este ficehro debe subirse al repositorio.** 


<img src="https://i.ibb.co/kKKyVz8/captura9.png" alt="captura9" border="0">

<img src="https://i.ibb.co/QMj1kmw/captura9-1.png" alt="captura9-1" border="0">
 

**10.- (1,5) Fusiónalo en main (consola) y resuelve el conflicto (en gitHUB).** 


<img src="https://i.ibb.co/F3vdPtv/captura10.png" alt="captura10" border="0">



> Sube los cambios al repositorio. 

 

**11.-(0,5) Borra las ramas SUMADORES Y RESTADORES.**

<img src="https://i.ibb.co/185fzs7/captura11.png" alt="captura11" border="0">



 

**12.- (0,5) entra a SOURCETREE y haz una captura del eje temporal del repositorio. Haz una breve explicación de lo que observas.** 


<img src="https://i.ibb.co/ZMyG0cF/captura12.png" alt="captura12" border="0">

He entrado a SOURCETREE y veo que hay un commit que no se ha realizado, y que solo se ha fusionado la rama de SUMADORES, aunque al entrar a git en main esta correcto, no se porque ha pasado esto
 

**13.- (1) ¿ Cuál es la diferencia entre “git pull” y “git clone” ?** 

Git clone sirve para descar un repositorio entero de git a local, mientras que git pull solo descarga el historial del marcador e incorpora cambios.


> 
 

 

**14.- (1) Abre el main y déjalo inservible. Sube los cambios. Deshaz el último commit.**


 

**15.- (1) Vuelve al estado en el que estaba el proyecto al acabar el ejercicio 3 en local.**
 
 
 **16.-(0,5) Añade este documento al repoitorio, con todas las imágenes para que se pueda ver desde git.**


**17.- Por último, ejecutad el siguiente comando:** 

> *history > historial.txt* 

**sube el resultado a aules junto al PDF de este documento.** 