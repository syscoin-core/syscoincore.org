{% assign _issues = include.issues | split: "," %}
{% for _issue in _issues %}
[#{{_issue}}]: https://github.com/syscoin/syscoin/issues/{{_issue}}
{% endfor %}
