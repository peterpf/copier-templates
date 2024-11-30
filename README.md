# A copier template for Typst projects

This repository provides a copier template to bootstrap Typst projects.

## Usage

Use the template by running the following command:

```bash
copier copy https://github.com/peterpf/copier-typst-template .
```

The above command generates your project's folder structure based on the type (you get prompted to select one).

## Supported Typst project structures

Two kinds of Typst projects are supported by this template.

#### Typst package

Initializes the folder structure for a Typst package that is intended to be uploaded to the [Typst Universe](https://typst.app/universe/).

```text
. root/
`- {{project_name}}/
   |- lib.typ
   |- typst.toml
   |- README.md
   |- LICENSE
   `- template/
      `- main.typ
```

#### Typst document

Initializes the folder structure for general Typst documents with minimal depencenies.

```text
. root/
`- {{project_name}}/
   |- README.md
   `- main.typ
```

## Reproducibility and dependency management

[nix flakes](https://nixos.wiki/wiki/flakes) simplify the bootstrapping process regarding the software/configuration of the host system.
A prompt asks whether to enable this feature, if selected, the following files will be added:

```text
. root/
`- {{project_name}}/
   `- flake.nix 
```

The `flake.nix` file contains the instructions to install base software (such as a specific Typst version) and other external dependencies.

