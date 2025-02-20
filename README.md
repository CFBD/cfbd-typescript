# cfbd
This is an API for query various college football datasets and analytics. API keys can be acquired from the CollegeFootballData.com website.

This TypeScript package is automatically generated by the [Hey API](https://heyapi.vercel.app/) project:

- API version: 5.5.1
- Package version: 5.5.1

## Requirements.

Node 18+

## Installation
### npm install

```sh
npm install cfbd
```

### yarn install

```sh
yarn add cfbd
```

### pnpm install

```sh
pnpm add cfbd
```

## Usage

### Authorization

To authorize requests, use the `setConfig` method to set the `Authorization` header using your personal API key. API keys can be acquired from the CollegeFootballData.com website.

```typescript
import { client } from 'cfbd';

client.setConfig({
    headers: {
        'Authorization': 'Bearer YOUR_API_KEY',
    }
});

```

### Example Usage

All API operations can be imported from the `cfbd` package and used as shown below.

```typescript
import { client, getGames } from 'cfbd';

// Set up the client with your API key
client.setConfig({
    headers: {
        'Authorization': 'Bearer YOUR_API_KEY',
    }
});

// Call the getGames endpoint
const games = await getGames({
    query: {
        year: 2023,
        classification: 'fbs',
    },
});

for (const game of games.data ?? []) {
    // Do something with the game data
    // For example:
    console.log(`${game.awayTeam} vs ${game.homeTeam} - ${game.excitementIndex}`);
}
```

## Author

admin@collegefootballdata.com


