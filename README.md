# AplicacaoNASA
Aplicação NASA Open APIs

Aplicação web em HTML, CSS e JavaScript (sem framework) que consome a API **APOD** (Astronomy Picture of the Day) da NASA, com três páginas: **Home**, **APOD** e **Contato**.

Referência: [Épico P0 — issue #1](https://github.com/sabrinauniville/univille-2026-2-1441AN-1111AN/issues/1) e as tarefas [#2 Home](https://github.com/sabrinauniville/univille-2026-2-1441AN-1111AN/issues/2), [#3 Contato](https://github.com/sabrinauniville/univille-2026-2-1441AN-1111AN/issues/3) e [#4 APOD](https://github.com/sabrinauniville/univille-2026-2-1441AN-1111AN/issues/4).

## Estrutura do projeto

```text
.
├── index.html                  # página Home (tarefa #2)
├── index.css                   # estilos da Home
├── pages/
│   ├── apod/                   # página APOD (tarefa #4)
│   │   ├── apod.html
│   │   ├── apod.css
│   │   └── apod.js
│   └── contact/                # página Contato (tarefa #3)
│       ├── contact.html
│       ├── contact.css
│       └── contact.js
├── scripts/
│   ├── build/
│   │   └── build.js            # build para produção
│   ├── dev/
│   │   └── dev-server.js       # servidor local (npm run dev)
│   ├── services/
│   │   └── service.js          # comunicação com a API da NASA
│   ├── shared/                 # funções compartilhadas
│   │   ├── date.js
│   │   ├── page-state.js
│   │   └── validation.js
│   └── utils/                  # utilitários reutilizáveis
│       ├── date.js
│       ├── format.js
│       ├── page-state.js
│       └── validation.js
└── styles/
    ├── design-tokens.css       # cores, fontes, espaçamentos
    ├── styles.css              # estilos globais
    └── components/
        ├── header.css          # cabeçalho e navegação
        └── footer.css          # rodapé
```

## Passos para criar a estrutura

1. Clonar o repositório e entrar na pasta:

   ```bash
   git clone <url-do-repositorio>
   cd AplicacaoNASA
   ```

2. Criar as pastas das páginas:

   ```bash
   mkdir -p pages/apod pages/contact
   ```

3. Criar as pastas de estilos:

   ```bash
   mkdir -p styles/components
   ```

4. Criar as pastas de scripts:

   ```bash
   mkdir -p scripts/build scripts/dev scripts/services scripts/shared scripts/utils
   ```

5. Criar os arquivos da Home e dos estilos:

   ```bash
   touch index.html index.css \
     styles/design-tokens.css styles/styles.css \
     styles/components/header.css styles/components/footer.css
   ```

6. Criar os arquivos das páginas APOD e Contato:

   ```bash
   touch pages/apod/apod.html pages/apod/apod.css pages/apod/apod.js \
     pages/contact/contact.html pages/contact/contact.css pages/contact/contact.js
   ```

7. Criar os arquivos de scripts:

   ```bash
   touch scripts/build/build.js scripts/dev/dev-server.js scripts/services/service.js \
     scripts/shared/date.js scripts/shared/page-state.js scripts/shared/validation.js \
     scripts/utils/date.js scripts/utils/format.js scripts/utils/page-state.js scripts/utils/validation.js
   ```

8. Conferir a estrutura criada:

   ```bash
   find . -path ./.git -prune -o -print | sort
   ```

## Fluxo de contribuição

1. Atualizar a branch principal: `git checkout main && git pull`.
2. Criar uma feature branch: `git checkout -b feature/<nome-da-tarefa>`.
3. Fazer commits pequenos e frequentes.
4. Enviar a branch (`git push -u origin feature/<nome-da-tarefa>`) e abrir um Pull Request para `main`.

## Plano de execução

- Dias 1 e 2: HTML completo das 3 páginas.
- Dias 3 e 4: CSS e estilização completa das 3 páginas.
- Dias 5 e 6: JavaScript das interações das páginas APOD e Contato.
