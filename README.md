Презентация Saint HighLoad++ 2021 (Санкт-Петербург, Россия). Тема LaTeX beamer
------------------------------------------------------------------------------

Конференция
===========

https://highload.ru/spb/2021

Особенности
===========

* Создан для использования с компилятором xelatex
* Требуются шрифты TT Traveler (кастомный), Calibri, Times New Roman, Courier New в системе
* Размеры подогнаны к стандартному шаблону, что в целом не очень верно
* Мне не известны лицензионные условия картинок шаблона
* Дополнения для листинга не вынесены в отдельный класс и болтаются внутри документа
* Изменения шрифта для библиографии тоже болтается в документе
* Требуется `<policy domain="coder" rights="read | write" pattern="PDF" />` в `/etc/ImageMagick-X/policy.xml` для сощдания gif
* При использовании docker учтите, что все ваши TTF-шрифты придется перенести в `~/.fonts`

[Скомпилированная презентация (PDF)](shl2021-example.pdf)
![](shl2021-example.gif)

Использование
=============

```console
docker run -ti --rm -u `id -u`:`id -g` -v /home:/home -w `pwd` -e HOME=$HOME texlive/texlive xelatex shl2021-example.tex
docker run -ti --rm -u `id -u`:`id -g` -v /home:/home -w `pwd` -e HOME=$HOME texlive/texlive biber shl2021-example
docker run -ti --rm -u `id -u`:`id -g` -v /home:/home -w `pwd` -e HOME=$HOME texlive/texlive xelatex shl2021-example.tex
docker run -ti --rm -u `id -u`:`id -g` -v /home:/home -w `pwd` -e HOME=$HOME texlive/texlive xelatex shl2021-example.tex
```

TODO
====

* Пример отсылок
* Вынести фонт в корень
* Поменять шрифт в библиографии
* (вряд ли) вынести всё в шаблоны

Donate
------

* PayPal https://www.paypal.me/schors
* Yandex.Money http://yasobe.ru/na/schors
* BTC: 18YFeAV12ktBxv9hy4wSiSCUXXAh5VR7gE
* LTC: LVXP51M8MrzaEQi6eBEGWpTSwckybqHU5s
* ETH: 0xba53cebd99157bf412a6bb91165e7dff29abd0a2

---
[![UNLICENSE](noc.png)](UNLICENSE)
