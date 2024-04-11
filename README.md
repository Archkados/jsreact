Шаг 1
Создаём react app
npx create-react-app название проекта

Шаг 2
1)Удаляем все ненужное в html файле
2)Меняем title на с react app на todo app
1)Удаляем все из файла index.js 
2)Заменяем все на console.log(‘Hello Samat’);

Шаг 3: создание todo list
удаляем console.log
Импортируем библиотеку React.
Импортируем модуль ReactDOM.
Создаем переменную element, которая содержит js-код для создания интерфейса.
В element находится корневой элемент(обертка) <div>.
<h1> - заголовок.
<input> - поле ввода с подсказкой "search".
<ul> - неупорядоченный список.
<li> - элементы списка, в нашем случае представляющие задачи.
ReactDOM.render(element, document.getElementById('root')); - используем функцию reactdom.render для отображения ‘element’. Она находит элемент root в html документе и заменяет его на этот компонент 


Шаг 4: создание компонентов
Вместо определения элемента создаем три функциональных компонента.
const TodoList = () => {  }: Создаем новый функциональный компонент TodoList, который представляет список задач.
const AppHeader = () => { }: Создаем новый функциональный компонент AppHeader, отвечающий за отображение заголовка приложения.
const SearchPanel = () => { }:  Создаем новый функциональный компонент SearchPanel, отвечающий за отображения поля поиска.
const App = () => {  }: Создаем новый функциональный компонент App, который является контейнером для других компонентов. 
Используем ReactDOM.render для отображения корневого компонента App в элементе с идентификатором 'root' в DOM.


шаг 5: jsx
создаем массив items, в котором находиться текст для списка
теперь элементы списка li получают свои значения из массива items
внутри компонента SearchPanel добавляем переменную searchText, который содержит текст для placeholder-а 
внутри компонента SearchPanel добавляем переменную searchStyle, которая определяет стили  для элемента input
Также <input> теперь имеет атрибут disabled={true}, что делает его неактивным.
В компоненте App, добавлена переменная value, которая включает <script>alert ("")</script>


Шаг 6: создание и форматирование структуры
создаем папку components в src 
добавляем в папку components app-header.js , search-panel.js , todo-list-item.js , todo-list.js
удаляем из index.js в папке src компоненты TodoList, AppHeader, SearchPanel 
удаляем из компонента App переменную value
импортируем в index.js appheader, searchpanel, todolist
в файле app-header.js создаем компонент appheader 
в файле search-panel.js создаем компонент searchpanel
в файле todo-list-item.js создаем компонент todolistitem
в файле todo-list.js создаем компонент todolist
в каждом из этих файлов экспортируем созданные компоненты


Шаг 7: использование свойств в Реакте
в todo-list-item.js удаляем компонент todolistitem и заменяет его на такой же но с параметрами label и important = false.
добавляем переменную style в todolistitem, в которой определяем цвет 
используем тернарное выражение, если important = false то цвет будет черным
 добавляем в файл todo-list.js списки li , а также используем компонент todolistitem внутри элемента списка li с передачей параметра label 


Шаг 8: Использование массивов в качестве компонентов
в todo-list.js удаляем списки li, и вместо них создаем списки Li , которые включают в себя компонент todolistitem и параметры label и important
в файл index.js в компонент app добавляем массив tododata, каждый объект которого включает в себя параметры label и important
добавляем в див компонент todolist в который передается tododata как параметр todos 


шаг 9: Использование метода Map в качестве компонентов
создаем переменную elements в todo-list.js в компоненте todolist, которая будет преобразовывать каждый элемент Item из массива todos с помощью метода map в соответствующий элемент списка Li
для каждого элемента item создается компонент todolistitem и в него передается параметры label и important которые беруться из Item
удаляем списки в ul и вместо них пишем массив elements, который будет отображать элементы списка



шаг 10: Оператор распространения для массивов
используем оператор расширения {... item} вместо предыдущего способа 

шаг 11: Параметр Rest для элементов массива
деструктуризуем объем item, берем свойство id  из объекта  item а все остальное сохраняем в объект  itemProps
в каждом элементы списка устанавливаем ключ в значение item.id
передаем объект itemprops  в компонент todolistitem с использованием оператора расширения 	


шаг 12: Импорт Bootstrap и CSS
1)Первый метод устанавливает стили элемента через объект style, второй метод присваивает элементу класс для применения стилей из CSS.


Шаг 13: Подготовка к фильтру статуса
1)создаем файл item-status-filter, в котором создаем компонент itemstatusfilter, который представляет собой фильтр для статуса элементов списка


шаг 14: Изменение структуры проекта
Создаем css файлы для app-header, item-status-filter, search-panel, index.css
дополняем файл todo-list-item css
меняем файл app-header.js. теперь он выводит todo list и more to do, а компонент appheader имеет 2 параметра, todo и done
в файле serch panel.js  меняем косметически импут
в файле todo-list-item.js меняем span на более сложный span с вложенным span и кнопками
делаем более сложную структуру в index.js в компоненте app



шаг 15: Восстановление структуры проекта html bootstrap links
переделали index.html, косметически в основном



шаг 16: Создание и структурирование папок для проекта и создание компонента приложения
меняем расположение файла на правильный

шаг 17: Редактирование каталогов проектов
для каждого компонента создаем отдельную папку в папке компонентс
для каждой из созданных папок создается файл index.js в котором сначала импортируем компонент а затем экспортируем его же
из index.js основного, мы удаляем весь код и затем импортируем компонент app
перенос из index.js в app.js компонент app и экспорт его 

шаг 18: Использовать компонент с отслеживанием состояния
определяем классовый компонент itemstatusfilter, который наследует функциональность от базового класса component
метод render является обязательным методом для классовых компонентов

извлекаем значения label и important из this.props 

шаг 19: Использовать конструктор
constructor(): Конструктор - это метод, который вызывается при создании экземпляра класса, в данном случае, при создании экземпляра компонента todolistitemview.

шаг 20: Используйте функцию OnLabelClick со стрелкой
удаляем конструктор и вместо него пишем компонент onlabelclick

шаг 21: Изменяет компонент состояния и использует значение true для done
меняем косметически span, теперь вместо “text” будет {text}
добавляем state в котором будет храниться информация о done:true/false
извлекаем done в State
создаем переменную classNames
проверяем если done = true то добавляем done к classNames


шаг 21: Используется функция onLabelClick для изменения состояния при нажатии на элементы todo-list-item
теперь при наводке будет срабатывать onlbelClick который будет обновлять состояние done на true

шаг 22: Модификации setState()
добавляем в state important:false
добавляем onMarkImportant который будет обновлять состояние Important на true
удаляем переменную style и ее призыв
теперь мы достаем из props только Label, а из State достаем done и important
проверяем если important = true то добавляем к classnames - important

шаг 23: обновить установленное состояние() для событий
функция this.setstate принимает функцию обратного вызова с 1 аргументом
деструктуризация состояния и извлечение значения done
затем с помощью оператора ! оно меняет состояние на обратное то есть true = false и false= true 
с значением important то же самое 

шаг 24: Рефакторинг основных компонентов с помощью функции setState() для событий
в ap.js к jsx элементу todolist добавляем свойство ondelete которая передается todolsit
теперь помимо label мы достаем Ondeleted из props
добавляем в кнопку ondeleted
в todo-list.js добавляем в компонент todolist свойство ondeleted
добавляем свойство ondeleted которая будет вызывать  функцию обратного вызова Ondeleted с идентификатором задачи (id)

шаг 25: удаление элементов устанавливает состояние и функцию DeleteItem.
добавляем deleteitem 
удаляем старую запись компонента и переписываем его другим методом используя классовый компонент который получает весь функционал от component
пишем обязательный render


шаг 26: удаленные элементы и создайте новый объект массива.
удаляем метод slice
создаем новый массив, который будет исключать элементы с индексом idx из исходного массива. для этого используется оператор расширения и сначала берем элементы до idx а потом после .

шаг 27: добавлена кнопка Добавить элемент. Добавляющий элемент
создаем папку item-add-form куда вписываем index.js, item-add-form.css , item-add-form.js
в item-add-form.js добавляем кнопку при нажатии на которую будет создаваться новый айтем с надписью hello world


шаг 28: добавлена кнопка Добавить элемент. Добавление элемента выполняется путем создания нового элемента 
устанавливаем maid = 100
создается новый объект  newitem  с полями label important id
обновляется состояние компонента, новый элемент добавляется в массив tododata используя оператор расширения, в результате создается новый массив.

шаг 29: Данные в приложении React
добавляем функции ontoggleimportant и ontoggledone, каждая их которых просто выводит в консоль информацию о событии а также айди
в компонент todolist добаляем эти функции.

шаг 30: Данные в приложении React и код очистки отходов
в тудулистайтем.дж удаляются state, onlabelclick, onmarkimportant

шаг 31: Редактирование элементов
хардкодированный элементы в тудудата меняем на this…..
добавляем метод createTodoItem который принимает  текст и возвращает уже с полями которые там определены
добавляем метод toggleproperty который переключает указанное свойство элемента с заданным идентификатором в массиве
добавляем метод 	ontoggledone который выводит в консоль toggle done и изменяет состояние задач
метод  Ontoggleimportante изменяет состояние переключая на импортант


шаг 32: Работа с формой добавить новый элемент с типом новый элемент списка
меняем css в item-add-form
при вводе текста в поле формы (input), вызывается метод onLabelChange, который обновляет состояние компонента
При отправке формы вызывается метод onSubmit

шаг 33: Управляемый компонент
добавили this.setstate который должен сбрасывать текст который ввели

шаг 34: Реализация поискового компонента
добавили onSearchChange метод который обновляет состояние компонента, устанавливая новое значение term, переданное в метод.
добавили search метод который принимает массив items и строку term.
Если term пуст, возвращает исходный массив items.
В другом случае фильтрует массив items, оставляя только те элементы, у которых значение поля label содержит подстроку, соответствующую term
добавили метод onSearchChange который обновляет состояние компонента при изменении значения текстового поля
Также вызывает функцию onSearchChange, переданную через свойства компонента, и передает ей текущее значение term.

шаг 35: Реализация компонента фильтра
метод onfilterchange обновляет состояние компонента, устанавливая новое значение для фильтра.
метод filter фильтрует массив объектов items в зависимости от значения фильтра и возвращается новый массив, содержащий элементы, соответствующие выбранному фильтру
создается массив объектов buttons, представляющих собой различные варианты фильтрации
код создает массив кнопок на основе заранее определенных фильтров. Каждая кнопка имеет стиль в зависимости от того, является ли она активной. При клике на кнопку вызывается функция, переданная через свойства компонента, для изменения фильтраци



