---
layout: page
title: Редакционная политика

---

* TOC
{:toc}

# Что такое журнал

Журнал - это коллективный блог о Rust, публикуемый совместными усилиями авторов
и редакторов по единым стандартам, описанным в этой редполитике.

# Цель журнала

Наша цель - нести людям практические знания о языке Rust, его инструментах,
экосистеме и методиках разработки.

Практические знания, в противовес теоретическим, направлены на решение реальных
рабочих задач.

Маленькие, заведомо учебные программы допускаются.

# Аудитория журнала

В первую очередь журнал должен быть интересен программистам, практикующим Rust
на оплачиваемой работе --- офисной или удалённой, на зарплате или контрактной.

Во вторую очередь журнал должен быть интересен программистам, которые изучают
язык с целью применять для себя или на работе --- с любым бэкграундом.

В третью очередь журнал должен быть интересен программистам, практикующим Rust в
своих хобби-проектах.

Теоретики --- остаются за бортом.

# Круг тем

Всё в контексте Rust:

- Синтаксис и семантика ядра языка (не включая стандартную библиотеку)
- Стандартная библиотека (включая детали реализации)
- Документирование программ
- Тестирование программ: модульные и интеграционные тесты
- Отладка программ
- Профилирование программ
- Инструменты и инфраструктура: cargo, crates.io
- Инструменты поддержки IDE: rustfmt, racer, RLS, сами IDE и редакторы
- Архитектура программ. Лучшие практики по высокоуровневому проектированию
- Экосистема
- FFI
- Кросс-компиляция
- Верификация и формальное доказательство семантики Rust
- Нестабильные возможности Rust
- Мета-информация: ведение проекта, управление сообществом

Предпочтение отдаётся статьям, рассматривающим стабильный Rust.

# Требования к статьям

## Минимальные

- У статьи должно быть введение, после которого идёт кат.

  Введение должно заинтересовывать читателя, но не быть слишком длинным.
  Оптимально --- 3 абзаца, максимум --- столько, сколько влезает в экран вместе
  с тизером.

- У статьи должна быть картинка-тизер.

  Тизер должен быть высотой в 400 пикселей и шириной от 400 до 900. Тег `<img>`
  должен быть в первой осмысленной строке статьи (после front matter).

  Он должен находиться в директории с картинками для статьи и называться
  `teaser.<расширение>`.

- Исходный текст статьи:
  - Должен быть написан в Markdown.
  - Находится в файле с названием (дата)-короткое-осмысленное-название.md в
    директории _posts.
  - Должен иметь строки не длиннее 80 символов. Использование более длинных
    строк допускается только в случае, если разбиение ухудшит читаемость.

- Все картинки для статьи должны находиться в директории, название которой
  совпадает с названием файла статьи, исключая расширение. Директория должна
  находиться в `_assets/images`:

  ```
  _assets/images/(дата)-короткое-осмысленное-название
  ```

- Все ссылки в статьях должны работать.

- В специальном поле в заголовке статьи должна быть указана минимальная версия
  компилятора Rust, который правильно компилирует приведённый код.
  - Нумерация начинается с 1.0 stable.
  - Если нет особых ограничений, пишем `1.0 < v`.
  - Если код перестаёт компилироваться на какой-то версии Rust, нужно
    указать верхнюю границу: `1.0 < v < 1.15`.
  - Если код требует nightly, пишем фиксированную версию nightly, в которой он
    точно компилируется: `rustc 1.19.0-nightly (4ed2edaaf 2017-06-01)`.

- Весь код, написанный в статье, должен компилироваться указанной версией
  компилятора Rust.

  Не компилироваться может код, про который отдельно сказано, что он не
  компилируется: если он демонстрирует ошибку компиляции или процесс поиска
  решения. В любом случае должен быть комментарий вида "этот код не
  скомпилируется".

- Весь код, написанный в статье, должен работать.

  Не работать может код, про который отдельно сказано, что он не работает: если
  он демонстрирует ошибку во время выполнения или процесс поиска решения. В
  любом случае должен быть комментарий вида "этот код не работает".

- Во всех бенчмарках должны быть указаны:
  - ЦП
  - объём системной памяти
  - ОС
  - версия компилятора
  - параметры командной строки компилятора

- Рекомендуется выложить код в репозиторий на GitHub и ссылаться на его части в
  статье.

- В статье, кроме тизера, должна быть как минимум одна иллюстрация - например,
  скриншот интерфейса работающей программы, визуализация результата, или
  текстовое представление результата.

- В статье не должно быть опечаток.
  - Вводимые статьёй новые термины должны быть внесены в список исключений
    словаря.

- Иноязычные названия не переводятся и не склоняются: Mozilla, Rust, Google; в
  Mozilla, у Rust, для Google.

- Автор статьи должен иметь разрешение на публикацию кода от владельцев
  интеллектуальных прав на этот код.

## К оплачиваемым статьям

Текст ниже не является публичной офертой.

- Работа над оплачиваемой статьёй начинается с её согласования с Панковым
  Михаилом (главредом).

  Согласование начинается с отправки ссылки на заявку на статью на почту
  rustycrate@michaelpankov.com.

  Заявка должна содержать:
  - Предполагаемое название статьи
  - Мотивацию статьи: почему это важно
  - Аудиторию статьи: кому это нужно

  Заявка должна быть в виде документа в Google Документах.

  Далее происходит обсуждение в документе. В результате обсуждения могут
  меняться все поля заявки. В процессе согласования заявки автор может
  отказаться. В процессе согласования главред может отказать в дальнейшей работе
  над статьёй.

  В процессе согласования автор предлагает:
  - Структуру статьи: заголовки первого и второго уровней

  Если обе стороны довольны итоговым видом заявки, автор начинает работу над
  статьёй.

- Работа над статьёй идёт в репозитории rustycrate.

  Содержимое статьи должно быть в этом репозитории в директории _posts. Код
  должен быть в этом репозитории в директории source в поддиректории с названием
  статьи.

  - Можно не выкладывать полный код, если интересный для обсуждения код гораздо
    меньше, чем полная программа. В этом случае все интересные части кода должны
    быть приведены в статье.

  - Если выкладывается полный код, и он пишется специально для статьи, нужно
    делать коммиты в репозитории с кодом соответственно логике изложения в
    статье, и ссылаться в статье на определённые коммиты.

- Описываемую в статье программу должно быть можно запустить и получить полезный
  результат, не имея знаний её автора.

  Это означает, что она должна собираться и запускаться стандартным образом и
  иметь понятный интерфейс. Это означает, что должно быть достаточно `cargo
  build` и `cargo run`. Опции командной строки должны быть документированы.

  В случае отклонений в процессе сборки и запуска они должны быть
  задокументированы (по умолчанию - в `README.md`).