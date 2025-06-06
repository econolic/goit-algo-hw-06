# Аналіз Транспортних та Баєсівських Мереж: Від Пошуку Шляхів до Оптимізації

Цей проєкт демонструє застосування графових алгоритмів для аналізу двох різних типів мереж: міської транспортної системи та Баєсівської мережі для діагностики захворювань. Використовуються такі алгоритми, як Пошук у Глибину (DFS), Пошук у Ширину (BFS) та алгоритм Дейкстри для знаходження та оптимізації шляхів.

## Огляд Ноутбуків

### 1. Аналіз Транспортних Мереж (`city_transport_analysis.ipynb`)

Цей ноутбук моделює спрощену транспортну мережу міста як неорієнтований граф.
- **Вузли**: Ключові локації міста (наприклад, Вокзал, Центр, Університет).
- **Ребра**: Транспортні сполучення між локаціями.
- **Мета**:
    - Побудова та візуалізація графа транспортної мережі.
    - Аналіз фундаментальних характеристик мережі (кількість вузлів/ребер, щільність, зв'язність, діаметр, кластеризація, центральність).
    - Дослідження маршрутів за допомогою DFS (знаходження одного з можливих шляхів) та BFS (знаходження найкоротшого шляху за кількістю зупинок).
    - Оптимізація маршрутів за часом у дорозі за допомогою алгоритму Дейкстри, після додавання ваг до ребер.

**Ключові алгоритми та концепції:**
- Побудова графів з `networkx`.
- Візуалізація графів з `matplotlib`.
- DFS (Depth-First Search - Пошук у глибину).
- BFS (Breadth-First Search - Пошук у ширину).
- Алгоритм Дейкстри для знаходження найкоротших шляхів у зважених графах.
- Розрахунок характеристик графа: щільність, зв'язність, діаметр, коефіцієнт кластеризації, середня довжина найкоротшого шляху, центральності (за ступенем, посередництвом, близькістю).

### 2. Аналіз Баєсівських Мереж (`bayesian_network_analysis.ipynb`)

Цей ноутбук моделює Баєсівську мережу для діагностики двох захворювань як орієнтований ациклічний граф (DAG).
- **Вузли**: Фактори ризику, захворювання, симптоми, результати тестів.
- **Ребра**: Причинно-наслідкові зв'язки між змінними.
- **Ваги ребер**: Обчислюються на основі взаємної інформації (Mutual Information, MI) між пов'язаними змінними.
- **Мета**:
    - Побудова та візуалізація Баєсівської мережі.
    - Визначення умовних ймовірностей (CPD) за допомогою `pgmpy`.
    - Обчислення ваг ребер на основі взаємної інформації.
    - Дослідження шляхів поширення впливу за допомогою DFS, BFS та алгоритму Дейкстри (з вагами MI).
    - Виконання ймовірнісного аналізу для оцінки ймовірностей захворювань за наявності доказів.
    - SWOT-аналіз моделі та підходу.

**Ключові алгоритми та концепції:**
- Моделювання Баєсівських мереж з `networkx` та `pgmpy`.
- Визначення таблиць умовних ймовірностей (CPD).
- Обчислення взаємної інформації (MI) як міри сили зв'язку.
- DFS, BFS, алгоритм Дейкстри для аналізу шляхів в орієнтованих зважених графах.
- Ймовірнісний висновок за допомогою `VariableElimination` з `pgmpy`.