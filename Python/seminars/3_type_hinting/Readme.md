## Типизирование Python
Тайп-хинты, или аннотации типов, в Python — это функциональность, предоставляющая возможность явно указывать типы переменных, параметров и возвращаемых значений функций.

https://peps.python.org/pep-0484/

Аннотации типов в Python являются непринудительными и не служат для проверки типов во время выполнения. Они предоставляют лишь информацию о типах, которую можно использовать инструментами статического анализа или другими инструментами, разрабатываемыми сообществом.
### История появления тайп-хинтов в Python.
* **Python 3.0**: В версии Python 3.0, выпущенной в 2008 году, появилась поддержка аннотаций функций в форме специального комментария, называемого "function annotation". Однако, этот механизм был ограничен и не имел формального синтаксиса.
* **Python 3.5**: С появлением Python 3.5 в 2015 году, было внесено значительное усовершенствование в форме специального синтаксиса для тип-хинтов, известного как "function type hinting". В Python 3.5 добавлены аннотации типов для переменных, параметров и возвращаемых значений функций с использованием синтаксиса аннотации после двоеточия (:).
* **Python 3.6** и выше: В более поздних версиях Python внесены некоторые улучшения в тип-хинтинг, включая поддержку подсказок типов для переменных классов и атрибутов экземпляров.

### Использование NewType
* **Улучшение читаемости кода**: NewType помогает создавать именованные типы, которые лучше отражают семантику вашего кода и делают его более понятным для других разработчиков. Например, вместо использования простого int можно создать UserId, что явно указывает на предназначение этого значения.
* **Более безопасное использование типов**: При использовании NewType типы становятся удобными для проверок типов на этапе статического анализа. Такие проверки могут помочь выявить ошибки на ранних этапах разработки, например, если вы случайно присваиваете значение несовместимого типа переменной нового типа.

**TypeVar** - когда создаете свою систему типов. 

**NewType** - когда нужно наследоваться для создания своего подтипа. Упрощает процесс.

### Protocol
**Protocol** - это классовый декоратор из модуля typing, доступный в Python 3.8 и выше. Он используется для определения "протокола" или "интерфейса", определяющего набор методов и атрибутов реализованных в классе.

* **Определение интерфейсов**: С помощью Protocol вы можете определить интерфейсы, которые описывают ожидаемое поведение объектов. Интерфейсы помогают обеспечить совместимость между классами и улучшить документирование кода, позволяя явно указывать, какие методы и атрибуты ожидаются.
* **Проверка соответствия протоколу**: Protocol позволяет проверять, соответствует ли класс или другой тип определенному протоколу. Эта проверка может быть осуществлена статическим анализатором типов, как например mypy, чтобы убедиться, что класс или объект имеет все необходимые методы и атрибуты, указанные в протоколе.
* **Расширение классов и типов данных**: Путем объявления протокола и аннотирования класса с помощью протокола Protocol, вы можете указать, что класс соответствует определенному интерфейсу или протоколу. Это позволяет вам декларативно указать, что класс реализует требуемое поведение или функциональность.

### Используемые инструменты для улучшения кода
Линтер (linter) - это инструмент статического анализа исходного кода, используемый для обнаружения потенциальных проблем, стилевых нарушений и ошибок программирования. Он проверяет исходный код на соответствие стандартам оформления кода, рекомендациям и правилам языка программирования или конкретной кодовой базы.

* Pylint: https://github.com/pylint-dev/pylint
* MyPy: https://github.com/python/mypy
* Black: https://github.com/psf/black
