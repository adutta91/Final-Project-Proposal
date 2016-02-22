
# SoundCloud Clone

Heroku link


## Minimum Viable Product

Description: A music sharing and exploration web browser
app built using Ruby and React.js.

Features:
- [ ] Create and manage account
- [ ] Log In / Log out
- [ ] Listen to and explore songs that are in the database
- [ ] Comment on songs
- [ ] Favorite/like songs, which are remembered in their account
- [ ] Upload their own songs



## Design Docs
* [Wireframes][wireframes]
* [Database Schema][schema]
* [Component Hierarchy][components]
* [Flux Stores][stores]
* [API endpoints][endpoints]


[wireframes]: ./docs/Wireframes.md
[schema]: ./docs/schema.md
[components]: ./docs/components.md
[stores]: ./docs/stores.md
[endpoints]: ./docs/endpoints.md


## Implementation Timeline

### Phase 1: Backend setup and User Authentication (0.5 days)

**Objective:** Functioning rails project with Authentication

- [ ] create new project
- [ ] create `User` model
- [ ] authentication
- [ ] user signup/signin pages
- [ ] blank landing page after signin

### Phase 2: Notes Model, API, and basic APIUtil (1.5 days)

**Objective:** Songs can be uploaded, displayed, and destroyed through
the API.

- [ ] create `Song` model
- [ ] seed the database with a small amount of test data
- [ ] CRUD API for songs (`SongsController`)
- [ ] jBuilder views for songs
- [ ] setup Webpack & Flux scaffold
- [ ] setup `APIUtil` to interact with the API
- [ ] test out API interaction in the console.

### Phase 3: Flux Architecture and Router (1.5 days)

**Objective:** Songs can be created, displayed, and destroyed with the
user interface.

- [ ] setup the flux loop with skeleton files
- [ ] setup React Router
- implement each song component, building out the flux loop as needed.
  - [ ] `NotesIndex`
  - [ ] `NoteIndexItem`
  - [ ] `NoteForm`
- [ ] save Notes to the DB when the form loses focus or is left idle
  after editing.

### Phase 4: Start Styling (0.5 days)

**Objective:** Existing pages (including singup/signin) will look good.

- [ ] create a basic style guide
- [ ] position elements on the page
- [ ] add basic colors & styles

### Phase 5: Notebooks (1 day)

**Objective:** Notes belong to Notebooks, and can be viewed by notebook.

- [ ] create `Notebook` model
- build out API, Flux loop, and components for:
  - [ ] Notebook CRUD
  - [ ] adding notes requires a notebook
  - [ ] moving notes to a different notebook
  - [ ] viewing notes by notebook
- Use CSS to style new views

Phase 3 adds organization to the Notes. Notes belong to a Notebook,
which has its own `Index` view.

### Phase 6: Tags (1.5 days)

**Objective:** Notes can be tagged with multiple tags, and tags are searchable.

- [ ] create `Tag` model and join table
- build out API, Flux loop, and components for:
  - [ ] fetching tags for notebook
  - [ ] adding tags to notebook
  - [ ] creating tags while adding to notebooks
  - [ ] searching notebooks by tag
- [ ] Style new elements

### Phase 7: Allow Complex Styling in Notes (0.5 days)

**objective:** Enable complex styling of notes.

- [ ] Integrate `react-quill` (based on Quill.js).
- [ ] Use Rails helpers to sanitize HTML before rendering.
- [ ] Style the new Quill elements.

### Phase 8: Styling Cleanup and Seeding (1 day)

**objective:** Make the site feel more cohesive and awesome.

- [ ] Get feedback on my UI from others
- [ ] Refactor HTML classes & CSS rules
- [ ] Add modals, transitions, and other styling flourishes.


### Bonus features (maybe)
- [ ] Create a queue of songs
- [ ] Songs continue to play as they navigate the site
- [ ] Follow artists
- [ ] Recommended songs based on interests (by genre)
