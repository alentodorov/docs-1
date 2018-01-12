---
$title: Incluir conteúdo de terceiros
---

Saiba como incluir componentes de terceiros em suas páginas.

[TOC]

## Incorporar um tweet

Incorpore um tweet na sua página
usando o elemento [`amp-twitter`](/pt_br/docs/reference/components/amp-twitter.html).

Para incluir um tweet em sua página,
em primeiro lugar inclua o seguinte script no `<head>`:

[sourcecode:html]
<script async custom-element="amp-twitter" src="https://cdn.ampproject.org/v0/amp-twitter-0.1.js"></script>
[/sourcecode]

Atualmente, os tweets são dimensionados automaticamente de acordo com sua proporção
para se ajustarem ao tamanho fornecido,
mas isso pode gerar uma aparência não muito boa.
Ajuste manualmente a largura e a altura fornecidas ou use o atributo de mídia
para selecionar a proporção com base na largura da tela.

<!-- embedded twitter example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.twitter.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

{% call callout('Dica', type='success') %}
Veja mais exemplos de `amp-twitter` na página [AMP By Example](https://ampbyexample.com/components/amp-twitter/).
{% endcall %}

## Incorporar uma imagem do Instagram

Incorpore uma imagem do Instagram em sua página
usando o elemento [`amp-instagram`](/pt_br/docs/reference/components/amp-instagram.html).

Para incluir uma imagem do Instagram,
em primeiro lugar inclua o seguinte script no `<head>`:

[sourcecode:html]
<script async custom-element="amp-instagram" src="https://cdn.ampproject.org/v0/amp-instagram-0.1.js"></script>
[/sourcecode]

Inclua o data-shortcode do Instagram encontrado no URL da foto no Instagram.
Por exemplo, em `https://instagram.com/p/fBwFP`,
`fBwFP` é o data-shortcode.
Além disso, o Instagram usa uma proporção fixa para os layouts responsivos,
de modo que os valores de largura e altura são universais.

<!-- embedded Instagram example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.instagram.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

{% call callout('Dica', type='success') %}
Veja mais exemplos de `amp-instagram` na página [AMP By Example](https://ampbyexample.com/components/amp-instagram/).
{% endcall %}

## Exibir postagem ou vídeo do Facebook

Exiba uma postagem ou um vídeo do Facebook na sua página
usando o elemento [`amp-facebook`](/pt_br/docs/reference/components/amp-facebook.html).

Você precisa incluir o seguinte script no `<head>`:

[sourcecode:html]
<script async custom-element="amp-facebook" src="https://cdn.ampproject.org/v0/amp-facebook-0.1.js"></script>
[/sourcecode]

##### Exemplo - Incorporação de uma postagem:

Source: 
```html
<amp-facebook width="486" height="657"
    layout="responsive"
    data-href="https://www.facebook.com/zuck/posts/10102593740125791">
</amp-facebook>
```
Preview: 
<amp-facebook width="486" height="657"
    layout="responsive"
    data-href="https://www.facebook.com/zuck/posts/10102593740125791">
</amp-facebook>

##### Exemplo - Incorporação de um vídeo:

Source: 
```html
<amp-facebook width="476" height="316"
    layout="responsive"
    data-embed-as="video"
    data-href="https://www.facebook.com/nasaearth/videos/10155187938052139">
</amp-facebook>
```
Preview: 
<amp-facebook width="476" height="316"
    layout="responsive"
    data-embed-as="video"
    data-href="https://www.facebook.com/nasaearth/videos/10155187938052139">
</amp-facebook>

{% call callout('Dica', type='success') %}
Veja mais exemplos de `amp-facebook` na página [AMP By Example](https://ampbyexample.com/components/amp-facebook/).
{% endcall %}

## Incluir um vídeo do YouTube

Inclua um vídeo do YouTube em sua página
usando o elemento [`amp-youtube`](/pt_br/docs/reference/components/amp-youtube.html).

Você precisa incluir o seguinte script no `<head>`:

[sourcecode:html]
<script async custom-element="amp-youtube" src="https://cdn.ampproject.org/v0/amp-youtube-0.1.js"></script>
[/sourcecode]

O `data-videoid` do YouTube pode ser encontrado em qualquer URL de uma página de vídeos do YouTube.
Por exemplo, em `https://www.youtube.com/watch?v=Z1q71gFeRqM`,
`Z1q71gFeRqM` é o ID do vídeo.

Use `layout="responsive"` para gerar layouts de forma correta para vídeos com proporção de 16:9.

<!-- embedded youtube example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/responsive.youtube.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

{% call callout('Dica', type='success') %}
Veja mais exemplos de `amp-youtube` na página [AMP By Example](https://ampbyexample.com/components/amp-youtube/).
{% endcall %}

## Exibir um anúncio

Exiba um anúncio em sua página
usando o elemento [`amp-ad`](/pt_br/docs/reference/components/amp-ad.html).
Somente anúncios veiculados via HTTPS são compatíveis.

Nenhuma rede de anúncios que forneça JavaScript pode ser executada dentro do documento de AMP.
Em vez disso, o tempo de execução da AMP carrega um iframe de uma
origem diferente (por meio de uma sandbox de iframe)
e executa o JS da rede de anúncios dentro da sandbox desse iframe.

Você precisa especificar a largura e a altura do anúncio e o tipo de rede de anúncios.
O `type` identifica o modelo da rede de anúncios.
Diferentes tipos de anúncios exigem diferentes atributos `data-*`.

<!-- embedded ad example -->
<div>
<amp-iframe height="212"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.ad-basic.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

Se compatível com a rede de anúncios,
inclua um `placeholder`
para ser mostrado quando nenhum anúncio estiver disponível:

<!-- embedded ad example -->
<div>
<amp-iframe height="232"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.ad-placeholder.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

A AMP é compatível com uma ampla gama de redes de anúncios. Consulte as [referências para ver a lista completa](/pt_br/docs/reference/components/amp-ad.html#supported-ad-networks).

{% call callout('Leia Mais', type='read') %}
Saiba mais sobre anúncios no guia [Como veicular anúncios em AMP](/pt_br/docs/guides/ads_on_amp.html).
{% endcall %}
