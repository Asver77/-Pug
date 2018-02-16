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

### Атрибуты
В Pug можно встраивать JavaScript код, благодаря чему возможны конструкции показанные ниже.

***
Pug
````pug
a(href='google.com') Google
|
|
a(class='button' href='google.com') Google
|
|
a(class='button', href='google.com') Google
````
HTML
````html 
<a href="google.com">Google</a>
<a class="button" href="google.com">Google</a>
<a class="button" href="google.com">Google</a>
````
***
Pug
````pug
- var authenticated = true
body(class=authenticated ? 'authed' : 'anon')
````
HTML
````html 
<body class="authed"></body>
````
***
Pug
````pug
input(
  type='checkbox'
  name='agreement'
  checked
)
````
HTML
````html 
<input type="checkbox" name="agreement" checked="checked" />
````
***
Pug
````pug
- var url = 'pug-test.html';
a(href='/' + url) Link
|
|
- url = 'https://example.com/'
a(href=url) Another link
````
HTML
````html 
<a href="/pug-test.html">Link</a>
<a href="https://example.com/">Another link</a>
````
***
Pug
````pug
- var classes = ['foo', 'bar', 'baz']
a(class=classes)
|
|
//- the class attribute may also be repeated to merge arrays
a.bang(class=classes class=['bing'])
````
HTML
````html 
<a class="foo bar baz"></a>
<a class="bang foo bar baz bing"></a>
````