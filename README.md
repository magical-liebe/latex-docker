# Docker image for LaTeX

日本語対応LaTeX環境Dockerイメージ.

## Pull Image

```bash
docker pull magicalliebe/latex-docker:latest
```

## Usage

### Convert LaTeX to PDF

コンパイルしたいtexファイルがあるディレクトリで以下を実行すると、PDFを生成できます.

```bash
docker run -u $(id -u):$(id -g) --rm -v $PWD:/workdir magicalliebe/latex-docker:latest latexmk main.tex
```

### Convert SVG to PDF

以下のコマンドでSVGファイルをPDF形式に変換できます.

```bash
docker run -u $(id -u):$(id -g) --rm -v $PWD:/workdir magicalliebe/latex-docker:latest svg2pdf sample.svg sample.pdf
```