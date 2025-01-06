# ft_transcendence FRONTEND

Frontend for the ft_transcendence game.

## Development

### Page routing

The page routing is handled by a view file (src/views/\<page\>.html) and it's controller (src/controllers/\<page\>Ctrl.js).
The configuration is done in the `app.js` file (see `ROUTES` and `DEFAULT_ROUTE` variables).

#### Controllers

Controllers are used to handle the logic of the page.
They are used to bind events and to initialize the page.

Example:

```js
// src/controllers/homeCtrl.js
/** @type {Controller} */
export default class Controller {
	titleSuffix = "Home";

	init(){
		console.log("Home Controller");
		this.#bindEvents();
	};

	#bindEvents(){
		// Bind events here
	};
}
```

#### Views

Views are used to display a page. They are html files that will be handled by the controllers.

---

### Translations

Translations are stored in the `i18n` folder.
To use a translation in html, use the `data-i18n` attribute.

Example:

```html
<h1 data-i18n="homepage-welcome">Welcome to the Home Page</h1>
```

To add a new translation, add a new key + value to all the languages in the `i18n` folder.
If there is no translation for a language, element's content will be displayed as the default value.