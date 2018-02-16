# Препроцессор Pug(Jade)
Pug - это препроцессор HTML и шаблонизатор, который был написан на JavaScript для Node.js.

### Теги
В Pug нет закрывающих тегов, вместо этого он использует строгую табуляцию (или отступы) для определения вложености тегов.
Для закрытия тегов в конце необходимо добавить символ `/`: `foo(bar='baz')/`

Pug
````pug
ul
  li Item A
  li Item B
  li Item C
````
HTML
````html
<ul>
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
</ul>
````

### Текст
Непосредственно в Pug можно вставлять элементы в HTML синтаксисе

Pug
````pug
p This is plain old <em>text</em> content.
````
HTML
```html
<p>This is plain old <em>text</em> content.</p>
````
***
Pug
````pug
p
  | The pipe always goes at the beginning of its own line,
  | not counting indentation.
````
HTML
````html 
<p>The pipe always goes at the beginning of its own line, not counting indentation.</p>
````
***
Pug
````pug
````
HTML
````html 
````


