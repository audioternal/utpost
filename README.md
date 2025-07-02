# Utpost.net Information Website

## Mission & Purpose

Utpost.net is a static information website designed to provide clear, reliable, and easily updatable content for our community. Our mission is to make information accessible and manageable for everyone, regardless of technical skill. The site is open source, hosted on GitHub Pages, and is easy to update by editing Markdown files.

**Key Goals:**
- **Simplicity:** Easy to update and maintain, even for non-technical users.
- **Transparency:** All content and code are open source.
- **Reliability:** Hosted on GitHub Pages with a custom domain (www.utpost.net) for maximum uptime and accessibility.
- **Minimalism:** As little JavaScript as possible—only the contact form uses JS.

---

## Features
- **Static site** built with [Astro](https://astro.build/)
- **Content in Markdown**: All pages and blog posts are written in Markdown
- **Blog**: Write and edit posts in Markdown
- **Editable Home, About, and Contact pages**
- **Minimal JavaScript**: Only the contact form uses JS
- **Deployed to GitHub Pages** with a custom domain: [www.utpost.net](http://www.utpost.net)
- **Markdown rendering**: All dynamic Markdown is rendered using the [marked](https://www.npmjs.com/package/marked) package and Astro's `innerHTML`.

---

## Getting Started

### 1. Prerequisites
- [Node.js 20.x](https://nodejs.org/) (use [nvm](https://github.com/nvm-sh/nvm) to manage versions)
- [Git](https://git-scm.com/)

### 2. Clone the Repository
```sh
git clone https://github.com/YOUR-USERNAME/utpost.net.git
cd utpost.net/wretched-wind
```

### 3. Set the Correct Node.js Version (IMPORTANT!)
Before running any commands, make sure you are using Node.js 20:
```sh
nvm use 20
```
If you see an error, install Node.js 20 with:
```sh
nvm install 20
nvm use 20
```

### 4. Install Dependencies
```sh
npm install
```

### 5. Start the Local Development Server
```sh
npm run dev
```
Visit [http://localhost:4321](http://localhost:4321) in your browser.

---

## Editing Content (Markdown)
- **Home, About, Contact:** Edit the files in `content/pages/*.md`
- **Blog posts:** Edit or add files in `content/posts/*.md`
- Use any Markdown editor or a simple text editor.
- The frontmatter (between `---` lines) contains metadata like the title. The body text goes after the frontmatter.

**Example:**
```markdown
---
title: About Utpost.net
---

## About Us

Utpost.net was founded to provide clear, reliable information to our community.
```

---

## Deployment

### Deploy to GitHub Pages
- All changes pushed to the `main` branch are automatically built and deployed via GitHub Actions.
- The site is published to the `gh-pages` branch and served at your custom domain (www.utpost.net).

### Custom Domain
- In your GitHub repo, go to **Settings > Pages** and set the custom domain to `www.utpost.net`.

---

## For Non-Technical Users
- **All content can be edited by editing Markdown files**—no need to touch code or understand GitHub Actions.
- If you need help, ask a technical friend to set up the project, then you can manage content yourself by editing Markdown files.

---

## Troubleshooting
- **Markdown body not rendering?**
  - Make sure your Markdown files have correct frontmatter (between `---` lines) and that the body text is after the frontmatter.
  - Example:
    ```markdown
    ---
    title: Example Page
    ---
    
    ## Heading
    Body text here.
    ```
- If you have issues with Node.js versions, always run `nvm use 20` before starting the dev server.

---

## Support & Contributions
- This project is open source. Contributions and suggestions are welcome!
- For help, open an issue on GitHub or contact the maintainers.
