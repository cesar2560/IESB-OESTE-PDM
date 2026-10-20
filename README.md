# Gerenciador de Despesas

Projeto desenvolvido para a atividade prática de expansão do gerenciador de despesas em React Native/Expo.

## O que foi implementado

- Campo `categoria` no modelo de cada despesa.
- Seleção de categoria com `Pressable`.
- Validação de descrição, valor e categoria.
- Validação do valor com `/^\d*\.?\d{0,2}$/`, limitando a duas casas decimais.
- Seleção de data com `@react-native-community/datetimepicker`.
- Categoria exibida como uma tag visual no `DespesaItem.js`.
- Soma feita com `despesas.reduce(...)` no `DespesaSumario.js`.
- Filtro dinâmico feito com `despesas.filter(...)`.
- `DespesaSaida.js` recebe a lista filtrada por props.
- `FlatList` usa `keyExtractor` e o resumo é recalculado de acordo com o filtro.
- Bônus: aviso visual quando o total exibido ultrapassa R$ 200,00.

## Como executar no VS Code

1. Instale o Node.js LTS no computador: https://nodejs.org
2. Abra esta pasta no VS Code.
3. Abra o terminal do VS Code em **Terminal > New Terminal**.
4. Execute:

```bash
npm install
npx expo start
```

5. Para testar no celular, instale o aplicativo **Expo Go**, conecte o celular e o computador à mesma rede Wi-Fi e leia o QR Code mostrado no terminal.
6. Para testar no navegador, pressione `w` no terminal do Expo.

## Como entregar pelo GitHub

### 1. Criar o repositório

1. Acesse https://github.com e entre na sua conta.
2. Clique em **New repository**.
3. Use um nome como `atividade-gerenciador-despesas`.
4. Deixe o repositório público, se a instituição pedir um link acessível.
5. Clique em **Create repository**.

### 2. Enviar o projeto pelo terminal do VS Code

Dentro da pasta do projeto, execute os comandos abaixo. Troque `SEU_USUARIO` pelo seu usuário do GitHub:

```bash
git init
git add .
git commit -m "Implementa categorias e filtro de despesas"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/atividade-gerenciador-despesas.git
git push -u origin main
```

Se o Git solicitar autenticação, faça login pelo navegador ou use o método de autenticação indicado pelo GitHub. Não compartilhe senha ou token no código.

### 3. Conferir a entrega

Abra o endereço:

```text
https://github.com/SEU_USUARIO/atividade-gerenciador-despesas
```

Copie esse link e envie na plataforma da aula. Se a plataforma pedir arquivos em vez de link, compacte a pasta do projeto em `.zip`, sem incluir a pasta `node_modules`.

## Estrutura principal

```text
src/
├── components/
│   └── despesa/
│       ├── DespesaItem.js
│       ├── DespesaLista.js
│       ├── DespesaSaida.js
│       └── DespesaSumario.js
└── screens/
    ├── DespesasRecentes.js
    ├── GerenciarDespesa.js
    └── TodasDespesas.js
App.js
```
