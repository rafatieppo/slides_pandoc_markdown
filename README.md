# exemplo básico markdown + pandoc = pdf


Após preparar sua apresentação (arquivo markdown), no terminal execute a seguinte linha de comando (vc deve estar no diretório de interesse):

```bash
rafatieppo@rt-av52a:~/Documents/pandoc_markdown$ pandoc -t beamer p05a_tecgerencfrota_paretocep_slides.md  --slide-level 3 -o p05a_tecgerencfrota_paretocep_slides.pdf
```

em que: [pandoc](https://pandoc.org/) é o executável, `-t beamer` é o tipo de saída do slide (referente ao beamer do *Latex*), `--slide-level 3` indica o nível (###) em que será gerado um novo slide, e `-o` indica o nome do arquivo de saída.

Como resultado será gerado um `pdf` com a formtação (cores, fontes, ...) básica.

Caso queira personalizar o slide, é possível gerar um arquivo *header* (`.sty`) e indicar na linha de comando:

```bash
rafatieppo@rt-av52a:~/Documents/pandoc_markdown$ pandoc -t beamer p05a_tecgerencfrota_paretocep_slides.md -H ./beamer_metrop_1.sty --slide-level 3 -o p05a_tecgerencfrota_paretocep_slides.pdf
```

