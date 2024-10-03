# Automate Building and releasing a Spring Boot application to GitHub Releases using GitHub Actions

This repository contains a simple Spring Boot application that is built and released to GitHub Releases using GitHub Actions. Also this repository contains a GitHub Actions workflow that is triggered manually and builds and releases the application to GitHub Packages.

## How it works

### Build and release a Spring Boot application to GitHub Releases

To build and release a user will create a new feature branch and make changes to the code. Once the changes are ready, the user will create a pull request and add a label to the pull request. Available labels are 

- MAJOR
- MINOR
- PATCH

The user can choose the appropriate label based on the changes made to the code. Once the pull request is merged, the GitHub Actions workflow will be triggered and the application will be built and released to GitHub Releases.

Above labels are based on [Semantic Versioning](https://semver.org/).

### Build and release a Spring Boot application to GitHub Packages

`.github/workflows/deploy-to-github-packages.yml` is a GitHub Actions workflow that is triggered manually. This workflow builds and releases the application to GitHub Packages.

## GitHub Actions Workflows

The GitHub Actions workflow is defined in the `.github/workflows/build-and-release.yml` file. The workflow is triggered when a pull request is merged to the `main` branch.

The workflow consists of the following steps:

### Build and release the application to GitHub Releases

- Checkout the repository
- Set up Java
- Build the application
- Create a release
- Upload the application to the release

### deploy-to-github-packages.yml

- Checkout the repository
- Set up Java
- Build the application
- publish maven package to GitHub Packages, this is done using the `mvn deploy` command and .m2/settings.xml file

## Eternal links
