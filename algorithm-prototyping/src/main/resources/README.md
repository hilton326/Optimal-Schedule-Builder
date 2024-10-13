# Resources

This directory contains the sample data to be used in our prototypes.

## Contents

- `courses.json`: JSON file containing sample course data. Includes all courses and sections listed in the [`Course Information`](https://docs.google.com/document/d/15_oJ8q1UvlBLBLKztub_5BtrNufYX5yk-8lavj_PnLw/edit?usp=sharing) Google Doc.
```json
{
  "courses": [
    {
      "course_code": "ENGL 1101",
      "sections": [
        {
          "CRN": 25013,
          "professor": "Daniel Barnum",
          "times": {
            "days": [
              "Monday",
              "Wednesday",
              "Friday"
            ],
            "start": "12:40",
            "end": "13:30"
          }
        },
        ...
      ]
    },
    ...
  ]
}
```

- `professors.json`: JSON file containing sample professor data. Includes all professors listed in `courses.json` and their corresponding RateMyProfessor quality ratings. If the professor has no RateMyProfessor rating, their quality is null.
```json
{
  "professors": [
    {
      "name": "Daniel Barnum",
      "quality": 5
    },
    ...
  ]
}
```

- `buildings.json`: JSON file containing sample building data. Includes all buildings listed in `courses.json` and their corresponding positions based on the map found in the [`Algorithm Prototyping`](https://drive.google.com/file/d/1J2_vlChwx_oWGYKRrmDkDBzWY6dORn6v/view?usp=drive_link) document.
```json
{
  "buildings": [
    {
      "name": "Park Hall",
      "x": 3,
      "y": 2
    },
    ...
  ]
}
```

- `scripts/generate_distance_matrix.py`: Python script that generates a JSON file called `distance_matrix.json` containing a distance matrix for the buildings in `buildings.json` using the Euclidean distance formula.


- `distance_matrix.json`: JSON file containing a precomputed distance matrix generated by `scripts/generate_distance_matrix.py`. The index of each building in the `buildings` array matches its index in the `distance_matrix` array.
```json
{
  "buildings": [
    "Park Hall",
    ...
  ],
  "distance_matrix": [
    [0, ...],
    ...
  ]
}
```