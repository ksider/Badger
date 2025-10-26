# Bly (2025)

A modern offline badge generator for conferences and events — built to run entirely **in your browser**.  
No servers, no dependencies: all data and custom templates are stored in `localStorage`, so you can simply open `index.html` and start designing.

## Features

- Import participants from JSON and search instantly.  
- Edit, duplicate, bulk-delete, or highlight attendees.  
- Fully customizable page and badge sizes with automatic print grid calculation.  
- Multiple built-in templates + visual editor for creating your own (HTML/CSS + field mapping).  
- Export participants back to JSON or reset all settings/templates in one click.  
- Print-ready: `@media print` hides the UI and displays only badge pages.

## Project Structure

```
index.html                 — main interface
assets/css/main.css        — global styles and layout for dialogs/panels
assets/js/                 — app logic (ES modules)
  ├─ main.js               — entry point and DOM operations
  ├─ state.js              — state management and events
  ├─ storage.js            — namespaced localStorage wrapper
  ├─ template-manager.js   — built-in and user-defined templates
  └─ utils.js              — rendering and helper functions
templates/                 — built-in template markup + styles
old_dist/                  — archived previous version
```

## Getting Started

1. Open `index.html` locally or via any static hosting.  
2. Choose a template — the preview updates automatically.  
3. Import a participant list in JSON or add people manually.  
4. Adjust page size, orientation, and margins as needed.  
5. Click **Print** — your browser’s print dialog will handle the rest.

### JSON Import Format

Use an array of objects where keys match template fields:

```json
[
  { "name": "Alexander Ivanov", "company": "RBC", "role": "Speaker" },
  { "name": "Ekaterina Smirnova", "company": "Yandex", "role": "Attendee" }
]
```

## Custom Templates

The **Customize Template** dialog lets you:

- Edit the name, description, and badge dimensions.  
- Modify available fields (`id` → `{{id}}` in markup).  
- Directly edit HTML and CSS in the browser.  

Saved templates are marked with a `•` in the dropdown list — you can edit or delete them anytime.

## Reset & Backup

- **Reset Settings** — restores page layout defaults.  
- **Clear List** — removes all participants (keeps templates).  
- **Reset All** — clears `localStorage` completely, removing participants, settings, and templates.  
- The previous release is available in `old_dist/`.

## Browser Support

Bly uses modern web APIs (`ES Modules`, `<dialog>`, Flexbox, Grid`).  
For the best experience, use the latest versions of **Chrome**, **Edge**, **Firefox**, or **Safari**.

## Contributing

Contributions are welcome!  
If you find a bug, want to suggest a feature, or improve the UI/UX, feel free to open an issue or a pull request on GitHub.

**Recommended setup:**
- Works without a server and in offline mode
- Keep commits clean and descriptive.
- Follow existing code style (ES modules, modern JS).

## Roadmap

- [ ] Add QR code and image field support  
- [ ] Expand built-in template library  
- [ ] Add drag-and-drop participant import  
- [ ] Enable theme customization  
- [ ] Create PWA version with offline caching  

## License

Licensed under the **MIT License**.  
© 2025 Bly contributors.

---

🧩 **Bly — generate and print smart badges directly from JSON, no backend required.**
