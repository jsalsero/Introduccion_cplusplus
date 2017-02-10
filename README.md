# Introduccion_c++

Bienvenido a la guía básica para pasar de ANSCI-C a C++
```c
#include <stdio.h>

int main() {
	printf("Hola mundo!");
	return 0;
}
```
Seguramente recordarás ese programa, ahora veamos cómo se hace en C++
```c++
#include <iostream>

int main() {
	std :: cout << "Hola mundo";
	return 0;
}
```

Whaat? ¿Qué es cout y los signos de '<<'?
No entremos en pánico (aún), sucede que podemos usar ambos para imprimir en C++ aunque veamos algunas ventajas que ofrece cout

ANSCI-C:
```c
	printf("%d %d %d", a, b, c);
```
C++
```c++
	std :: cout << a << b << c;
```

Como te podrás dar cuenta no necesitas indicar el tipo de dato a imprimir, basta con que sea ¨imprimible¨. 

```
  std :: cout << 1 << 2 << " tambien imprime cadenas!\n";
```

Sin embargo aún no hemos dicho nada sobre 'std ::', podemos pensar en std como el archivo en el que está guardado el código para utilizara cout, esto quiere decir que puedes crear tus propias funciones con el mismo nombre que tiene la std.


Compilación
----------

Para compilar un programa en C++ utilizamos el siguiente comando
```
  g++ nombre.cpp 
```

Este comando te devolverá un archivo a.out(si estás en linux) a.exe(windows), siempre y cuando no tenga errores de compilación el archivo ¿lógico no?














