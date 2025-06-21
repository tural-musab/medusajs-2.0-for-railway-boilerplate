<p align="center">
  <a href="https://www.medusajs.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/59018053/229103275-b5e482bb-4601-46e6-8142-244f531cebdb.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/59018053/229103726-e5b529a3-9b3f-4970-8a1f-c6af37f087bf.svg">
      <img alt="Medusa logo" src="https://user-images.githubusercontent.com/59018053/229103726-e5b529a3-9b3f-4970-8a1f-c6af37f087bf.svg" width=100>
    </picture>
  </a>
  <a href="https://railway.app/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://railway.app/brand/logo-light.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://railway.app/brand/logo-dark.svg">
      <img alt="Railway logo" src="https://railway.app/brand/logo-light.svg" width=100>
    </picture>
  </a>
</p>

<h2 align="center">
  MedusaJS 2.0 Monorepo for Railway
</h2>
<h4 align="center">
  Backend + Storefront + PostgreSQL + Redis + MinIO + MeiliSearch
</h4>

<h2 align="center">
  <a href="https://railway.app">🚀 Deploy on Railway</a>
</h2>

<h1 align="center">
  Complete E-commerce Solution<br>
  <a href="#-backend-setup">📖 Quick Start Guide</a>
</h1>

<p align="center">
Combine Medusa's modules for your commerce backend with the newest Next.js 14 features for a performant storefront.</p>

## 🙏 Acknowledgment

This project is forked from [rpuls/medusajs-2.0-for-railway-boilerplate](https://github.com/rpuls/medusajs-2.0-for-railway-boilerplate).  
**Special thanks to Rasmus Puls** for creating this amazing boilerplate and making it available to the community!

## 🎯 What's This?

A complete, production-ready e-commerce solution featuring:
- **Modern Backend**: MedusaJS 2.0 with advanced commerce features
- **Fast Storefront**: Next.js 14 with optimized performance  
- **Cloud Storage**: MinIO for scalable file management
- **Smart Search**: MeiliSearch integration
- **Payment Ready**: Stripe integration included
- **Email Service**: Resend integration for transactional emails

## About this boilerplate
This boilerplate is a monorepo consisting of the officially released MedusaJS 2.0 backend and storefront application. It is a pre-configured, ready-to-deploy solution, optimized for seamless deployment on [Railway](https://railway.app).

Updated: to `version 2.8.4` 🥳

## ✨ Preconfigured 3rd party integrations

- **MinIO file storage**: Replaces local file storage with MinIO cloud storage, automatically creating a 'medusa-media' bucket for your media files. [README](backend/src/modules/minio-file/README.md)
- **Resend email integration** [Watch setup video](https://youtu.be/pbdZm26YDpE?si=LQTHWeZMLD4w3Ahw) - special thanks to [aleciavogel](https://github.com/aleciavogel) for Resend notification service, and react-email implementation! [README](backend/src/modules/email-notifications/README.md)
- **Stripe payment service**: [Watch setup video](https://youtu.be/dcSOpIzc1Og)
- **Meilisearch integration** by [Rokmohar](https://github.com/rokmohar/medusa-plugin-meilisearch): Adds powerful product search capabilities to your store. When deployed on Railway, MeiliSearch can be automatically configured. (Setup video: [Watch here](https://youtu.be/hrXcc5MjApI))

# 🛠️ Backend Setup

### Local setup
Video instructions: https://youtu.be/PPxenu7IjGM

- `cd /backend`
- `pnpm install` or `npm i`
- Rename `.env.template` →  `.env`
- To connect to your online database from your local machine, copy the `DATABASE_URL` value auto-generated on Railway and add it to your `.env` file.
  - If connecting to a new database, for example a local one, run `pnpm ib` or `npm run ib` to seed the database.
- `pnpm dev` or `npm run dev`

### Requirements
- **PostgreSQL database** (Can be auto-configured when deploying on Railway)
- **Redis** (Can be auto-configured when deploying on Railway) - fallback to simulated redis.
- **MinIO storage** (Can be auto-configured when deploying on Railway) - fallback to local storage.
- **Meilisearch** (Can be auto-configured when deploying on Railway)

### Commands

`cd backend/`

- `npm run ib` or `pnpm ib` will initialize the backend by running migrations and seed the database with required system data.
- `npm run dev` or `pnpm dev` will start the backend (and admin dashboard frontend on `localhost:9000/app`) in development mode.
- `pnpm build && pnpm start` will compile the project and run from compiled source. This can be useful for reproducing issues on your cloud instance.

# 🎨 Storefront Setup

### Local setup
Video instructions: https://youtu.be/PPxenu7IjGM

Install dependencies `npm i` or `pnpm i`
Rename `.env.local.template` →  `.env.local`

### Requirements
- A running backend on port 9000 is required to fetch product data and other information needed to build Next.js pages.

### Commands
`cd storefront/`

- `npm run dev` or `pnpm dev` will run the storefront on uncompiled code, with hot-reloading as files are saved with changes.

## 📚 Useful Resources
- How to setup credit card payment with Stripe payment module: https://youtu.be/dcSOpIzc1Og
- Original deployment guide: https://funkyton.com/medusajs-2-0-is-finally-here/#succuessfully-deployed-whats-next

## 🤝 Contributing

This is a forked repository. For contributions to the original work, please visit [rpuls/medusajs-2.0-for-railway-boilerplate](https://github.com/rpuls/medusajs-2.0-for-railway-boilerplate).

For issues specific to this fork, please open an issue in this repository.

## 📄 License

MIT License - see LICENSE file for details.

---

<p align="center">
  <strong>Ready to build your e-commerce empire? 🚀</strong><br>
  <a href="https://github.com/tural-musab/medusajs-2.0-for-railway-boilerplate">⭐ Star this repo if it helped you!</a>
</p>
