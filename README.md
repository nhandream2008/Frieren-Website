# Frieren Landing Page – React + TypeScript + Vite

<img width="1904" height="1071" alt="image" src="[https://github.com/user-attachments/assets/6c0ca0a4-68b6-486a-ba52-9c67f339bbcc](https://github.com/nhandream2008/profile-assets/blob/main/Screenshot%202025-10-03%20132713.png?raw=true)" />

## 🚀 Cách khởi chạy

```bash
npm install
```

```bash
npm run dev
```

- Cổng mặc định để truy cập là: **http://localhost:5173/**

---

## ✨ Bạn có thiết kế sẵn và cần một dev để biến nó thành sản phẩm?

Xin chào! 👋 Mình là **nhandream**, lập trình viên **fullstack**.  
Mình có thể giúp bạn:
- Biến bản thiết kế (Figma/PSD) thành website hoàn chỉnh, mượt mà.  
- Hoặc phát triển toàn bộ hệ thống web/app theo yêu cầu.  

Nếu bạn quan tâm, hãy liên hệ mình:  
📩 **nhandreamowo@gmail.com**

---

## 🧩 Về Template Vite

Template này cung cấp cấu hình tối giản để chạy **React** trên **Vite** với **HMR** (Hot Module Replacement) và một số rule ESLint cơ bản.

Hiện có hai plugin chính thức:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/tree/main/packages/plugin-react) sử dụng **Babel** cho Fast Refresh  
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/tree/main/packages/plugin-react-swc) sử dụng **SWC** cho Fast Refresh  

---

## 🧠 Mở rộng cấu hình ESLint

Nếu bạn đang phát triển ứng dụng cho môi trường production, nên cập nhật cấu hình để bật các rule lint “type-aware”:

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Các cấu hình khác...

      // Thay tseslint.configs.recommended bằng:
      ...tseslint.configs.recommendedTypeChecked,
      // Hoặc nghiêm ngặt hơn:
      ...tseslint.configs.strictTypeChecked,
      // Tuỳ chọn: rule về phong cách code
      ...tseslint.configs.stylisticTypeChecked,

      // Các cấu hình khác...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // tuỳ chọn khác...
    },
  },
])
```

---

Bạn cũng có thể cài thêm các plugin dành riêng cho React để có rule tốt hơn:

```bash
npm i -D eslint-plugin-react-x eslint-plugin-react-dom
```

Cấu hình trong `eslint.config.js`:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Các cấu hình khác...
      // Rule dành cho React
      reactX.configs['recommended-typescript'],
      // Rule dành cho React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // tuỳ chọn khác...
    },
  },
])
```

---

## ❤️ Made with love by nhandream
