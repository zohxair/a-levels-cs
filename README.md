# 9618 Computer Science Notes

Revision notes, worked examples and exam-style questions with mark schemes for **Cambridge International AS & A Level Computer Science (9618)**. Everything is in a single `index.html` file, with no build step and no dependencies.

## Features

- **All 20 syllabus topics.** AS Level (topics 1 to 12, Papers 1 and 2) and A Level (topics 13 to 20, Papers 3 and 4). Each level has its own overview page.
- **Exam-style questions** for every topic. Each question has a lined answer box, a marks total, and a collapsible mark scheme you can check your answer against.
- **Interactive tools** for practising calculations and algorithms (see the table below).
- **Search** across every section of every topic, with keyboard navigation.
- **Progress tracking.** Mark each topic as revised. Progress shows in the sidebar and on the overview pages.
- **Light and dark themes.** Follows your system setting until you choose one.
- **Code examples** in Cambridge pseudocode, Python, SQL, assembly and Prolog, with syntax highlighting and a copy button.
- **Diagrams** drawn as inline SVG: logic gates, circuits, network topologies, flowcharts, data structures, state diagrams and more.
- **Works on phones.** On narrow screens the topic list becomes a slide-out drawer with a floating "Topics" button.
- **Readable and accessible.** Uses the Atkinson Hyperlegible font, visible keyboard focus, ARIA labels, and respects reduced-motion settings.

## Topics

| # | Topic | Paper | Interactive tool |
|---|-------|-------|------------------|
| 1 | Information representation | 1 | Number converter |
| 2 | Communication | 1 | |
| 3 | Hardware | 1 | Truth table builder |
| 4 | Processor fundamentals | 1 | |
| 5 | System software | 1 | |
| 6 | Security, privacy and data integrity | 1 | |
| 7 | Ethics and ownership | 1 | |
| 8 | Databases | 1 | |
| 9 | Algorithm design and problem-solving | 2 | |
| 10 | Data types and structures | 2 | Sorting stepper |
| 11 | Programming | 2 | |
| 12 | Software development | 2 | |
| 13 | Data representation | 3 | Floating-point workbench |
| 14 | Communication and internet technologies | 3 | |
| 15 | Hardware and virtual machines | 3 | Truth table builder |
| 16 | System software | 3 | RPN converter |
| 17 | Security | 3 | |
| 18 | Artificial intelligence | 3 | Dijkstra stepper |
| 19 | Computational thinking and problem-solving | 3 and 4 | Sorting stepper |
| 20 | Further programming | 3 and 4 | |

### The tools

- **Number converter:** denary, binary, hexadecimal, BCD and two's complement, with the working shown.
- **Truth table builder:** type an expression using `AND`, `OR`, `NOT`, `NAND`, `NOR`, `XOR` (or `.` and `+`) with up to five variables, and get the truth table and sum of products.
- **Sorting stepper:** bubble sort (with a swap flag) and insertion sort, one comparison at a time, on your own values.
- **Floating-point workbench:** converts two's complement mantissa/exponent pairs to denary and back, checks normalisation, and reports overflow, underflow and rounding error.
- **RPN converter:** infix to Reverse Polish Notation, with a step-by-step stack evaluation when the operands are numbers.
- **Dijkstra stepper:** walks through the shortest-path algorithm on a six-node graph.

## Running it

Open `index.html` in any up-to-date browser. That's it.

To publish it, upload `index.html` to any static host (GitHub Pages, Netlify, a school web server, and so on).

An internet connection is only needed for the two Google Fonts. Without it, the page falls back to system fonts and everything else still works.

## Your data

Progress, theme and the last topic viewed at each level are saved in the browser's `localStorage`, under these keys:

| Key | Holds |
|-----|-------|
| `cs9618-progress` | Which topics are marked as revised |
| `cs9618-theme` | `light` or `dark` |
| `cs9618-last` | The last topic opened at each level |

Nothing is sent anywhere. Progress stays in that browser on that device, and clearing the site's data resets it. **Answers typed into the answer boxes are not saved** and are lost when the page reloads.

## Links

Each topic has its own URL, so pages can be bookmarked and shared:

- `#as-0` and `#a-0` are the AS and A Level overviews
- `#as-3` is AS topic 3, `#a-15` is A Level topic 15
- `#as-3--logic-gates` jumps to a section. The part after `--` is the section heading in lower case with spaces and punctuation replaced by hyphens.

## How the file is organised

`index.html` has three parts:

1. **`<style>`**: all the CSS. Colours are custom properties on `:root`, redefined for dark mode. The accent colour switches between teal (AS) and indigo (A Level) through `data-level` on the root element.
2. **`<main>`**: the content, one `<article class="topic">` per topic.
3. **`<script>`**: builds the navigation and runs the interactive parts. It generates the topic headers, the "On this page" contents, the previous/next links, the sidebar, the overview cards, the search index, the answer boxes and the widgets from the article markup, so most edits only touch the content.

## Editing and adding content

### A topic

```html
<article class="topic" id="as-5" data-level="as" data-num="5"
         data-title="System software" data-paper="Paper 1"
         data-subs="5.1 Operating systems|5.2 Language translators">
  <p class="lead">One-paragraph introduction.</p>
  <h2>First section</h2>
  ...
</article>
```

- `id` is `as-N` or `a-N`. `data-num="0"` marks an overview page, which gets no header and isn't counted in progress.
- `data-subs` is a `|`-separated list of syllabus subsections, each starting with its number.
- Topics appear in the sidebar and in previous/next order in the same order as in the file.
- Every `<h2>` becomes a search result and an entry in the "On this page" list (shown when a topic has three or more).

### An exam question

```html
<div class="q">
  <div class="q-top"><span class="q-n">1</span><span class="q-src">Paper 1 style</span></div>
  <div class="q-text">
    <div class="qp"><span class="ql">(a)</span><div>Question text.</div><span class="mk">[2]</span></div>
    <div class="qp"><span class="ql">(b)</span><div>Question text.</div><span class="mk">[1]</span></div>
  </div>
  <details class="ms"><summary>Show mark scheme</summary><div class="ms-body">
    <ul class="ticks"><li>Marking point</li></ul>
    <p class="note">Max 2.</p>
  </div></details>
</div>
```

The answer box and the marks total (added up from each `[n]`) are inserted automatically.

### Code

```html
<pre class="code" data-lang="pseudo">...</pre>
```

`data-lang` can be `pseudo`, `python`, `sql`, `asm`, `prolog`, or `text` for no highlighting. Escape `<` as `&lt;` and `&` as `&amp;` inside code. To support another language, add its keywords to `KW`, built-in functions to `FN`, its comment pattern to `COM`, and its label to `LANG` in the script.

### A widget

```html
<div data-widget="truth" data-expr="(A AND B) OR NOT C"></div>
```

Available widgets: `numconv`, `truth` (with an optional starting `data-expr`), `sort`, `float`, `rpn`, `dijkstra`. To add a new one, define `W.yourname = el => { ... }` in the script, then use `<div data-widget="yourname"></div>`.

### Other building blocks

| Markup | Use |
|--------|-----|
| `<dl class="terms">` | Two-column glossary of key terms |
| `<div class="tip">` / `<div class="tip warn">` | Exam tip / common mistake callout |
| `<table class="tbl">` | Table (wrapped for horizontal scrolling automatically). Add `c` to centre cells, `mono` for monospaced text; `class="hl"` highlights a cell |
| `<figure class="fig">` | Diagram with an optional `<figcaption>` |
| `<span class="ov">A</span>` | Overbar for NOT in Boolean algebra |
| `<use class="gate" href="#g-and" ...>` | Logic gate symbol: `g-and`, `g-or`, `g-not`, `g-nand`, `g-nor`, `g-xor` |

## About the questions

The questions are written in the style of real 9618 papers, testing the same skills and the kinds of answers examiners credit. They are **not** copies of official Cambridge papers. For genuine past papers and mark schemes, use the Cambridge School Support Hub or ask your teacher.

This project is not affiliated with or endorsed by Cambridge University Press & Assessment. Check the notes against the syllabus for your exam year.
