# Quiz CLI

A simple Node.js command-line quiz application that loads questions from `data/questions.json`, prompts the user in the terminal, and displays results with colored output.

## Overview

This repository appears to be a lightweight quiz/game app built with Node.js. The code is organized into small modules for input handling, quiz flow, and terminal colors.

## Setup

### Prerequisites

- Node.js
- npm

### Install dependencies

```bash
npm install
```

If the project does not define an `npm` start script, you can run it directly with Node.js:

```bash
node index.js
```

## Usage

Start the quiz from the project root:

```bash
node index.js
```

The quiz will:

- read questions from `data/questions.json`
- prompt for user input in the terminal
- evaluate answers
- display feedback and/or results in color

## Key Features

- Terminal-based quiz flow
- Question data stored in JSON
- Modular source structure
- Colored console output
- Separate input and quiz logic for easier maintenance

## Project Structure

```text
.
├── index.js
├── data/
│   └── questions.json
├── src/
│   ├── colors.js
│   ├── input.js
│   └── quiz.js
├── package.json
└── .gitignore
```

### File responsibilities

- `index.js` — application entry point
- `src/quiz.js` — quiz logic and orchestration
- `src/input.js` — terminal input handling
- `src/colors.js` — console color helpers
- `data/questions.json` — quiz questions and answers

## Customization

To change the quiz content, edit `data/questions.json`.

If you want to adjust terminal styling or output colors, check `src/colors.js`.

## Notes

This README is based on the repository structure and available filenames. If you want a more precise setup or usage guide, share the contents of `package.json` and the source files.