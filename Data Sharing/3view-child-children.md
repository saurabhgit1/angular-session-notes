# View Child and View Children

1. If we want to access DOM elements that are present inside the HTML Template of the same or child component. In that case, we can use View Child and View Children Decorators.

2. Also, if we want to access child component properties and methods, that is possible by using View Child and View Children Decorators.

3. viewchild - The change detector looks for the first element or the directive matching the selector in the view DOM

4. viewchildren - Returns a QueryList containing all matching elemetns

## Example

1. Boiler Plate Examples
2. [read metadata](https://blog.angular-university.io/angular-viewchild/)

## Additional Points

1. Can subscribe to viewChildren - subscribe callback will run whenever there is a update in query list.
2. But can't subscribe to viewChild as it represents the component only

```javascript
@ViewChildren("appchild") public inputchild;
ngAfterViewInit(){
    this.inputchild?.changes?.subscribe((res) => {
        console.log('changes', res);
        });
}
```
