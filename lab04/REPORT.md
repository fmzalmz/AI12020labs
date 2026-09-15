# Lab 04 report

Student name: Fatima Al Mazrouei

Date: 15 September 2026

Repository: AI12020labs

Status: Complete.

## Exercise 1 - Explore and make a commit

- Working folder: `~/new/lab04`
- Git repository root: `~/new`
- Initial report commit hash (`Start lab04 report`): `b11206b`
- Files included in that commit: `lab04/REPORT.md` only.
- What was saved in that commit: My name, date, repository name, and the initial in-progress report.
- Which file owns the playlist, and why: `backend.py` owns the playlist because it stores the server-side `songs` list and assigns IDs.
- Which file displays the playlist, and why: `index.html` displays the playlist because its JavaScript creates the visible song list in the browser.
- How the initial song gets from the server to the page: The page calls `loadSongs()`, which sends `GET /songs`; the server returns the seed song as JSON and JavaScript adds it to the page.
- Codex access issues and instructor-supported alternatives, if any: No access issue. I used the supplied starter files and checked the application locally.

## Exercise 2 - Backend

- Explain your completed `create_song(payload)` function: It validates both fields before changing any global data, trims valid values, creates a song using `next_id`, appends it to `songs`, advances the ID, and returns the stored song.
- Explain how both fields are validated and stored: The function checks that title and artist exist and are strings, trims surrounding whitespace, and requires each trimmed value to contain 1 to 80 characters. Only the trimmed values are stored.
- Explain how rejected input leaves the playlist and next ID unchanged: Every validation check occurs before `songs.append()` and before `next_id` is increased, so a raised `ValueError` cannot change either value.
- Accepted direct request checked before Exercise 3, and observation: A POST containing spaces around Quiet Road and Sample Artist returned 201, stored the trimmed values, and assigned ID 2.
- Rejected direct request checked before Exercise 3, and observation: A whitespace-only title returned 400 with a helpful length error. The following GET contained only IDs 1 and 2, confirming that the rejection changed nothing.

## Exercise 3 - Frontend

- Visible heading after your edit: `My playlist`.
- Explain your completed `sendSong(title, artist)` function: It returns `requestJSON()` with the `/songs` path and an options object containing the POST method, JSON content header, and serialized title and artist.
- Explain how the request method, path, headers, and body match the contract: It sends POST to `/songs`, uses `Content-Type: application/json`, and converts `{title, artist}` into a JSON request body.
- Observed behavior after an accepted form submission: Blue Sky / Test Duo appeared exactly once, both input fields cleared, and the page displayed `Song added.`
- Observed behavior after a rejected form submission: A whitespace-only title displayed the validation error, retained the inputs, and left the three-song list unchanged.
- How you checked that the display matches what the server stores: I refreshed the page and compared the displayed list with the JSON returned by `GET /songs`.

## Exercise 4 - Actual verification observations

Fill in the actual result and pass/fail only after running each check.

| Check from page 3 | Actual observation | Pass/fail |
| --- | --- | --- |
| Fresh start: page and GET show only First Light / Demo Band, ID 1 | After restarting, the page showed only First Light / Demo Band and GET returned ID 1. | Pass |
| Form: Blue Sky / Test Duo appears once; fields clear | The song appeared once, the fields cleared, and `Song added.` appeared. | Pass |
| Refresh: both songs remain | First Light and Blue Sky remained after refreshing. | Pass |
| Form: another invented song with different values works | Find Your Love / Drake was added successfully. | Pass |
| Direct addition: 201, trimmed values, next unused ID; visible after refresh | Quiet Road / Sample Artist returned 201 with trimmed values and ID 5 and appeared in the server list. | Pass |
| Whitespace-only title: 400; no new song | Returned 400 with `Title must contain between 1 and 80 characters.` and added nothing. | Pass |
| Missing artist: 400 | Returned 400 with `Artist is required.` | Pass |
| Numeric title: 400 | Returned 400 with `Title must be a string.` | Pass |
| 81-character title: 400 | Returned 400 with the title-length error. | Pass |
| 80-character title: accepted | Returned 201 and stored the 80-character title as ID 6. | Pass |
| Rejected additions do not consume an ID | Quiet Road received ID 5 and the later valid 80-character title received ID 6 after all rejected requests. | Pass |
| Form rejection: visible error, retained inputs, unchanged list | The red error appeared, Test Artist remained entered, and the list stayed unchanged. | Pass |
| Corrected form submission succeeds | Test Song / Test Artist was accepted and the fields cleared. | Pass |
| Keyboard: Tab and Enter work | Tab moved through the form controls and Enter submitted the corrected song. | Pass |
| Network: POST payload, 201 status, JSON response, following GET | Safari showed POST `/songs`, status 201, the JSON response for Network Song / Browser Test, and a following GET `/songs`. | Pass |
| Restart and refresh: only the seed song remains | After stopping and restarting Python, refresh showed only First Light / Demo Band. | Pass |

### One successful request and response

Request method and path: `POST /songs`

Request headers: `Content-Type: application/json`

Actual request body:

```json
{"title":"  Quiet Road  ","artist":"Sample Artist"}
```

Actual response status and headers: `201 Created`; `Content-Type: application/json`; `Cache-Control: no-store`.

Actual response body:

```json
{"id":5,"title":"Quiet Road","artist":"Sample Artist"}
```

What the following GET and page showed: The server list contained Quiet Road with trimmed values and ID 5, and it appeared on the page after the list refreshed.

### One failed request and response

Request method and path: `POST /songs`

Request headers: `Content-Type: application/json`

Actual request body:

```json
{"title":"   ","artist":"Sample Artist"}
```

Actual response status and headers: `400 Bad Request`; `Content-Type: application/json`; `Cache-Control: no-store`.

Actual response body:

```json
{"error":"Title must contain between 1 and 80 characters."}
```

Evidence that the playlist and next ID were unchanged: The rejected request added no song, and the next accepted song received the next consecutive ID.

### One code change I reviewed

File and change: `backend.py` — completed `create_song(payload)`.

My explanation of the change: The function validates both values before changing state, trims them, stores a new song using the next server ID, and advances that ID only after acceptance.

Observed result and why it agrees with the contract: Valid JSON returned 201 with trimmed stored values, while invalid values returned 400 without changing the playlist or consuming an ID.

## Submission

- Final commit hash (`Complete lab04 playlist`): `895364d`
- Files included and review notes: `REPORT.md`, `backend.py`, `index.html`, `README.md`, and `.gitignore`; syntax, whitespace, backend validation, frontend submission, and browser behavior reviewed.
- Push and GitHub verification: Pushed the Lab 4 commits to `course/main`; verified by the successful push output and the `lab04` folder on GitHub.
- Optional stretch, if attempted: Not attempted.
