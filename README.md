# Azure VM Deploy Guide

[![Build PDF](https://github.com/kolosovpetro/AzureVMDeploy/actions/workflows/build-pdf.yml/badge.svg)](https://github.com/kolosovpetro/AzureVMDeploy/actions/workflows/build.yml/badge.svg)
[![Build and Deploy PDF](https://github.com/kolosovpetro/AzureVMDeploy/actions/workflows/build-and-deploy-pdf.yml/badge.svg)](https://github.com/kolosovpetro/AzureVMDeploy/actions/workflows/build-and-deploy.yml/badge.svg)
![contributors count](https://img.shields.io/github/contributors/kolosovpetro/AzureVMDeploy)

## Build and run in Intellij IDEA

- Install `MikTeX`: https://miktex.org/download
- Update `MikTeX`
- Install `SumatraPDF` viewer: https://www.sumatrapdfreader.org/download-free-pdf-viewer
- Install `Intellij IDEA Ultimate`: https://www.jetbrains.com/idea/download/#section=windows
- Activate `Intellij IDEA Ultimate`
- Install `TeXiFy IDEA` plugin: https://plugins.jetbrains.com/plugin/9473-texify-idea
- Clone this repository locally: `https://github.com/kolosovpetro/AzureVMDeploy.git`
- Open `AzureVMDeploy` folder in `Intellij IDEA Ultimate` and configure as follows
    - LaTeX Configuration
      ![LaTeX Configuration](img/latex_configuration.PNG?raw=true "LaTeX Configuration")
    - BibTeX Configuration
      ![BibTeX Configuration](img/bibtex_configuration.PNG?raw=true "BibTeX Configuration")
- Configure Inverse Search in `Intellij IDEA` for SumatraPDF: `Tools -> LaTeX -> Configure Inverse Search`
- Compile document using `Shift + F10`

## Configure CI / CD

Set repository secrets

- `GH_ACCESS_TOKEN`: Generate Github Personal access token at
  `Settings -> Developer Settings -> Personal access tokens -> Generate mew token` and assign in to
  secret `GH_ACCESS_TOKEN`
- `GH_NAME`: Your Github username
- `GH_EMAIL`: Your Github email

## Actions and their trigger policy

- `build-pdf.yml` builds project using `TeXLive`. Triggered on `pull_request`, `push` to `develop` branch
- `build-and-deploy-pdf.yml` builds project using `TeXLive` and deploys to `GitHub Pages`. Triggered on `push` to `main`
  branch

## Template example

Compiled document looks like as follows

<p align="center">
  <img src="img/template_example.PNG" alt="template_example"/>
</p>
