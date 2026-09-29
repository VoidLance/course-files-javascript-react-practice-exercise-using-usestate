# React `useState` Practice Exercise

This repository contains a small React and TypeScript practice project powered by
[Bun](https://bun.com/). The app demonstrates React state with a production-bot
dashboard: users can run jobs, see the run counter update, and review a list of
bot statuses.

## Why this project is useful

- Provides a focused example of `useState` in a React component.
- Shows a minimal React 19 application with Bun's development server and bundler.
- Includes a small API route and an API tester component for experimenting with
  GET and PUT requests.
- Keeps the codebase small enough to modify while learning React fundamentals.

## Requirements

- [Bun](https://bun.com/docs/installation) 1.3 or newer
- A modern browser

## Getting started

The application lives in the `Test Website` directory:

```bash
cd "Test Website"
bun install
bun dev
```

Open the local URL printed by Bun in your browser. The development server
enables hot module reloading, so changes to files in `src/` appear without
manually restarting the server.

### Production build

Create an optimized browser build and run the application in production mode:

```bash
cd "Test Website"
bun run build
bun start
```

## Using the app

Click **Run Job** to increment the production job counter. The dashboard also
lists each sample bot and its current status.

The repository also includes these example route handlers in
`Test Website/src/frontend.tsx`:

| Method | Endpoint | Response |
| --- | --- | --- |
| `GET` | `/api/hello` | A JSON greeting and method |
| `PUT` | `/api/hello` | A JSON greeting and method |
| `GET` | `/api/hello/:name` | A personalized JSON greeting |

To run that Bun server directly:

```bash
bun src/frontend.tsx
```

Then, in another terminal, try:

```bash
curl http://localhost:3000/api/hello/Ada
```

## Project structure

```text
Test Website/
├── src/
│   ├── App.tsx          # Main application component
│   ├── CreateJob.tsx    # useState job counter and bot list
│   ├── APITester.tsx    # API request testing UI
│   ├── frontend.tsx     # Bun server and API routes
│   └── index.ts         # React entry point
├── package.json         # Scripts and dependencies
└── bunfig.toml          # Bun configuration
```

## Getting help

For project-specific questions or bug reports, [open an issue](https://github.com/VoidLance/course-files-javascript-react-practice-exercise-using-usestate/issues).
The following documentation is useful when working on the project:

- [React documentation](https://react.dev/learn)
- [React `useState` reference](https://react.dev/reference/react/useState)
- [Bun documentation](https://bun.com/docs)

## Contributing

Contributions are welcome. To propose a change:

1. Fork the repository and create a focused feature or fix branch.
2. Make the change in `Test Website/`.
3. Run the relevant commands locally, including `bun run build`.
4. Open a pull request describing the change and how it was tested.

Please keep examples beginner-friendly and limit each pull request to a
focused improvement. The project is maintained by [VoidLance](https://github.com/VoidLance)
with help from contributors.
