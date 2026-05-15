This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy Frontend Only on Vercel

This repository is a monorepo. To deploy only the frontend, deploy `querify-frontend/app` as the Vercel project root.

### Option 1: Vercel Dashboard (recommended)

1. Import the repository in Vercel.
2. In **Project Settings -> Root Directory**, select `querify-frontend/app`.
3. Keep defaults:
	- Framework Preset: `Next.js`
	- Build Command: `npm run build`
	- Output Directory: `.next`
4. Add environment variable:
	- `NEXT_PUBLIC_API_BASE` = your deployed backend URL, for example `https://your-backend-domain.com/api`
5. Deploy.

### Option 2: Vercel CLI

Run from repository root:

```bash
npx vercel --cwd querify-frontend/app
```

For production deployment:

```bash
npx vercel --cwd querify-frontend/app --prod
```

### Important

If `NEXT_PUBLIC_API_BASE` is not set in Vercel, the app falls back to `http://localhost:8080/api`, which will not work in production.
