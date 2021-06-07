# "🤖 Generated automatically" warnings

Various string templates warnings, depending of the language used.

Ready to copy/paste.

Example for markdown.md files:

---

> 🤖 This file has been generated automatically through Ansible and **should not be edited by hand**.
> See the [original script](https://hey.com)
> & [original template file](https://hey.com).
> *Generated (yyyy-mm-dd) {{ currentTimestamp }}*.

---

^ Adapt ansible role/task to generate currentTimestamp:

```yml
- name: Generate dat file
  vars:
    currentTimestamp: "{{ lookup('pipe', 'date +%Y-%m-%d--%Hh%Mm%Ss') }}"
  template:
    dest: './README-generated-{{ currentDateTime }}.md'
    src: templates/README.md.j2
```
