# Getting Started with Angular
Following the [getting started page][getting-started] (tested on **Angular 15**):

```terminal
$ sudo npm install -g @angular/cli
$ npm new <app-name>  # create a workspace with a root app
$ ng serve --open     # deploy app & open browser to serve it
```

[getting-started]: https://angular.io/guide/setup-local#install-the-angular-cli

# Angular notions
## Workspace
- A collection of projects (applications) makes a workspace.
- The root-level application files located in `/src` folder.

## Component
- Mediate between view (template to render) and application logic (model) for user experience.

## Service
- For tasks not involving view or model, e.g. fetch data from server, validate user input, logging...
- Available to any component through dependecy injection.

## Interceptors
- Transforms request before passing it to next interceptor.
- Very similar to Expressjs' middlewares.

## Modules
- Container for cohesive code, containing components, services...
- Role: Defines the root component, associate routes with components, registers componentts and services...
- e.g. root module: app.module.ts

## Pipes
- Used in templates to transform text (e.g. to lower/uppercase, format number as a currency...).
- Similar to Django templates's filters, and also applied with pipe (|) symbol.

## Resolve
- Used to pre-fetch the data before the router navigates to a component.

## Directives
- **Attribute directives:** changes the behavior/appearance of template DOM elements (e.g. ngClass, ngStyle...).
- **Structural directives:** changes the DOM layout by adding/removing DOM elements (e.g. \*ngIf, \*ngFor...).

## Binding
- **Property binding:** Moves value in component class property into DOM element property (using brackets: `[src]="variable"`).
- **Event binding:** Binds an event on a DOM element to a component class method (using parentheses: `(click)="function"`).
- **Two-way binding:** Combines two latter bindings by listening for events and updating values simultaneously. IOW, the field value establishes the initial value, while a method responds to events (``).
