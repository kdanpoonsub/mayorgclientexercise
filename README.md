# mayorgclientexercise

Client Coding Exercise for the May Organization. We don't want this to take you more than an hour.
The goal of the exercise is to gauge your personal coding style and problem-solving abilities.
Do your best to write clean, maintainable code.

**Instructions:**

As a developer of our application, you will be asked to design and maintain common UI components in our Next.js application.
With that in mind, imagine you have been tasked with creating a common grid component that can be used by anyone on the team.
At a minimum, the common component must display grid data that can be formatted in one of three ways to support both legacy and current API responses (i.e., different data formats may be returned depending on the version or age of the API).
If you wish, you may add additional functionality, improvements, or creative touches, but this is entirely optional.

- There is no single correct answer. Solutions can be creative or simple, as long as they meet the requirements.
- You may use any framework or library you prefer. If you want to use Next.js, see the bootstrapping instructions below.
- You may add features, improve usability, or keep it minimal and focused.
- Please include comments or documentation about any non-obvious design decisions.
- The goal is to demonstrate your approach to problem-solving, code quality, and communication.

**Advanced (Optional) Challenges:**

## Next.js Bootstrapping Instructions

If you would like to use Next.js for your solution, you can quickly bootstrap a new project with:

```sh
npx create-next-app@latest mayorg-grid-challenge
cd mayorg-grid-challenge
```

Then copy the provided data files from the root of this repository into your new project and begin your implementation.

## Data Formats

### 1. Array of Arrays

The first array entry is the headers and subsequent entries are detail rows:

```js
[
  ["KPI Name", "KPI Id", "...", "Col N Value"],
  ["WalkIn Conversion Rate", "123143", "...", "45.6%"],
  // ... more rows ...
  ["Gross Add Count", "124123", "65"],
];
```

### 2. Array of Pipe-Delimited Strings

The first array entry is the headers and subsequent entries are detail rows:

```js
[
  "KPI Name|KPI Id|...|Col N Value",
  "WalkIn Conversion Rate|123123|...|45.6%",
  // ... more rows ...
  "Gross Add Count|124123|65",
];
```

### 3. Array of Objects (Cell-Based)

Each object represents one cell in the grid. Row 0 is the headers; rows greater than 0 are detail rows.

```js
[
  { col: 0, row: 0, value: "KPI Name" },
  { col: 1, row: 0, value: "KPI ID" },
  // ... more header cells ...
  { col: n, row: 0, value: "Row 0 Col N Value" },
  // ... more data cells ...
  { col: 0, row: n, value: "Col 0 Row N Value" },
  // ...
  { col: n, row: m, value: "Col n Row M Value" },
];
```

## Data

The datasets are in the root of this repository. All of the data is the same; only the structures differ:

- `arrayofarray.json`: Data as an array of arrays.
- `arrayofdelimited.json`: Data as an array of pipe-delimited fields.
- `arrayofobjects.json`: Data as an array of objects for each cell.
