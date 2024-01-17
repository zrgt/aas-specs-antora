# aas-specs-antora

## Description
This is repository contains the documentation for the project [aas-specs](https://github.com/rwth-iat/aas-specs) whose generation is within the scope of this very repository itself as well as the means to generate it on demand by compiling and assembling the respective content from numerous remote repositories and sources written in ascii-doc using [Antora](https://antora.org/).

#### Note
Please note that this repository is in active development and things might not work.

## Usage

If you wish the set up this environment locally to generate the collective documentation or edit the due process to alter the results in the direction of your needs and desires, this section covers the steps and requirements in the process and aims to guide you broadly to ease the procedure. If you require more assistance or proper documentation along the way, you should make use of the official [Antora documentation](https://docs.antora.org/antora/latest/).

### Prerequisites

Before proceeding, you are required to have the latest [Node.js LTS release](https://nodejs.org/en/download) installed on your Linux, Windows, or macOS machine. You can then follow the steps [here](https://docs.antora.org/antora/latest/install/install-antora/) to install Antora and set it up.

### Building
In order to locally build the documentation website on your own, you have to make sure you have Antora CLI installed on your machine first. You can then continue with cloning this repository. All you have to do is run the following commands in order:
```
npm i
npx antora generate antora-playbook.yml
```
The generated website should appear under build.

## CI/CD Pipeline
This repository is scheduled to re-build and deploy the website at 00:00 UTC every day. This means content from the source repositories are pulled and website is built again accordingly. This once a day cycle might be changed to several times a day in the future, once it makes sense. If documentation changes are pushed to one of the source repositories, it might not appear instantly once they are pushed, you have to wait until the website rebuilds automatically.

## License
This project is under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.
