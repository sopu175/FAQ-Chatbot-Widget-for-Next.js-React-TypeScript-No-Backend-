<div align="center">

# @sopu/faq-chatbot

### FAQ Chatbot Widget for Next.js & React

**Add an instant-answer customer support chatbot to your website in minutes. TypeScript-ready, App Router and SSR safe, no backend, no API key.**

[![npm version](https://img.shields.io/npm/v/@sopu/faq-chatbot?style=flat-square)](https://www.npmjs.com/package/@sopu/faq-chatbot)
[![npm downloads](https://img.shields.io/npm/dm/@sopu/faq-chatbot?style=flat-square)](https://www.npmjs.com/package/@sopu/faq-chatbot)
[![bundle size](https://img.shields.io/bundlephobia/minzip/@sopu/faq-chatbot?style=flat-square)](https://bundlephobia.com/package/@sopu/faq-chatbot)
[![TypeScript](https://img.shields.io/badge/TypeScript-ready-3178c6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![license](https://img.shields.io/github/license/{{user}}/faq-chatbot?style=flat-square)](LICENSE)
[![stars](https://img.shields.io/github/stars/{{user}}/faq-chatbot?style=flat-square)](https://github.com/{{user}}/faq-chatbot/stargazers)

[Quick Start](#-quick-start) · [Props](#-props) · [Report Bug](https://github.com/{{user}}/faq-chatbot/issues) · [Request Feature](https://github.com/{{user}}/faq-chatbot/issues)

![FAQ chatbot widget screenshot](./assets/demo.gif)

</div>

---

## 📌 What is @sopu/faq-chatbot?

`@sopu/faq-chatbot` is a free, open-source **FAQ chatbot component for Next.js and React**. It renders a floating chat widget that answers visitors' questions from your own FAQ list.

It works with the **Next.js App Router** and **Pages Router**, is **SSR-safe**, and needs **no database, no OpenAI/ChatGPT key, and no backend**.

**Perfect for:** business websites, landing pages, SaaS products, e-commerce stores, agency and portfolio sites, real-estate and hospitality websites, and any **customer support or help widget**.

## ✨ Features

- ⚡ **Lightweight**: tiny bundle, built with tsup
- 🤖 **FAQ-based chatbot**: instant answers from your own questions
- ⚛️ **Next.js and React ready**: App Router, Pages Router, SSR-safe
- 🟦 **TypeScript support**: fully typed props and exports
- 🎨 **Customizable UI**: title, colors, position, welcome message
- 🌐 **Multi-language**: English, Bangla (বাংলা), or any language
- 📱 **Responsive**: works on mobile, tablet, and desktop
- 🔌 **Zero backend**: no API key, no server, no database
- 🔒 **Privacy-friendly**: no user data leaves the browser

## 🚀 Quick Start

### 1. Install

```bash
npm install @sopu/faq-chatbot
# or
yarn add @sopu/faq-chatbot
# or
pnpm add @sopu/faq-chatbot
```

### 2. Use it (Next.js App Router)

```tsx
// app/layout.tsx
import { FaqChatbot } from "@sopu/faq-chatbot";

const faqs = [
  {
    question: "What are your opening hours?",
    answer: "We are open 9am to 6pm, Sunday to Thursday.",
  },
  {
    question: "How can I contact support?",
    answer: "Email us at support@example.com.",
  },
];

export default function RootLayout({ children }: { children: React.ReactNode }) {
  return (
    <html lang="en">
      <body>
        {children}
        <FaqChatbot faqs={faqs} title="Need help?" />
      </body>
    </html>
  );
}
```

### 3. Client Component note

If you get `You're importing a component that needs useState`, wrap it in a client file:

```tsx
// components/Chatbot.tsx
"use client";
import { FaqChatbot } from "@sopu/faq-chatbot";

export default function Chatbot() {
  return <FaqChatbot faqs={[{ question: "Hi?", answer: "Hello!" }]} />;
}
```

### Pages Router

```tsx
// pages/_app.tsx
import type { AppProps } from "next/app";
import { FaqChatbot } from "@sopu/faq-chatbot";

export default function App({ Component, pageProps }: AppProps) {
  return (
    <>
      <Component {...pageProps} />
      <FaqChatbot faqs={[{ question: "Hi?", answer: "Hello!" }]} />
    </>
  );
}
```

## 📖 Props

| Prop             | Type                                     | Default                   | Description                 |
| ---------------- | ---------------------------------------- | ------------------------- | --------------------------- |
| `faqs`           | `{ question: string; answer: string }[]` | **required**              | List of FAQ entries         |
| `title`          | `string`                                 | `"FAQ Assistant"`         | Chat window title           |
| `welcomeMessage` | `string`                                 | `"Hi! How can I help?"`   | First message shown         |
| `placeholder`    | `string`                                 | `"Type your question..."` | Input placeholder           |
| `position`       | `"bottom-right" \| "bottom-left"`        | `"bottom-right"`          | Widget position             |
| `primaryColor`   | `string`                                 | `"#2563eb"`               | Brand color                 |

> Update this table to match your real props.

## 🧩 Use Cases

- Add a **customer support chatbot** to a Next.js website
- Reduce repetitive support emails with an **automated FAQ assistant**
- Build a **website help widget** without paying for SaaS chat tools
- Ship an **AI-free, privacy-friendly chatbot** with no third-party requests

## 🆚 Why choose it?

| Feature                | @sopu/faq-chatbot | SaaS chat widgets | AI chatbots     |
| ---------------------- | ----------------- | ----------------- | --------------- |
| Free and open source   | ✅                | ❌                | ❌              |
| No API key             | ✅                | ❌                | ❌              |
| Works offline / static | ✅                | ❌                | ❌              |
| Bundle size            | Tiny              | Heavy             | Heavy           |
| Data privacy           | Full              | Third-party       | Third-party     |

## 🛠 Development

```bash
git clone https://github.com/{{user}}/faq-chatbot.git
cd faq-chatbot
npm install
npm run dev     # watch mode
npm run build   # build with tsup
```

## 🤝 Contributing

Contributions are welcome. Look for issues labeled `good first issue`.

1. Fork the repo
2. `git checkout -b feature/my-feature`
3. Commit your changes
4. Push and open a Pull Request

## ❓ FAQ

**Does it need an OpenAI or ChatGPT API key?**
No. It answers from the FAQ list you provide.

**Does it work with the Next.js App Router?**
Yes. It also works with the Pages Router and plain React.

**Does it support TypeScript?**
Yes. Types are included.

**Can I use it in Bangla or other languages?**
Yes. Any language and any Unicode text.

**Is it free for commercial use?**
Yes, MIT licensed.

## 📄 License

MIT © [Sopu](https://github.com/sopu175)

---

<div align="center">

**If this saved you time, please give it a ⭐. It helps other developers find it!**

</div>
