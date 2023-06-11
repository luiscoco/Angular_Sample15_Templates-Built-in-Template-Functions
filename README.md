# built-in-template-functions

In Angular, built-in template functions are predefined functions provided by the framework that can be used directly in Angular templates. These functions allow you to perform various operations and manipulations within the template itself, without the need to write additional code in the component class.

Here's a simple example to illustrate the usage of built-in template functions in Angular:

Let's say you have an Angular component with a property called name which holds a string value. You want to display a greeting message in your template based on the value of name. You can achieve this using the ngIf and toUpperCase() built-in template functions.

In your component class:


```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-greeting',
  template: `
    <div *ngIf="name">
      Hello, {{ name.toUpperCase() }}!
    </div>
  `
})
export class GreetingComponent {
  name: string = 'John';
}
```

In the template above, *ngIf is an Angular structural directive that conditionally renders the div element only if name is truthy (i.e., not null, undefined, or an empty string). Inside the div, the name.toUpperCase() expression is used to convert the value of name to uppercase.

So, when the component is rendered, it will display the greeting message "Hello, JOHN!" because the value of name is 'John'.

Angular provides several other built-in template functions such as ngFor, ngSwitch, date, json, etc. These functions allow you to dynamically generate HTML elements, handle conditional rendering, format data, and perform other operations directly within the template.

Note that built-in template functions are specific to Angular and are distinct from JavaScript functions, although they may share similar names or syntax.
