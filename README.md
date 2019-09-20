PHP RFC Experiment
==================

## Why to setup wiki alternative?

Continuing to use Dokuwiki has a couple of large downsides:

Collaborating on changes is difficult. It's much easier for people 
to suggest changes via github.

Editing is slow and painful. Although the syntax is probably more 
powerful that markdown, markdown is significantly easier to edit.

Only people with php.net can edit documents, which means that 
community members who do not have php.net accounts basically can't 
suggest changes.

## TODO
[ ] Figure out what is a good alternative.
[ ] Figure out how we can generate CSS that maintains the PHP.net brand
[ ] Make a list of what pages should be kept from: https://wiki.php.net/?do=index

## Usage

Creating new content of type *RFC* (these are called _Archetypes_ 
in *Hugo* - the template is in `/archetypes/rfc.md`):

```bash
hugo new rfc/[rfc-name].md
```

Rendering with *Hugo* requires invoking:

```bash
hugo serve
```
