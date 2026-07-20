
BRENNEN GABRIEL MULTI-PAGE SVELTEKIT PORTFOLIO
===============================================

WHAT IS INCLUDED
----------------
- Home page
- About page
- Projects page
- Experience page
- Resume page
- Contact page
- Shared responsive navigation
- Mobile menu
- Complete site styling
- GitHub Pages-safe links using SvelteKit's base path

HOW TO INSTALL
--------------
1. Make a backup copy of your current project.

2. Unzip this package.

3. Copy the included "src" folder into the root of your SvelteKit project.
   Replace your existing src folder when prompted.

4. Copy the included "static" folder into the root of your project.
   Merge it with your existing static folder.

5. From your project folder, run:

   npm install
   npm run check
   npm run dev

6. Open the local address shown in Terminal.

RESUME
------
Place your resume PDF here:

static/resume/Brennen-Gabriel-Resume.pdf

CONTACT PAGE
------------
Open:

src/routes/contact/+page.svelte

Replace:
- your-email@example.com
- linkedin.com/in/your-profile

PROJECT CONTENT
---------------
Edit project details in:

src/routes/projects/+page.svelte

PROFILE PHOTO
-------------
The About page currently uses a "BG" placeholder.
You can later replace it with an image inside:

src/routes/about/+page.svelte

GITHUB PAGES
------------
The navigation uses "$app/paths", so it works with a GitHub Pages base path
when your SvelteKit configuration is already set up correctly.

IMPORTANT
---------
This package intentionally does not replace your package.json, svelte.config.js,
or vite.config files, because your current project already contains the GitHub
Pages deployment configuration.
