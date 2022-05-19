## Реализация автокомплита через класс
### при вызове new Autocomplite(params) нужно передать:
#### ajaxOption - параметры для обращение к контроллеру
#### checkSelected - параметр, булеан значение, проверять ли, если пользователь не выбрал элемент из выпадающего списка
#### container - контейнер внутри которого будет происходить обращение по селектору к выпадающему списку и инпуту, для возможности вызвать класс на одной странице несколько раз и не словить конфликт
#### formatter - коллбек функция, определяет формат в каком виде отобразить элементы выпадающего списка, если параметр не передается, используется значение по умолчанию пример вызова 
formatter: (elem) => {
  return `<span class="autocomplete_item" data-code="${elem.code}">${elem.name}</span>`;
}
#### onSelect - слушатель событий, передается коллбек функция, которая описывает действие при выборе элемента из выпадающего списка
#### onChange - слушатель событий, передается коллбек функция, которая описывает действие при снятии фокуса с инпута, если элемент из выпадающего списка не был выбран, нужно что бы значение checkSelected стояло в true
