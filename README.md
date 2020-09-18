# 💻 Dicas Javascript

Olá! Minha intenção com esse repositório é acumular conhecimento (Seja o que eu aprendi durante meu tempo de desenvolvimento,
como também de referências de vídeos e artigos que encontro durante meus estudos, afim de ter uma referência rápida, e uma boa
leitura para iniciantes, bem como desenvolvedores avançados!


## :clipboard: Sumário

[Performance com grande quantidade de Dados](#JSON-Parse)
[Transformar Objeto em Array](#Transformar-Objeto-em-Array)
[Transformar Array em Objeto](#Transformar-Array-em-Objeto)

## JSON Parse
const data = { user: 'Daniel', email: 'email@provider.com', ... } + 10000

Como deixar o uso desses dados mais performático?

### Server-Side Rendering 

O servidor contém o dado processado, e não necessita do javascript para o carregamento inicial,
e não precisa carregar esses dados totalmente

### JSON.parse

Quando os dados PODEM ser representados através de um JSON, ao invés de trabalhar com os dados de forma literal,
pode-se tornar em uma string literal, e passá-las por JSON.parse, com 

const data = JSON.parse('{ user: 'Daniel', email: 'email@provider.com', ... }')

Para uma explicação mais detalhada, veja esse [vídeo](https://www.youtube.com/watch?v=ff4fgQxPaO0) explicativo do Google Chrome Developers: 


## Transformar Objeto em Array

Digamos que você queira pegar o nome do objeto, ou o valor que ele tenha e transformar esses dados em um array. Podemos fazer isso de duas formas:

Pegando as chaves dos valores:
```javascript
const object = {
 a: 1, b: 2, c: 3, d: 4
}

const arrayOfPropertyNames = Object.keys(object)

console.log(arrayOfPropertyNames) // [ "a" , "b" , "c" , "d"]
```
Ou, por outro lado, podemos pegar os valores dessas propriedades: 

```javascript
const object = {
 a: 1, b: 2, c: 3, d: 4
}

const arrayOfPropertyValues = Object.values(object);

console.log(arrayOfPropertyValues) // [1, 2, 3, 4]
```

## Transformar Array em Objeto

Da mesma forma que podemos transformar um objeto em array, podemos transformar um array em um objeto!

```javascript
const array = [{a: 1}, { b: 2}, { c: 3}];

const objectOfArrays = Object.assign({}, ...array);

console.log(objectOfArrays); // { a: 1, b: 2, c: 3}
```
