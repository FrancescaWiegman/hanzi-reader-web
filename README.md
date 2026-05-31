# Hanzi Reader - Web Frontend (Angular)

Multi-platform Chinese language learning application. This is the web frontend built with Angular.

## Features

- 📖 Chinese text segmentation and annotation
- 🔤 Pinyin and tone marks display
- 🎨 Color-coded HSK levels
- 📊 Vocabulary statistics
- 📚 User knowledge tracking
- 🎯 HSK practice lists
- 🔊 Text-to-speech integration

## Project Structure

```
src/
├── app/
│   ├── components/          # Reusable components
│   │   ├── text-reader/
│   │   ├── dictionary-search/
│   │   ├── vocabulary-manager/
│   │   ├── hsk-practice/
│   │   └── statistics/
│   ├── services/            # API and business logic
│   │   ├── text.service.ts
│   │   ├── dictionary.service.ts
│   │   ├── vocabulary.service.ts
│   │   └── hsk.service.ts
│   ├── store/               # NgRx state management
│   │   ├── actions/
│   │   ├── reducers/
│   │   └── selectors/
│   ├── models/              # TypeScript interfaces
│   ├── interceptors/        # HTTP interceptors
│   ├── guards/              # Route guards
│   ├── pipes/               # Custom pipes
│   ├── app.component.ts
│   ├── app.routing.module.ts
│   └── app.module.ts
├── assets/                  # Static files
├── styles/                  # Global styles
├── environments/            # Environment configs
├── index.html
├── main.ts
├── styles.scss
and └── test.ts
```

## Tech Stack

- **Angular 17** - Frontend framework
- **TypeScript 5** - Language
- **NgRx 17** - State management
- **TailwindCSS** - Styling
- **Axios** - HTTP client
- **Karma/Jasmine** - Testing

## Getting Started

### Prerequisites
- Node.js 18+
- npm 9+
- Angular CLI 17

### Installation

```bash
# Install Angular CLI
npm install -g @angular/cli

# Install dependencies
npm install
```

### Development

```bash
# Start development server
npm start

# Navigate to http://localhost:4200/
# The application will automatically reload if you change any source files
```

### Production Build

```bash
npm run build
# Output will be in dist/hanzi-reader-web/
```

### Running Tests

```bash
npm run test
```

### Linting

```bash
npm run lint
```

## Architecture

### Component Hierarchy

```
AppComponent
├── HeaderComponent
├── SidebarComponent
├── RouterOutlet
│   ├── TextReaderComponent (reader route)
│   ├── VocabularyComponent (vocabulary route)
│   ├── HSKPracticeComponent (hsk route)
│   ├── DictionaryComponent (dictionary route)
│   └── StatisticsComponent (stats route)
└── FooterComponent
```

### State Management (NgRx)

```
Store
├── Text State
│   ├── currentText
│   ├── annotatedTokens
│   └── loading
├── Vocabulary State
│   ├── userWords
│   ├── filters
│   └── pagination
└── Dictionary State
    ├── searchResults
    ├── selectedWord
    └── cache
```

### API Integration

All API calls go through services:

```
Component
  ↓
Service (text.service, vocabulary.service, etc.)
  ↓
HttpInterceptor (add auth, handle errors)
  ↓
Backend API (localhost:8080/api)
```

## Configuration

### Environment Variables

Create `src/environments/environment.ts`:

```typescript
export const environment = {
  production: false,
  apiUrl: 'http://localhost:8080/api',
  logLevel: 'debug'
};
```

Create `src/environments/environment.prod.ts`:

```typescript
export const environment = {
  production: true,
  apiUrl: 'https://api.hanzi-reader.app/api',
  logLevel: 'error'
};
```

## Styling

Uses TailwindCSS for utility-first styling:

```bash
# TailwindCSS is already configured in angular.json
# Add custom styles in src/styles.scss
```

## Related Repositories

- [Backend API](https://github.com/FrancescaWiegman/hanzi-reader-api)
- [Data Pipeline](https://github.com/FrancescaWiegman/hanzi-reader-data-pipeline)
- [Android](https://github.com/FrancescaWiegman/hanzi-reader-android)
- [iOS](https://github.com/FrancescaWiegman/hanzi-reader-ios)
