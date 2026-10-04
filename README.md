# Blog & Tutorials

A Next.js blog and tutorials platform. Tutorials, books and PDFs are loaded from a JSON file, can be filtered by tag, searched by title, paginated, and saved as favorites.

## Overview

- **Tutorial catalog:** the home page lists tutorials, books and PDFs from `public/tutoriels.json`, with tag filtering and pagination (5 per page).
- **Favorites:** items can be added to or removed from favorites, which are saved in the browser's `localStorage` and listed on the Profile page.
- **Search:** a search page filters tutorials by title.
- **Dynamic routes:** `/tutoriels/[tutorielId]` and `/tutoriels/[tutorielId]/[sectionId]` display a tutorial and its sections.
- **Static pages:** About, Blog and a Contact form (client-side state, logged to the console on submit).
- **Shared header:** navigation bar built with CSS Modules and `classnames`, showing the app name from an environment variable.

## Technologies Used

- **Framework:** Next.js 15 (Pages Router), React 19
- **Styling:** CSS Modules, `classnames`
- **Data:** static JSON file (`public/tutoriels.json`)
- **Persistence:** browser `localStorage` (favorites)
- **Linting:** ESLint

## Prerequisites

- Node.js 18+

## Run Locally

Clone the project:

    git clone https://github.com/RajaAifa/blog.git

Go to the project directory:

    cd blog

Install dependencies:

    npm install

Create a `.env.local` file at the project root:

    NEXT_PUBLIC_APP_NAME=My Blog

Start the development server:

    npm run dev

The app runs at http://localhost:3000.

## How to Use

1. `/` — browse tutorials, filter by tag, paginate, and add items to favorites.
2. `/recherche` — search tutorials by title.
3. `/tutoriels/1` and `/tutoriels/1/1` — open a tutorial and read its sections.
4. `/profile` — view your favorite tutorials.
5. `/blog`, `/about`, `/contact` — static pages and the contact form.

## Project Structure

    projet/
    ├── src/
    │   ├── components/
    │   │   └── Header.js              # Navigation bar
    │   ├── pages/
    │   │   ├── api/hello.js           # Sample API route
    │   │   ├── blog/index.js          # Blog page
    │   │   ├── tutoriels/
    │   │   │   ├── [tutorielId].js            # Tutorial page
    │   │   │   └── [tutorielId]/[sectionId].js # Tutorial section page
    │   │   ├── about.js
    │   │   ├── contact.js             # Contact form
    │   │   ├── profile.js             # Favorites
    │   │   ├── recherche.js           # Search
    │   │   └── index.js               # Home: list, tag filter, pagination
    │   └── styles/                    # Global and CSS Module styles
    ├── public/
    │   └── tutoriels.json             # Tutorials data
    ├── next.config.mjs
    └── package.json
