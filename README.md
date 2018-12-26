Шаблон ВКР в LaTeX
==================

<!-- Table of Contents GitLab -->

* [base.tex -- основной файл, подключает все остальные файлы](#basetex-основной-файл-подключает-все-остальные-файлы)
* [thesis.sty -- оформление:](#thesissty-оформление)
* [Файлы, содержащие текст работы](#Файлы-содержащие-текст-работы)
* [Список литературы оформляется вручную](#Список-литературы-оформляется-вручную)
* [Как получить итоговый pdf:](#Как-получить-итоговый-pdf)

<!-- /Table of Contents -->

## base.tex -- основной файл, подключает все остальные файлы

## thesis.sty -- оформление:

1. Поля:

* Левое 3 см
* Правое 1 см
* Верх и низ по 2 см

2. Шрифт Times New Roman

3. Кегль 14

4. Выравнивание по ширине

5. Нумерация страниц:

* В верхнем правом углу
* Со страницы введения

6. Автоматическое оглавление:

* Новые главы и параграфы подключаются автоматически
* Оглавление оформляется как ссылки

7. Интервал полуторный

8. Разрывы страниц после каждого заголовка ПЕРВОГО уровня

* Разрывы добавляются с помощью `\pagebreak`

9. Абзацный отступ 0,75 см:

* Для абзацев и заголовков всех уровней

## Файлы, содержащие текст работы

1. Заголовки:

* Заголовки глав начинаются с "Глава \$номер." (в файлах глав "sectonN.tex")
* Заголовки второго уровня: "№ главы.№ заголовка второго уровня относительно главы"
* Заголовки третьего уровня: "№ главы.№ заголовка второго уровня относительно главы.№ заголовка третьего уровня относительно второго"

2. Заголовки помещаются в фигурные скобки:

* Первого уровня: `\section{}`

* Второго уровня: `\subsection{}`

* Третьего уровня: `\subsubsection{}`

3. Абзацы отдеяются пустой строкой, абзацный отсутуп добавляется автоматически

4. Списки:

* Нумерованные списки размещаются следующим образом:

```
\begin{enumerate}
\item $текст
\end{enumerate}
```

* Ненумерованные списки размещаются следующим образом:

```
\begin{itemize}
\item $текст
\end{itemize}
```

5. Выделение:

* Жирный: текст заключается в фигурные скобки `\textbf{}`
* Курсив: текст заключается в фигурные скобки `\textit{}`

6. Тире: тройной дефис `---`

7. Кавычки-елочки: два знака меньше для открывающей, два больше для закрывающей `<<>>`

## Список литературы оформляется вручную

## Как получить итоговый pdf:

`latexmk -pdfxe -f -g base.tex`

