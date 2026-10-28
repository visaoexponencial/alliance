# Alliance Cristo Redentor — versão compacta

O site completo está em `index.html`: CSS, JavaScript, imagens e fontes estão incluídos dentro dele. Não há pasta de imagens para esquecer no deploy. Foram mantidas as 11 fotos diferentes, o logo, a headline aprovada e todas as interações do site anterior.

## Publicar no GitHub e depois na Vercel

Este é um site estático em HTML/CSS/JavaScript. Não usa React, Next.js, npm, banco de dados ou variáveis de ambiente. O GitHub armazena o código e a Vercel publica o site.

### 1. Enviar ao GitHub

1. Crie um repositório novo e vazio ou use uma pasta limpa no seu repositório.
2. Use **Add file → Upload files**.
3. Envie os três arquivos separados: **index.html**, **vercel.json** e **README.md**.
4. Confirme o commit na branch que será publicada (normalmente `main`).
5. Confira a listagem: os três arquivos precisam estar na raiz do repositório, lado a lado.

**O nome da página inicial deve ser exatamente `index.html`, todo em minúsculas.** Se o navegador acrescentar `(1)`, `(8)`, `-copia` ou `.txt` ao baixar, renomeie antes de enviar. `index(8).html` ou `index.html.txt` não são a página inicial esperada. Mantenha também o nome `vercel.json` exatamente assim.

Não envie um ZIP como se fosse o site nem envie os arquivos dentro de uma pasta extra sem ajustar a Root Directory. Caso já exista um site React/Next.js no repositório, prefira um repositório novo para evitar configurações antigas.

### 2. Importar na Vercel

1. Acesse **Add New → Project** e importe o repositório do GitHub.
2. Configure **Framework Preset: Other**.
3. Deixe **Root Directory: ./** (raiz do repositório).
4. O arquivo `vercel.json` define **Build Command vazio**, **Install Command vazio** e **Output Directory: .**.
5. Se houver overrides antigos na interface, use os mesmos valores: não escreva `npm run build`, `dist`, `build` ou `public` para esta entrega.
6. Clique em **Deploy**.

Não precisa editar o código nem instalar dependências para essa publicação. O HTML já contém o CSS, o JavaScript, o logo, as 11 fotos e as fontes. O mapa usa o serviço externo do Google.

### 3. Conferir o resultado

Abra a URL informada pela Vercel. Confirme a headline, as fotos e o menu. Teste o botão de agendamento e a galeria. O agendamento abre a opção de ligação para a academia, não um formulário de reserva automática.

Se aparecer 404, confira primeiro o nome `index.html` e a Root Directory. Se a Vercel tentar executar npm, confira o framework e os comandos de instalação/build. Um erro de permissão para importar o repositório deve ser resolvido na conexão entre GitHub e Vercel, sem alterar o HTML.

### Prévia no computador

Você pode abrir o `index.html` diretamente no navegador. Para testar por HTTP, se tiver Python instalado, execute `python -m http.server 8080` na pasta e abra `http://localhost:8080`. Esse comando não é usado pela Vercel.

## Funcionalidades mantidas

- Menu mobile, navegação entre seções e voltar ao topo.
- Carrosséis de aulas e depoimentos, setas, indicadores e rolagem por toque.
- Reprodução automática com pausa em interações e respeito a movimento reduzido.
- Galeria ampliável com setas, teclado, gesto horizontal e Esc.
- Agendamento com seleção de interesse e link para ligar.
- Mapa e link de rota para a academia.
- Janela de privacidade e layout responsivo.

O contato é `tel:+555135741435`. O agendamento é confirmado por ligação, não por reserva automática. Nenhuma chamada ou mensagem é disparada sem a ação do visitante. O mapa e os links externos dependem da internet e do Google; todo o visual, as fotos, fontes e código do site estão no arquivo.

## O que mudou para reduzir o tamanho

- Uma única versão WebP otimizada para cada fotografia, com as mesmas dimensões da versão anterior; removidos JPEGs alternativos e múltiplas cópias responsivas.
- Fontes incorporadas com os caracteres necessários para português, latim, pontuação e símbolos, mantendo as famílias e pesos usados.
- CSS e JavaScript incorporados ao HTML.
- Documentação, licenças e instruções reunidas neste README.

Foi aplicada compressão com perda moderada às fotos para reduzir o peso, sem alterar pessoas, enquadramento ou conteúdo. As ampliações existentes continuam limitadas pelos detalhes dos arquivos originais.

## Manutenção

Edite textos, telefone e horários no `index.html`. O CSS está no bloco `<style>` e o JavaScript no bloco `<script>` ao fim. As sequências longas começando com `data:image` e `data:font` são os arquivos incorporados: não as apague nem substitua parcialmente. Em caso de troca de endereço ou telefone, atualize também o JSON-LD, mapa e link de rota. Depois de definir o domínio final, você pode incluir as tags canonical e og:url no `<head>`.

A versão compacta funciona em navegadores atuais com suporte a WebP e aos diálogos nativos do HTML. Não depende de login do ChatGPT.

## Referências de publicação

- https://vercel.com/docs/project-configuration/vercel-json
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Validação desta versão

- Imagens incorporadas decodificadas sem erro e todas as imagens da página carregadas na prévia do navegador.
- Fontes incorporadas validadas e sintaxe do JavaScript conferida.
- Testados seleção Kids, agendamento, galeria, setas do carrossel e privacidade.
- Testados menu mobile, navegação até Contato, fechamento do menu e botão de agendamento no celular.
- Sem transbordamento horizontal na prévia de celular.
- Nenhuma chamada telefônica, mensagem, reserva ou publicação externa foi realizada durante os testes.
- O site ainda deve ser publicado na sua conta da Vercel seguindo as instruções acima. A configuração JSON foi validada com o esquema oficial da Vercel; essa validação não substitui a confirmação do deploy na sua conta.

## Licenças das fontes

### barlowcondensed-OFL.txt

```text
Copyright 2017 The Barlow Project Authors (https://github.com/jpt/barlow)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
http://scripts.sil.org/OFL


-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded, 
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.

```

### inter-OFL.txt

```text
Copyright 2020 The Inter Project Authors (https://github.com/rsms/inter)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
https://scripts.sil.org/OFL


-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded, 
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.

```
