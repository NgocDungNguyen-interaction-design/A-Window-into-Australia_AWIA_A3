# A Window into Australia 

An interactive archive-exploration interface for the National Film and Sound Archive of Australia (NFSA). The interface retrieves collection records at runtime and provides search, browsing, item detail, loading/error/empty states, and a random discovery feature.

## Pages
- Home: dynamically loaded featured records
- Explore: search and filter collection results
- Search: query, year/medium filters, and load-more pagination
- Item detail: record information loaded by item ID
- Surprise Me: randomly selected collection record
- About: project purpose and attribution

## Run locally
1. Open the project folder in VS Code.
2. Copy `api-config.example.js` and rename the copy to `api-config.js`.
3. Add the API base URL supplied in your unit's private learning materials, if permitted.
4. Keep `api-config.js` local and do not commit it to a public repository.
5. Run the project using VS Code Live Server (recommended), rather than opening files directly.
6. Do not commit `api-config.js` to a public repository unless your lecturer has confirmed that this is permitted. The file is listed in `.gitignore`.

## API behaviour
The app uses the NFSA collection search endpoint for search/browse results and the title-by-ID endpoint for individual record details. Requests have a timeout and display loading, empty and error states. Search requests are limited to 12 records per page; load-more requests fetch the next page rather than loading a large collection at once. Metadata fields are rendered only when present.

## Attribution
This project was developed in the Faculty of Arts and Design at the University of Canberra, using data from the National Film and Sound Archive of Australia.

## Development notes
The project builds on the Assessment 1 HTML/CSS prototype. Dynamic record cards are generated from API responses, and missing fields are handled with fallback labels or explanatory text.

## GenAI use statement
Generative AI was used to assist with planning, code drafting, debugging, and refinement of the interface. The student is responsible for reviewing, testing, adapting, and understanding the final implementation.


## Image handling
The interface displays NFSA preview imagery when a usable image URL is present in the record. Where the API record has no preview, it uses a clearly labelled illustrative editorial photograph. Illustrative images are not original NFSA collection media and should not be described as such.
