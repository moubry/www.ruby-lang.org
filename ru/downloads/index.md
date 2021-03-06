---
layout: page
title: "Скачать Ruby"
lang: ru
---

Здесь вы найдете последние дистрибутивы Ruby на любой вкус. Текущая
стабильная версия {{ site.downloads.stable[0].version }}.
Пожалуйста, ознакомьтесь с [лицензией Ruby][license].
{: .summary}

### Способы установки Ruby

У нас имеются инструменты для всех основных платформ для установки Ruby:

* На Linux/UNIX, вы можете использовать систему управления пакетами вашей
  операционной системы или сторонние инструменты (rbenv и RVM).
* На OS X вы можете использовать сторонние инструменты (rbenv и RVM).
* На Windows вы можете использовать RubyInstaller.

Смотрите на странице [Установка][installation] подробности об использовании
систем управления пакетами или сторонних инструментов.

И конечно, вы можете также установить Ruby из исходников на всех основных
платформах.

### Компиляция Ruby – Исходный код

Установка из исходного кода – отличный способ для тех, кто хорошо знаком
со своей платформой и кому, возможно, нужны специальные настройки для
своего окружения. Это также хорошее решение в случае, когда для вашей
платформы нет готовых собранных пакетов.

Смотрите на странице [Установка][installation] подробности о сборке Ruby
из исходников. Если у вас возникла сложность с компиляцией Ruby, попробуйте один из
сторонних инструментов из следующей секции. Они могут помочь вам.

* **Стабильные релизы:**{% for release in site.downloads.stable %}
  * [Ruby {{ release.version }}]({{ release.url.gz }})<br>
    sha256: {{ release.sha256.gz }}{% endfor %}

{% if site.downloads.security_maintenance %}
* **На стадии поддержки безопасности (скоро будет остановлена):**{% for release in site.downloads.security_maintenance %}
  * [Ruby {{ release.version }}]({{ release.url.gz }})<br>
    sha256: {{ release.sha256.gz }}{% endfor %}
{% endif %}

{% if site.downloads.eol %}
* **Больше не поддерживается (EOL):**{% for release in site.downloads.eol %}
  * [Ruby {{ release.version }}]({{ release.url.gz }})<br>
    sha256: {{ release.sha256.gz }}{% endfor %}
{% endif %}

* **Слепки:**
  * [Стабильный слепок]({{ site.downloads.stable_snapshot.url.gz }}):
    Это архив свежайшего слепка текущей стабильной ветки.
  * [Nightly слепок]({{ site.downloads.nightly_snapshot.url.gz }}):
    Это архив того, что в SVN, сделанный ночью.
    Может содержать баги и другие проблем, используйте на собственный риск.

За информацией о Ruby Subversion и Git репозиториях пожалуйста,
посмотрите страницу о [ядре Ruby](/ru/community/ruby-core/).

Исходный код Ruby доступен по всему миру на нескольких
[зеркальных сайтах][mirrors].
Пожалуйста, попробуйте использовать зеркало, которое находится
недалеко от вас.



[license]: {{ site.license.url }}
[installation]: /ru/documentation/installation/
[mirrors]: /en/downloads/mirrors/
