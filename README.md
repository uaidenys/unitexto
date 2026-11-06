<p align="center">
  <img src="assets/app-icon/hicolor/128x128/apps/ai.storyteller.wordcraft.png" alt="UniTexto" width="96">
</p>

<h1 align="center">UniTexto</h1>

<p align="center">
  O editor de textos da <b>Uniphar Indústria Farmacêutica</b>. Abre e salva documentos do Word.
</p>

<p align="center">
  <a href="https://github.com/uaidenys/unitexto/releases/latest"><b>Baixar a versão mais recente</b></a>
</p>

---

## O que ele faz

- **Familiar:** faixa de opções (abas Página Inicial, Inserir, Layout, Referências, Revisão…),
  atalhos de teclado e comportamento parecidos com os do Word.
- **Seus arquivos:** abre e salva .docx; também abre e salva .odt, .rtf, .html, .md e .txt, abre
  .doc antigos (97-2003) e exporta para PDF.
- **Texto e formatação:** fontes, estilos, listas numeradas e com marcadores, tabelas, imagens,
  formas, caixas de texto, cabeçalhos e rodapés, números de página, colunas e quebras.
- **Documentos longos:** sumário, notas de rodapé, citações e bibliografia, legendas, referências
  cruzadas e índice.
- **Revisão:** ortografia, controle de alterações, comentários, comparação de documentos e contagem
  de palavras.
- **Mala direta:** a partir de uma planilha CSV, com envelopes e etiquetas.
- **Privado:** tudo funciona no computador, sem conta e sem enviar documentos para a internet.
- **Em português:** a interface segue o idioma do Windows (português do Brasil e mais de 20 idiomas).

## Como instalar

- **Pelo Uni Launcher (recomendado):** instale o
  [Uni Launcher](https://github.com/uaidenys/uni-launcher/releases/latest) e clique em instalar no
  UniTexto. O launcher também cuida das atualizações.
- **Direto:** na [página da versão mais recente](https://github.com/uaidenys/unitexto/releases/latest),
  em **Assets**, baixe o arquivo `-windows-x64.msi` e abra. Se o Windows mostrar "O Windows protegeu
  o computador", clique em **Mais informações › Executar assim mesmo**. O instalador ainda não tem
  assinatura digital de código.

Requisitos: Windows 10 ou 11, 64 bits.

## Para desenvolvedores

O UniTexto é feito em Rust, com [egui](https://github.com/emilk/egui).

```bash
cargo run --release -p wordcraft
```

Para gerar o instalador do Windows (precisa do [WiX v5](https://wixtoolset.org)):

```powershell
powershell -ExecutionPolicy Bypass -File packaging/windows/package.ps1 -Arch x64
```

O arquivo sai em `dist/release/`. Os nomes internos `wordcraft` (programa, pacotes e arquivos)
foram mantidos do projeto original; o Uni Launcher reconhece os dois nomes.

A ferramenta de linha de comando `wordcraft-cli` e o servidor MCP permitem automatizar o editor;
a documentação técnica está em [docs/](docs/).

## Licença e créditos

- **Código:** MIT ou Apache-2.0, à sua escolha ([LICENSE-MIT](LICENSE-MIT),
  [LICENSE-APACHE](LICENSE-APACHE)). Avisos obrigatórios em [NOTICE](NOTICE).
- **Marca:** os nomes Uni e Uniphar, o ícone e as imagens da animação de abertura pertencem à
  Uniphar Indústria Farmacêutica e **não** estão cobertos pela licença do código. Termos em
  [docs/brand/LICENSE-brand.txt](docs/brand/LICENSE-brand.txt). Quem fizer uma versão modificada
  precisa usar nome e identidade visual próprios.
- **Materiais de terceiros:** fontes, dicionários e outros arquivos com suas licenças, listados em
  [ATTRIBUTION.md](ATTRIBUTION.md).

O UniTexto é uma versão modificada do [WordCraft](https://github.com/storytold/wordcraft), criado
pela equipe ArtCraft e colaboradores (MIT OR Apache-2.0).

Desenvolvido por Denys Rodrigues de Oliveira para a Uniphar Indústria Farmacêutica ·
[uniphar.com.br](https://uniphar.com.br/)
