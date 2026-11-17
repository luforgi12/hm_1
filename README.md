# Домашнє завдання: Створення веб-сторінки «Mathematical formulas»

> **Модуль 1:** Походження веб-сторінок і основи HTML  
> **Формат:** Самостійна практична робота (Домашнє завдання)  
> **Рівень:** Базовий / Закріплення знань

---

## 🎯 Мета завдання

- Закріпити навички побудови валідного HTML5-документа від початку й до кінця.
- Освоїти роботу з верхніми (`<sup>`) та нижніми (`<sub>`) індексами для запису математичних виразів і фізичних величин.
- Навчитися коректно застосовувати спеціальні символи **HTML Entities** (`&pi;`, `&times;`, `&cap;`, `&isin;`, `&mdash;`, `&ne;`).
- Оформити списки формул і властивостей за допомогою `<ul>` або `<ol>`.
- Навчитися проводити автоматичну перевірку якості коду через **W3C Nu HTML Validator** та здійснювати AI-рев'ю коду.

---

## 📁 Структура файлів завдання

```text
task-03-math-formulas/
├── index.html     # Ваш головний файл домашнього завдання
├── raw-text.txt   # Вихідний текст та математичні вирази
└── README.md      # Ця покрокова інструкція
```

---

## 📝 Вихідний текст (із `raw-text.txt`)

```text
Mathematical formulas

Linear Equations
A linear equation is any equation that can be written in the form
ax + b = 0
where a and b are real numbers and x is a variable. This form is sometimes called the standard form of a linear equation. Note that most linear equations will not start off in this form. Also, the variable may or may not be an x so don’t get too locked into always seeing an x there.

Quadratic Equation
The standard form of a quadratic equation looks like this:
ax^2 + bx + c = 0
where a, b, c are known values and x is the variable or unknown (we don't know it yet). Also, a can't be 0.

The area of a circle (A)
Pi times the radius (r) squared:
A = π × r^2

or, when you know the diameter (D):
A = (π / 4) × D^2

or, when you know the circumference (C):
A = C^2 / (4 × π)

Intersection
The intersection of two sets A and B, denoted by A ∩ B, is the set of all objects that are members of both the sets A and B. In symbols,
A ∩ B = { x : x ∈ A and x ∈ B }
That is, x is an element of the intersection A ∩ B if and only if x is both an element of A and an element of B.
```

---

## 🚀 Покроковий план виконання

### Крок 1. Базова розмітка документа

1. Відкрийте файл `index.html` у VS Code.
2. Переконайтеся, що налаштовано стандартний скелет HTML5:
   ```html
   <!DOCTYPE html>
   <html lang="uk">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Mathematical formulas - Домашнє завдання</title>
   </head>
   <body>
     <!-- Контент сторінки -->
   </body>
   </html>
   ```

---

### Крок 2. Структура заголовків

1. Створіть головний заголовок сторінки першого рівня:
   ```html
   <h1>Mathematical formulas</h1>
   ```
2. Створіть 4 тематичні підзаголовки `<h2>`:
   - `<h2>Linear Equations</h2>`
   - `<h2>Quadratic Equation</h2>`
   - `<h2>The area of a circle (A)</h2>`
   - `<h2>Intersection</h2>`

---

### Крок 3. Верстка секції «Linear Equations»

1. Додайте абзац із поясненням лінійного рівняння.
2. Оформіть формулу окремим блоком або абзацом, виділивши змінні курсивом:
   ```html
   <p class="formula-block">
     <i>a</i><i>x</i> + <i>b</i> = 0
   </p>
   ```
3. Додайте пояснення параметрів, зазначивши, що <i>a</i> та <i>b</i> є дійсними числами.

---

### Крок 4. Верстка секції «Quadratic Equation» (верхній `<sup>` та нижній `<sub>` індекси)

1. Додайте вступний абзац.
2. Оформіть формулу квадратного рівняння зі степенем `<sup>2</sup>`:
   ```html
   <p class="formula-block">
     <i>a</i><i>x</i><sup>2</sup> + <i>b</i><i>x</i> + <i>c</i> = 0
   </p>
   ```
3. Вкажіть у тексті додаткову умову, що <i>a</i> не дорівнює нулю (`<i>a</i> &ne; 0`).
4. Для закріплення тегу нижнього індексу `<sub>`, додайте позначення коренів рівняння:
   ```html
   <p>
     Корені квадратного рівняння позначаються як <i>x</i><sub>1</sub> та <i>x</i><sub>2</sub>.
   </p>
   ```

> 💡 **Примітка щодо тегів `<i>` та `<em>`:**  
> У математичній типографіці змінні ($x, y, a, b$) традиційно виділяють тегом `<i>` (шрифтовий італік) за стандартом ISO для формул. У звичайному тексті для логічного смислового наголосу слід надавати перевагу семантичному тегу `<em>`.

---

### Крок 5. Верстка секції «The area of a circle» (спецсимволи `&pi;`, `&times;` та список)

1. Оформіть три альтернативні формули для обчислення площі кола за допомогою маркованого списку `<ul>`:
   ```html
   <ul>
     <li>
       <strong>Через радіус (<i>r</i>):</strong> 
       <i>A</i> = &pi; &times; <i>r</i><sup>2</sup>
     </li>
     <li>
       <strong>Через діаметр (<i>D</i>):</strong> 
       <i>A</i> = (&pi; / 4) &times; <i>D</i><sup>2</sup>
     </li>
     <li>
       <strong>Через довжину кола (<i>C</i>):</strong> 
       <i>A</i> = <i>C</i><sup>2</sup> / (4 &times; &pi;)
     </li>
   </ul>
   ```

> 💡 **Зверніть увагу на сутності:**
> - `&pi;` генерує грецьку літеру **&pi;** (Pi).
> - `&times;` генерує типографічний знак множення **&times;** (хрестик, а не англійську літеру x).

---

### Крок 6. Верстка секції «Intersection» (теорія множин, `&cap;` та `&isin;`)

1. Додайте текстовий опис операції перетину множин.
2. Оформіть символьний запис перетину, використовуючи спецсимволи:
   - `&cap;` для перетину (&cap;)
   - `&isin;` для належності елемента множині (&isin;)
   ```html
   <p class="formula-block">
     <i>A</i> &cap; <i>B</i> = { <i>x</i> : <i>x</i> &isin; <i>A</i> and <i>x</i> &isin; <i>B</i> }
   </p>
   ```
3. Додайте пояснювальний абзац про умови належності.

---

### Крок 7. Стилізація для привабливого вигляду (за бажанням)

Для того щоб формула візуально виділялася як у навчальному посібнику, додайте у `<head>`:

```html
<style>
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    line-height: 1.6;
    color: #1e293b;
    background-color: #f8fafc;
    margin: 0;
    padding: 30px 15px;
  }

  .container {
    max-width: 800px;
    margin: 0 auto;
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    padding: 30px 40px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
  }

  h1 {
    color: #0f172a;
    border-bottom: 3px solid #4f46e5;
    padding-bottom: 10px;
  }

  h2 {
    color: #334155;
    margin-top: 25px;
  }

  .formula-block {
    background-color: #fee2e2;
    border-left: 4px solid #ef4444;
    padding: 10px 16px;
    font-size: 1.15rem;
    font-weight: 500;
    border-radius: 4px;
    display: inline-block;
    margin: 12px 0;
  }

  i {
    font-family: "Times New Roman", serif;
    font-style: italic;
    font-weight: bold;
  }

  sup {
    font-size: 0.75em;
    color: #b91c1c;
  }

  ul {
    padding-left: 20px;
  }

  li {
    margin-bottom: 8px;
  }
</style>
```

---

### Крок 8. Валідація через W3C та AI Code-Review

1. **W3C Nu HTML Checker:**
   - Перейдіть на офіційний валідатор: [https://validator.w3.org/#validate_by_input](https://validator.w3.org/#validate_by_input).
   - Оберіть вкладку **Direct Input**.
   - Вставте весь код вашого `index.html` і натисніть **Check**.
   - Переконайтеся, що результат зеленого кольору: **"Document checking completed. No errors or warnings to show."**

2. **AI Code-Review:**
   - Надішліть код своєму AI-асистенту з таким промптом:

```text
Перевір моє домашнє завдання з HTML (тема: Математичні формули, сутності, індекси):
```html
[ВСТАВТЕ ВАШ КОД СЮДИ]
```
Дай відповідь за чек-лістом:
1. Чи валідний HTML5 DOCTYPE і метатеги?
2. Чи правильно використано <sup> для квадратів (x^2, r^2, D^2, C^2)?
3. Чи використано HTML Entities для π (&pi;), × (&times;), ∩ (&cap;)?
4. Чи коректно вкладені теги?
5. Оціни охайність форматування від 1 до 10.
```

---

## 🏆 Критерії оцінювання (10-бальний чек-ліст)

| № | Критерій | Бали |
| :-: | :--- | :-: |
| 1 | Валідний HTML5 скелет (`<!DOCTYPE html>`, `html`, `head`, `body`) | 1 бал |
| 2 | Коректні метатеги `charset="UTF-8"` та адаптивний `viewport` | 1 бал |
| 3 | Рівно один заголовок `<h1>` та 4 тематичні підзаголовки `<h2>` | 1 бал |
| 4 | Текст розбито на змістовні абзаци `<p>` | 1 бал |
| 5 | Квадрати змінних оформлено за допомогою верхнього індексу `<sup>` | 1 бал |
| 6 | Змінні виділено курсивом `<i>` або `<em>` згідно з математичним стандартом | 1 бал |
| 7 | Застосовано спецсимволи `&pi;` та `&times;` у формулах кола | 1 бал |
| 8 | Застосовано спецсимволи `&cap;` та `&isin;` у теорії множин | 1 бал |
| 9 | Створено маркований або нумерований список (`<ul>`/`<ol>` + `<li>`) | 1 бал |
| 10 | Успішна валідація W3C (0 помилок) та відсутність зламаних тегів | 1 бал |

**Разом: 10 / 10 балів**
