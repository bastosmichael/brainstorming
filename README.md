# Brainstorming

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Brainstorming is a collaborative whiteboard application that lets teams sketch ideas, draw shapes, and add sticky notes together in real time. It uses Next.js, Convex, and Liveblocks for a smooth multi‑user experience with built‑in organization management and optional Pro subscriptions.

## Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Setup](#setup)
  - [Simple Mode Setup](#simple-mode-setup)
  - [Advanced Mode Setup](#advanced-mode-setup)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [FAQ](#faq)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Features

- Draw rectangles, ellipses, freehand paths, text, and sticky notes.
- Real-time presence and cursor syncing for all participants.
- Undo and redo history with keyboard shortcuts.
- Invite teammates to boards and manage organizations.
- Favorite boards and search across your workspace.
- Stripe-powered Pro upgrade for unlimited boards.
- Persistent storage backed by Convex.
- Authentication and user management via Clerk.
- Responsive UI built with TailwindCSS and ShadcnUI.

## Demo

[YouTube Demo](https://youtu.be/ADJKbuayubE)

## Setup

Both quick-start and advanced setup options are available. Make sure to provide the environment variables listed below.

### Simple Mode Setup

1. **Clone the Repository**
   ```bash
   git clone [repo-url]
   cd brainstorming
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Configure Environment**

   ```bash
   cp .env.example .env.local
   ```

   Required variables:

   * `APP_MODE=simple`
   * `CONVEX_DEPLOYMENT=`
   * `NEXT_PUBLIC_CONVEX_URL=`
   * `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=`
   * `CLERK_SECRET_KEY=`
   * `LIVEBLOCKS_SECRET_KEY=`

4. **Run the App**

   ```bash
   npm run dev
   ```

### Advanced Mode Setup

For production use you can enable additional features such as Stripe billing and custom domains.

1. Set `APP_MODE=advanced` in `.env.local`.
2. Provide `STRIPE_API_KEY`, `STRIPE_WEBHOOK_SECRET`, and `NEXT_PUBLIC_APP_URL`.
3. Run database migrations with `npx convex deploy` if deploying to Convex Cloud.
4. Start the server as in simple mode.

## Usage

1. Sign in or create an organization.
2. Create a new board from the dashboard.
3. Use the toolbar to add shapes, notes, or freehand drawings.
4. Invite teammates to collaborate in real time.
5. Mark important boards as favorites for quick access.

## Deployment

Deploy to Vercel for a serverless setup.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

1. Push your repository to GitHub.
2. In Vercel, import the project and set the environment variables from `.env.example`.
3. Deploy the `production` branch.

## Contributing

Contributions are welcome! Fork the repo and open a pull request with your changes.

## FAQ

**How do I invite collaborators?** Use the **Invite members** button in the dashboard to send organization invites.

**What happens if I exceed the free board limit?** You can upgrade to Pro at any time to unlock unlimited boards.

**Does the app work on mobile?** Yes. The UI is responsive and supports modern mobile browsers.

## License

This project is licensed under the MIT license.

## Acknowledgements

- [Next.js](https://nextjs.org/)
- [Convex](https://www.convex.dev/)
- [Liveblocks](https://liveblocks.io/)
- [Clerk](https://clerk.com/)
- [Stripe](https://stripe.com/)
- [ShadcnUI](https://ui.shadcn.com/)

## Contact

For support or questions, please open an issue on GitHub.
