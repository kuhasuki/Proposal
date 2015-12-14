# Phase 3: Albums and Playlists (2 days)

## Rails
### Models
* Notebook
* Tag
* Tagging

### Controllers
* Api::AlbumsController (create, destroy, index, show, update)
* Api::AlbumsController (create, destroy, index, show, update)

### Views
* albums/index.json.jbuilder
* albums/show.json.jbuilder
* playlists/index.json.jbuilder
* playlists/show.json.jbuilder

## Flux
### Views (React Components)
* AlbumsIndex
  - AlbumIndexItem
* AlbumForm
* PlaylistIndex
  - PlaylistIndexItem
* PlaylistForm
* SearchIndex

### Stores
* Album
* Playlist

### Actions
* ApiActions.receiveAllAlbums -> triggered by ApiUtil
* ApiActions.receiveSingleAlbum
* ApiActions.deleteAlbum
* AlbumActions.fetchAllAlbums -> triggers ApiUtil
* AlbumActions.fetchSingleAlbum
* AlbumActions.createAlbum
* AlbumActions.editAlbum
* AlbumActions.destroyAlbum
* ApiActions.receiveAllPlaylists -> triggered by ApiUtil
* ApiActions.receiveSinglePlaylist
* ApiActions.deletePlaylist
* PlaylistActions.fetchAllPlaylists -> triggers ApiUtil
* PlaylistActions.fetchSinglePlaylist
* PlaylistActions.createPlaylist
* PlaylistActions.editPlaylist
* PlaylistActions.destroyPlaylist

### ApiUtil
* ApiUtil.fetchAllAlbums
* ApiUtil.fetchSingleAlbum
* ApiUtil.createAlbum
* ApiUtil.editAlbum
* ApiUtil.destroyAlbum
* ApiUtil.fetchAllPlaylists
* ApiUtil.fetchSinglePlaylist
* ApiUtil.createPlaylist
* ApiUtil.editPlaylist
* ApiUtil.destroyPlaylist

## Gems/Libraries
