# CoinPulse

CoinPulse is a modern crypto dashboard built with Next.js and Tailwind CSS. It delivers real-time cryptocurrency data from the CoinGecko API and live price updates using WebSocket streams.

## Features

- Real-time coin price updates and live trading data
- Trending coins list with 24-hour percentage changes
- Coin market overview and category performance
- Detailed coin pages with price chart, recent trades, and on-chain pool data
- Built-in converter for crypto price conversion across supported currencies
- Responsive UI with server-side data fetching and client-side live updates

## Tech Stack

- Next.js 16
- React 19
- TypeScript
- Tailwind CSS 4
- CoinGecko API
- WebSocket data streams
- Lightweight Charts

## Getting Started

### Prerequisites

- Node.js 20+ recommended
- npm or yarn

### Install dependencies

```bash
npm install
```

### Environment Variables

Create a `.env.local` file in the project root and add the following variables:

```env
COINGECKO_BASE_URL=https://api.coingecko.com/api/v3
COINGECKO_API_KEY=your_coingecko_api_key
NEXT_PUBLIC_COINGECKO_WEBSOCKET_URL=your_websocket_url
NEXT_PUBLIC_COINGECKO_API_KEY=your_websocket_api_key
```

> If you are using the free CoinGecko public API, set `COINGECKO_BASE_URL` to `https://api.coingecko.com/api/v3`. For premium users, use the CoinGecko Pro base URL and API key as needed.

### Development

```bash
npm run dev
```

Open `http://localhost:3000` to view the dashboard.

### Build

```bash
npm run build
```

### Start

```bash
npm run start
```

## Project Structure

- `app/` — Next.js app routes and pages
- `components/` — UI components and dashboard widgets
- `hooks/` — custom hooks for WebSocket live updates
- `lib/` — API helpers and utility functions
- `constants.ts` — chart configuration and shared constants
- `type.d.ts` — TypeScript global type definitions

## Notes

- The dashboard uses a CoinGecko client-side WebSocket hook for live price and trade updates.
- Remote image loading is configured for `assets.coingecko.com` and `coin-images.coingecko.com`.
- The `Converter` component supports currency conversion using the fetched coin price list.

## License

This project is provided as-is for demonstration purposes.
