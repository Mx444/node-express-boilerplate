# Express Boilerplate

Questa è una boilerplate per un progetto Node.js con Express e TypeScript. Include configurazioni per lo sviluppo continuo usando Nodemon e la compilazione TypeScript.

## Struttura del Progetto

```markdown
/your-project
/src
server.ts
/build
(file generati dopo la compilazione)
package.json
tsconfig.json
README.md
```

## Prerequisiti

- Node.js (versione LTS raccomandata)
- npm (o yarn)

## Installazione

1. Clona il repository.
2. Installa le dipendenze.

```bash
git clone <url-del-tuo-repository>
cd your-project
npm install
```

## Script NPM

### `npm run build`

Compila i file TypeScript nella directory `build`.

### `npm run dev`

Avvia l'applicazione in modalità sviluppo usando Nodemon. Rileva modifiche nei file TypeScript nella directory `src` e riavvia automaticamente il server.

### `npm run start`

Avvia l'applicazione dal file compilato `build/server.js`.

## Configurazione TypeScript

Assicurati che il tuo `tsconfig.json` sia configurato correttamente:

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "ESNext",
    "lib": ["DOM", "ES6", "DOM.Iterable", "ScriptHost"],
    "allowJs": true,
    "skipLibCheck": true,
    "esModuleInterop": true,
    "allowSyntheticDefaultImports": true,
    "strict": true,
    "forceConsistentCasingInFileNames": true,
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "noEmit": false,
    "jsx": "react-jsx",
    "baseUrl": "./",
    "paths": {
      "@/": ["src/"]
    },
    "outDir": "./build",
    "rootDir": "./src"
  },
  "include": ["src//"],
  "exclude": ["node_modules", "build"]
}
```

## Variabili d'Ambiente

Per gestire le variabili d'ambiente, utilizza il pacchetto `dotenv`. Crea un file `.env` nella root del progetto. Ad esempio:

```markdown
PORT=3000
```

Puoi accedere a queste variabili nel tuo codice usando `process.env`.

## Esempio di Codice

Ecco un esempio di `src/server.ts`:

```typescript
import express from "express";

const app = express();
const PORT = process.env.PORT || 3000;

app.get("/", (req, res) => {
  res.send("Hello, world!");
});

app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
```

## Contributi

Si accettano contributi! Sentiti libero di fare il fork del repository e creare una pull request.

## Licenza

Questo progetto è distribuito sotto la licenza ISC.

## Istruzioni

1. Sostituisci `<url-del-tuo-repository>` con l'URL reale del tuo repository.
2. Aggiungi le variabili d'ambiente necessarie nel file `.env`.
3. Personalizza le informazioni come il nome dell'autore e i dettagli della licenza se necessario.
