# 9618 Computer Science Notes

A free, interactive revision website for **Cambridge International AS & A Level Computer Science (9618)**. It covers every topic in the syllabus with clear notes, diagrams, worked examples in Cambridge-style pseudocode and Python, interactive tools, and exam-style questions with mark schemes.

The whole site is a single HTML file. There is nothing to install and no build step: open it in a browser, or host it on GitHub Pages.

---

## Features

- **All 20 syllabus topics** in two tabs: AS Level (topics 1–12, Papers 1 and 2) and A Level (topics 13–20, Papers 3 and 4).
- **95 exam-style questions** in the style of Papers 1 to 4. Each has its marks shown, a lined box to write an answer in, and a mark scheme to check it against point by point.
- **55 code examples** in Cambridge-style pseudocode, Python (for Paper 4), SQL, assembly language and Prolog, with syntax highlighting and copy buttons.
- **Diagrams** for logic gates and circuits, CPU architecture, network topologies, flowcharts, stacks, queues, linked lists, binary trees, the TCP/IP stack, process states, half adders, flip-flops and class diagrams.
- **Interactive tools:**
  | Tool | Topic |
  |---|---|
  | Number converter: denary, binary, hexadecimal, BCD and two's complement, with working | 1. Information representation |
  | Truth table builder: type any logic expression to get its truth table and sum of products | 3. Hardware; 15. Boolean algebra |
  | Bubble sort and insertion sort, step by step | 10. Data types and structures; 19. Algorithms |
  | Floating-point workbench: binary to denary, denary to normalised binary, normalisation | 13. Data representation |
  | Reverse Polish Notation converter and stack evaluator | 16. System software |
  | Dijkstra's algorithm, step by step on a weighted graph | 18. Artificial intelligence |
- **Search** across every topic and section.
- **Progress tracking**: mark topics as revised (saved in your browser only).
- **Light and dark themes**, a layout that works on phones, and keyboard navigation.

## Syllabus coverage

The content follows the Cambridge 9618 syllabus for **2026**. The **2027–2029** update changes only administrative details (which papers are taken for each level, and calculator use), not the topics, so the site applies to both.

| AS Level | A Level |
|---|---|
| 1. Information representation | 13. Data representation |
| 2. Communication | 14. Communication and internet technologies |
| 3. Hardware | 15. Hardware and virtual machines |
| 4. Processor fundamentals | 16. System software |
| 5. System software | 17. Security |
| 6. Security, privacy and data integrity | 18. Artificial intelligence |
| 7. Ethics and ownership | 19. Computational thinking and problem-solving |
| 8. Databases | 20. Further programming |
| 9. Algorithm design and problem-solving | |
| 10. Data types and structures | |
| 11. Programming | |
| 12. Software development | |

### Papers

| Paper | Duration | Marks | Topics |
|---|---|---|---|
| 1. Theory Fundamentals | 1 h 30 min | 75 | 1–8 |
| 2. Fundamental Problem-solving and Programming Skills | 2 h | 75 | 9–12 |
| 3. Advanced Theory | 1 h 30 min | 75 | 13–20 |
| 4. Practical | 2 h 30 min | 75 | 19–20 |

## Getting started

### Open it locally

Download `index.html` and double-click it. It opens in any modern browser (Chrome, Edge, Firefox, Safari).

### Host it on GitHub Pages

1. Create a new repository and upload `index.html` (rename `cs9618-computer-science.html` to `index.html` if needed) and this `README.md`.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select the `main` branch and the `/ (root)` folder, then **Save**.
4. After a minute or two, the site is live at `https://<your-username>.github.io/<repository-name>/`.

### Linking to a topic

Every topic and section has its own link, so you can send students straight to it:

```
https://<your-username>.github.io/<repository-name>/#as-4     → AS topic 4, Processor fundamentals
https://<your-username>.github.io/<repository-name>/#a-16     → A Level topic 16, System software
```

`as-0` and `a-0` are the overview pages for each level.

## How it works

- Everything (content, styles and scripts) is in one self-contained HTML file with no frameworks or libraries.
- Diagrams are inline SVG and follow the light or dark theme.
- Fonts (Atkinson Hyperlegible and JetBrains Mono) load from Google Fonts. Offline, the page falls back to system fonts and still works.
- Progress, the last topic visited and the theme choice are stored in the browser's `localStorage`. Nothing is sent to a server.

## Accuracy

Every worked answer and mark-scheme value (binary conversions, file sizes, floating-point values, parity blocks, trace tables, K-maps, scheduling, Dijkstra and A* traces, tree traversals and more) was recomputed independently in code before release. If you spot an error in the content, a code example or a mark scheme, please [open an issue](../../issues) with the topic and question number.

## Contributing

Contributions are welcome, especially new questions, corrections and examples in Java or Visual Basic .NET for Paper 4.

1. Fork the repository and create a branch.
2. Make your change in `index.html`. Each topic is an `<article>` with an id such as `as-8` or `a-19`.
3. Open a pull request describing what you changed and why.

## Disclaimer

This is an independent revision resource. It is **not affiliated with, endorsed by or produced by Cambridge University Press & Assessment**. "Cambridge International" and the syllabus code 9618 are used only to identify the course the notes cover.

The questions are original, written in the style of 9618 examination papers. They are **not** copies of past papers. For official past papers, mark schemes, the pseudocode guide and the current syllabus, use the [Cambridge International website](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-international-as-and-a-level-computer-science-9618/) or ask your teacher.

## License

No license has been chosen yet. Until one is added, all rights are reserved by the repository owner. To let others reuse and adapt the material, add a `LICENSE` file; for example, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) suits educational content.
