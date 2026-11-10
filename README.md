<div align="center">

# Gabarito de Ouro: Caderno de Pedagogia

**Página de venda de um caderno digital de estudos para quem cursa Pedagogia, do 1º ao 8º período.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Sem framework](https://img.shields.io/badge/sem_framework-071321?style=for-the-badge)

</div>

<p align="center">
  <img src="docs/preview-desktop.webp" width="72%" alt="Página do Caderno de Pedagogia no computador">
  <img src="docs/preview-mobile.webp" width="22%" alt="Página do Caderno de Pedagogia no celular">
</p>

## Sobre

O Gabarito de Ouro é uma linha de cadernos digitais por curso. Este repositório é a página de venda
do **Caderno de Pedagogia**, que reúne fichas de estudo, resumos, flashcards com revisão espaçada,
questões comentadas, planos de aula, diário de estágio e modelos de TCC, organizados por período e
por disciplina.

É a versão para Pedagogia da [página de Medicina](https://github.com/MatheusMattos-Dev/study-guide):
mesma estrutura e mesmos recursos interativos, com conteúdo, exemplos e grade reescritos para o curso,
e um capítulo dedicado a planejamento de aulas.

## Destaques

- **Capa com o caderno sobre a mesa.** Páginas de marfim (resumo da psicogênese da escrita, ficha de
  consciência fonológica e flashcard de Didática) acompanham o ponteiro do mouse. O flashcard vira ao
  toque e, na entrada, mostra uma resposta sozinho para ensinar o gesto.
- **Fichas por período.** Abas do 1º ao 8º período (`role="tablist"`, navegação pelas setas do
  teclado), agrupadas em fundamentos, metodologias e estágio e TCC. Cada aba monta a ficha do período
  com tema, palavras-chave, bloco de estudo de 80 minutos e atividades práticas.
- **Baralho de amostra com revisão espaçada.** O cartão gira, o visitante avalia a própria resposta
  e o próximo sobe. Os intervalos do algoritmo SM-2 explicam quando cada cartão volta; uma galeria
  completa a amostra.
- **Questão comentada.** Uma questão de alfabetização no estilo dos concursos de Pedagogia: ao
  marcar a alternativa, a página mostra o gabarito explicado e permite refazer.
- **Planejamento e estágio.** Modelos de plano de aula, sequência didática, plano e relatório de
  estágio, diário de regência e um caso prático comentado de turma em alfabetização.
- **Amostras do curso.** Índice de resumos (Alfabetização, Didática, Psicologia da Educação, Educação
  Infantil, Avaliação, legislação) e três modelos de TCC (alfabetização, educação inclusiva e gestão escolar).
- **Feita para o celular.** Fileiras deslizantes com marcador de posição, grupos de "o que está
  incluído" que se reorganizam abaixo de 620 px e ajuste para telas de 320 px.
- **Barra de compra no celular.** Aparece depois que o botão da capa sai da tela e some quando a
  seção de preço está visível.
- **Oferta em um só lugar.** Checkout, valor, e-mail de suporte, processador e CNPJ ficam no objeto
  `OFERTA` do script; a página inteira acompanha.

## Seções da página

1. **Capa**: nome do caderno, "Seu conhecimento vale ouro.", chamada de compra e números do caderno.
2. **Sumário**: os dez capítulos da página, com âncoras.
3. **I. Fichas de estudo** (`#fichas`): abas por período.
4. **II. Resumos** (`#resumos`): amostra do índice, uma página de resumo e as grandes áreas.
5. **III. Flashcards** (`#flashcards`): baralho interativo, intervalos de revisão e galeria de cartões.
6. **IV. Disciplinas** (`#disciplinas`): grade por período e as disciplinas e áreas do curso.
7. **V. Planejamento e estágio** (`#estagio`): planos de aula, regências, relatórios, diário e caso prático.
8. **VI. Questões** (`#questoes`): ENADE, concursos públicos e provas de pós-graduação, com questão interativa.
9. **VII. TCC e pesquisa** (`#tcc`): três modelos de TCC.
10. **VIII. Para cada fase** (`#fases`): do primeiro período à vida de pedagogo formado.
11. **IX. Preço e garantia** (`#preco`): recibo com formas de pagamento, acesso, garantia e tudo o que está incluído.
12. **X. Perguntas frequentes** (`#perguntas`): acesso, uso, pagamento, reembolso e suporte.
13. **Rodapé** e barra de compra fixa no celular.

## Tecnologias

| Camada | Ferramentas |
| --- | --- |
| Interface | HTML, CSS e JavaScript puros, em um único `index.html` (sem framework e sem build) |
| Tipografia | Spectral (títulos) e Archivo (interface), via Google Fonts |
| Identidade | Paleta marinho, ouro e marfim em variáveis CSS, com tema claro por seção (`.claro`) |
| Animação | Web Animations API, transições CSS e `IntersectionObserver` |
| Medição | Pixel da Meta e script da UTMify |
| Pagamento | Checkout externo configurado no objeto `OFERTA` |

## SEO, desempenho e acessibilidade

- `lang="pt-BR"`, título, meta description, Open Graph com imagem (`assets/og.jpg`) e cartão grande do Twitter.
- `theme-color`, favicon e ícone para a tela inicial do iPhone.
- Fontes com `preconnect` e `display=swap`; emblemas em WebP com dimensões e `loading="lazy"`.
- Respeita `prefers-reduced-motion`: sem contagem, sem revelação, sem paralaxe e sem giro animado.
- Abas acessíveis (`tablist`, `tab`, `tabpanel`, `aria-selected`) e elementos decorativos com `aria-hidden`.

## Estrutura

```text
index.html              página completa: estilos, marcação e scripts
assets/
  emblema.webp          emblema dourado da marca
  emblema-livro.webp    emblema do recibo da oferta
  favicon.png
  icone-180.png
  og.jpg                imagem de compartilhamento
docs/                   prints usados neste README
```

## Como rodar localmente

Não há dependências nem build:

```bash
python -m http.server 8000
# ou
npx serve .
```

E abrir `http://localhost:8000`.

## Como editar

- **Oferta**: objeto `OFERTA` no começo do `<script>` principal.
- **Fichas por período**: lista `PERIODOS` no mesmo script.
- **Cores**: variáveis `--marinho`, `--ouro`, `--ouro-luz`, `--ouro-velho` e `--marfim` no topo do CSS.

## Família Gabarito de Ouro

| Repositório | Caderno |
| --- | --- |
| [study-guide](https://github.com/MatheusMattos-Dev/study-guide) | Medicina, do 1º ao 12º período |
| [study-guideV2](https://github.com/MatheusMattos-Dev/study-guideV2) | Psicologia, do 1º ao 10º período |
| [study-guideV3](https://github.com/MatheusMattos-Dev/study-guideV3) | Pedagogia, do 1º ao 8º período |

## Deploy

Site estático sem etapa de build: qualquer hospedagem estática, como a Vercel, publica a pasta como está.

---

<sub>Feito por [Matheus Mattos Chaves](https://matheusdev-lovat.vercel.app) · [GitHub](https://github.com/MatheusMattos-Dev)</sub>
