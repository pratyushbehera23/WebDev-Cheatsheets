# TypeScript

```ts
/*
    Data Types
    Unions
    Interface
    ...
*/

// Types 
const myName:string = 'Pratyush';
let id:number = 23;
let isDev:boolean = true;


// Unions 
let gender: 'male'|'female';
gender = 'male';


// Interface 
interface Person{
    name:string
    age:number
    gender:'male'|'female'
    isFit?:boolean
}

let naruto:Person = {
    name:'Naruto',
    age:27,
    gender:'male',
    // isFit:true
}

let sasuke:Partial<Person> = {
    name:'Sasuke',
    gender:'male'
}


// Functions
const sum = (x:number, y:number):number => {
    return x+y;
}
sum(2,3);


// 
```
