{% capture /dev/null %}
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!!! NB: for this file to render correctly, !!!
!!! you must also include references.md   !!!
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

{% case page.lang %}
  {% else %}{% comment %}fallback to English{% endcomment %}
    {% assign _includes_dev_keys-name = "Name" %}
    {% assign _includes_dev_keys-fingerprint = "Fingerprint" %}
    {% capture _includes_dev_keys-import %}You can import a key by running the following command with that individual's fingerprint: `gpg{{site.strings.gpg_keyserver}} --recv-keys "<fingerprint>"`  Ensure that you put quotes around fingerprints containing spaces.{% endcapture %}
{% endcase %}
{% endcapture %}

| {{_includes_dev_keys-name}} | {{_includes_dev_keys-fingerprint}}         |
|-----------------------------|--------------------------------------------|
| Jagdeep Sidhu               | <code>{% include fingerprint-split.html hex="51C50FDF431BDCD772CE0EF0428294DB7DF03805" %}</code> |
| Willy Ko                    | <code>{% include fingerprint-split.html hex="79D00BAC68B56D422F945A8F8E3A8F3247DBCBBF" %}</code> |

{{_includes_dev_keys-import}}
