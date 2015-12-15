# .io compoze/ songspace/ soundspace/ audioshare/ beatlab/ audio.space .space .audio .xyz .io .live .studio

[Heroku link][heroku] **NB:** This should be a link to your production site

[heroku]: http://www.herokuapp.com

## Minimum Viable Product

TBD is a web application inspired by Soundcloud built using Ruby on Rails
and React.js. TBD allows users to:

<!-- This is a Markdown checklist. Use it to keep track of your progress! -->

- [ ] Create an account
- [ ] Log in / Log out
- [ ] Upload, update, play, and delete tracks
- [ ] Render a waveform representation of each track
- [ ] Any track can be added to a playlist

## Reach Goals

- [ ] Allow users to leave timestamped comments for a track which are shown in sync when the song is played by others
- [ ] Allow browsing through the site while maintaining song playback
- [ ] Tracks can organized into albums by their creator
- [ ] Search for tracks by artist, song title, album, popularity(play count)

## Design Docs
* [View Wireframes][view]
* [DB schema][schema]

[view]: ./docs/views.md
[schema]: ./docs/schema.md

## Implementation Timeline

### Phase 1: User Authentication, Track Model and JSON API (1.5 days)

In Phase 1, I will begin by implementing user signup and authentication (using
BCrypt). There will be a basic landing page after signup that will contain the
container for the application's root React component. Before building out the
front end, I will begin by setting up a full JSON API for Tracks.

[Details][phase-one]

### Phase 2: Flux Architecture and Track CRUD (2.5 days)

Phase 2 is focused on setting up Flux, the React Router, and the React view
structure for the main application. After the basic Flux architecture has been
set up, a Track store will be implemented and a set of actions corresponding to
the needed CRUD functionality created. Once this is done, I will create React
views for the Tracks `Index`, `IndexItem` and `Form`. At the end of Phase 2,
Tracks can be created, read, edited and destroyed in the browser. Urls to tracks should
save to the database when the artist uploads a file. This file will has to be uploaded to a cdn and the resulting link saved.
I think using AWS to host these files will be the key to completing this phase.

[Details][phase-two]

### Phase 3: Playlists and Search (2 days)

Phase 3 adds organization to the Tracks. Tracks optionally belong to an Album, which has
its own `Index` view. Create JSON API for Albums. Tracks can also now be
aggregated into playlists by users of the site. Users can search for tracks in a separate `SearchIndex`
view by searching for their title, name. Once the tag search is implemented, I will
extend this to a fuzzy search through every Note's content.

[Details][phase-three]

### Phase 4: Rendering Waveforms and comments (1 day)

Using the wave-surfer library (http://wavesurfer-js.org/), render mp3 file waveform. Create comments model and api. Allow comments to be timestamped to a discrete point in the waveform of a track. Comments should appear in their timestamped order when a track is played back.

[Details][phase-four]

### Phase 5: Persistent Audio Player (1 day)

In this phase I will ensure that the audio playback can not only occur when viewing a track's show page, but also can also persistently play in the single page app that is TBD.

[Details][phase-five]

### Phase 6: Styling Cleanup and Follows (1 day)

I will try to make sure that everything looks nice and make sure that users can follow each other.

[phase-one]: ./docs/phases/phase1.md
[phase-two]: ./docs/phases/phase2.md
[phase-three]: ./docs/phases/phase3.md
[phase-four]: ./docs/phases/phase4.md
[phase-five]: ./docs/phases/phase5.md
