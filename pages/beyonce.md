# Beyonce

## Компоненты

### Кнопки / Buttons

Для использования стандартной синей кнопки достаточно добавить класс **.button**;
Отталкиваясь от базового класса мы можем модифицировать кнопку, добавляя ей новые классы, описанные ниже.

Модификатор **disabled** может быть добавлен аттрибутом, либо классом **.disabled** - результат одинаковый.

**Шрифт** регулируется классами **font-normal** и **font-bold**.

```html
  <button class="button">Button default</button>
  <button class="button" disabled>Button disabled</button>

  <button class="button button-white">Button white</button>
  <button class="button button-white" disabled>Button disabled</button>

  <button class="button button-small">Button small</button>
  <button class="button button-white button-small">Button white and small</button>

  <button class="button button-extra-small">Update</button>
  <button class="button button-white button-extra-small">Save</button>
```

<buttons />

<br>

### Кнопка-ссылка / button link

**Кнопка, похожая на ссылку**.
В проекте встречается тип кнопки, который выглядит как ссылка, но является кнопкой согласно правилу [разметка для тестов](http://localhost:8080/pages/rules.html#%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%82%D0%BA%D0%B0-%D0%B4n%D1%8F-%D1%82%D0%B5%D1%81%D1%82%D0%BE%D0%B2).
Такой вид кнопки используется, например, для загрузки документа, либо для любого события, которое не сопровождается переходом на другую страницу, но запускает какое-то действие на странице.

```html
<button class="button-link">Email confirmation.pdf</button>
<button class="button-link disabled">Email confirmation.pdf</button> <!-- disabled класс или аттрибут -->

<div class="button-link-group"> <!-- этот класс обязательный -->
  <button class="button-link">
    <span class="icon icon-add" />
    <span class="text">Add new item</span>
  </button>
  <button class="button-link">
    <span class="icon icon-delete" />
    <span class="text">Delete item</span>
  </button>
</div>
```
<button-link />

<br>

### Ссылки / links

Ссылки есть двух типов:
- которые отправляют на другую страницу, т.е. меняют url адрес
- которые открывают окна на текущей странице (popup, popover etc.)

Для каждого типа используется разное нижнее подчеркивание.

```html
<a class="link" href="/path">Ссылка для перехода на другую страницу</a>
<a class="link dashed" href="/path">Ссылка для открытия модальных окон</a>
```
<links />

<br>

### Табы / tabs

#### Пример использования табов верхнего уровня (tfx-tabs-blue)

```html
<div tfx-component="tabs" class="tfx-tabs tfx-tabs-blue">
  <a href="/admin/b/clients/1/status" class="tab tab-link">
    <span class="tab-inner">
      Status/Notes
    </span>
  </a>
  <a href="/admin/b/clients/1/info" class="tab tab-link">
    <span class="tab-inner">
      Info
    </span>
  </a>
</div>
```

<tfx-tabs customClass="tfx-tabs-blue" />

#### Пример использования табов второго уровня (tfx-tabs-sky)

```html
<div tfx-component="tabs" class="tfx-tabs tfx-tabs-sky">
  <a href="/admin/b/clients/1/status" class="tab tab-link">
    <span class="tab-inner">
      Status/Notes
    </span>
  </a>
  <a href="/admin/b/clients/1/info" class="tab tab-link">
    <span class="tab-inner">
      Info
    </span>
  </a>
</div>
```

<tfx-tabs customClass="tfx-tabs-sky" />

<br/>

### Таблица / table

#### Пример использования табов второго уровня (tfx-tabs-sky)

Для использования таблицы достаточно двух обязательных классов

``.tfx-table-wrapper`` - это оболочка, добавляет border-radius для скругления таблицы и минимальный padding в 1 пиксель, что создает эффект рамки вокруг таблицы в 1px;

``.tfx-table`` - основной класс, от которого наследуются все стили для дочерних элементов

Для корректного отображения таблицы придерживайтесь правильный структуры с использованием ``thead>tr>th`` и ``tbody>tr>td``

Также есть возможность вручную задавать ширину для каждого столбца используя аттрибут width в процентах для **th** в шапке таблицы

Все дополнительные модификации ячеек осуществляются с помощью хелперов, таких как:
``font-bold, font-normal, text-left, text-center, text-right`` и т.д (см. [Хелперы](#))

```html
<div class="tfx-table-wrapper">
  <table class="tfx-table">
    <thead>
      <tr>
        <th width="15%">Name</th>
        <th width="30%">Email</th>
        <th width="9%">Country</th>
        <th width="7%">Phone</th>
        <th width="12%">Last Login</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          Mr. Willette Willette Rowe
        </td>
        <td>
          test@taxesforexpats.com (login)<br>
          test@clients.tfx.life
        </td>
        <td>
          Ukraine
        </td>
        <td>
          +79631257200
        </td>
        <td>
          Nov-11-2019
        </td>
      </tr>
    </tbody>
  </table>
</div>
```

<b-table />

<br/>

### Инпут / input

### Селект / селект
