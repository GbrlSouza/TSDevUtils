# TSDevUtils

**TSDevUtils** é uma biblioteca utilitária projetada para auxiliar desenvolvedores TypeScript em diversas tarefas comuns, como validação de tipos, geração de documentação, análise de segurança, refatoração de código, gerenciamento de estado e muito mais.

Essa biblioteca é modular, permitindo que você use apenas os módulos que precisar para melhorar a produtividade no desenvolvimento com TypeScript.

## Módulos Disponíveis

### 1. **TypeValidator**
Funções utilitárias para validação de tipos em tempo de execução.

#### Métodos:
- `TypeValidator.isString(value: any): boolean`  
  Verifica se o valor é uma string.

- `TypeValidator.isNumber(value: any): boolean`  
  Verifica se o valor é um número.

- `TypeValidator.validateObject(value: any, type: { [key: string]: Function }): boolean`  
  Valida se um objeto corresponde a um tipo específico.

---

### 2. **TypeGenerator**
Gera tipos TypeScript com base em dados JSON dinâmicos.

#### Métodos:
- `TypeGenerator.generateTypeFromJson(json: any): string`  
  Gera uma interface TypeScript a partir de um objeto JSON.

---

### 3. **AsyncFlow**
Controle de fluxo assíncrono com validação de tipos.

#### Métodos:
- `AsyncFlow.process(promise: Promise<T>): Promise<T>`  
  Processa uma promessa e valida seu tipo.

---

### 4. **TypeMapper**
Realiza o mapeamento de tipos entre TypeScript e outras linguagens (ex: Java, Python).

#### Métodos:
- `TypeMapper.toPythonType(tsType: string): string`  
  Converte tipos de TypeScript para tipos Python.

---

### 5. **DocGenerator**
Gera documentação a partir de funções e comentários no código.

#### Métodos:
- `DocGenerator.generateDocumentation(types: any): string`  
  Gera documentação simples a partir de tipos definidos no código.

---

### 6. **Refactorer**
Realiza refatoração simples de código.

#### Métodos:
- `Refactorer.refactorCode(code: string): string`  
  Refatora o código removendo espaços extras.

---

### 7. **TestAutomation**
Gera casos de teste automaticamente com base no código.

#### Métodos:
- `generateTestCases(code: string): string[]`  
  Gera casos de teste a partir das funções presentes no código.

---

### 8. **TypeTranslation**
Converte código de Java para TypeScript com mapeamento básico de tipos.

#### Métodos:
- `convertJavaToTS(javaCode: string): string`  
  Converte código Java para TypeScript.

---

### 9. **StateManager**
Gerenciador de estado simples para rastrear e atualizar estados.

#### Métodos:
- `createStateManager(initialState: object)`  
  Cria um gerenciador de estado com métodos `get` e `update`.

---

### 10. **SecurityAnalyzer**
Analisa padrões inseguros no código.

#### Métodos:
- `analyzeSecurity(code: string): string[]`  
  Realiza uma análise básica de segurança, como identificar o uso de `eval()`.

---

### 11. **Explicação dos Módulos (Resumo)**

- **TypeValidator**: Fornece métodos estáticos para validação de tipos em tempo de execução.
- **TypeGenerator**: Gera tipos TypeScript com base em dados JSON dinâmicos.
- **AsyncFlow**: Controla o fluxo assíncrono de promessas, com validação de tipos.
- **TypeMapper**: Mapeia tipos de TypeScript para outras linguagens (ex: Java para Python).
- **DocGenerator**: Gera documentação básica a partir de funções e comentários no código.
- **Refactorer**: Um módulo básico para refatoração de código, com um exemplo simples.
- **TestAutomation**: Gera casos de teste automaticamente com base no código.
- **TypeTranslation**: Converte código Java para TypeScript (com mapeamento básico de tipos).
- **StateManager**: Cria um gerenciador de estado simples para rastrear e atualizar estados.
- **SecurityAnalyzer**: Realiza uma análise simples do código para encontrar padrões inseguros, como o uso de `eval()`.

---

## Instalação

Você pode adicionar a biblioteca diretamente ao seu projeto TypeScript copiando o código para um arquivo, como `TSDevUtils.ts`. Caso deseje publicar no npm, basta empacotar o código com ferramentas como `webpack` ou `rollup`.

```bash
# Com npm
npm install tsdevutils
```

## Exemplo de Uso

```typescript
import { TSDevUtils } from './TSDevUtils';

// Exemplo de validação de tipo
const isString = TSDevUtils.TypeValidator.isString('hello'); // true

// Exemplo de geração de documentação
const docs = TSDevUtils.DocGenerator.generateDocumentation({
  myFunction: 'function description',
});
console.log(docs);

// Exemplo de gerenciamento de estado
const stateManager = TSDevUtils.StateManager.createStateManager({ count: 0 });
stateManager.update('count', 10);
console.log(stateManager.get('count')); // 10
```

## Como Utilizar a Biblioteca:

1. **Instalação**:
   - Crie um arquivo `TSDevUtils.ts` e cole o código acima.
   - Para utilizar no seu projeto, basta importar os módulos desejados.

   ```typescript
   import { TSDevUtils } from './TSDevUtils';

   // Exemplo de uso:
   const testCases = TSDevUtils.TestAutomation.generateTestCases('function myFunction() {}');
   console.log(testCases);
   ```

2. **Publicação**:
   - Caso queira publicar no `npm`, você pode empacotar o código utilizando ferramentas como `webpack` ou `rollup`.
   - Adicione um `package.json` com as informações do projeto, como nome, versão, descrição, etc.

3. **Documentação**:
   - Use os módulos da biblioteca para melhorar seu fluxo de trabalho no desenvolvimento TypeScript, gerando documentação, gerenciando estado, criando testes automáticos e muito mais.

---

## Contribuindo

1. Fork este repositório.
2. Crie uma branch para sua feature (`git checkout -b feature/nome-da-feature`).
3. Faça commit das suas mudanças (`git commit -am 'Adiciona nova feature'`).
4. Envie para o repositório (`git push origin feature/nome-da-feature`).
5. Crie um Pull Request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

## Contato

Se você tiver dúvidas ou sugestões, sinta-se à vontade para abrir uma **issue** ou enviar um **pull request**. Você também pode me encontrar nas redes sociais ou enviar um e-mail.

---

**TSDevUtils** foi criado para ajudar desenvolvedores TypeScript a realizar tarefas do dia a dia de maneira mais eficiente e com menos código boilerplate.
