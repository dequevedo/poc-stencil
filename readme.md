
# Stencil.js Cheatsheet

Stencil é um compilador para Web Components reutilizáveis que usa sintaxe similar ao React/TypeScript.

## Comandos úteis

```bash
npm init stencil   # novo projeto
npm install        # instalar deps
npm start          # dev server
npm run build      # build prod
npm test           # rodar testes
npm run lint       # lint do código
npm run docs       # gerar docs
```

## Props e States

```tsx
@Prop() name: string;          // externa (html)
@State() count: number = 0;    // interna (reativa)
```

## Lifecycle Methods

```tsx
componentWillLoad() {}
componentDidLoad() {}
componentShouldUpdate() { return true; }
componentWillUpdate() {}
componentDidUpdate() {}
componentDidUnload() {}
```

## Eventos

```tsx
@Event() myEvent: EventEmitter<string>;

this.myEvent.emit('Hello!');
```

## Testando

```bash
npm test
```

## Usando em HTML

```html
<my-component name="Daniel"></my-component>
<script type="module" src="/build/my-component.js"></script>
```

## Dicas

- Use `shadow: true` para Shadow DOM encapsulado.
- Exporte o componente no `components.d.ts` para autocomplete em outros projetos.
- Compatível com Angular, React, Vue e puro HTML.

---