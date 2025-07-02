# Utpost.net Information Website

## Mission & Purpose

Utpost.net is a static information website designed to provide clear, reliable, and easily updatable content for our community. Our mission is to make information accessible and manageable for everyone, regardless of technical skill. The site is open source, hosted on GitHub Pages, and uses TinaCMS—a user-friendly content management system—so that even computer-illiterate users can update the site with ease.

**Key Goals:**
- **Simplicity:** Easy to update and maintain, even for non-technical users.
- **Transparency:** All content and code are open source.
- **Reliability:** Hosted on GitHub Pages with a custom domain (www.utpost.net) for maximum uptime and accessibility.
- **Minimalism:** As little JavaScript as possible—only the CMS and contact form use JS.

---

## Features
- **Static site** built with [Astro](https://astro.build/)
- **Content managed with [TinaCMS](https://tina.io/)** (open source, visual, and easy to use)
- **Blog**: Write and edit posts in Markdown
- **Editable Home, About, and Contact pages**
- **Minimal JavaScript**: Only TinaCMS admin and contact form use JS
- **Deployed to GitHub Pages** with a custom domain: [www.utpost.net](http://www.utpost.net)
- **Markdown rendering**: All dynamic Markdown (from TinaCMS or content files) is rendered using the [marked](https://www.npmjs.com/package/marked) package and Astro's `innerHTML`.

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
npx astro dev
```
Visit [http://localhost:4321](http://localhost:4321) in your browser.

---

## Editing Content (with TinaCMS)
1. Go to `/admin` on your local site (e.g., [http://localhost:4321/admin](http://localhost:4321/admin))
2. Log in with your Tina Cloud account (set up at [tina.io](https://tina.io/))
3. Edit pages or blog posts visually—no coding required!

**Content files:**
- Home, About, Contact: `content/pages/*.md`
- Blog posts: `content/posts/*.md`

---

## Deployment

### Deploy to GitHub Pages
- All changes pushed to the `main` branch are automatically built and deployed via GitHub Actions.
- The site is published to the `gh-pages` branch and served at your custom domain (www.utpost.net).

### Set Up GitHub Secrets
- In your repo settings, add:
  - `TINA_PUBLIC_CLIENT_ID`
  - `TINA_TOKEN`
- These are required for TinaCMS to work in production. Get them from your [Tina Cloud dashboard](https://app.tina.io/projects).

### Custom Domain
- In your GitHub repo, go to **Settings > Pages** and set the custom domain to `www.utpost.net`.

---

## For Non-Technical Users
- **All content can be edited visually**—no need to touch code or understand Git.
- If you need help, ask a technical friend to set up the project, then you can manage content yourself via the TinaCMS admin interface.

---

## Troubleshooting
- **Markdown rendering:** If you see errors about `Astro.renderMarkdown` or `<Markdown>`, make sure you are using the `marked` package to render Markdown to HTML, and use `innerHTML` to display it. This project does not use Astro's built-in Markdown renderer for dynamic content.
- If you have issues with Node.js versions, always run `nvm use 20` before starting the dev server.

---

## Support & Contributions
- This project is open source. Contributions and suggestions are welcome!
- For help, open an issue on GitHub or contact the maintainers.

```