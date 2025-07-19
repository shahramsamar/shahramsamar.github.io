# Shahram Samar - Professional Resume

![GitHub Pages](https://github.com/shahramsamar/shahramsamar.github.io/actions/workflows/deploy.yml/badge.svg)
![HTML Validation](https://img.shields.io/badge/HTML-Valid-brightgreen)

This repository hosts my professional resume/portfolio website, automatically deployed to GitHub Pages.

## 🌐 Live Website
[Go live](shahramsamar.netlify.app/)

## 🚀 Features
- Clean, responsive HTML/CSS resume
- Automated deployment via GitHub Actions
- HTML validation on every commit
- Always up-to-date with my latest experience

## 🛠️ Technical Stack
- **Frontend**: HTML5, CSS3, Bootstrap 5
- **Backend**: GitHub Pages
- **CI/CD**: GitHub Actions
- **Tools**: Git, GitHub, Markdown

## 📂 Repository Structure
```
├── index.html        Main resume HTML file
├── static/           Static assets (CSS, images)
│└── styles.css       Custom styles
├── .github/workflows/ CI/CD workflows
│ └── deploy.yml     Deployment configuration
   └── README.md
```
# This documentation
## 🚄 Automatic Deployment
The site automatically deploys on every push to the `main` branch through GitHub Actions:
name: Deploy Resume to GitHub Pages
``` yml
  on:
    push:
      branches: ["main"]
    workflow_dispatch:
  
  permissions:
    pages: write
    id-token: write
  
  concurrency:
    group: "pages"
    cancel-in-progress: true
  
  jobs:
    deploy:
      environment:
        name: github-pages
        url: ${{ steps.deployment.outputs.page_url }}
      runs-on: ubuntu-latest
      steps:
        - name: Checkout
          uses: actions/checkout@v4
  
        - name: Setup Pages
          uses: actions/configure-pages@v3
          with:
            static_site_generator: "none"
  
        - name: Upload artifact
          uses: actions/upload-pages-artifact@v2
          with:
            path: "."
  
        - name: Deploy to GitHub Pages
          id: deployment
          uses: actions/deploy-pages@v2
```
        
## 🛠️ Local Development
To run locally:

Clone the repository:

bash
git clone https://github.com/shahramsamar/shahramsamar.github.io.git
Open index.html in your browser

## 📜 License
This project is licensed under the **MIT License** - see the LICENSE file for details.

## 📬 Contact
Email: [email me](shahramsamar.dev@gmail.com)

LinkedIn:[shahram samar](https://www.linkedin.com/in/shahram-samar/) 

GitHub: [shahramsamar]( https://github.com/shahramsamar)
