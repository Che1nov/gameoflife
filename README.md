## Конвейер "Жизнь" (Conway's Game of Life) на Go
Это реализация классической игры "Жизнь" Джона Конвея на языке программирования Go. Игра представляет собой клеточное automaton, где клетки могут быть "живыми" или "мертвыми", и они взаимодействуют с соседями согласно определённым правилам.

### Описание игры
Игра "Жизнь" состоит из сетки клеток, каждая из которых может быть либо живой, либо мёртвой. В каждом шаге времени происходит обновление состояния всех клеток на основе состояния их соседей.

### Правила игры
- Рождение: Если у мёртвой клетки есть ровно 3 живых соседа, она становится живой.
- Выживание: Если у живой клетки 2 или 3 живых соседа, она остаётся живой.
- Смерть: Если у живой клетки меньше 2 или больше 3 живых соседей, она умирает.
- Игровое поле представляет собой двумерную решётку с ограниченными размерами, и при выходе за границу поля клетки "появляются" с другой стороны (периодическая граница).

### Основные компоненты
- Universe: структура, представляющая собой двухмерный массив клеток, где каждая клетка может быть либо живой (true), либо мёртвой (false).
- NewUniverse: функция, которая создаёт новую пустую вселенную с заданными размерами.
- Seed: функция, которая заполняет вселенную случайными живыми клетками.
- Set: функция для установки состояния клетки в конкретной ячейке (живая/мертвая).
- Alive: функция для проверки, является ли клетка живой.
- Neighbors: функция для подсчёта количества живых соседей вокруг клетки.
- Next: функция для вычисления следующего состояния клетки на основе её соседей.
- Step: функция, которая обновляет состояние вселенной для следующего шага.
- Show: функция для отображения текущего состояния вселенной на экране.

### Как запустить
- Убедитесь, что у вас установлен Go. Если Go не установлен, скачайте и установите его с официального сайта: https://golang.org/dl/

- Скачайте или клонируйте этот репозиторий на свою машину.

- Перейдите в директорию проекта и выполните команду:

`go run main.go`

Игра будет запущена, и вы увидите анимацию изменения состояния клеток. Каждое обновление будет происходить с интервалом в 1/30 секунды.

### Структура проекта
- main.go: Основной файл программы, который содержит всю логику игры и отображение клеток.
- README.md: Этот файл с инструкциями и описанием проекта.

### Дополнительные настройки
- Вы можете изменить размер вселенной, подстроив значения констант width и height в начале файла.
- Также можно изменить скорость игры, изменив задержку в time.Sleep(time.Second / 30) в функции main.

### Пример вывода
При запуске программы, на экране будут отображаться живые клетки (обозначенные символом *) и мёртвые клетки (обозначенные пробелами). Игра будет продолжаться, пока не будет остановлена вручную.

#### Лицензия
Этот проект распространяется под лицензией MIT. См. LICENSE для подробной информации.

