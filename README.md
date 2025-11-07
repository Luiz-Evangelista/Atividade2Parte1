# Atividade2Parte1

#### Nessa primeira parte da segunda atividade, iremos responder algumas pergutas e dar alguns exemploes refetes a elas.

### *1. O que é JSON e por que ele se tornou tão popular para troca de dados entre aplicações?*

*JSON (JavaScript Object Notation)* é um formato leve de *troca de dados* baseado em texto, fácil de *ler e escrever por nós* e fácil de *interpretar por máquinas*.
Ele é usado principalmente para *enviar dados entre um servidor e uma aplicação web*.

* A popularidade do JSON muito se da por conta de sua simplicidade e facilidade de leitura.
   Sua compatibilidade praticamente *todas as linguagens de programação*, ele substituiu o XML em muitas aplicações por ser *mais leve* e *mais rápido* e também ele é *nativo do JavaScript*, o que o torna ideal para aplicações web modernas.

*Exemplo de um codigo em JSON:*
```json
{
  "nome": "Luiz",
  "idade": 20,
  "curso": "TSI"
}
```

---

### *2. Diferença entre JSON.stringify() e JSON.parse()*

Esses dois métodos são usados para converter dados entre objetos JavaScript e JSON.

- *JSON.stringify()* : Converte um *objeto JavaScript em uma string JSON*.
  Usado quando queremos *enviar dados para um servidor* ou *armazenar em um arquivo*.

- *JSON.parse()* : Converte uma *string JSON em um objeto JavaScript*.
  Usado quando *recebemos dados de um servidor* e precisamos *usá-los no código*.

*Exemplos:*
```js
// Objeto JavaScript
const pessoa = { nome: "Luiz", idade: 20 };

// Converter para JSON (string)
const jsonString = JSON.stringify(pessoa);
console.log(jsonString);
// Saída: {"nome":"Luiz","idade":20}

// Converter de volta para objeto
const obj = JSON.parse(jsonString);
console.log(obj.nome);
// Saída: Luiz
```

---
### 3. Considerando a string "JavaScript é baseada em ECMA Script", quais métodos você usaria para:

- **VERIFICAR SE TEM A PALAVRA "SCRIPT".**

```js
const frase = "JavaScript é baseada em ECMA Script";

js
console.log(frase.includes("Script")); // true
```

- **Remover a palavra "JavaScript" e gerar uma nova string:**


```js
const frase = "JavaScript é baseada em ECMA Script";

js
const novaFrase = frase.replace("JavaScript ", "");
console.log(novaFrase);
// Saída: "é baseada em ECMA Script"
```

- **Substituir "baseada" por "tem origem":**

```js
const frase = "JavaScript é baseada em ECMA Script";


js
const fraseAlterada = frase.replace("baseada", "tem origem");
console.log(fraseAlterada); 
// Saída: "JavaScript é tem origem em ECMA Script"
```

---
### *4. Quais as vantagens de usar Template Strings (``) em vez de concatenação com + para criar strings complexas?*

As *Template Strings* (ou *Template Literals) permitem criar strings de forma mais **legível e dinâmica, usando **crases (``)* no lugar das aspas.

*Vantagens:*
- Permitem inserir variáveis e expressôes diretamente com ${}
- Aceitam múltiplas linhas sem precisar usar \n
- Faz o código ser mais limpo,legível e organizado 
- Facilitama manutenção e reduzem erros de concatenação
- São o padrão moderno do JavaScript


*Exemplo com concatenação (+):*
```js
const nome = "Luiz";
const idade = 20;
const texto = "Meu nome é " + nome + " e tenho " + idade + " anos.";
console.log(texto);
```

*Exemplo com Template String (``):*
```js
const nome = "Luiz";
const idade = 20;
const texto = `Meu nome é ${nome} e tenho ${idade} anos.`;
console.log(texto);
```

Em geral, as Template Strings facilitam a vida de nós programadores,<br/> 
a concatenação com + é um jeito mais antigo, em que a gente precisa ficar abrindo e fechando aspas e colocando o sinal de + toda hora,<br/> 
totalmente diferente das  Template Strings que só precisamos colocar as crases e colocar as variáveis direto dentro do texto <br/> 
usando ${}, organizando e facilitando a leitura.

