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

* [ ] Figure out what is a good alternative.
* [x] Figure out how we can generate CSS that maintains the PHP.net 
  brand - this is handled in theme repository
* [ ] Make a list of what pages should be kept from: 
  [PHP Wiki Index](https://wiki.php.net/?do=index)
* [ ] Convert DokuWiki to Markdown documents using 
  [this tool](https://github.com/wgroeneveld/dokuwiki-to-hugo)
  (remember to include Frontmatter data, generated files may need 
  some cleaning in tags)

## Contributing

This repository needs Hugo installed locally to build and server static files.
Follow the [installation guide](https://gohugo.io/getting-started/installing/)
instructions.

Docker image can be also used if you don't want to install Hugo locally
then running commands through `make` will use Hugo through Docker container.

## Usage

Creating new content of type *RFC* (these are called _Archetypes_ 
in *Hugo* - the template is in `/theme/php/archetypes/rfc.md`):

```bash
make new name=rfc/[rfc-name].md
```

Possible archetypes to use: `rfc`, `page`

Building and serving static files:

```bash
make serve
```
