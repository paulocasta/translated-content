---
title: '<ul>: The Unordered List element'
slug: Web/HTML/Element/ul
translation_of: Web/HTML/Element/ul
---
{{HTMLRef}}

**HTML-элемент `<ul>` **используется для неупорядоченного списка - в частности для маркированного списка.

{{EmbedInteractiveExample("pages/tabbed/ul.html", "tabbed-standard")}}

| [Категории контента](/ru/docs/HTML/Content_categories) | [Основной поток](/ru/docs/Web/Guide/HTML/Content_categories#Flow_content), и если дочерний элемент `<ol>` включает в себя хотя бы один элемент {{HTMLElement("li")}}, [явный контент](/ru/docs/Web/Guide/HTML/Content_categories#Palpable_content).                                                                                     |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Разрешённое содержимое                                 | Ноль или больше {{ HTMLElement("li") }} элементов, содержат вложенные элементы {{ HTMLElement("ol") }} или {{ HTMLElement("ul") }}.                                                                                                                                                                                 |
| Пропуск тегов                                          | {{no_tag_omission}}                                                                                                                                                                                                                                                                                                                       |
| Разрешённые родители                                   | Любой элемент, который принимает [основной поток](/ru/docs/Web/Guide/HTML/Content_categories#Flow_content).                                                                                                                                                                                                                                    |
| Разрешённые ARIA-роли                                  | {{ARIARole("directory")}}, {{ARIARole("group")}}, {{ARIARole("listbox")}}, {{ARIARole("menu")}}, {{ARIARole("menubar")}}, {{ARIARole("radiogroup")}}, {{ARIARole("tablist")}}, {{ARIARole("toolbar")}}, {{ARIARole("tree")}}, {{ARIARole("presentation")}} |
| DOM-интерфейс                                          | {{domxref("HTMLUListElement")}}                                                                                                                                                                                                                                                                                                       |

## Свойства

Этот элемент включает [глобальные атрибуты](/ru/docs/Web/HTML/Общие_атрибуты).

- {{ htmlattrdef("compact") }} {{Deprecated_inline}}
  - : Атрибут логического значения (bool) говорит о том, что список будет представлен в более компактном стиле. Интерпретация этого атрибута зависит от {{glossary("user agent")}} и не работает со всеми браузерами.

  > **Предупреждение:** Не используйте этот атрибут, ибо он устаревший и больше не используется, используйте [CSS](/ru/docs/CSS). Для схожего эффекта с `compact`, подойдёт свойство CSS {{cssxref("line-height")}} с значением `80%`.
- {{ htmlattrdef("type") }} {{Deprecated_inline}}
  - : Этот атрибут добавляет маркеры (bullets) в список. Значения установлены под [HTML3.2](/ru/docs/HTML3.2) и переходными на [HTML 4.0/4.01](/ru/docs/HTML4.01) являются:\* `circle`
    - `disc`
    - `square`Четвёртый маркер задан в интерфейсе WebTV, но не все браузеры смогут его отобразить: `triangle`.Если данный атрибут отсутствует и если атрибут [CSS](/ru/docs/CSS) {{ cssxref("list-style-type") }} не присвоен к данному элементу, пользовательский агент (user agent) выберет маркер в зависимости от вложенного уровня в списке.

  > **Предупреждение:** Не используйте этот атрибут, ибо он устаревший; используйте свойство [CSS](/ru/docs/Web/CSS) {{ cssxref("list-style-type") }}.

## Примечания об использовании

- Элемент `<ul>` используется для группировки непронумерованных элементов данных, и их последовательность в списке не нужна. Что характерно, непорядочные списки используют маркеры, которые могут быть разных форм (в форме точки, круга или прямоугольной формы). Стиль задаётся не в HTML, а со связанным с ним CSS, используя свойство {{ cssxref("list-style-type") }}.
- Элементы `<ul>` и {{HTMLElement("ol")}} могут быть вложены на любом уровне. Более того, вложенные списки могут чередоваться между `<ol>` и `<ul>` без ограничений.
- Элементы {{ HTMLElement("ol") }} и `<ul>` используются для списков. Различие лишь в том, что в элементе {{ HTMLElement("ol") }} порядок имеет значение. Согласно эмпирической закономерности (или правилу большого пальца), чтобы определить, какую маркировку использовать, попробуйте поменять порядок элементов в списке. Если суть списка меняется, то тогда подойдёт элемент {{ HTMLElement("ol") }}, в противном случае используйте `<ul>`.

## Примеры

### Простой список

```html
<ul>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>
```

Результат HTML кода выше:

{{EmbedLiveSample("Простой_список", 400, 100)}}

### Вложенный список

```html
<ul>
  <li>first item</li>
  <li>second item
  <!-- Look, the closing </li> tag is not placed here! -->
    <ul>
      <li>second item first subitem</li>
      <li>second item second subitem
      <!-- Same for the second nested unordered list! -->
        <ul>
          <li>second item second subitem first sub-subitem</li>
          <li>second item second subitem second sub-subitem</li>
          <li>second item second subitem third sub-subitem</li>
        </ul>
      </li> <!-- Closing </li> tag for the li that
                  contains the third unordered list -->
      <li>second item third subitem</li>
    </ul>
  <!-- Here is the closing </li> tag -->
  </li>
  <li>third item</li>
</ul>
```

Результат HTML кода выше:

{{EmbedLiveSample("Вложенный_список", 400, 220)}}

### Упорядоченный список внутри неупорядоченного списка

```html
<ul>
  <li>first item</li>
  <li>second item
  <!-- Look, the closing </li> tag is not placed here! -->
    <ol>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ol>
  <!-- Here is the closing </li> tag -->
  </li>
  <li>third item</li>
</ul>
```

Результат HTML кода выше:

{{EmbedLiveSample("Упорядоченный_список_внутри_неупорядоченного_списка", 400, 150)}}

## Спецификации

{{Specifications}}

## Поддержка браузерами

{{Compat}}

## Смотрите также

- Остальные списковые HTML-элементы: {{ HTMLElement("ol") }}, {{ HTMLElement("li") }}, {{ HTMLElement("menu") }} и устаревший {{ HTMLElement("dir") }};
- CSS-свойства, которые могут быть полезны для стилизации `<ul>` элементов:

  - свойство [list-style](/ru/docs/Web/CSS/list-style), полезное для выбора способа отображения маркеров,
  - [CSS счётчики](/ru/docs/Web/CSS/CSS_Lists_and_Counters/Using_CSS_counters), для более сложных вложенных списков,
  - свойство [line-height](/ru/docs/Web/CSS/line-height), для замены убранного свойства {{ htmlattrxref("compact", "ul") }},
  - свойство [margin](/ru/docs/Web/CSS/margin), для контроля отступа в списке.