# The semi-offical Lyp package index

## Editorial tools

* [edition-engraver](https://github.com/noteflakes/lyp-edition-engraver) - Editorial tweaking for lilypond.

## Fonts

* [bravura](https://github.com/noteflakes/lyp-bravura) - Bravura SMuFL font for lilypond.
* [gootville](https://github.com/noteflakes/lyp-gootville) - Gootville SMuFL font for lilypond (based on Gonville)
* [lilyjazz](https://github.com/noteflakes/lyp-lilyjazz) - LilyJazz font package.
* [smufl](https://github.com/noteflakes/lyp-smufl) - Support for SMuFL fonts.

## Harmony

* [microlily](https://github.com/noteflakes/lyp-microlily) - Microtonal support for Lilypond.
* [roman-numerals](https://github.com/noteflakes/lyp-roman-numerals) - A package for roman numeral harmonic analysis.

## Support Libraries

* [assert](https://github.com/noteflakes/lyp-assert) - Assertions for lilypond packages.

# Contributing

This repository contains a YAML index of lilypond packages that can be installed using [lyp](https://github.com/noteflakes/lyp), the lilypond package manager.

To add your package to the index:

1. Fork this repository
2. Add your package to <code>index.yml</code> under the <code>packages</code>, using the following format:

```yaml
packages:
  <package-name>:
    url: <public git url>
    description: <short description>
    author: <author>
```

3. Add your package to this README file under the proper section (or possibly create a new section).
4. Submit a pull request

## The rules

1. The package name must be unique, the packages in the index file should be ordered alphabetically.
2. The git url could be a github repository id (i.e. <code>userid/mypackage</code>), a partially-qualified URL (i.e. <code>acme.com/myrepo.git</code>), or a fully-qualified URL (i.e. <code>https://github.com/blah/blah.git</code>)
2. The package should include a <code>package.ly</code> file in its root directory. This is the entry point for the package.
3. Additional <code>.ly</code> files can be included using relative <code>\include</code>s.
4. The package should have a README and include a license, either as part of the code, in the README, or in a separate file.
5. Transitive dependencies are defined as usual using <code>\require</code>.
6. The package repository should be versioned using git tags. Version tags can be optionally prefixed with <code>v</code> (for example <code>v0.2</code>).
7. Including the package in the index is optional. It allows users to install your package using a short unique name, but your package could always be installed using its publicly-accessible git URL.
