## Objetivo
Poor security at your business can lead to disastrous results for you, your customers, and your suppliers. Latest news can give us an idea about the magnitude of the problem.
## Solución

Se dan 2 archivos txt con caracteres distintos. Al comparar estos archivos con el siguiente código en c++

```cpp
int main() {
    ifstream archivo1("news.txt");
    ifstream archivo2("newsf.txt");

    if (!archivo1.is_open() || !archivo2.is_open()) {
        cerr << "No se pueden abrir los archivos." << endl;
        return 1;
    }

    string linea1, linea2;
    bool diferenciasEncontradas = false;

    while (getline(archivo1, linea1) && getline(archivo2, linea2)) {
        for (int i = 0; i < linea1.length(); i++) {
            if (linea1[i] != linea2[i]) {
                cout << linea1[i];
                diferenciasEncontradas = true;
            }
        }
    }

    archivo1.close();
    archivo2.close();

    if (!diferenciasEncontradas) {
        cout << "Los archivos son idénticos." << endl;
    }

    return 0;
}
```

Nos da la siguiente cadena: ZmxhZ01Ye3Bvb3JzZWN1cml0eX0=
La convertimos a base 64 y tenemos:
flagMX{poorsecurity}
## Notas adicionales

## Referencias