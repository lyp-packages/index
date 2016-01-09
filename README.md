# lyp-index

A semi-official index of lilypond packages (for lyp).

## How to contribute

This repository contains a YAML index of lilypond packages that can be installed using [lyp](https://github.com/noteflakes/lyp), the lilypond package manager.

To add your package to the index:

1. Fork this repository
2. Add your package to <code>index.yml</code> under the <code>packages</code>, using the following format:

```yaml
packages:
  <package-name>:
    url: <git url>
    description: <short description>
    author: <author>
```

3. Submit a pull request

Alternatively, you can directly [edit the index file]() on github.

## The rules

1. The package name must be unique, the packages in the index file should be ordered alphabetically.
2. The package should include a <code>package.ly</code> file in its root directory. This is the entry point for the package.
3. Additional <code>.ly</code> files can be included using relative <code>\include</code>s.
4. Transitive dependencies are defined as usual using <code>\require</code>.
5. Including the package in the index is optional. It allows users to install your package using a short unique name. But your package could always be installed using its publically-accessible git URL.