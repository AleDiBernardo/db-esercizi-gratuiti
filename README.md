# DB esercizi gratuiti

Un catalogo aperto di esercizi fisici in formato JSON, con istruzioni, gruppi muscolari, attrezzatura e classificazioni in italiano. Utile per applicazioni fitness, strumenti per la creazione di schede e progetti personali.

## Contenuto

La raccolta contiene **876 esercizi**, derivati da [Free Exercise DB](https://github.com/yuhonas/free-exercise-db). Titoli, istruzioni, gruppi muscolari, attrezzature e classificazioni sono tradotti in italiano con una terminologia naturale per il contesto fitness. I termini tecnici d’uso comune, come squat, curl e kettlebell, possono essere mantenuti. Gli identificativi originali rimangono invariati. La traduzione è aperta a correzioni e miglioramenti.

Il file `exercises.json` contiene l'intero catalogo.

## Struttura dei dati

| Campo | Contenuto |
| --- | --- |
| `id` | Identificativo originale stabile |
| `name` | Nome dell'esercizio in italiano |
| `force` | Tipo di forza, oppure `null` |
| `level` | Livello di difficoltà |
| `mechanic` | Tipologia del movimento, oppure `null` |
| `equipment` | Attrezzatura, oppure `null` |
| `primaryMuscles` | Gruppi muscolari principali |
| `secondaryMuscles` | Gruppi muscolari secondari |
| `instructions` | Passaggi per l'esecuzione in italiano |
| `category` | Categoria dell'esercizio |

I valori `null` indicano informazioni non specificate nella fonte.

## Utilizzo

Scarica [`exercises.json`](https://raw.githubusercontent.com/AleDiBernardo/db-esercizi-gratuiti/main/exercises.json) e importalo nel tuo progetto. Non sono necessari account, chiavi API o dipendenze.

```javascript
import exercises from './exercises.json';

const addominali = exercises.filter(exercise =>
  exercise.primaryMuscles.includes('addominali')
);
```

L'importazione JSON dipende dal runtime o dal bundler utilizzato. Per applicazioni pubbliche è consigliabile importare il catalogo o conservarne una copia nella propria infrastruttura, anziché dipendere dal ramo corrente del repository.

## Provenienza

Dati originali: [yuhonas/free-exercise-db](https://github.com/yuhonas/free-exercise-db), distribuiti sotto [Unlicense](https://github.com/yuhonas/free-exercise-db/blob/main/LICENSE.md). Il progetto originale deriva dal lavoro di [Ollie Jennings](https://github.com/wrkout/exercises.json).

Questa raccolta contiene una traduzione italiana dei titoli, delle istruzioni e delle classificazioni. Non è una traduzione ufficiale del progetto originale.

## Contribuire

Sono benvenute correzioni linguistiche, miglioramenti delle descrizioni e segnalazioni di errori. Conserva gli identificativi esistenti per mantenere la compatibilità con le applicazioni che usano il catalogo.

## Licenza

La traduzione italiana e i contributi originali di questa raccolta sono distribuiti sotto **Creative Commons Attribution 4.0 International (CC BY 4.0)**. Consulta [LICENSE](LICENSE) e il [riepilogo ufficiale](https://creativecommons.org/licenses/by/4.0/).

Sono consentiti copia, modifica e uso commerciale, a condizione di riconoscere i crediti, fornire un collegamento alla licenza e indicare eventuali modifiche. Attribuzione suggerita: «DB esercizi gratuiti — AleDiBernardo e contributori, CC BY 4.0», accompagnata dal collegamento https://github.com/AleDiBernardo/db-esercizi-gratuiti.

La CC BY 4.0 si applica soltanto ai diritti sulla traduzione e sui contributi originali, nella misura in cui tali diritti sussistono. I dati originali di Free Exercise DB rimangono disponibili sotto Unlicense; il relativo testo è conservato in [LICENSE-UPSTREAM.md](LICENSE-UPSTREAM.md).

Le concessioni CC BY 4.0 già ricevute non sono revocabili per chi rispetta le condizioni della licenza.

## Nota sull'esecuzione

Il catalogo ha finalità informative e non costituisce un programma personalizzato. Le istruzioni tradotte non risultano sottoposte a una revisione tecnica completa. Cinque esercizi non hanno istruzioni nella fonte: il relativo array è lasciato vuoto. Eventuali indicazioni ambigue della fonte sono segnalate nel testo.
