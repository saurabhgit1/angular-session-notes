# Template Variables

## Definition - [Angular Doc](https://angular.dev/guide/templates/reference-variables#)

1. Template variables helps to use data from one part of template in another part of template.
It helps us to gain access to part of our template.
2. Can refer following -
   - A DOM element within a template.
   - A directive or component.
   - A Template Ref.
   - A web Component.

## Syntax

- Use # symbol to declare a template variable.

  ```html
  <input #phone placeholder="phone number" />
  <button type="button" (click)="callPhone(phone.value)">Call</button>
  <!-- phone refer to the input element -->
  ```

## How Angular assigns values to Template Variables
- Angular assigns value based on where we declare.
1. component - Refers to the component Instance
2. HTML Tag - Refers to the element
3. ng-template - Refers to a templateRef Instance which represent the template.

## Variable specifying a name
- We can explicitly bind a reference to the directives
    ```html
    <input type="text" ngModel #coffee="ngModel">
    ```

## Template Variables Scope
- Are scoped to the template that declares them.
- ngIf, ngFor or ng-template create new nested template scope.

### Accessing in a nested template
1. ```html
    <input #ref1 type="text" [(ngModel)]="firstExample" />
    @if (true) {
        <span>Value: {{ ref1.value }}</span>
    }
    ```
2. ```html
    <input *ngIf="true" #ref2 type="text" [(ngModel)]="secondExample" />
    <span>Value: {{ ref2?.value }}</span> <!-- doesn't work -->
    ```
### Accession in the ts file
- Using View Child - Returns first matching element.
- Using View Children - Return a Query List Array with all matching elements.
# Template Input Variables
- It's a variable with a value that is set when instance of that template is created.

```html
<ul>
  <li *ngFor="let hero of heroes; let i = index">
    {{ i }}: {{ hero.name }}
  </li>
</ul>
```

