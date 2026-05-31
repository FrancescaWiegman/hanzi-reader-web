# Hanzi Reader - Web Frontend

Multi-platform Chinese language learning application. This is the web frontend.

## Features

- 📖 Chinese text segmentation and annotation
- 🔤 Pinyin and tone marks display
- 🌈 Color-coded HSK levels
- 📊 Vocabulary statistics
- 💾 User knowledge tracking
- 🎯 HSK practice lists
- 🔊 Text-to-speech integration

## Project Structure

```
src/
├── components/          # Reusable React components
├── pages/              # Page components (Reader, Stats, Settings)
├── services/           # API calls and external services
├── store/              # Redux/Zustand state management
├── types/              # TypeScript interfaces
├── styles/             # Tailwind CSS + global styles
├── hooks/              # Custom React hooks
├── utils/              # Helper functions
└── App.tsx
```

## Tech Stack

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Vite** - Build tool
- **TailwindCSS** - Styling
- **Redux Toolkit** - State management
- **Axios** - HTTP client

## Getting Started

### Prerequisites
- Node.js 16+
- npm or yarn

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

The app will be available at `http://localhost:5173`

### Production Build

```bash
npm run build
npm run preview
```

## API Integration

The frontend connects to the backend API at `http://localhost:8080/api`

## Related Repositories

- [Backend API](https://github.com/FrancescaWiegman/hanzi-reader-api)
- [Data Pipeline](https://github.com/FrancescaWiegman/hanzi-reader-data-pipeline)
- [Android](https://github.com/FrancescaWiegman/hanzi-reader-android)
- [iOS](https://github.com/FrancescaWiegman/hanzi-reader-ios)
