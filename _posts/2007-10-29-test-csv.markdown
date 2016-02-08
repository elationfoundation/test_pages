---
layout: none
search: exclude
---
{
    "entries":
[
    {% for page in site.data.test_data | where:"country","Burkina Faso" %}
    {
      "country"    : "{{ page.country }}",
      "project"    : "{{ page.project }}",
    } {% unless forloop.last %},{% endunless %}
  {% endfor %}
]
}
