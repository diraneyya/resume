# orwa.tech

## Fork's documentation

This section is a WIP.

### Bun vs. Node/pnpm

I am currently using `bun` v1.1.33 both as the Astro Javascript runtime and as the package manager.

This choice was originally driven by the desire to deploy the site automatically using Cloudflare Pages (in a manner similar to GitHub/GitLab pages where the deployment script is triggered via a push).

In practice, it was much easier and much more practical to use the `wrangler` cli tool from Cloudflare to deploy the site. This had many advantages:

1. I no longer needed to login via a browser to see if the deployment failed/succeeded.
2. I was more in control of the build environment and did not have to bother with a myriad of issues resulting from Cloudflare's CI/CD implementation, which was just painful to be honest (sometimes the build failed for no clear reason, with files missing that are not missing from the repository)
3. Decouple deployments from commits, which I find really convenient and more suitable for a personal site of this nature.

Currently, to deploy the site I use the following command:

```bash
bun run deploy:cloudflare
```

### Shine effect

I am still working on perfecting the shine effect, which is currently only visible in the title, the freelance/skill badges.

The challenge there is how to apply it to a replaced-element like an "img" tag without absolute positioning, I am still trying to figure this out.

An important part of perfecting the effect is also making it dark-theme-compatible, which it currently is not.

### Geist-mono font

The mono font currently used on the site is modified. The space is 33% narrower than the space found in the `woff2` fonts obtained through Google Fonts.

I used FontForge (which is free and open source) to edit the font on a Mac OS X, which was straitforward.

### Employment duration

One important aspect of any resume is how it displays employment/education date ranges.

I have opted for encoding the exact dates in the HTML, but showing only the year as part of the range. In addition, I used the exact dates to display a duration of the eymployment, while opting for other simplifications to make that duration easier to understand.

## Original documentation

<div align="center">
<img src="logo.png" height="90px" width="auto" /> 
<h2>
    <em>Minimalist Resume/CV Layout for Web and PDF</em>
</h2>
<p>
JSON CV schema from <a href="https://jsonresume.org/schema/">jsonresume.org</a>
</p>


<p>
Based on design by <a href="https://github.com/BartoszJarocki/cv">Bartosz Jarocki</a>

</p>

</div>

<div align="center">
    <a href="#-getting-started">
        Getting Started
    </a>
    <span>&nbsp;✦&nbsp;</span>
    <a href="#-commands">
        Commands
    </a>
    <span>&nbsp;✦&nbsp;</span>
    <a href="#-license">
        License
    </a>
    <span>&nbsp;✦&nbsp;</span>
    <a href="https://midu.dev">
        Personal
    </a>
   
</div>

<p></p>

<div align="center">

![Astro Badge](https://img.shields.io/badge/Astro-BC52EE?logo=astro&logoColor=fff&style=flat)
![GitHub stars](https://img.shields.io/github/stars/midudev/minimalist-portfolio-json)
![GitHub issues](https://img.shields.io/github/issues/midudev/minimalist-portfolio-json)
![GitHub forks](https://img.shields.io/github/forks/midudev/minimalist-portfolio-json)
![GitHub PRs](https://img.shields.io/github/issues-pr/midudev/minimalist-portfolio-json)

</div>

<img src="portada.png"></img>

## 🛠️ Tech Stack

- [**Astro**](https://astro.build/) - The modern web framework
- [**Typescript**](https://www.typescriptlang.org/) - Type syntax for JavaScript
- [**Ninja Keys**](https://github.com/ssleptsov/ninja-keys) - Pure JavaScript keyboard shortcut dropdown

## 🚀 Getting Started

### 1. Use this [repo](https://github.com/midudev/minimalist-portfolio-json) as an Astro project template


- I use [pnpm](https://pnpm.io/installation) as package manager

```bash
# Enable pnpm on MacOS, WSL & Linux:
corepack enable
corepack prepare pnpm@latest --activate

# Initialize project
pnpm create astro@latest -- --template midudev/minimalist-portfolio-json
```

### 2. Add your content:
Edit the `cv.json` file to create your printable Portfolio/CV
### 3. Start dev server:

```bash
# See the result
pnpm dev
```


1. Open [**http://localhost:4321**](http://localhost:4321/) in your browser to view 🚀


## 🧞 Commands

|     | Command          | Action                                        |
| :-- | :--------------- | :-------------------------------------------- |
| ⚙️  | `dev` or `start` | Starts local dev server at `localhost:4321`  |
| ⚙️  | `build`          | Builds production bundle to `./dist/`        |
| ⚙️  | `preview`        | Local preview of production build            |


## 🔑 License

[MIT](LICENSE.txt) - Created by [**midudev**](https://midu.dev).
