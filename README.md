# Keep Screen On

**A free, browser based tool for keeping your display awake.** Keep Screen On uses the [Screen Wake Lock API](https://developer.mozilla.org/en-US/docs/Web/API/Screen_Wake_Lock_API) to request that a supported browser keep the screen on while you work, present, read, or monitor a dashboard.

**Try it:** [keepscreenon.dev](https://keepscreenon.dev) | [No Sleep Page](https://keepscreenon.dev/no-sleep-page)

No app install, extension, or simulated mouse movement is needed. Open the page, choose how long to stay awake, and turn on the wake lock. The browser releases it when it can no longer keep the page active, such as when the tab closes or the timer ends.

## Highlights

- One click to request or release a screen wake lock.
- Preset durations and a custom countdown, or choose no limit.
- Clear active, paused, and unavailable states.
- Light and dark themes, plus a dimmed ambient display.
- Informational guides and an interactive wake lock control embedded in articles.
- Localized homepages in English, German, Chinese, Japanese, Spanish, Portuguese, French, Italian, and Korean.
- Server rendered pages, metadata, structured data, sitemap, and crawler guidance.

> Wake Lock support depends on the browser, device, and page visibility. The browser may release the lock when the page is backgrounded or the device enters a state where the lock cannot be maintained. Keep the page open and visible for the most reliable behavior.

## How it works

The app requests a screen wake lock from the browser after the user turns it on. It does not change operating system power settings or generate mouse and keyboard activity. A countdown can automatically release the lock when it expires.

## Built with

- [Next.js](https://nextjs.org/) App Router
- [React](https://react.dev/) and [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Vercel Analytics](https://vercel.com/analytics) and Speed Insights

## Run locally

### Requirements

- Node.js (LTS recommended)
- npm

### Start the development server

```bash
git clone <repository-url>
cd neversleep
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Available commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start the local development server |
| `npm run build` | Create a production build |
| `npm run start` | Serve the production build locally |
| `npm run lint` | Run ESLint |
| `npm run submit:indexnow` | Submit sitemap URLs through the configured IndexNow script |

## Project layout

```text
src/
  app/          Routes, page metadata, sitemap, and robots rules
  components/   Wake lock controls and shared interface components
  data/         Blog content and localized homepage copy
  hooks/        Wake lock state and timer behavior
public/         Static assets and LLM-readable site guides
scripts/        Search indexing utilities
```

## Content and search metadata

- Blog articles are maintained in `src/data/blogPosts.ts`; the blog listing and sitemap use this content.
- The sitemap and crawler rules are generated from `src/app/sitemap.ts` and `src/app/robots.ts`.
- Site guides for AI tools are maintained in `public/llms.txt` and `public/llms-full.txt`.
- `PROJECT.md` contains internal planning and SEO notes; it is not required to run the app.

## License

No license is currently specified. Contact the repository owner before redistributing or reusing this project.
