# Laboratorio: Minimax y Poda Alfa-Beta

## Descripción
Este proyecto implementa los algoritmos Minimax y Poda Alfa-Beta para resolver un árbol de decisión simplificado.

## Objetivo
Comparar el resultado y la eficiencia de Minimax frente a Poda Alfa-Beta.

## Instalación
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Ejecución
```bash
python -m src.main
```

## Pruebas
```bash
pytest --cov=src --cov-report=term-missing
```

## Preguntas de análisis
1. ¿Por qué Minimax y Alfa-Beta devuelven el mismo valor?
Minimax y Alfa-Beta devuelven el mismo valor porque ambos evalúan exactamente el mismo árbol de juego y buscan la mejor decisión posible. La diferencia es que Alfa-Beta elimina ramas que no pueden influir en el resultado final, pero sin alterar la decisión óptima obtenida por Minimax.

2. ¿Cuándo Alfa-Beta reduce más nodos?
Alfa-Beta reduce más nodos cuando los movimientos están ordenados de manera favorable, es decir, cuando las mejores jugadas se evalúan primero. En estos casos, se producen más podas y se evita analizar una gran cantidad de nodos innecesarios.

3. ¿Qué ocurre si el árbol está mal ordenado?
Si el árbol está mal ordenado, Alfa-Beta realiza menos podas y debe explorar más nodos. En el peor caso, su rendimiento puede ser similar al de Minimax, perdiendo gran parte de la ventaja de optimización que ofrece.

4. ¿Cómo se aplicaría este algoritmo en ajedrez, damas o tres en raya?
En juegos como el ajedrez, las damas o el tres en raya, Minimax y Alfa-Beta se utilizan para analizar las posibles jugadas futuras del jugador y del oponente. El algoritmo evalúa los diferentes escenarios y selecciona el movimiento que maximiza las posibilidades de ganar o minimizar las pérdidas, actuando como la inteligencia artificial del juego.
```