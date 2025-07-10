# Phareyo Ji

In Punjabi when you want someone to buy something for you, you would usually "X phar ke leayo" or "X phareyo dukan to" the "ji" is added to show respect :).

## Core Feature List

[ ] User Authentication: Social sign in with Google, Facebook or WhatsApp
[ ] Create list
[ ] Edit list
[ ] Smart item suggestions
[ ] Add quantity to items
[ ] Add pictures to items
[ ] Share list for collaboration with others
[ ] Offline mode
[ ] Multiple list
[ ] Sections within lists
[ ] Barcode scanner
[ ] Pantry inventory
[ ] Store mapping: Tag items to geo-locations or store names
[ ] Reminders & Notifications: "Don't forget milk!" at the right time and place.
[ ] Voice assistant integration: Add items hands-free via Alexa/Siri/Google.

### UX/UI Considerations

- Simple interface: Minimalist design, easy navigation, quick add/remove buttons.
- Drag-and-Drop: Rearrange item order easily.
- Dark Mode: Because no one likes blinding whites at night.
- Accessibility: Voiceover compatibility, readable fonts, contrast options.

### Security & Sync

- Cloud syncing
- Data privacy: Compliant with GDPR and respectful of user data.

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      ...tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      ...tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      ...tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
