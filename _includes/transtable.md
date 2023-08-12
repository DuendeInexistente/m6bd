{% capture libro %}l{{ page.libro }}{% endcapture %}
{% capture cap %}c{{ page.capitulo }}-{{ page.pagina }}{% endcapture %}


{% capture table %}
| **Linea** | **Traduccion** | **Nota** | 
|=======|============|======|
{% for linea in site.data.transcripciones.[libro].[cap] %}{% unless linea.linea == nil %}|{{ linea.linea }}|{{ linea.traduccion }}|{{ linea.nota }}|
{% endunless %}{% endfor %}


{% for linea in site.data.transcripciones.[libro].[cap] %}
{% if linea.tipo == "alt" %}
# Alt
{{ linea.linea }}

---

{{ linea.traduccion }}
{% endif %}

{% if linea.tipo == "diatriba" %}
# diatriba
{{ linea.linea }}

---

{{ linea.traduccion }}
{% endif %}
{% endfor %}




{% endcapture %}

{{ table | markdownify }}