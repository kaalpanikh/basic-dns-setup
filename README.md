# Basic DNS Setup for GitHub Pages & AWS Static Site Server

This project demonstrates how to deploy two distinct websites with custom DNS configurations:
- **GitHub Pages Deployment Workflow:** Hosted at [pages.nikhilmishra.live](https://pages.nikhilmishra.live) via GitHub with DNS configured using a CNAME file and a matching Cloudflare CNAME record.
- **AWS Static Site Server:** Hosted at [static.nikhilmishra.live](https://static.nikhilmishra.live) on AWS with DNS set up using an A record.

A detailed project overview and additional guidance can be found on the [project page](https://roadmap.sh/projects/basic-dns).

---

## Table of Contents

- [Overview](#overview)
- [Repositories](#repositories)
- [DNS Setup Details](#dns-setup-details)
  - [GitHub Pages Deployment Workflow](#github-pages-deployment-workflow)
  - [AWS Static Site Server](#aws-static-site-server)
- [Project Page](#project-page)
- [Setup Instructions](#setup-instructions)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This project illustrates two approaches for hosting websites with custom DNS records:

1. **GitHub Pages Workflow:** A repository (`gh-deployment-workflow`) uses a deployment workflow that automatically sets up a CNAME file. Once pushed, Cloudflare is configured with a corresponding CNAME record so that the site is accessible at [pages.nikhilmishra.live](https://pages.nikhilmishra.live).

2. **Static Site on AWS:** A separate repository (`static-site-server`) provides a static site served from an AWS instance. DNS is configured by adding an A record that maps your domain to the AWS server IP, making the site available at [static.nikhilmishra.live](https://static.nikhilmishra.live).

These configurations provide examples of modern DNS management alongside continuous deployment and static server hosting.

---

## Repositories

- **gh-deployment-workflow**  
  This repository includes:
  - A GitHub Actions workflow that deploys the site.
  - A `CNAME` file within the repository, which GitHub Pages uses to configure custom domains.
  - Instructions on setting up Cloudflare DNS to point your custom domain ([pages.nikhilmishra.live](https://pages.nikhilmishra.live)).  
  *Reference: citeturn0search0*

- **static-site-server**  
  This repository includes:
  - Code for running a static site server on AWS.
  - Documentation describing the DNS setup using an A record that binds the AWS server’s IP address to the custom domain ([static.nikhilmishra.live](https://static.nikhilmishra.live)).  
  *Reference: citeturn0search1*

---

## DNS Setup Details

### GitHub Pages Deployment Workflow

1. **CNAME File:**  
   A `CNAME` file in the repository specifies the custom domain. This file is crucial for GitHub Pages to correctly serve the site under the designated domain.

2. **Cloudflare Configuration:**  
   After adding the CNAME file, a CNAME record is created in Cloudflare pointing to GitHub’s pages servers. This ensures that [pages.nikhilmishra.live](https://pages.nikhilmishra.live) resolves correctly.

3. **Deployment:**  
   GitHub Actions automatically deploys updates. Once the workflow is triggered, the new changes are published to GitHub Pages.

### AWS Static Site Server

1. **A Record Configuration:**  
   An A record is added to your DNS settings (via Cloudflare or another DNS provider) that points the custom domain ([static.nikhilmishra.live](https://static.nikhilmishra.live)) to the IP address of the AWS server hosting the static site.

2. **Server Setup:**  
   The repository contains instructions and configuration files to set up and run a static site server on AWS. This setup allows you to serve static content directly from your server environment.

*Reference for DNS concepts: citeturn0search2*

---

## Project Page

For a broader roadmap and further details on DNS projects, check out the project page on roadmap.sh:  
[Basic DNS Project](https://roadmap.sh/projects/basic-dns)

---

## Setup Instructions

### GitHub Pages Workflow

1. **Clone the Repository:**  
   ```bash
   git clone https://github.com/kaalpanikh/gh-deployment-workflow.git
   cd gh-deployment-workflow
   ```

2. **Configure the CNAME:**  
   Ensure the `CNAME` file contains `pages.nikhilmishra.live`.

3. **Deploy via GitHub Actions:**  
   Push your changes to trigger the deployment workflow.

4. **DNS Configuration:**  
   In Cloudflare, create a CNAME record pointing `pages.nikhilmishra.live` to the appropriate GitHub Pages domain.

### AWS Static Site Server

1. **Clone the Repository:**  
   ```bash
   git clone https://github.com/kaalpanikh/static-site-server.git
   cd static-site-server
   ```

2. **Set Up the Server:**  
   Follow the instructions in the repository’s README to launch and configure your AWS server.

3. **DNS Configuration:**  
   In your DNS provider (e.g., Cloudflare), add an A record for `static.nikhilmishra.live` pointing to your AWS server’s public IP.

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes with clear descriptions.
4. Open a pull request and describe your changes.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

This README is designed to be a single point of reference for setting up both the GitHub Pages deployment workflow and the AWS static site server. It outlines the necessary DNS configurations, links to the source repositories, and provides step-by-step setup instructions. Feel free to expand or modify sections to better suit your project's evolving needs.

*References:*
- GitHub Deployment Workflow details: citeturn0search0
- Static Site Server details: citeturn0search1
- DNS Project Roadmap: citeturn0search2
