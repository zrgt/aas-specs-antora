# Antora Meta-Repository - Asset Administration Shell (AAS) 

This is repository contains the structure for building the documentation website for the AAS by [the Industrial Digital Twin Association](https://industrialdigitaltwin.org). This includes the means to generate it on demand by compiling and assembling the respective content from numerous remote repositories and sources written in ascii-doc using [Antora](https://antora.org/).

## Sources
This repository does not contain the website's content itself; instead, it coordinates the assembly of content from external sources, including:
- [Part 1: Core Concepts](https://github.com/admin-shell-io/aas-specs/)
- [Part 2: API Specifications](https://github.com/admin-shell-io/aas-specs-api)
- [Part 3a: IEC 61360 Compliance](https://github.com/admin-shell-io/aas-specs-iec61360)
- [Part 5: AASX Package Format](https://github.com/admin-shell-io/aas-specs-aasx)

Detailed information about source management is available in the [Antora playbook](antora-playbook.yml).

## User-Interface
The user interface for the documentation is maintained separately in [aas-specs-antora-ui](https://github.com/admin-shell-io/aas-specs-antora-ui). 

## Building the Documentation
The documentation is dynamically generated
- automatically every 6-hours or
- manually by authorized individuals

## Contribution Guidelines
Contributors should test changes locally before pushing to remote repositories to maintain the integrity of the documentation. If local testing is not feasible, or if you require assistance, please [open an issue](https://github.com/admin-shell-io/aas-specs-antora/issues) for detailed guidance or to request manual build privileges. While direct testing on the live website is possible, it's discouraged due to potential complications. The site is also automatically updated several times a day, allowing for a natural review of changes.

## Reporting Issues
For issues related to the documentation structure or content, please [open an issue](https://github.com/admin-shell-io/aas-specs-antora/issues). We are proactive in addressing structural concerns upstream and welcome pull requests for improvements. Source maintainers are encouraged to report any structural issues directly in this repository.

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
