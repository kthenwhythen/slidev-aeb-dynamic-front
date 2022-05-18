---
theme: aeb
layout: title
---

::title::

# (Not) Dynamic Front-end

::description::

Динамический фронт управляемый через LowCode на примере Платформы АЭБ v3

<!--
Всех приветствую
- - -
Думаю у вас могут возникнуть вопросы по поводу терминалогии (Что такое динамический фронт, лоу код и даже платформа АЭБ версии 3). Поэтому для начала проведем краткую вводную
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Platform AEB v3
preload: false
---

<div
  v-motion
  :initial="{opacity: 0, x: 200 }"
  :enter="{opacity: 1, x: 0, transition: {
      delay: 200,
    },
  }">
  <h1>Платформа АЭБ v3</h1>
</div>

<div class="flex h-full items-center pb-10">
  <div>
    <div v-click class="text-2xl">
      <mdi-alert-decagram /> Развитие до версии 3
    </div>
    <div v-click class="text-2xl my-6">
      <mdi-television-guide /> Конфигуратор пользовательского интерфейса
    </div>
    <div v-click class="text-2xl">
      <mdi-cogs /> Конфигуратор системы
    </div>
  </div>
</div>

<!--
Итак основные моменты Платформы АЭБ версии 3
- - -
Развитие до версии 3 подразумевает: сильное изменение составных микросервисов, создание миграции с предыдущей версии, Разбиение монолитного бэка в микросервисы, а так же Интеграцию ProcessManagement
- - -
Конфигуратор пользовательского интерфейса это возможность задавать некоторые настройки отображения данных
- - -
Конфигуратор системы включает в себя разработку инструментов управления системой таких как менеджер платформы (требуется для конфигурации системы с нуля, включается в CI/CD), админка платформы с конфигурацией интерфейса, а так же визульное представление текущего состояния системы. Итак если ничего особо понятнее не стало, то можно сказать, что вся платформа станет сильнее, быстрее, но самое главное гибче.
-->

---
layout: content
title: Low code
preload: false
---

<div
  v-motion
  :initial="{opacity: 0, x: 200 }"
  :enter="{opacity: 1, x: 0, transition: {
      delay: 200,
    },
  }">
  <h1>Low Code</h1>
</div>

<div class="flex h-full items-center pb-10">
  <div>
    <div v-click class="text-2xl">
      <mdi-account-hard-hat /> Меньше разработчиков, больше конструкторов
    </div>
    <div v-click class="text-2xl my-6">
      <mdi-television-guide /> Функционально ядро Low Code систем
    </div>
  </div>
</div>

<!--
Low Code
- - -
Меньше разработчиков, больше конструкторов. Основная концепция строится на полностью конфигурабельной системе, где через различные конструкторы / конфигураторы / дизайнеры можно создать все необходимое для запуска решения
- - -
Функционально ядро Low Code систем. включает в себя Модель данных, UI, Процессы, Интеграции.
Модель данных - создание таблиц данных без разработчиков. UI - конфигурирование отображения данных. Процессы - создание и запуск процессов. Интеграции - интеграционная шина.
Low Code может быть слишком растяжимым понятием.
Меньше кодинга не означает его отсутствие.
Нужно найти золотую середину между просто мало функциональной базовой платформой с абстрактным доменом и специфичной платформой с предопределенным функционалом
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Dynamic front
preload: false
---

<div
  v-motion
  :initial="{opacity: 0, x: 200 }"
  :enter="{opacity: 1, x: 0, transition: {
      delay: 200,
    },
  }">
  <h1>Динамический фронт</h1>
</div>

<div class="flex h-full items-center pb-10">
  <div>
    <div v-click class="text-2xl">
      <mdi-cloud-question /> !static == dynamic
    </div>
    <div v-click class="text-2xl my-6">
      <mdi-database-cog /> Metadata
    </div>
    <div v-click class="text-2xl">
      <mdi-code-tags /> Low code
    </div>
  </div>
</div>

<!--
Так что же такое динамический фронт?
- - -
Если взять в пример слово статичное и объединить в термин "статичный фронт" мы получим образ приложения, в котором нет никаких данных с бекенда. Абсолютно все данные захардкодены в шаблоне фронт приложения. Таким образом можно предположить, что любое веб-приложение имеющее поток данных с бека будет называться динамическим? Думаю, да. Но в нашем случае не все так просто. 
- - -
Дело в том, что повседневные динамичные веб-приложения берут данные с бекенда для последующего их отображения, а наш динамический фронт (я бы даже назвал гибкий динамический фронт), берет не только данные, но и метаданные (данные о данных). Проще говоря данные о том как отобразить полученные данные.
- - -
Получается, гибкий динамический фронт не сильно и отличается от обычного динамического фронта, но в связке с лоу код системой дает возможность кастомизации функционала без участия разработчика
-->

---
layout: title
title: Tech demo - agency
preload: false
---

::title::

<div
  v-motion
  :initial="{opacity: 0 }"
  :enter="{opacity: 1, transition: {
      delay: 200,
    },
  }">
  <h1>ТехноДемо:</h1>
  <h1>Агентский портал</h1>
</div>

::description::

<div class="flex h-full items-center pb-10"
  v-motion
  :initial="{opacity: 0 }"
  :enter="{opacity: 1, transition: {
      delay: 200,
    }, 
  }">
  Введение в проект
</div>

<!--
Теперь перейдем от теории к прикладному решению в нашей техно демке Агентского портала. В кратце пройдемся по процессу займа. 
-->

---
layout: img
image: /agency.png
backgroundSize: contain
title: Agency portal
---

# Агентский портал

<!--
Перейти в режим маркера
- - -
Перед нами процесс выдачи кредита. Точкой старта является клиент, который желает получить займ. Далее Агент проводит консультацию, а после Back office проверяет возможность выдать займ. Затем агент подбирает продукт и формирует заявку. Back office начинает полную проверку возможности выдать займ и отправляет заявку на авторизацию. Агент вскоре получает результат рассмотрения заявки и сообщяет о нем клиенту. Потом агент инициирует процесс подготовки документов, а Back office формирует необходимую документацию. Далее Агент производит печать договора и документации, а клиент все подписывает. Агент подтверждает корректность, а Back office получает инфорамацию о согласии клиента и инициирует процесс передачи средств клиенту. И вот наконец клиент получает займ.
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Agency portal - borders
preload: false
---

<div
  v-motion
  :initial="{opacity: 0, x: 200 }"
  :enter="{opacity: 1, x: 0, transition: {
      delay: 200,
    },
  }">
  <h1>Агентский портал: Границы</h1>
</div>

<div class="flex h-full items-center pb-10">
  <div>
    <div v-click class="text-2xl">
      <mdi-account-question /> Проведение консультации
    </div>
    <div v-click class="text-2xl my-6">
      <mdi-file-document-multiple /> Подбор продукта и формирование заявки
    </div>
    <div v-click class="text-2xl">
      <mdi-clipboard-check-multiple /> Получение результата рассмотрения заявки
    </div>
  </div>
</div>

<!--
Наши границы в процессе займа
- - -
Агент проводит консультацию клиента. Что за этим стоит и как это должно быть реализовано мне не известно, поэтому скажем, что оно просто есть
- - -
Подбор продукта и формирование заявки, то где и реализован динамический фронт. Бек отсылает данные формы, а агент заполняет  заявку, в которой поля могут быть разных типов, размеров, видов и так далее.
- - -
Получение результата рассмотрения заявки - Тоже должна была быть частью динамического фронта. В зависимости от статуса заявки страница заявки преображается.
-->

---
layout: title
title: Tech demo - screens
preload: false
---

::title::

<div
  v-motion
  :initial="{opacity: 0 }"
  :enter="{opacity: 1, transition: {
      delay: 200,
    },
  }">
  <h1>ТехноДемо: Скриншоты</h1>
</div>

::description::

<div class="flex h-full items-center pb-10"
  v-motion
  :initial="{opacity: 0 }"
  :enter="{opacity: 1, transition: {
      delay: 200,
    }, 
  }">
  Демонстрация динамического фронта
</div>

<!--
Теперь мы посмотрим как это выглядит в текущий момент
-->

---
layout: img
image: /dynamic-3.png
backgroundSize: contain
title: Tech demo - screen 1
---

# ТехноДемо скриншоты

<!--
Здесь у нас отображены категории заявок. Агент может выбрать в данный момент какую заявку он может создать
-->

---
layout: img
image: /dynamic-1.png
backgroundSize: contain
title: Tech demo - screen 2
---

# ТехноДемо скриншоты

<!--
А здесь у нас сама форма заявки. Есть разные поля с разыми типами. Они занимают разное кол-во пространства по сетке.
-->

---
layout: img
image: /dynamic-2.png
backgroundSize: contain
title: Tech demo - screen 3
---

# ТехноДемо скриншоты

<!--
Далее у нас страница клиентов и их созданных заявок
-->

---
layout: img
image: /dynamic-4.png
backgroundSize: contain
title: Tech demo - screen 4
---

# ТехноДемо скриншоты

<!--
Заявка клиента выглядит также как форма заявки на ипотеку, но с разницей в том, что данные уже заполнены.
-->

---
layout: title
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Activity admin
---

::title::

# Activity admin

::description::

Конфигурация Activity с использованием low code механик

<!--
Админка активити, то место где и просиходит вся конфигурация метаданных динамического фронта
-->

---
layout: img
image: /admin-2.png
backgroundSize: contain
title: Activity admin - screen 1
---

# Activity скриншоты

<!--
На этой странице админки можно заметить сходство с формой заявки на ипотеку. Дело в том, что это она и есть. Здесь мы можем задавать параметры полей и их отображение.
-->

---
layout: img
image: /admin-1.png
backgroundSize: contain
title: Activity admin - screen 2
---

# Activity скриншоты

<!--
На вкладке группы отображения можно создать дополнительные панели (в данном случае в динамическом фронте будет отображен dynamic-panel-container на каждую группу отображения)
-->

---
layout: img
image: /compare.png
backgroundSize: contain
title: Activity admin compare screen
---

# Activity сравнение с динамическим фронтом

<!--
На этом слайде отображено сопоставление формы заявки с лоукод конструктором из админки.
- - -
Достать маркер и сравнить
-->

---
layout: title
title: Dive in to code
---

::title::

# ТехноДемо:
# Реализация

::description::

Погружение в техническую часть

<!--
Теперь поговорим наконец о том как это реализовано с технической части
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Dive in to code - 1
---

# Модуль Mortgage

![Mortgage](/mortgage.png)

<!--
Тут отображен модуль Mortgage, а проект в котором лежит модуль основан на ActivityServiceFront из которого был вырезан почти весь текущий функционал. Основой являются три компонента контейнера в которых и заключена главная логика.
- - -
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Dive in to code - 2
---

# Dynamic-view-container

```html {3-6}
<p *ngIf="!isObjectDataLoaded">Загрузка объекта...</p>
<p *ngIf="status">{{ status }}</p>

<form [formGroup]="dynamicForm">
  <ng-container #dynamicViewContent></ng-container>
</form>
```

```ts {2-5|6-9|10-13}
// ...
const dynamicPanelContainerComponentFactory =
  this._componentFactoryResolver.resolveComponentFactory(
    DynamicPanelContainerComponent
  );
const dynamicPanelContainerComponent =
  this._dynamicViewContent.createComponent(
    dynamicPanelContainerComponentFactory
  );
dynamicPanelContainerComponent.instance.headerText = viewGroup.displayName;
dynamicPanelContainerComponent.instance.grid = viewGroup.grid;
dynamicPanelContainerComponent.instance.formGroup = this.dynamicForm
  .controls[viewGroup.id] as FormGroup;
// ...
```

<!--
Dynamic-view-conatiner это умный компонент, который отвечает за отображение некоторой части страниц с названием занимаемого места (например main). 
- - -
В шаблоне компонента мы видим референс на #dynamicViewContent здесь и будут программно рендериться компоненты
- - -
В логике компонента главным является некая функция, которая создает Factory на основе референса нужного компонента. В данном случае это dynamicPanelContainerComponentFactory. И стоит упомянуть, что componentFactoryResolver не поддерживается с 13 версии Ангуляра.
- - -
Далее мы создает инстанс комопнента благодаря Factory
- - -
И теперь мы можем свободно перекидвать необходимые пропсы внутрь созданного инстанса. в итоге данная функция вызывается столько раз сколько viewGroups находиться в респонсе от бекенда. Получается внутри формы будет лежать три компонента DynamicPanelContainerComponent если бекенд отправил массив из трех viewGroups
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Dive in to code - 3
---

# Dynamic-panel-container

```html {5}
...
<div [ngClass]="{ hidden: !isOpen }">
  <div *ngIf="!_hideLine" class="line"></div>
  <div class="panel-content">
    <ng-container #dynamicPanelContent></ng-container>
  </div>
</div>
```

```ts {10-11}
// ...
private _loadDynamicRow(row: ViewGroupGridItem[]): void {
  const dynamicRowComponentFactory =
    this._componentFactoryResolver.resolveComponentFactory(
      DynamicRowContainerComponent
    );
  const dynamicRowComponent = this._dynamicPanelContent.createComponent(
    dynamicRowComponentFactory
  );
  dynamicRowComponent.instance.row = row;
  dynamicRowComponent.instance.formGroup = this.formGroup;
}
// ...
```

<!--
imporvise
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Dive in to code - 4
---

# Dynamic-row-container

```html {2}
<div class="row">
  <ng-container #dynamicRowContent></ng-container>
</div>
```

```ts {3|4-6|7-15}
// ...
private _loadDynamicField(field: ViewGroupGridItem): void {
  switch (field.control.controlType) {
    case ControlTypes.buttonControl: {
      // ...
    }
    case ControlTypes.fieldControl: {
      const cf = this.cfr.resolveComponentFactory(FieldComponent);
      const c = this._drc.createComponent(fieldComponentFactory);
      c.instance.label = field.control.configuration.displayName;
      c.instance.control = this.formGroup.controls[field.control.configuration.name] as FormControl;
      c.instance.dataType = field.control.configuration.dataType;
      c.instance.size = field.size;
      break;
    }
    // ...
  }
}
// ...
```

<!--
test
- - -
-->

---
layout: content-img
image: https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80
title: Roadmap
preload: false
---

<div
  v-motion
  :initial="{opacity: 0, x: 200 }"
  :enter="{opacity: 1, x: 0, transition: {
      delay: 200,
    },
  }">
  <h1>Планы</h1>
</div>

<div class="flex h-full items-center pb-10">
  <div>
    <div v-click class="text-2xl">
      <mdi-refresh /> Рефактор
    </div>
    <div v-click class="text-2xl mt-6">
      <mdi-folder-plus /> Добавление новых видов контролов
    </div>
    <div v-click class="text-2xl my-6">
      <mdi-book-open-page-variant /> Добавление динамических страниц
    </div>
    <div v-click class="text-2xl">
      <mdi-package-variant-closed /> Отделение функционала в библиотеку
    </div>
  </div>
</div>

<!--
test
- - -
-->

---
layout: content
image: /dream.png
backgroundSize: contain
title: Dream low code page
preload: false
---

<div
  v-motion
  :initial="{opacity: 0, x: 200 }"
  :enter="{opacity: 1, x: 0, transition: {
      delay: 200,
    },
  }">
  <h1>Low code моей мечты</h1>
</div>

<img src="/dream.png" class="h-100" />

<!--
test
-->

---
layout: thanks
image: /avatar.png
title: Thanks
---

::title

# Конец

::description::

Авксентьев А.Н.

<!--
test
- - -
-->
