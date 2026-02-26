# Distribusion Connections/Find Prototype

Interactive prototype for the `/connections/find` API endpoint with advanced filtering and trip matching.

## Features

- **Filter Mode**: Traditional filtering with hard constraints
- **Match Mode**: Trip specification mode with intelligent ranking
- **Configurable Matching**: Drag-to-reorder priorities, adjustable buffers
- **Vehicle Similarity**: Smart matching with Levenshtein distance (80% threshold)

## How to Use

1. Open `prototype/index.html` in your browser
2. Fill in search criteria (departure/arrival locations and times)
3. Add filters (vehicle numbers, operating carriers, travel/fare classes)
4. Select search mode:
   - **none**: Traditional filtering (returns all matches)
   - **match**: Trip specification (returns ranked best match)
5. Adjust config priorities and buffers via the Config page
6. Click Search to see results

## Test Data

Test responses are provided in `cf_responses/`:
- `cf_response01.json` - Sample Berlin→Munich connections
- `cf_response02.json` - Alternative test data
- `cf_response_combined_test.json` - 8 connections for testing match mode scoring

## Running Locally

```bash
cd prototype
python3 -m http.server 8899
```

Then open `http://localhost:8899/`
