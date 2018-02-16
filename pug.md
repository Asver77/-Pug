# Препроцессор Pug(Jade)
Pug - это препроцессор HTML и шаблонизатор, который был написан на JavaScript для Node.js.

### Теги
В Pug нет закрывающих тегов, вместо этого он использует строгую табуляцию (или отступы) для определения вложености тегов.
Для закрытия тегов в конце необходимо добавить символ `/`: `foo(bar='baz')/`

Pug
```pug
ul
  li Item A
  li Item B
  li Item C
```
Html
```html
<ul>
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
</ul>
````

#### Текст

```pug
p This is plain old <em>text</em> content.
```html
<p>This is plain old <em>text</em> content.</p>
