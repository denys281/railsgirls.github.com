---
layout: default
title: Add design to your App with HTML and CSS
permalink: design-html-css
---

## *1.* Дизайн заголовка

Додайте рядки в кінець файлу `app/assets/stylesheets/application.css`:

{% highlight css %}
.navbar {
  min-height: 38px;
  background-color: #f55e55;
}
{% endhighlight %}


Оновiть сторінку і перевірте зміни. Ви можете змінити колір і шрифт заголовка на свій смак. Посилання на коди кольору [http://color.uisdc.com/](http://color.uisdc.com/).

Після цього, помістіть ці рядки внизу файлу:

{% highlight css %}
.navbar a.brand { font-size: 18px; }
.navbar a.brand:hover {
 color: #fff;
 background-color: transparent;
 text-decoration: none;
}
{% endhighlight %}


**Тренер:** поясніть про 4-и стани посилання

## *2.* Дизайн таблиці

Ми використовуємо twitter [Bootstrap](http://getbootstrap.com/) для дизайну нашої таблиці. Знайдіть ці рядки в файлі `app/views/ideas/index.html.erb` і замініть:

{% highlight html %}
<table>
{% endhighlight %}
с
{% highlight html %}
<table class="table">
{% endhighlight %}

Змініть розмір зображення, доповнивши код між рядків

{% highlight erb %}
<%= image_tag(idea.picture_url, :width => 600) if idea.picture.present? %>
{% endhighlight %}


спробуйте змінити ширину і подивіться, що станеться

Додайте рядки в кінець файлу `app/assets/stylesheets/ideas.css.scss`:

{% highlight css %}
.container a:hover {
  color: #f55e55;
  text-decoration: none;
  background-color: rgba(255, 255, 255, 0);
}
{% endhighlight %}


Спробуйте додати фоновий стиль використовуючи `background-image`, посилання на патерни [http://subtlepatterns.com/](http://subtlepatterns.com/)

## *3.* Додавання стилів для підвалу

Додайте рядки в кінець файлу `app/assets/stylesheets/application.css`:

{% highlight css %}
footer {
  background-color: #ebebeb;
  padding: 30px 0;
}
{% endhighlight %}

спробуйте додати більше різних стилів до підвалу.

## *4.* Додавання стилів для кнопки

Відкрийте [http://localhost:3000/ideas/new](http://localhost:3000/ideas/new) і знайдіть кнопку Create Idea.

Додайте рядки в кінець файлу `app/assets/stylesheets/ideas.css.scss`


{% highlight css %}
.container input[type="submit"] {
  height: 30px;
  font-size: 13px;
  background-color: #f55e55;
  border: none;
  color: #fff;
}
{% endhighlight %}


**Тренер:** поясніть, як використовувати рамки в css, спробуйте змінити стиль кнопки, наприклад закруглити, додати тінь або колір і т.д.
