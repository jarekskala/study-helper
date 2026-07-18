# Flash Cards & Quizzes

A personal study app for flashcards and quiz questions. Content is organized
in folder trees and via tags; a study run or quiz is composed by selecting
folders and/or tags. Single-user, Czech UI, deployed on Vercel.

## Features

- 📁 **Folder trees** — separate sections for flashcards and quizzes, unlimited nesting
- 🏷️ **Tags** — cross-cutting labels across folders
- 🎓 **Study runs** — select folders and/or tags (union), optional shuffle,
  flip cards with the keyboard
- ❓ **Quizzes** — multiple-choice questions, instant feedback, attempts are saved
- 📊 **History** — overview of quiz attempts with a per-answer breakdown
- ✍️ **Markdown** — card and question content is rendered as Markdown
- 🔒 **Password protection** — Basic Auth for public deployment

## Tech stack

| Layer      | Technology                                                                    |
| ---------- | ----------------------------------------------------------------------------- |
| Framework  | [Next.js 16](https://nextjs.org) (App Router, TypeScript)                     |
| UI         | [Tailwind CSS](https://tailwindcss.com) + [shadcn/ui](https://ui.shadcn.com)  |
| Database   | [Neon Postgres](https://neon.tech) (serverless)                               |
| ORM        | [Drizzle ORM](https://orm.drizzle.team)                                       |
| Validation | [Zod](https://zod.dev)                                                        |

## Getting started

### Prerequisites

- Node.js 20+
- npm
- A [Neon](https://neon.tech) account (database)

### Installation

1. Clone the repository and install dependencies:

   ```bash
   git clone https://github.com/jarekskala/study-helper.git
   cd study-helper
   npm install
   ```

2. Copy `.env.example` to `.env.local` and fill in the values:

   ```bash
   cp .env.example .env.local
   ```

   | Variable       | Description                 |
   | -------------- | --------------------------- |
   | `DATABASE_URL` | Connection string from Neon |
   | `APP_PASSWORD` | Password for Basic Auth     |

3. Apply database migrations:

   ```bash
   npm run db:migrate
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

   The app runs at [http://localhost:3000](http://localhost:3000).

## License

Private project, no license — the code is not intended for redistribution.
