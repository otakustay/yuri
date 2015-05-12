# YURI - Yet the Unknown Rich Interface

## Why the Unknown

YURI is named **Y**et the **U**nknown **R**ich **I**nterface because at the time this project is created, we were really trying to explore some unknown fields.

Thanks [ESUI](https://github.com/ecomfe/esui) where we have tried a traditional style of UI kit along with many minor inventions, and all of us are aware that the future of UI kit should live with [HTML imports](https://www.polymer-project.org/platform/html-imports.html), [Shadow DOM](http://webcomponents.org/articles/introduction-to-shadow-dom/), [Custom elements](http://webcomponents.org/articles/introduction-to-custom-elements/) and [Template element](http://webcomponents.org/articles/introduction-to-template-element/), however they are not that realistic these days.

YURI is a little step forward from traditional API-based UI kit to the future web components solutions. YURI should employ many features that ease the develop of rich interfaces, these feature will be introduced later here.

## Basic features

### Written in ES6, use in AMD

YURI from the beginning is ready for edge technoligies, the first to go is to introduce ES6 as the main language, however YURI should be usable under any ES5 envorionment, so we will carefully pick a subset of ES6 features, and the module system should be [AMD](https://github.com/amdjs/amdjs-api).

Other than the ES6, YURI also use [stylus](https://learnboost.github.io/stylus/) as its style solution.

### Behave as control, use as data

Each YURI control is a representation of structured data, which we called **model**. a model is a simple wrap of Object in JavaScript, which exposes a `get` and `set` method along with a `change` event.

YURI control does not expose any more API, it should be used just as a plain model, all UI interactions and paintings are encapsulated under model property changes.

### Binding as first-class feature

Since each YURI control is just an abstraction of model, the visual effects are bound to property changes, which also provides binding mechanics natively.

In YURI we can have one-way binding as well as dual binding, so in all cases we just work with a data model - no UI concerns at all.

We believe this feature enables YURI to work with most of the MVVM frameworks, also it would increase testability and maintainability of large scale projects.

### Customizable templates

YURI controls use templates to render its content, by default we use a target-based template [etpl](https://github.com/ecomfe/etpl).

Every template can be overriden, so the entire appearance is customizable through templates.

In this case YURI controls behaves more like a logic-control, you can design and implement the appearance and YURI takes interactions for you.
