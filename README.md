# 💻 Dicas Javascript

Olá! Minha intenção com esse repositório é acumular conhecimento (Seja o que eu aprendi durante meu tempo de desenvolvimento,
como também de referências de vídeos e artigos que encontro durante meus estudos, afim de ter uma referência rápida, e uma boa
leitura para iniciantes, bem como desenvolvedores avançados!


## :clipboard: Sumário

[Performance com grande quantidade de Dados](#JSON-Parse)

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
