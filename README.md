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
npm i @antora/cli@3.1 @antora/site-generator@3.1
npx antora generate antora-playbook.yml
```
The generated website should appear under build/site/.

## CI/CD Pipeline
This repository is ```not yet, but will be``` scheduled to build ```not determined``` times per day```maybe hour?```. If you push your documentation changes to one of the source repositories, it might not appear instantly once you have pushed, you have to wait until the website rebuilds automatically.

## License
License not yet determined to publish the project under. At this point no permission granted for anything regarding the source or the project itself for the time being. Only those with respective rights are authorized. 

This project is under the ```not determined```. See the [LICENSE](LICENSE) file for details.
