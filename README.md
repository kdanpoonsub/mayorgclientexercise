# mayorgclientexercise
Client Coding Exercise for the May Organization. We don't want this to take you more than an hour. 
The goal of the exercise is to gauge your personal coding style and problem solving abilities.
Do your best to write clean, maintanable code.

As a developer of our application, you will be asked to design and maintain common ui components in our next.js application.
With that in mind, imagine you have been tasked with creating a common grid component that can be used by anyone on the team. 
At a minimum, the common component must display grid data that can be formatted in one of three ways depending on the age of the api. 
Add additional functionality as you see fit.

As an array of arrays where the first array entry is the headers and subsequent entries are detail rows:

[
  ['KPI Name', 'KPI Id', ... 'Col N Value'],
  ['WalkIn Conversion Rate', '123143', ... '45.6%'],
  .
  .
  .
  ['Gross Add Count', '124123', '65']
]

As an array pipe delimited columns where the first array entry is the headers and subsequent entries are detail rows:

[
  'KPI Name|KPI Id|...|Col N Value',
  'WalkIn Conversion Rate|123123|...|45.6%'
  .
  .
  .
  'Gross Add Count|124123|65'
]

As an array of objects where each object represents one cell in the grid. Row 0 are the headers and rows greater than 0 are the detail rows.

[
  { col: 0, row: 0, value: 'KPI Name' },
  { col: 1, row: 0, value: 'KPI ID' },
  .
  .
  .
  { col: n, row: 0, value: 'Row 0 Col N Value' }
  .
  .
  .
  { col: 0, row: n, value: 'Col 0 Row N Value' }
  .
  .
  .
  { col: n, row: m, value: 'Col n Row M Value' } 
]

The datasets are in the project under the /data folder. All of the data is the same with only the structures changing.
arrayofarray.json contains the data as an array of arrays.
arrayofdelimited.json contains the data as an array of pipe delimited fields.
arrayofobjects.json contains the data as an array of objects for each cell. 
