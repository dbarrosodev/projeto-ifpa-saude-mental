# 🧠 App Saúde Mental — IFPA

Aplicativo mobile de saúde mental desenvolvido como projeto acadêmico do **IFPA** (Instituto Federal do Pará). O app conecta pacientes a profissionais da saúde mental, permitindo a busca por especialistas, agendamento de consultas e gerenciamento de perfil — tudo de forma simples e acessível.

---

## 📱 Funcionalidades

| Funcionalidade | Descrição |
|---|---|
| **Autenticação por perfil** | Tela inicial que diferencia o fluxo entre **profissional da saúde** e **paciente** |
| **Login & Cadastro** | Telas de login e registro para usuários comuns (pacientes) |
| **Login Profissional** | Tela de login exclusiva para profissionais da saúde mental |
| **Tela Home** | Dashboard principal com menu de navegação rápida |
| **Listagem de Doutores** | Catálogo dos profissionais disponíveis com nome e especialidade |
| **Agendamento de Consultas** | Seleção de duração e horário para agendar consultas |
| **Perfil do Usuário** | Visualização e gerenciamento dos dados pessoais |

---

## 🛠️ Tecnologias

- **[React Native](https://reactnative.dev/)** — Framework para desenvolvimento mobile cross-platform
- **[Expo SDK 53](https://expo.dev/)** — Plataforma de desenvolvimento e build
- **[Expo Router](https://docs.expo.dev/router/introduction/)** — Roteamento baseado em arquivos (file-based routing)
- **[TypeScript](https://www.typescriptlang.org/)** — Tipagem estática para JavaScript
- **[React Navigation](https://reactnavigation.org/)** — Navegação com Bottom Tabs
- **[EAS Build](https://docs.expo.dev/build/introduction/)** — Build nativo na nuvem (Android APK / iOS)

---

## 📂 Estrutura do Projeto

```
app-saude-mental/
├── app/
│   ├── index.tsx                  # Tela inicial (seleção de perfil)
│   ├── _layout.tsx                # Layout raiz com Stack Navigator
│   ├── +not-found.tsx             # Tela 404
│   ├── (common_user)/             # Fluxo do paciente
│   │   ├── login.tsx              # Login do paciente
│   │   └── register.tsx           # Cadastro do paciente
│   ├── (professional)/            # Fluxo do profissional
│   │   └── login.tsx              # Login do profissional
│   └── (tabs)/                    # Navegação principal (Bottom Tabs)
│       ├── home.tsx               # Tela Home
│       ├── doctors.tsx            # Listagem de doutores
│       ├── appointment.tsx        # Agendamento de consultas
│       └── profile/
│           └── profile.tsx        # Perfil do usuário
├── components/
│   ├── BodyIcons.tsx              # Ícones do menu principal
│   ├── Buttons.tsx                # Componentes de botão reutilizáveis
│   ├── Header.tsx                 # Componente de cabeçalho
│   ├── Inputs.tsx                 # Campos de entrada
│   ├── Modal.tsx                  # Componente de modal
│   ├── SearchBar.tsx              # Barra de pesquisa
│   └── UserContext.tsx            # Contexto global do usuário (React Context)
├── assets/
│   ├── fonts/                     # Fontes customizadas
│   └── images/                    # Imagens e ícones do app
├── app.json                       # Configuração do Expo
├── eas.json                       # Configuração do EAS Build
├── package.json                   # Dependências e scripts
└── tsconfig.json                  # Configuração do TypeScript
```

---

## 🚀 Como Executar

### Pré-requisitos

- **[Node.js](https://nodejs.org/)** (v18 ou superior)
- **[npm](https://www.npmjs.com/)** ou **[yarn](https://yarnpkg.com/)**
- **[Expo CLI](https://docs.expo.dev/get-started/installation/)** (instalado globalmente ou via `npx`)
- **[Expo Go](https://expo.dev/go)** no celular (para testes rápidos)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/dbarrosodev/projeto-ifpa-saude-mental.git

# Entre na pasta do projeto
cd projeto-ifpa-saude-mental

# Instale as dependências
npm install
```

### Executando o App

```bash
# Inicie o servidor de desenvolvimento
npx expo start
```

Após iniciar, você pode abrir o app:

- 📱 **Expo Go** — Escaneie o QR Code com o app Expo Go (Android/iOS)
- 🤖 **Emulador Android** — Pressione `a` no terminal
- 🍎 **Simulador iOS** — Pressione `i` no terminal (somente macOS)
- 🌐 **Navegador Web** — Pressione `w` no terminal

### Build de Produção (APK)

```bash
# Gere o APK para Android via EAS
eas build --profile preview --platform android
```

---

## 📋 Scripts Disponíveis

| Script | Comando | Descrição |
|---|---|---|
| `start` | `npm start` | Inicia o servidor de desenvolvimento Expo |
| `android` | `npm run android` | Inicia no emulador/dispositivo Android |
| `ios` | `npm run ios` | Inicia no simulador iOS |
| `web` | `npm run web` | Inicia no navegador |
| `lint` | `npm run lint` | Executa o ESLint para análise de código |

---

## 🤝 Contribuindo

1. Faça um **fork** do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/minha-feature`)
3. Faça commit das alterações (`git commit -m 'feat: adiciona minha feature'`)
4. Faça push para a branch (`git push origin feature/minha-feature`)
5. Abra um **Pull Request**

---

## 📄 Licença

Este projeto está sob a licença **MIT**. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 👥 Autores

- **Daniel** — [@dbarrosodev](https://github.com/dbarrosodev)

---

<p align="center">
  Feito com 💙 no IFPA
</p>
