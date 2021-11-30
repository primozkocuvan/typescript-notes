# Typescript shorts

You need to install node.js to be able to traspile the typescript to javascript. Browser only understand javascript language.

`npm install -g typescript`

### Traspiling or language compiling to javascript

`tsc script.ts`
`tsc script.ts -w`

### Generating tsconfig.json

In your project folder type in the terminal:

`tsc --init`

You can change the `rootDir` and others. Then you can call only `tsc` without any specific file.

### Data types

```typescript
let a: number = 10;
let b: string = "Hello world!";
let c: boolean = false;
```
### Example arrow function - with data types

```typescript
let sum = (a: number, b: number) => {
    return a + b;
}
```

### Union types

One variable can be of two or more types. The `|` symbol is the pipe symbol and means logical or.

```typescript
let a: string|number;
let b: number|string|boolean;
let arr: (string|number)[] = []; 
```

### Any type

To use typescript as javascript, so without datatypes. You can declare it as any type

```typescript
let a: any = 'hello';
a = 32;
a = true;
```

### Type aliases

You can add alias for particular type, or mixed type.

```typescript
type someobj = {name: string, age: number};

// The function receives someobj and returns "Success". The return type is a string.
let somefunction = (obj: someobj): string => {
	return "Success";
}
```

### Optional

You can say to the compiler with the sign '?' after the variable name, that this is optional.

```typescript
func = (a: number, b?: number) => {
	console.log(a);
}

func(10);
```

### Not null 

When selecting an HTML element in the DOM, it can be null so with the sign '!' at the end we prevent from any errors.

```typescript
let ele = document.querySelector('a')!;
```
###  As
By using `as` keyword at the end, we can suggest which type of element we have in the DOM.

```typescript
let ele = document.querySelector('form') as HTMLFormElement;
``` 

### Access modifiers
We have three access modifiers `public`, `private` and `readonly`. The default one is `public`.

```typescript

class Person {
	public name: String;
	private age: number;
	readonly birthday: number;
	
	// At the readonly we cannot change it outside or inside the class. It is fixed.
}

```
