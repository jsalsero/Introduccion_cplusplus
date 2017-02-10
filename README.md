# Introduccion_c++

Bienvenido a la guía básica para pasar de ANSCI-C a C++


Seguramente recordarás el siguiente programa
```c
#include <stdio.h>

int main() {
  printf("Hola mundo!");
  return 0;
}
```

Compáralo con el siguiente código
```c++
#include <iostream>

int main() {
  std :: cout << "Hola mundo";
  return 0;
}
```

Whaat? ¿Qué es cout y los signos de ```<<```?
No entremos en pánico (aún), sucede que podemos utilizar uno u otro imprimir __JAMÁS AMBOS__, hablemos un poco sobre las ventajas que ofrece cout

ANSCI-C:
```c
  printf("%d %d %d", a, b, c);
```
C++
```c++
  std :: cout << a << b << c;
```

Como te podrás dar cuenta no necesitas indicar el tipo de dato a imprimir, basta con que sea ¨imprimible¨. Tampoco es necesario que todo tenga el mismo tipo de dato:
```
  std :: cout << 1 << 2 << " tambien imprime cadenas!\n";
```

Sin embargo aún no hemos dicho nada sobre 'std ::'. Podemos pensar en std como el archivo en el que está guardado el código para utilizara cout, esto quiere decir que puedes crear tus propias funciones con el mismo nombre que tiene la std.

-----------
```
#include <stdio.h>

int main() {
  int numero;
  scanf("%d", &numero);
  return 0;
}
```

El programa de arriba lee un número y lo guarda en la variable ```número```, veamos cómo hacerlo en C++

```
#include <iostream>

int main() {
  int numero;
  std :: cin >> numero;
  return 0;
}
```

Vaya, resulta que scanf también tiene su análogo como printf y efectivamente cin ofrece facilidades similares a las de cout ya que no hace falta indicar el tipo de dato a leer y podemos leer tantos datos como queramos.

```
#include <iostream>

int main() {
  int a, b, c;
  std :: cin >> a >> b >> c;
  return 0;
}
```

Compilación
----------

Si utilizas windows te recomendamos descargar [MinGW](https://sourceforge.net/projects/mingw/files/latest/download?source=files) e instalarlo siguiendo estos pasos:

1. Extrae los archivos en C:\MinGW (si no existe la carpeta, crea una con ese nombre)
2. Agrega ```C:\MinGW\bin;``` a la variable de entorno PATH. 

Para compilar un programa basta con abrir la terminal 
* Windows: _Win + R_ >> escribe ```cmd``` >> Enter
* Linux:   _Ctrl + Alt + T_

Y escribir el siguiente comando
```
  g++ nombre.cpp 
```

Este comando te devolverá un archivo a.out(si estás en linux) a.exe(windows), siempre y cuando no tenga errores de compilación el archivo ¿lógico no?














