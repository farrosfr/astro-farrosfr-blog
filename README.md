# Astro Starter Kit: Blog

```sh
npm create astro@latest -- --template blog
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

Features:

- ✅ Minimal styling (make it your own!)
- ✅ 100/100 Lighthouse performance
- ✅ SEO-friendly with canonical URLs and OpenGraph data
- ✅ Sitemap support
- ✅ RSS Feed support
- ✅ Markdown & MDX support

## 🚀 Project Structure

This Astro project follows a standard structure to organize its files and features:

- `public/`: Contains static assets like fonts, images, and `favicon.svg`. These files are served directly at the root of the domain.
- `src/`: The main source directory for all Astro-related code.
    - `assets/`: Stores static assets used within components or pages, such as blog post images.
    - `components/`: Houses reusable UI components built with Astro, or other frameworks like React, Vue, etc. Examples include `Header.astro`, `Footer.astro`, and `ThemeToggle.astro`.
    - `content/`: Dedicated to content collections, primarily Markdown (`.md`) and MDX (`.mdx`) files. This project uses `src/content/blog/` for blog posts, leveraging Astro's Content Collections API for type-safe content management.
    - `layouts/`: Defines the structural templates for pages, such as `BlogPost.astro`, which provides a consistent look and feel across different content types.
    - `pages/`: Astro's file-based routing mechanism. Each `.astro`, `.md`, or `.mdx` file in this directory becomes a route.
        - `index.astro`: The homepage.
        - `blog/index.astro`: The blog listing page.
        - `blog/[...slug].astro`: A dynamic route for individual blog posts, where `slug` captures the path of the post.
    - `styles/`: Contains global CSS files, like `global.css`, for styling the application.
- `astro.config.mjs`: Astro configuration file.
- `package.json`: Project dependencies and scripts.
- `tsconfig.json`: TypeScript configuration.

## Components

Components in this project are located in `src/components/`. These are self-contained, reusable blocks of UI. They can be written in Astro's `.astro` format or integrated with other UI frameworks. Examples include:

- `BaseHead.astro`: Defines the common `<head>` elements for HTML pages.
- `Footer.astro`: The website footer.
- `FormattedDate.astro`: A utility component for displaying dates consistently.
- `Header.astro`: The navigation bar.
- `HeaderLink.astro`: A component for navigation links within the header.
- `SearchModal.astro`: A component likely used for a search overlay or modal.
- `ThemeInitializer.astro`: Handles the initial setup of the theme (e.g., dark/light mode).
- `ThemeToggle.astro`: A component for switching between light and dark themes.

## Routing

Astro utilizes a file-based routing system. Any `.astro`, `.md`, or `.mdx` file placed in the `src/pages/` directory automatically becomes an endpoint on your website.

- **Static Routes:** Files like `src/pages/index.astro` map directly to `/` and `src/pages/about.astro` maps to `/about`.
- **Dynamic Routes:** For content like blog posts, dynamic routes are used. For example, `src/pages/blog/[...slug].astro` handles all routes under `/blog/`, allowing for fetching content based on the `slug` parameter.

## State Management

As Astro primarily focuses on server-side rendering and static site generation, it does not include a built-in client-side state management solution. State management is typically handled in the following ways:

- **UI Framework Components:** If interactive components are built with frameworks like React, Vue, or Svelte, their native state management features (e.g., React's `useState`, `useContext`, or external libraries like Redux/Zustand) are used within those specific components.
- **URL Parameters/Local Storage:** For simpler state persistence across page loads or between components, URL query parameters or browser's `localStorage`/`sessionStorage` can be utilized.
- **Server-Side Data Fetching:** Most data is fetched and rendered on the server during the build process or on request, minimizing the need for complex client-side state.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Check out [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## Credit

This theme is based off of the lovely [Bear Blog](https://github.com/HermanMartinus/bearblog/).
