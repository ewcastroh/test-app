# quiz-cli

An interactive command-line quiz game for learning JavaScript.

This repository contains a Node.js CLI app that loads quiz questions from `data/questions.json`, lets you choose a category and number of questions, then runs a scored quiz with progress updates, answer feedback, explanations, and a final results summary.

## Project overview

The app is organized around a simple CLI flow:

1. Show a banner
2. Select a quiz category
3. Choose how many questions to answer
4. Run the quiz loop
5. Display final results
6. Offer to play again

It uses ES modules and Node’s built-in APIs only.

## Features

- Category-based quiz selection
- Configurable number of questions
- Shuffled question order
- Multiple-choice answer selection
- Score tracking
- Answer history
- Progress feedback during the quiz
- Correctness feedback after each question
- Explanations for answers
- Final results summary
- Colorized terminal output
- Replay prompt after finishing

## Requirements

- Node.js `>=18.0.0`

## Installation

No dependencies are declared in `package.json`, so there is nothing to install.

Clone the repository and make sure you are using a compatible Node.js version:

```bash
git clone https://github.com/ewcastroh/test-app.git
cd test-app
```

## Usage

Run the quiz with:

```bash
npm start
```

Or run the entry point directly:

```bash
node index.js
```

## Available scripts

From `package.json`:

```json
{
  "start": "node index.js",
  "test": "node --test"
}
```

### Start the app

```bash
npm start
```

### Run tests

```bash
npm test
```

## Project structure

```text
.
├── data/
│   └── questions.json
├── index.js
├── package.json
└── src/
    ├── colors.js
    ├── input.js
    └── quiz.js
```

### Key files

- `index.js` — application entry point; loads questions, handles category and question-count selection, runs the quiz, and shows results
- `src/quiz.js` — quiz engine with shuffling, scoring, answer history, progress, feedback, explanations, and final results
- `src/input.js` — `readline` helpers for prompts, numbered selections, yes/no confirmation, and waiting for Enter
- `src/colors.js` — ANSI terminal color helpers
- `data/questions.json` — quiz content and category data

## Quiz data format

The quiz content lives in `data/questions.json`.

Based on the current repository structure, the quiz data includes:

- quiz categories
- question entries
- multiple-choice options
- correct answer indexes
- explanations

If you want to add or modify questions, update this file to match the existing structure used by the app.

## Extending the question bank

To add more quiz content:

1. Open `data/questions.json`
2. Add questions to an existing category or create a new category
3. Make sure each question includes:
   - question text
   - a set of answer options
   - the index of the correct option
   - an explanation

Keep the format consistent with the current data so the quiz can load it correctly.

## Testing

Run the built-in test runner with:

```bash
npm test
```

This uses Node’s native test runner (`node --test`).

## License

MIT