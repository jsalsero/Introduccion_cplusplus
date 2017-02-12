#strings

Veamos algunas operaciones básicas utilizando cadenas

```c++
#include <string>
using namespace std;

int main() {
  string cad = "club";
  string cad2;

  // Copia de cad en cad2
  cad2 = cad;

  // También es posible concatenar mediante el operador +=
  string club = "club ";
  club       += "de ";
  club       += "algoritmia.";
  return 0;
}
```

La lectura de un string es la siguiente

```c++
string nombre;
cin >> nombre;
```

Sin embargo para cin los espacios en blanco, las tabulaciones y los enter indican el final de la cadena a leer. El 
siguiente ejemplo ayudará a entender "el fin de la cadena".

```c++
#include <iostream>
#include <string>
using namespace std;

int main() {
  string cad;
  cin  >> cad;
  cout << cad;
  
  return 0;
}
```
Ejecutando el programa anterior y escribiendo la frase "pepe pica papas" sucede lo siguiente

![alt tag](/strings/img/pepe.png)

¿Qué sucedió? ¿Por qué no leyó toda la frase? Tal como lo mencionamos, el primer espacio le indicó a cin que
ahí termina la cadena omitiendo todo lo demás.

Ahora bien, si queremos leer una línea completa debemos usar getline

```c++
#include <iostream>
#include <string>
using namespace std;

int main() {
  string cad;
  getline(cin, cad);
  cout << cad;
  
  return 0;
}
```

![alt tag](/strings/img/getline_pepe.png?raw=true)
