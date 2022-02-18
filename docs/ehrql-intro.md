# ehrQL: Data Builder's language for querying electronic health record data

---8<-- 'includes/data-builder-danger-header.md'

This page will introduce the specialised query language, ehrQL, that
[Data Builder](data-builder-intro.md) introduces, explaining:

* what it is
* give an overview of its use
* mention that there is a [more comprehensive
  reference](ehrql-reference.md)

## Goal

We need to be able to describe all this:

```
# TODO: make this a snippet
patients = tables.global.patients

year_of_birth = patients.date_of_birth.year
dataset = Dataset()
dataset.set_population(year_of_birth <= 2000)
dataset.year_of_birth = year_of_birth
```

TODO: It feels like having a simple explanation of a small snippet,
followed by a more in-depth coverage of the concepts is one way to
introduce ehrQL. A full, and possibly interactive, tutorial might also be
useful.

---8<-- 'includes/glossary.md'
