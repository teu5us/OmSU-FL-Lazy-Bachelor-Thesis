# Шаблон ВКР в LaTeX

Шаблон выпускной квалификационной работы факультета иностранных языков ОмГУ им. Ф.М. Достоевского.

## base.tex -- основной файл, подключает все остальные файлы

## thesis.sty -- форматирование:

1. Поля:

* Левое 3 см
* Правое 1 см
* Верх и низ по 2 см

2. Times New Roman 14

3. Выравнивание по ширине

4. Нумерация страниц:

* В верхнем правом углу
* Начинается со страницы введения

5. Оглавление:

* Новые главы и параграфы добавляются в оглавление автоматически
* Каждый пункт оглавления является ссылкой на соответствующую страницу

6. Полуторный интервал

7. Разрывы страниц после каждого заголовка **первого** уровня

* Разрывы добавляются с помощью `\pagebreak`

8. Абзацный отступ 0,75 см для абзацев и заголовков всех уровней

## Файлы, содержащие текст работы

1. Заголовки:

* Первого уровня: `\section{введение/оглавление/глава/заключение/список литературы/приложения}`

* Второго уровня: `\subsection{}`

* Третьего уровня: `\subsubsection{}`

* Введение, оглавление, заключение, список литературы и приложения уже обозначены в соответствующих файлах

* Названия глав размещаются как заголовки первого уровня в соответствующих файлах: "Глава №. 'название главы' "

* Заголовки глав начинаются с "Глава \$номер." (в файлах глав "sectonN.tex")

* Заголовки второго уровня: "№ главы.№ заголовка второго уровня относительно главы"

* Заголовки третьего уровня: "№ главы.№ заголовка второго уровня относительно главы.№ заголовка третьего уровня относительно второго"

2. Абзацы отделяются пустой строкой, абзацный отступ будет добавлен автоматически

3. Списки:

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

4. Выделение:

* **Жирный**: текст заключается в фигурные скобки `\textbf{текст}`

* *Курсив*: текст заключается в фигурные скобки `\textit{текст}`

5. Тире: тройной дефис `---`

6. Кавычки-елочки: `<<>>`

## Список литературы оформляется вручную

## Как получить итоговый pdf:

`latexmk -pdfxe -f -g base.tex`

