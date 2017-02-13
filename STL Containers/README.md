#STL Containers

- [Vector](#vector)
- [Stack](#stack)
- [Queue](#queue)
- [Set](#set)
- [Map](#map)

## Vector

El vector nos permite almacenar datos tal como lo hacíamos con un arreglo, la diferencia principal radica en que un vector es de tamaño dinámico, puedes crecer o reducirse. 
```c++
#include <iostream>
#include <vector>
using namespace std;

int main() {
	vector<int> data;	// Vector vacío

	// push_back inserta elementos al vector
	for (int i = 0; i < 5; ++i)
		data.push_back(i);

	for (int i = 0; i < data.size(); ++i)
		cout << data[i] << ' ';
	cout << '\n';

	return 0;
}
```

El programa anterior produce la siguiente salida
```
0 1 2 3 4
```

Si queremos reservar memoria para un tamaño específico podemos hacer lo siguiente
```c++
#include <iostream>
#include <vector>
using namespace std;

int main() {
	int tam = 4;

	vector<int> data(tam);		// 4 enteros con valor de 0

	for (int i = 0; i < tam; ++i)
		cin >> data[i];

	vector<int> cinco(5, 5);	// 5 enteros con valor de 5

	return 0;
}
```


## Stack

El stack o pila es un almacena datos con un comportamiento **LIFO** (last-in
first-out).

```c++
#include <iostream>
#include <stack>
using namespace std;

int main() {
	stack<char> pila;

	pila.push('a');
	pila.push('b');
	pila.push('c');
	pila.push('d');
	pila.push('e');

	cout << "La pila tiene " << pila.size() << " eltos\n";

	while (!pila.empty()) {
		cout << pila.top() << ' ';
		pila.pop();
	}
	cout << '\n';

	return 0;
}
```

## Queue

La queue o cola es un contenedor con un comportamiento **FIFO** (first-in first out).
```c++
#include <iostream>
#include <queue>
using namespace std;

int main() {
	string cad;
	queue<string> cola;

	while (cin >> cad)
		cola.push(cad);

	cout << "La cola tiene " << cola.size() << " eltos\n";

	while (!cola.empty()) {
		cout << cola.front() << ' ';
		cola.pop();
	}
	cout << '\n';

	return 0;
}
```

## Set

El set es un guarda elementos únicos siguiendo un orden específico.
```c++
#include <iostream>
#include <set>
using namespace std;

int main() {
	set<int> S;

	for (int i = 7; i > 0; --i)
		S.insert(i);

	S.insert(2);
	S.insert(2);	// Ningún elemento se inserta
	S.insert(3);

	// Esto es c++11
	for (int elto : S)
		cout << elto << ' ';

	return 0;
}
```
Decidimos utilizar c++11 debido a que es más fácil iterar sobre los elementos. Para compilar
en c++11 es necesario agregar la siguiente bandera
```
g++ nombre.cpp -std=c++11
```

## Map

El mapa nos ayuda a asociar elementos mediante una relación llave-valor. Veamos un ejemplo

Supongamos que queremos almacenar el nombre y matrícula de una persona
```c++
#include <iostream>
#include <map>
using namespace std;

int main() {
	map<string, int> personas;

	personas["Adriana"]   = 1234;
	personas["Manuel"]    = 946;
	personas["Alain"]     = 231;
	personas["John"]      = 1;
	personas["Alejandra"] = 5431;

	// El tipo de dato de un mapa es un pair
	// el primer elemento es la llave
	// y el segundo es el valor
	for (auto p : personas)
		cout << "Nombre: " << p.first << " Matricula: " << p.second << '\n';

	return 0;
}
```

Si ejecutas el código anterior te darás cuenta que los elementos son desplegados en orden
alfabético, esto sucede porque el mapa ordena automáticamente los elementos que agregas.
