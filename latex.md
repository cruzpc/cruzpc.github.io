# LaTeX para gerar documentos formatados em MDT - UFSM

Este tutorial é para usuários de Ubuntu (ou outras distros baseadas em Debian) que querem gerar documentos em PDF de acordo com as normas da MDT - UFSM, totalmente offline.

## Instalação do LaTeX

Instale o LaTeX pelo terminal:

```bash
$ sudo apt-get install texlive-full
```
Esse comando irá instalar todos os pacotes do LaTex.

Após instalar, verifique se os seguintes pacotes foram instalados:

- texlive-base
- texlive-lang-portuguese
- abntex
- texlive-latex-extra

Se não foram instalados, instale-os:

```bash
$ sudo apt-get install abntex
```

## Template

Utilize o modelo disponibilizado pela UFSM [aqui](https://www.ufsm.br/orgaos-suplementares/biblioteca/mdt/).

## Compilação

Para compilar e gerar o documento:

```bash
$ pdflatex arquivo_2015.tex

```
Isto vai gerar o documento com "?????" no lugar das referências.

```bash
$ bibtex arquivo_2015		    
```
Vai compilar o arquivo .bib e gerar metadados sobre as referências.

```bash
$ pdflatex arquivo_2015.tex
```
Este comando vai gerar o documento com as referências corretas.

```bash
$ pdflatex arquivo_2015.tex 
```
Apenas para o caso de alguma referência gerar quebra de página em algum lugar.

## Visualização e Edição

Para vizualização, qualquer leitor de PDF funcionará. Mas recomendo algum que atualize automaticamente toda vez que uma compilação é feita. Portanto, o Evince ou o Zathura serão os melhores.

Para edição, recomendo o Vim.