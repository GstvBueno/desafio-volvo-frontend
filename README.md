# Desafio Front-End Volvo

Teste técnico para uma vaga de front-end na Volvo Cars: uma vitrine dos carros elétricos e híbridos "Recharge", com um cartão por modelo e paginação diferente para desktop e celular, seguindo o design do enunciado (abaixo).

## Tecnologias

- [Next.js](https://nextjs.org/) 12 (pasta `pages`)
- React 17 e TypeScript
- [VCC-UI](https://vcc-ui.vercel.app/), a biblioteca de componentes da Volvo
- Axios

## Como rodar

Pré-requisito: Node.js (testado com a versão 24).

```bash
npm ci        # instala as dependências
npm run dev   # abre em http://localhost:3000
```

A página busca os carros na rota interna `/api/cars`, que lê `public/api/cars.json`. O endereço está fixo em `http://localhost:3000`, então rode na porta 3000.

Outros comandos:

```bash
npm run build # gera a versão de produção
npm start     # roda a versão de produção
npm run lint  # verifica o código
```

## Estrutura

```
pages/_app.tsx          # página principal (tema VCC-UI + HomeComponent)
pages/api/cars.ts       # API que devolve a lista de carros
src/components/         # CarCard, HomeComponent, paginação desktop/mobile, Spacer
src/hooks/useCars.ts    # busca os carros
src/types/              # tipo Car
public/                 # dados (api/cars.json), imagens e CSS
```

---

## Enunciado original

# Volvo Cars (Global Online Digital)

## Front-end coding test (React)

Our team's designer has come up with a new design to show our latest and greatest recharge cars on the website.

Here is how the design look like for desktop and mobile (files are stored under `docs` folder)

### Desktop

![ProductListDesktop](./public/images/docs/ProductList-Desktop.png)

### Mobile

![ProductListDesktop](./public/images/docs/ProductList-Mobile.png)

The data required to render the design is under `public/api/cars.json` folder. You need to fetch the data and render it in the browser. The data looks like this:

```json
[
  {
    "id": "xc90-recharge",
    "modelName": "XC90 Recharge",
    "bodyType": "suv",
    "modelType": "plug-in hybrid",
    "imageUrl": "/images/xc90_recharge.jpg"
  }
]
```

The product owner is telling you that you can generate the links to the learn and shop pages of each car by concatating the `id` of the car to the learn (`/learn/`) and shop (`/shop/`) urls.

Two extra SVG icons are also provided by our designer which are stored under `docs` folder.

## Requirements

- The project is bootstraped using [Next.js](https://nextjs.org/).
- Browser support is modern ever-green browsers.
- Implement this design using React and Typescript.
- Accessibility is important.
- Code Structure and reusablity is important.

## Bonus Points:

- If you use our design system component library, [VCC-UI](https://vcc-ui.vercel.app/)
- If you add a filter bar on the top to filter cars by `bodyType`

## Submission

Clone this repository to get started. Due to a number of reasons, not least privacy, you will be asked to zip your solution and mail it in, instead of submitting a pull-request. In order to maintain an unbiased reviewing process, please ensure to keep your name or other Personal Identifiable Information (PII) from the code.

