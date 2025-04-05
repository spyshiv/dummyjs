# 🧠 dummytextjs

**dummytextjs** is a lightweight utility to generate realistic dummy text (words, sentences, or paragraphs) for development and testing. It also supports automatic injection of dummy content into HTML elements via the `data-dummy` attribute.

---

## 🚀 Features

- 🔤 Generate random words, sentences, and paragraphs.
- ⚡ Auto-inject dummy content into HTML elements using `data-dummy`.
- ✅ Framework-agnostic – works with **Vue**, **React**, **Angular**, and vanilla JS.
- 💡 TypeScript support out of the box.
- 📦 Lightweight and zero dependencies.

---

## 📦 Installation

```bash
npm install dummytextjs
```

---

## ✨ Usage

### 📥 Import API

```ts
import {
  generateWords,
  generateSentences,
  generateParagraphs,
  autoInjectDummyContent
} from "dummytextjs";
```

---

## 🧩 Framework Usage Examples

### ✅ Vue

#### Manual

```vue
<template>
  <div>{{ dummyText }}</div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { generateWords } from "dummytextjs";

const dummyText = ref("");

onMounted(() => {
  dummyText.value = generateWords(10);
});
</script>
```

#### Auto Inject

```vue
<template>
  <div data-dummy="3p"></div>
</template>

<script setup>
import { onMounted } from "vue";
import { autoInjectDummyContent } from "dummytextjs";

onMounted(() => {
  autoInjectDummyContent();
});
</script>
```

---

### ⚛️ React

#### Manual

```tsx
import React, { useEffect, useState } from "react";
import { generateSentences } from "dummytextjs";

function App() {
  const [text, setText] = useState("");

  useEffect(() => {
    setText(generateSentences(5));
  }, []);

  return <div>{text}</div>;
}

export default App;
```

#### Auto Inject

```tsx
import React, { useEffect } from "react";
import { autoInjectDummyContent } from "dummytextjs";

function App() {
  useEffect(() => {
    autoInjectDummyContent();
  }, []);

  return (
    <div>
      <h2 data-dummy="2s"></h2>
      <p data-dummy="3p"></p>
    </div>
  );
}

export default App;
```

---

### 🅰️ Angular

#### Manual

```ts
import { Component, OnInit } from "@angular/core";
import { generateParagraphs } from "dummytextjs";

@Component({
  selector: "app-dummy",
  template: `<div [innerHTML]="dummyText"></div>`
})
export class DummyComponent implements OnInit {
  dummyText = "";

  ngOnInit(): void {
    this.dummyText = generateParagraphs(2);
  }
}
```

#### Auto Inject

```ts
import { Component, AfterViewInit } from "@angular/core";
import { autoInjectDummyContent } from "dummytextjs";

@Component({
  selector: "app-auto-dummy",
  template: `<div data-dummy="5p"></div>`
})
export class AutoDummyComponent implements AfterViewInit {
  ngAfterViewInit(): void {
    autoInjectDummyContent();
  }
}
```

---

## 🔠 `data-dummy` Attribute Syntax

The `data-dummy` attribute supports the following formats:

| Syntax | Meaning      |
| ------ | ------------ |
| `5w`   | 5 words      |
| `3s`   | 3 sentences  |
| `2p`   | 2 paragraphs |

These values can be used to instruct `autoInjectDummyContent()` to replace the content of elements dynamically.

---

## 📘 API Reference

### `generateWords(count: number): string`

Generates the specified number of random words.

### `generateSentences(count: number): string`

Generates the specified number of random sentences.

### `generateParagraphs(count: number): string`

Generates the specified number of random paragraphs.

### `autoInjectDummyContent(): void`

Automatically finds elements with the `data-dummy` attribute and injects dummy text into them.

---

## 🛠 Example HTML (Vanilla JS)

```html
<body>
  <h1 data-dummy="2s"></h1>
  <p data-dummy="1p"></p>

  <script type="module">
    import { autoInjectDummyContent } from "dummytextjs";

    autoInjectDummyContent();
  </script>
</body>
```

---

## 📄 License

MIT

---

## ✨ Author

Created with 💻 by [@spyshiv](https://github.com/spyshiv)
