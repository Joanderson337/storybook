# Projeto Storybook + Vite (com TypeScript)

Este repositório contém um projeto configurado para usar **Storybook** em conjunto com **Vite** e **TypeScript**, oferecendo uma experiência de desenvolvimento moderna, rápida e tipada.

## 🚀 Tecnologias Utilizadas

- [Storybook](https://storybook.js.org/) - Ferramenta para criação de UI components.
- [Vite](https://vitejs.dev/) - Builder rápido e moderno para projetos web.
- [TypeScript](https://www.typescriptlang.org/) - Superset do JavaScript para tipagem estática.

## 📦 Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```

2. Instale as dependências:
   ```bash
   cd seu-repositorio
   npm install
   ```

## 🛠 Configuração

Este projeto já vem pré-configurado para utilizar **Storybook** com o **Vite** e **TypeScript**.

### Configuração do Storybook

O arquivo de configuração principal do Storybook está localizado em:  
`/.storybook/main.ts`  

Exemplo de configuração para usar o Vite com TypeScript:
```typescript
import type { StorybookConfig } from '@storybook/react-vite';

const config: StorybookConfig = {
  framework: '@storybook/react-vite',
  stories: ['../src/**/*.stories.@(ts|tsx)'],
  addons: ['@storybook/addon-essentials'],
};

export default config;
```

### Configuração do TypeScript

O arquivo de configuração do TypeScript está localizado em `tsconfig.json`.  
Certifique-se de que o `tsconfig.json` inclui os caminhos para os arquivos necessários:

```json
{
  "compilerOptions": {
    "strict": true,
    "jsx": "react",
    "module": "ESNext",
    "target": "ESNext",
    "moduleResolution": "Node",
    "esModuleInterop": true,
    "skipLibCheck": true,
    "types": ["vite/client"]
  },
  "include": ["src", ".storybook"]
}
```

### Estrutura do Projeto

```plaintext
├── .storybook/         # Configurações do Storybook
│   ├── main.ts         # Configuração principal
│   ├── preview.ts      # Personalizações globais
├── src/                # Código fonte do projeto
│   ├── components/     # Componentes reutilizáveis
│   └── stories/        # Exemplos de histórias para os componentes
├── package.json        # Dependências e scripts do projeto
├── tsconfig.json       # Configuração do TypeScript
└── vite.config.ts      # Configuração do Vite
```

## 🖥 Executando o Projeto

1. Para iniciar o Storybook:
   ```bash
   npm run storybook
   ```

2. O Storybook estará disponível em: [http://localhost:6006](http://localhost:6006)

## 🔧 Scripts Disponíveis

- `npm run storybook` - Inicia o servidor do Storybook.
- `npm run build-storybook` - Gera a versão estática do Storybook.

## 🤝 Contribuindo

1. Faça um fork do projeto.
2. Crie uma branch para sua feature:
   ```bash
   git checkout -b minha-feature
   ```
3. Faça suas alterações e faça commit:
   ```bash
   git commit -m "Minha nova feature"
   ```
4. Envie suas alterações:
   ```bash
   git push origin minha-feature
   ```

## 📝 Licença

Este projeto está sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.

---

🎉 Aproveite e boas contribuições!
