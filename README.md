# 1. Что такое React?

Это билблиотека JavaScript c открытым исходным кодом, созданная facebook для
разработки сложных интерактивных пользовательских интерфейсов в веб и мобильных
приложениях. Основаная цель React - создание компонентов пользовательского интефейса,
их часто называют "V" ("View") в архитектуре "MVC". Прогандирует конпонентный подход

## 2. Что такое Виртуальная DOM?

Виртуальны DOM является претавлением реального DOM в памяти. React создает структуры
данных в памятиб вычисляет результирующие различия и затем эффективно обновляет
отображаему DOM браузера. Это позволяет программисту писать код, как будто вся страница
отображается при каждом изменении, в то же время как библиотека React отображает только
те компонеты, которые действительно изменяются. Очень крутая оптимизация.

## 3. В чем разница между состоянием и свойством?

И своства и состояния являются простыми объектами JS. Хотя обо они содержат информацию,
которая влияет на результаты рендеринга, они различаются по отношению к компонету:

- Свойство аналогично параметрам функции;

- Состояние управляется внутри компонета аналогично переменным, объявленным внутри функции

## 4. Какие существуют фазы жизненного цикла компонентов React?

Существует 4 различных  этапа жизненного цикла компанента React:

- Иницализация. На этом этапе компонет React готовит установку начального состояния и
  параметров по умолчанию

- Монтирование. Компонет React готов для монтировани в DOM браузера. Этот этап охватывает
  методы жизненного цикла componentWillMount =>renderM<= componentDidMount 

- Обновление. На этом этапе компоненты обновляются двумя способами, отправляя новые свойства и
  обновляя состояния. Этот этап охватывает методы жизненного цикла shouldcomponentUpdate
  componentWillUpdate, componentDidUpdate

- Размантирование. На последнем этапе компонент не нужен и отключается из DOM браузера.
  Этот включает метод жизненного цикла componentDidUnmount

## 5. Как работает React?

React запускает виртуальны DOM. Когда состояние изменяется в копонете, он сначала запускает
алгоритм различий, который определяет, что изменилось в виртуальном DOM. Вторым этапом
является согласование, при котором обновляется DOM с рузультами сравнения отличий.

## 6. Что такое JSX?

JSX является расширением синтексиса JavaScript и поставляется с полной функциональностью
JS. JSX производит элементы React. Вы можете встроить любое выражем JS в JSX, заключив его в
круглые скобки. После компиляции выражения JSX становяться обычными объектами JavaScript. Это
означает, что вы можете использовать JSX внутри операторов if и циклов for, назначать его
переменным, принимать его в качестве аргументов и возвращать из функции.

## 7. Что такое потомки?

В выражениях JSX, которые содержать закрывающие и открывающие теги, содежимое между тегами
передается в компонеты автоматически в качестве специального свойства {props.children}. В React
API есть несколько методов для работы с этими объектом. К ним относяться React.Сhildren.map,
React.children.forEach, React.children.count, React.children.only, React.children.toAray

## 8. Что такое состояние в React?

Состояние похоже на свойства, но оно является частным и полностью компонентом. State = это обязательно объект, который содержит данные и определяет, как компонет отображается и ведет себя

## 9. Что такое контролируемые компоненты?

В HTML элементы формы, такие как input, textarea и select, как правило поддерживают свое собственное состояние и обновляют его на основе пользовательского ввода. Когда пользователь отправляет форму, значение из этих элементов, значение из этих элементов, упомянутых выше отправляются вместе с формой. В React это работает по другому. Компонент, содержащий форму, будет отслеживать значение ввода в своем состоянии и повторно визуализировать компонент каждый раз, когда вызывается функция обратного вызова onChange, например, при обнавлении состояния. Элементы ввода формы, значение которого контролирует React, называются контролируемыми компонентами.

## 10.Что такое Flux?

Flux - это парадигма разработки приложения, используемая в качестве замены более традиционного шаблона MVC. Это не фреймворк или библиотека, а новый тип архитектуры, который дополняет React и концепцию однонаправленного потока данных. Facebook использовал этот шаблон при работе над React для создания рабочего процесса между компонентами диспатчера, хранилища и представлениями с различными входами и выходами следующим образом.

## 11.Что такое Redux?

React  по своей сути инструмент для визуализации. Redux - это библиотека, которая позволяет работать с потоком данных отдельно от приложения. И с помощью react-redux мы связываем модель данных и отображение. Один объект для состояния всего приложения. Redux - это контейнер с предсказуемым состоянием для JS, основанный на шаблоне проектирования Flux.Redux может использоваться вместе с ReactJS или любой другой библиотекой представлений. Он очень компактный (около 2КБ) и не имеет никаких зависимостей.

## 12.Как изменяется состояние в Redux?

Единственный способ изменить состояние - это создать действие,объект, описывающий произошедшее. Это гарантирует, что ни представления, ни сетевые обратные вызовы никогда не будут выполнять запись напрямую в состояние. Поскольку все изменения централизованы и происходят одно за другим в строгом порядке, не существует существенных условий конкуренции. Поскольку действия просто обычными объектам, их можно регистрировать, сериализироват, хранить и затем вопспроизводить для целей отладки и тестирования.

## 13.Что такое «store» в Redux?

Хранилище - это объект, которое хранит состояние приложения и предоставляет несколько спомогательных методов для доступа к состоянию, отправки действий и регистрации прослушивателей( getState - изменять состояние) Все состояние представлено одним хранилище. Любое действие возвращает новое состояние через редукторы. Это делает Redux очень простым и предсказуемым.

## 14. Что такое чистая функция?

В компьютерном программировании чистая функция = это функция, котораяимеет следующие свойства:

- Ее возвращаемое значение одинаково для тех же аргументов(без изменений с локальными статическими переменными, нелокальными переменными, изменяемыми ссылочными аргументами или входными потоками с устройств ввода-вывода)

- ее оценка не имеет побочных эффектов( нет мутации локльных статических переменных, нелокальных переменных, изменяемых ссылочных аргументов или потоков ввода-вывода). Таким образом, чистая функция вычисляется аналогично математической функции.

## 15.Как бы вы отключили хранилище Redux, чтобы оно не принимало никаких изменений в состоянии?

Один из способов сделать это - установить для флага exit в редукторе корневого состояния значение true, просто оставляя состояние неизменным

## 16.Почему Мы Должны Использовать ReactJS?

- Virtual DOM вместо реального DOM

- Быстротa и масштабируемость

- JSX предоставляет код, который легко читать и писать

- React JS это библиотека, которая легко интегрируется с другими JavaScript фреймворками

- Легко писать юнит тесты

## 17. Может Ли Веб-Браузеры Читать JSX?

Нет, не могут. Для преобразования необходима использовать конвектор

## 18. В Чём Различие Между React JS и React Native?

- самостоятельная платформа

- не используется html разметка, а используются компоненеты

- готовый bangle собирает сервер.

- более грамоздкие приложения

- ограниченный функционал

## 19.Какие есть ограничения в React?

- Это библиотека (часть решений он не поддерживает из коробки)

- Требуется время на освоение

- Не самая простая архитектура и инфраструктура

## 20.Что такое Props(свойства)?

Существуют для передачи свойст от родителя к дочернему элементу и рендеринга компонента

## 21. Что такое state и как он используется?

Это объект, который содержит определенные состояния, он является мутабельным. И отрисовывает интерфейс

```javascript
 constructor(props) {
super(props)

    this.state = {
        isOpen: false,
        youtubeChannel: 'EvgenPrushak'
    }

}
```

## 21. Что такое state и как он Ref?

Это означает в переводе с ангийского, что мы можем создавать ссылки на DOM элемент. Данный функционал нам нужен для создания фокуса на элемент, когда мы хотим выделить текст, когда мы хотим взаимодействовать с анимацией или взаимодействие со сторонними библиотеками(как вариант взаимодействие с DOM)

```javascript
class Mycomponent extends React.Component {
  constructor(props) {
    super(props);
    this.input = React.createRef();
  }

  render() {
    return <input type="text" ref={this.inputRef} />;
  }

  componentDidMount() {
    this.inputRef.current.focus();
  }
}
```

## 22. Что такое JEST?

Предназначен для юнит тестирования. Разработчиком JEST является компания Facebook и основан на фреймворке JASMIN.

## 23. Когда стоит использовать классовые компоненты, а когда функциональные?

Если у Вас компонент используется для отрисовки интерфейса, то его следует делать функциональным (т.к. он потребляет меньше ресурсов). Но если у Вас компонент со сложным доступом ( например жизненные этапы компанентов), то его стоит сделать классовым.

## 24. Что происходит, когда вы вызываете setState?

В первую очередь React получает тот объект, которые мы передаем в функцию setState и соединяет его(merge) со стейтом, который был. Как результат мы болучаем новый стейт, на основе которого React создает новый виртуальный DOM. Затем идет сравнение виртуального и реального DOM. Найдя различия, он изменяет только места, где есть различия. Одним словом setState позволяет максимально эффективно взаимодействоавть с интерфейсом.

## 25. В чем разница между state и props?

state - это структура данных, который имеет начальные значения и для отрисовки React использует начальное значение state. state может менять и как правило это происходит из-за пользовательских действий. props - это параметры, которые поступают в компанент (от родителя). Эти параметры не изменяемые, однонаправленное состояние, которое передается по древавидной структуре.

## 26. Когда стоит делать асинхронные запросы на сервер?

- componentDidMount(). Если ответ с сервера придет до того, как html готов, то могут произойти ошибки

## 27. В чем смысл специального атрибута key?

Позволяет менеджерить состояние каждого элемента. И задаем уникальное значение. И при удалении удалить только один элемент из списка, а не будет работ со всем списком. Index - не рекомендуется использовать в качесте key.

```javascript
 const todoItmes = todos.map(todo) =>
<li key={todo.id}> {todo.text}</li>
```

## 28. Что значит компонент mounted?

Это значит, что наш компонент вмонтирован в DOM дерево (html) и компонент готов к работе

## 29. Назовите разницу между контролируемыми и не контролируемыми компонентамии?

Контролируемый компонет, это компонет в котором есть state, за которым мы следим. (например input)
На каждое измение инпута мы вызываем функцию setState или используем hook. В неконтролиремом компоненте так же есть state, но мы его необрабатывает (контролирем). Например textarea

## 30. Что такое фрагменты ?

Бывают силуации, когда нам неоюходимо отрендерить text и мы не хотим, чтобы у данного шаблона был корневой элемент. И по сути не создается родительский элемент, тем самым облегчается html. Второй вариант создания фрагмента <></>. При создании родительского элемента через фрагмент, он будет пустым

```javascript
render() {
    return(
        <React.Fragment>
        Some text
        <h2>A heading</h2>
        </React.Fragment>
    )
}

```

## 31. Как реакт обрабатывает пользовательские события?

Для того, чтобы оптимировать работу React добавляет одно событие для корневого элемента(хотя в приложении может быть много кликов). Когда иы получаем объект событие (event). React нам предлагает свой специальный class SyntheticEvent. Который представляет собой обертку, которая позволяет работать в старых браузерах. В результате мы получаем общий API,который можем использовать.

## 32. В компонент setState можно передавать объект или функцию. В чем разница и что лучше использовать?

По умолчанию передается объект. Но мы может передавать и функцию, которая принимает в себя предыдущее состостояние мы формируем новое состояние. Дело в том, что props и state в React работают асинхронно. И когда в метод setState Вы передаете объект, то это не гарантрует Вам, что Вы будете работать с предыдущим состоянием. Вот по этой причине для работы с предыдущим состоянием мы будем передвать функцию.

## 33. В чем разница между презентационным компонентом и контейнер компонентом?

По сути презентационные компонты - это компоненты, которые говорят нам, как должно все выглядеть и на основании props рисуют нам интерфейс. Контейнер компонеты говорят нам, как все должно работать и взаимодействовать. В них содержится информацию по state, поведению и обычно он раздает различне свойства.

## 34. Что такое Context?

Специальный метод,  в которым мы передаем начальные состояние и в итоги мы получаем специальный объект context. И дальше мы можем использовать объект context не совсем по обычному при этом мы можем использовать или Provider или Consumer. В React может быть большая вложенность и для передачи на некоторый уровень вложенности использует context. Через контекст мы можем передвать состояния, функции на нужный нам уровень вложенности.

```javascript
const Mycontext = React.createContext(defaultValue);
<Mycontext.Provider value={/* some value */}> 
<Mycontext.Consumer>
{value => /* render something based on the context value*/}
</Mycontext.Consumer>
```

## 35. Что такое Higher-Order компоненты?

Это такие конструкции, которые как input принимают component и добавляют к нему какой-то функционал(возможности) и на выходе мы получает новый компонент с расширенными возможностями




## 36. Что делает shoudComponentUpdate и почему он важен?

Данный метод служит для оптимизациии render  React. И он отвечает на вопрос: Нужен ли нам процесс render сейчас или его можно избежать. По результаты мы получать значение try or false. Если false= то рендеринг не будет происходить. Например нам приходит state и он не влияет на отображение, то мы просим React не делать перерендеринг. В React присутствует class pure component, который реализует shoudComponentUpdate или если мы используем функциональные компонты, то react memo.

## 37. Что делает shoudComponentUpdate и почему он важен?

JavaScript объект, в котором содержится состояние приложения. Дополнительно
отвечает за следующее:

- state может быть получен через getState()

- Изменять state можно через dispatch(action)

- Регистрировать изменения через subscribe(listener)

## 38. Что нельзя делать в методе render?

Нельзя изменять состояние компонента (например вызывать setState). Должен быть
чистой (pure) функцией

## 39. Что такое action в Redux?

Объект, который обязательно должен содержать ключ type. С помощью него Redux
понимает, что именно нужно сделать со стейтом

## 40. Какие типы middleware есть в redux для работы с асинхронностью?

- Redux Thunk
- Redux Promise
- Redux Saga

## 41. Что такое Pure Components?

Тоже самое, что и Component, кроме того, что автоматически за вас реализует метод
shouldComponentUpdate.

## 42. Почему не стоит изменять state напрямую?

Не будет запущен процесс ре-рендеринга и интерфейс не поменяется. Корректно
использовать метод setState().

## 43.  Как изменить state используя динамический ключ?

```javascript
inutChangeHandler(event) {
    this.setState({
        [event.target.name]: event.target.value;
    })
}
```

## 44. Что такое Error Boundaries в React?

React - компонент, позволяющий обрабатывать ошибки в дочерних компонентах. Для
это присутствует метод componentDidCatch(error, info)

## 45.  Что такое React Hooks?

Функционал, добавленный в React 16.8. С помощью хуков, можно писать приложения,
используя только функциональные компоненты, без классов.
С помощью хуков можно следить за стейтом, эмулировать жизненные этапы
компонента, работа с ссылками и многое другое

## 46.   В чем разница между useRef и createRef?

- createRef - всегда создает новую ссылку. Используется в class компонентах
- useRef - возвращает одинаковую ссылку на объект, которое были при
начальном рендеринге

## 47.   Что такое useState?

Встроенные React хук. Позволяет работать со стейтом в функциональных
компонентах. Принимает начальное значение. Возвращает массив, состоящий всегда
из 2х элементов (кортеж), где:
● первый элемент - само состояние
● второй элемент - функция, меняющая состояние

## 48.   Что такое prop drilling и как этого избежать?

Передача свойств на прямую от родителя к ребенку через сложную и длинную
иерархию компонентов.
Избежать можно используя Context или например Redux (Flux)

## 49.    Как валидировать props в React?

Для этого есть дополнительная библиотека - PropTypes

## 50.   Зачем делать eject?

На случай, если необходимо модифицировать конфигурацию проекта (webpack, babel)

## 51.   Разница между Flux и MVC?

MVC (model view controller) - парадигма, разделяющая отображение и данные, однако
присутствуют следующие минусы:
● каскадная модель данных, сложно отслеживать состояние
● данные могут быть изменены где угодно. Как следствие непредсказуемое
поведение UI
Flux позволяет решить проблему каскадной модели данных. Данные получаются из
отдельного store и менять напрямую их нельзя.

## 52.   Что не так с этим кодом?

```javascript
this.setState((prevState, props) =>{
  return {
    counter: PrevState.counter + props.counter
  }
}
```

С этим кодом все хорошо. Изменяем state на основе прошлого состояния и входящих
параметров

## 53.  Какой второй опциональный параметр можно передать в метод setState и за что он отвечает?

Функция, уведомляющая, что компонент закончил процесс ре-рендеринга

## 54.  Что такое mapStateToProps и mapDispatchToProps?

Функции в Redux, позволяющие приводить к более удобному формату данные из store
в компонент

## 55.   Что такое React Fiber?

Fiber - это новый механизм и базовый алгоритм для рендеринга в React 16. Основная
цель - реализовать пошаговый рендеринг виртуального DOM для более быстрого
рендеринга, работы с анимациями и дебагом

## 56.   Разница между Flow и PropTypes?

● Flow - статический инструмент для проверки типов. Использует аннотации и
позволяет найти ошибки при компиляции (аналог TypeScript)
● PropTypes - проверяет типы входящих параметров в runtime

## 57.   Правда ли, что React делает ре-рендер всех компонентов и дочерних компонентов каждый раз когда вызывается setState?

По умолчанию - да. Однако мы этим можем управлять в
shouldComponentUpdate(nextProps, nextState)

## 58.   Как можно улучшить производительность React Redux приложения?

По умолчанию - да. Однако мы этим можем управлять в
shouldComponentUpdate(nextProps, nextState)

Избавиться от лишних рендеров (самой затратной операции).
Для этого можно использовать:

1. shouldComponentUpdate в класс компонентах
2. PureComponent для класс компонентов
3. React.memo() - для функциональных компонентов

## 59.   Зачем нужен Redux Thunk?

Middleware позволяющая изменять состояние приложения в Redux в асинхронном
режиме

## 60.   В чем ключевое отличие между React и Angular?

React - библиотека для отрисовки приложения. Для другого функционала нужны
другие решения (например для данных - Redux)
Angular - обширный фреймворк, где все решения есть в ядре (в коробке)
● Используя React - можно более гибко создавать приложения и более точечно
управлять его частями
● Используя Angular - проще разрабатывать и поддерживать приложения

## 61.   Перечислите некоторые ситуации, в которых следует использовать ссылки?

Ниже приведены ситуации, в которых следует использовать ссылки:

Необходимо управлять фокусом, выбирать текст или воспроизведение мультимедиа
Запускаемая анимация
интегрировать со сторонними библиотеками DOM

### JavaScript

## 62 .   Типы данных в JavaScript?

1. 7  Примитивных типов данных: Boolean, string, number, , bigInt, sumbol,null, undefined.
2. Не приммитивный тип данных: Object.

## 63 .   Типы данных в JavaScript?

1. 7  Примитивных типов данных: Boolean, string, number, , bigInt, sumbol,null, undefined.
2. Не приммитивный тип данных: Object.

## 64 .   Приведение типов в JavaScript?
console.log(1+'2'); // string 12
console.log("+1+0) //1
console.log("-1+0) //-1
console.log('3'*'8') //24
console.log(4+10 +'px') //14px
console.log('px'+ 5+10 +) //px510
console.log('42'- 40 +) //2
console.log('42px'- 2 ) //NaN
console.log(null + 2) //2
console.log(undefined+ 41) //NaN  т.к. undefined  не приводиться к числу

 // == vs ===  (== сравнивает по значению с приведения типов, === без приведения типов)
console.log(2 == '2'); // true
console.log(2 === '2'); // false
console.log(undefined == null); // true
console.log(undefined === null); // false
console.log('0' == false); // true
console.log('0' == 0); // true
console.log('0' === 0); // false
console.log('0' === false); // false

// Неодназначные сравнения
https://dorey.github.io/JavaScript-Equality-Table/
console.log(false == ''); // true
console.log(false == []); // true
console.log(false == {}); // false т.к  объект приводиться к строке 'object object'
console.log('' == 0); // true
console.log('' == []); // true
console.log('' == {}); // false
console.log(0 == null) //false

## 64 .   Отсортировать массив чисел?
const array= [1,25, 55,77, -5,108]
array.sort((a,b)=> {return a -b}));


## 64 .   Перебирающие методы массива?
1. Map -  возвращает новый массив не изменяя исходный,  выполняя действия над  каждым элементом массива
2. filter
3. .forEach
4. .reduce
Arrray.prototype.myMap = function(callback){
const result=[]
const theisArray = this
for(let i= 0; i< theisArray.length; i++){
result.push(callback(theisArray[i], i, theisArray))

}
return result
}
## 65 .   Управляемые и не управляемые компоненты?

 const [state, setState]= useState()
 const input2 =useRef();
 const click =() =>{
 console.log(state)
 console.log(input2.current.values)
 }
 return(
 <div>
 <input onchange={(event)=> setState(event.target.value))  placeholder='Управляемый'/>
   <input ref={input2}  placeholder='Не управляемый'/>
  <button onClick={click}>Get Value </button>
   </div>
 )
 
 ## 65 .   Что ввела ЕS6?
 
1. Введены let  и const
2. Объект можно делать const.
3. Диструктуризаци объекта или массива.
4. Итераторы  for of   для перебора элементов массива.
5. Итераторы  for of   для перебора и разбиение строки по символьно.
6. ``  для переноса строк.
7. В функцию можно передавать значение по умаолчанию
8. Диструктуризация в функциях
9. Стрелочные функции.
10. Мультилайн  string \n.
11. Наследование с помощью   super и extends.

 ## 66 .   Что ввела ЕS7?
 
1. Array.includes() - содержит ли массив значение  или массив значений.
2. Math.pow() - оператор возведения в степень

 ## 67.   Что ввела ЕS8?
 1. String — padStart() и padEnd()
   ```javascript
const str = 'test'.padStart(10)
const str1 = 'test'.padEnd(10,'*')

console.log(`'${str}'`) //'      test'
console.log(`'${str1}'`) //'test******'
```
 3. Object.values() 
  ```javascript
const person = { name: 'Fred', age: 87 }
const personValues = Object.values(person) 
console.log(personValues) // ['Fred', 87]
```
 4. Метод Object.entries() 
 ```javascript
const person = { name: 'Fred', age: 87 }
const personValues = Object.entries(person) 
console.log(personValues) // [['name', 'Fred'], ['age', 87]]
```
 5.Object.getOwnPropertyDescriptors(obj) -он принимает объект, сведения о свойствах которого нужно узнать, и возвращает объект, содержащий эти сведения.
Один из вариантов сделать копию объекта и копирует геттеры и сеттеры в отличиие Object.assign()
```javascript
const person = { name: 'Fred', age: 87 }
const propDescr = Object.getOwnPropertyDescriptors(person)
console.log(propDescr) 
/*
{ name:
   { value: 'Fred',
     writable: true,
     enumerable: true,
     configurable: true },
  age:
   { value: 87,
     writable: true,
     enumerable: true,
     configurable: true } }
```
6. Завершающие запятые в параметрах функций
7. Асинхронные функции 
В стандарте ES2017 появилась конструкция async/await, которую можно считать важнейшим новшеством этой версии языка.

Асинхронные функции представляют собой комбинацию промисов и генераторов, они упрощают конструкции, для описания которых раньше требовался большой объём шаблонного кода и неудобные в работе цепочки промисов. Фактически, речь идёт о высокоуровневой абстракции над промисами.

Когда в стандарте ES2015 появились промисы, они призваны были решить существующие проблемы с асинхронным кодом, что они и сделали. Но за те два года, которые разделяют стандарты ES2015 и ES2017, стало ясно, что промисы нельзя считать окончательным решением этих проблем.

В частности, промисы были нацелены на решение проблемы «ада коллбэков», но, решив эту проблему, они сами показали себя не с лучшей стороны из-за усложнения кода, в котором они используются. Собственно говоря, конструкция async/await решает проблему промисов и повышает удобство работы с асинхронным кодом.
```javascript
function doSomethingAsync() {
  return new Promise((resolve) => {
      setTimeout(() => resolve('I did something'), 3000)
  })
}
async function doSomething() {
  console.log(await doSomethingAsync())
}
console.log('Before')
doSomething()
console.log('After')
```
Как видно, после вызова doSomething() программа продолжает выполняться, после Before в консоль тут же выводится After, а после того, как пройдут три секунды, выводится I did something.

8. Последовательный вызов асинхронных функций
При необходимости асинхронные функции могут формировать нечто вроде цепочек вызовов. Такие конструкции отличаются лучшей читабельностью, чем нечто подобное, основанное исключительно на промисах. Это можно видеть на следующем примере.
```javascript
function promiseToDoSomething() {
  return new Promise((resolve)=>{
      setTimeout(() => resolve('I did something'), 10000)
  })
}
async function watchOverSomeoneDoingSomething() {
  const something = await promiseToDoSomething()
  return something + ' and I watched'
Здесь речь идёт об объекте SharedArrayBuffer, который позволяет описывать разделяемые области памяти, и об объекте Atomics, который содержит набор атомарных операций в виде статических методов. Подробности о возможностях, которые дают программисту эти объекты, можно почитать здесь.
async function watchOverSomeoneWatchingSomeoneDoingSomething() {
  const something = await watchOverSomeoneDoingSomething()
  return something + ' and I watched as well'
}
watchOverSomeoneWatchingSomeoneDoingSomething().then((res) => {
  console.log(res) // I did something and I watched and I watched as well
})
```

9. Разделяемая память и атомарные операции
Здесь речь идёт об объекте SharedArrayBuffer, который позволяет описывать разделяемые области памяти, и об объекте Atomics, который содержит набор атомарных операций в виде статических методов. Подробности о возможностях, которые дают программисту эти объекты, можно почитать здесь.


 ## 68.   Что ввела то ввела ЕS9?
 1. Применение операторов spread и rest к объектам
 Мы уже говорили об операторах rest и spread, которые появились в ES6 и могут быть использованы для работы с массивами. Оба они выглядят как три точки. Оператор rest, в следующем примере деструктурирования массива, позволяет поместить его первый и второй элементы в константы first и second, а все остальные — в константу others.
 ```javascript
const numbers = [1, 2, 3, 4, 5]
const [first, second, ...others] = numbers
console.log(first) //1
console.log(second) //2
console.log(others) //[ 3, 4, 5 ]
```
Оператор spread позволяет передавать массивы в функции, ожидающие обычные списки параметров.
 ```javascript
const numbers = [1, 2, 3, 4, 5]
const sum = (a, b, c, d, e) => a + b + c + d + e
const res = sum(...numbers)
console.log(res) //15
```
Теперь, используя тот же подход, можно работать и с объектами. Вот пример использования оператора rest в операции деструктурирующего присваивания.
 ```javascript
const { first, second, ...others } = 
  { first: 1, second: 2, third: 3, fourth: 4, fifth: 5 }
console.log(first) //1
console.log(second) //2
console.log(others) //{ third: 3, fourth: 4, fifth: 5 }
```
Вот оператор spread, применяемый при создании нового объекта на основе существующего. Этот пример продолжает предыдущий.
 ```javascript
const items = { first, second, ...others }
console.log(items) //{ first: 1, second: 2, third: 3, fourth: 4, fifth: 5 }
```

2.Асинхронные итераторы

Новая конструкция for-await-of позволяет вызывать асинхронные функции, возвращающие промисы, в циклах. Такие циклы ожидают разрешения промиса перед переходом к следующему шагу. Вот как это выглядит.
 ```javascript
for await (const line of readLines(filePath)) {
  console.log(line)
}
```
3. Метод Promise.prototype.finally()
Если промис успешно разрешается — осуществляется вызов очередного метода then(). Если что-то идёт не так — вызывается метод catch(). Метод finally() позволяет выполнять некий код независимо от того, что происходило до этого.
 ```javascript
fetch('file.json')
  .then(data => data.json())
  .catch(error => console.error(error))
  .finally(() => console.log('finished'))
```
4. Улучшения регулярных выражений
В регулярных выражениях появилась возможность ретроспективной проверки строк (?<=). Это позволяет искать в строках некие конструкции, перед которыми есть какие-то другие конструкции.

Возможность опережающих проверок, использующая конструкцию ?=, имелась в регулярных выражениях, реализованных в JavaScript, и до стандарта ES2018. Такие проверки позволяют узнать, следует ли за неким фрагментом строки другой фрагмент.
 ```javascript
const r = /Roger(?= Waters)/
const res1 = r.test('Roger is my dog')
const res2 = r.test('Roger is my dog and Roger Waters is a famous musician')
console.log(res1) //false
console.log(res2) //true
```
Конструкция ?! выполняет обратную операцию — совпадение будет найдено только в том случае, если за заданной строкой не идёт другая строка.
 ```javascript
const r = /Roger(?! Waters)/g
const res1 = r.test('Roger is my dog')
const res2 = r.test('Roger is my dog and Roger Waters is a famous musician')
console.log(res1) //true
console.log(res2) //false
```
При ретроспективной проверке, как уже было сказано, используется конструкция ?<=.
 ```javascript
const r = /(?<=Roger) Waters/
const res1 = r.test('Pink Waters is my dog')
const res2 = r.test('Roger is my dog and Roger Waters is a famous musician')
console.log(res1) //false
console.log(res2) //true
```
Операцию, обратную описанной, можно выполнить с помощью конструкции ?<!.
 ```javascript
const r = /(?<!Roger) Waters/
const res1 = r.test('Pink Waters is my dog')
const res2 = r.test('Roger is my dog and Roger Waters is a famous musician')
console.log(res1) //true
console.log(res2) //false
```
Управляющие последовательности Unicode в регулярных выражениях
В регулярных выражениях можно использовать класс \d, соответствующий любой цифре, класс \s, соответствующий любому пробельному символу, класс \w, который соответствует любому буквенно-цифровому символу, и так далее. Возможность, о которой идёт речь, расширяет набор классов, которыми можно пользоваться в регулярных выражениях, позволяя работать с Unicode-последовательностями. Речь идёт о классе \p{} и об обратном ему классе \P{}.

В Unicode каждый символ имеет набор свойств. Эти свойства указываются в фигурных скобках группы \p{}. Так, например, свойство Script определяет семейство языков, к которому принадлежит символ, свойство ASCII, логическое, принимает значение true для ASCII-символов, и так далее. Например, выясним, содержат ли некие строки исключительно ASCII-символы.
 ## 68.   Что ввела то ввела ЕS10?
 1. Array.flat() и Array.flatMap()
 Метод Array.flat() возвращает новый массив, в котором все элементы вложенных подмассивов были рекурсивно подняты на указанный уровень depth.
Метод Array.flatMap() сначала применяет функцию к каждому элементу, а затем преобразует полученный результат в плоскую структуру и помещает в новый массив. Это идентично функции map() с последующим применением функции flat() с параметром depth, равным 1, но flatMap() чаще более эффективен, поскольку совмещает в себе оба подхода в одном методе.

2. String.trimStart() & String.trimEnd()
могут быть использованы для обрезки пробелов в начале или в конце строки.
 ```javascript
const greeting = "    Hello everyone";
console.log(greeting.trimStart());
// "Hello everyone"
```
 ```javascript
const greeting = "Hello world    ";
console.log(greeting.trimEnd());
// "Hello world"
```
3. Необязательная привязка catch
 ```javascript
try {
  // some code
} catch {
  // error handling code
}
```
4. Object.fromEntries()
Object.fromEntries() создает объект или преобразует пары ключ-значение в объект. Он принимает только итерации: Object.fromEntries(someIterable).
 ```javascript
const students = new Map([
  ["name", "john"],
  ["age", 22],
]);

console.log(Object.fromEntries(students));
// { name: 'john', age: 22 }

const students = [
  ["john", 22],
  ["alex", 22],
  ["julia", 21],
  ["alex", 20],
];

Сценарий, который приводит к потери данных:

const studentObj = Object.fromEntries(students);
// { john: 22, alex: 20, julia: 21 }
// первый alex был перезаписан
```
5. Symbol.description
Свойство description только для чтения - это строка, возвращающая необязательное описание объектов Symbol.
 ```javascript
const mySymbol = `My Symbol`;

const symObj = Symbol(mySymbol);

console.log(symObj); // Symbol(mySymbol);

console.log(String(symObj) === `Symbol(${mySymbol})`); // true

console.log(symObj.description); // "My Symbol"
```
6. Хорошо сформированный JSON.stringify()
Исправленный вывод JSON.stringify() при обработке суррогатных кодовых точек UTF-8 (от U+D800 до U+DFFF).

Перед этим изменением вызов JSON.stringify() возвращал некорректный символ Unicode («�»).

Теперь эти суррогатные кодовые точки можно безопасно представить в виде строк, используя JSON.stringify(), и преобразовать обратно в их исходное представление, используя JSON.parse().
