
# 🧪 Tarea 3: Comunicación colectiva y medición de latencia en MPI

Este repositorio contiene la solución a la Tarea 3 del curso de **Computación Paralela y Distribuida**, utilizando `mpi4py` y ejecutable en **Google Colab**.

## 👨‍🏫 Profesor
Johansell Villalobos Cubillo

## 🧑‍💻 Autor
Daniel Matarrita

---

## 📁 Estructura del repositorio

```
Tarea3_MPI/
├── parteA_estadisticas_mpi.py     # Parte A: Operaciones colectivas
├── parteB_latencia_mpi.py         # Parte B: Medición de latencia
├── Tarea3_MPI_Explicada.ipynb     # Notebook completo para Colab
└── README.md                      # Instrucciones y documentación
```

---

## 🚀 Requisitos

Este proyecto se puede ejecutar en:

- Google Colab
- Entornos Linux con MPI y Python 3

Dependencias:
```bash
sudo apt-get install libopenmpi-dev openmpi-bin
pip install mpi4py
```

---

## ▶️ Ejecución

### Parte A – Estadísticas con MPI

Distribuye un arreglo entre procesos y calcula el mínimo, máximo y promedio global usando:

- `MPI_Bcast`
- `MPI_Scatter`
- `MPI_Reduce`

```bash
mpirun -np 4 python3 parteA_estadisticas_mpi.py 1000000
```

### Parte B – Medición de Latencia Punto a Punto

Mide el tiempo que toma enviar y recibir mensajes pequeños entre dos procesos.

```bash
mpirun -np 2 python3 parteB_latencia_mpi.py
```

---

## 📈 Resultados esperados

### Parte A:
```
Min global: 0.0003
Max global: 99.9984
Promedio global: 50.1021
```

### Parte B:
```
Mensaje de 1 byte transmitido 10000 veces.
Latencia promedio (ida y vuelta): 3.2 µs
Latencia estimada unidireccional: 1.6 µs
```

---

## 📌 Notas

- Asegúrate de que el valor de `N` en la parte A sea divisible entre el número de procesos.
- Puedes editar los scripts para probar diferentes tamaños de mensaje o número de iteraciones.

---

## 📄 Informe

El informe se encuentra integrado en el archivo `.ipynb` con explicaciones de cada paso y análisis de resultados.
