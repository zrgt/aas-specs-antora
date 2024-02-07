# aas-specs-antora

## Description
This is repository contains the structure for building the documentation website for the Asset Administration Shell by [the Industrial Digital Twin Association](https://industrialdigitaltwin.org). This includes the means to generate it on demand by compiling and assembling the respective content from numerous remote repositories and sources written in ascii-doc using [Antora](https://antora.org/).

## Sources & Structure
This very repository is responsible for automatically building the documentation website either manually on demand by someone with required privileges or also automatically 4 times a day. The contents of the website is not to be found in this repo. The user interface is hosted in [aas-specs-antora-ui](https://github.com/admin-shell-io/aas-specs-antora-ui).

The sources for [Part 1](https://github.com/admin-shell-io/aas-specs/), [Part 2](https://github.com/admin-shell-io/aas-specs-api), [Part 3a](https://github.com/admin-shell-io/aas-specs-iec61360) and [Part 5](https://github.com/admin-shell-io/aas-specs-aasx) are all pulled from various different upstream repositories. As with all documentation websites that are built using Antora and automated, the information of the sources can be found in the [Antora playbook](antora-playbook.yml).

These sources should be edited carefully. If you are developing or maintaining this documentation sources, try testing locally on your machine before doing pushes. If you cannot do this for some reason or would like personal assistance, please open an issue here so that we can provide you with further detailed instructions. If you want to test on the website directly for your convenience anyway, you can open an issue and we can grant you the required privileges to run the build workflow manually. This way, you can do your changes and build & deploy again manually to see your changes. We strongly recommend to refrain from this option as it may introduce further complications on the process. The website also builds every 6 hours, so it might be also reasonable to wait to see your changes.

If you reckon there are problems with the sources in any way, you can open an issue here and we can try to fix those structural problems upstream. We are happy to open pull request on the sources. If you maintain one of the sources, don't hesitate to open issues here for structural fixes.

## Usage

If you wish the set up this environment locally to generate the collective documentation or edit the due process to alter the results in the direction of your needs and desires, this section covers the steps and requirements in the process and aims to guide you broadly to ease the procedure. If you require more assistance or proper documentation along the way, you should make use of the official [Antora documentation](https://docs.antora.org/antora/latest/).

### Prerequisites

Before proceeding, you are required to have the latest [Node.js LTS release](https://nodejs.org/en/download) installed on your Linux, Windows, or macOS machine. You can then follow the steps [here](https://docs.antora.org/antora/latest/install/install-antora/) to install Antora and set it up.

### Building Locally
In order to locally build the documentation website on your own, you have to make sure you have Antora CLI installed on your machine first. You can then continue with cloning this repository. All you have to do is run the following commands in order:
```
npm i
npx antora generate antora-playbook.yml
```
The generated website should appear under build.

### CI/CD Pipeline
This repository is scheduled to re-build and deploy the website 4 times a day. Specifically, this happens at 00:00, 06:00, 12:00 and 18:00 UTC every day. This means content from the source repositories are pulled and website is built again accordingly. This is a 6 hour cycle. If documentation changes are pushed to one of the source repositories, it might not appear instantly once they are pushed, you have to wait until the website rebuilds automatically.

### Manual Building and Deployment
You can not trigger the workflow to build and deploy the documentation website by yourself if you do not have the privileges in the repository. If you do, then you can for troubleshooting. Anyone can still fork the repository and manually build on their own github subdomain. In this case, relevant files need to be edited to replace the url to your own fork before deployment. This is unnecessary in most cases and is of little benefit for development if any, as most anything can be tested locally on demand.

## License
This project is under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.
