# Commands to manage Angular project

1. start dev local server (with hot reload)

```
ng serve
```

- if the port already in use

```
ng serve --port 4300
```

1. build for production (creates optimized output in the dist/ folder)

```
ng build
```

1. create angular components (components, services)

'ng generate' creates structure, naming, and boilerplate:
- <b>component is a piece of UI</b> — typically 3 files: a TypeScript file (logic), an HTML file (template), and an SCSS file (styles).
- <b>service is a class with no UI</b> — it handles calling your backend API, managing shared state, or doing business logic that multiple components need.

```
ng generate component features/customers/customer-form
ng generate service core/services/customer
```
* can use 'c' instead of 'component' and 's' instead of 'service'
