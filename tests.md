---
layout: comicpage
imagen: ksbdcoverchapter1.webp
alt: MATA SEIS BILLONES DE DEMONIOS - Capitulo 1
capitulo: 99
pagina: 99
libro: 99
creditos: Duende Inexistente
oglink: http://killsixbilliondemons.com/comic/ksbd-chapter-1-1
---

<ul>
{% for member in site.data.libros %}
  <li>
    {{ member.numero }}-{{ member.original }}-{{ member.traduccion }}
  </li>
{% endfor %}
</ul>


<table>
<thead>
<th>Numero</th><th>Original</th><th>Traduccion</th><th>Nota</th>
</thead>
{% for libro in site.data.libros2 %}

<tr>
<td>{{ libro[1].numero }}</td><td>{{ libro[1].nombre }}</td><td>{{ libro[1].traduccion }}</td><td>{{ libro[1].nota }}</td>
</tr>
{{ libro.numero }}
{% endfor %}
</table>



<br> {{ page.title }}<br> 
site.url: {{ site.url }}<br>
site.githhub.url {{ site.github.url }}<br>
site.baseurl {{ site.baseurl }}

<br>


{% if site.baseurl == "/m6bd" %}
asdasdsadasd
{% assign linkz = "bla" %}

{% endif %}

{% assign linkz2 = "bla2" %}

{{ linkz }}
{{ linkz2 }}
