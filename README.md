# cookin-up

Este modelo deve ajudá-lo a começar a desenvolver com o Vue 3 no Vite.

## Configuração recomendada do IDE

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (e desativar Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Suporte de tipo para importações .vue no TS

O TypeScript não pode manipular informações de tipo para importações `.vue` por padrão, então substituímos o CLI `tsc` por `vue-tsc` para verificação de tipo. Em editores, precisamos do [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) para tornar o serviço de linguagem TypeScript ciente dos tipos `.vue`.

O TypeScript não pode manipular informações de tipo para importações .vue por padrão, portanto, substituímos a CLI tsc por vue-tsc para verificação de tipo. Nos editores, precisamos do [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) para tornar o serviço de linguagem TypeScript ciente dos tipos .vue.

Se o plugin TypeScript autônomo não parecer rápido o suficiente para você, o Volar também implementou um [Modo Take Over](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) que é mais eficiente. Você pode ativá-lo seguindo estas etapas:

1. Desative a Extensão TypeScript integrada
    1) Execute `Extensions: Show Built-in Extensions` no painel de comandos do VSCode
    2) Encontre `TypeScript and JavaScript Language Features`, clique com o botão direito e selecione `Disable (Workspace)`
2. Recarregue a janela do VSCode executando `Developer: Reload Window` no painel de comandos.

## Configuração Personalizada

Consulte a [Referência de Configuração do Vite](https://vitejs.dev/config/).

## Configuração do Projeto

```sh
npm install
```

### Compilar e Recarregar Automaticamente para Desenvolvimento

```sh
npm run dev
```

### Verificação de Tipos, Compilação e Minificação para Produção

```sh
npm run build
```
# p r o j e t o - c o o k i n - u p 
 
 
