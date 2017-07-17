[![](https://scdn.rapidapi.com/RapidAPI_banner.png)](https://rapidapi.com/package/Deezer/functions?utm_source=RapidAPIGitHub_DeezerFunctions&utm_medium=button&utm_content=RapidAPI_GitHub)

# Deezer Package
Deezer Simple API provides a nice set of services to build up web applications allowing the discovery of Deezer's music catalogue.
* Domain: deezer.com
* Credentials: appId, appSecret, code, accessToken

## How to get credentials: 
1. Sign in [deezer.com](http://www.deezer.com).
2. Register new [application](https://connect.deezer.com/oauth/auth.php)
3. Receive code on this endpoint:
```
https://dribbble.com/oauth/authorize
```
Parameters:
```
app_id - The id of your application, generated when you created your application on developer page..
redirect_uri - The URL the user will be redirected after authentication. redirect_uri must be in the same domain as the domain you defined when you created the application.
perms - The permissions your application will ask to the user.
```
4. Call ```getAccessToken``` block.

## Custom datatypes:
 |Datatype|Description|Example
 |--------|-----------|----------
 |Datepicker|String which includes date and time|```2016-05-28 00:00:00```
 |Map|String which includes latitude and longitude coma separated|```50.37, 26.56```
 |List|Simple array|```["123", "sample"]```
 |Select|String with predefined values|```sample```
 |Array|Array of objects|```[{"Second name":"123","Age":"12","Photo":"sdf","Draft":"sdfsdf"},{"name":"adi","Second name":"bla","Age":"4","Photo":"asfserwe","Draft":"sdfsdf"}] ```

## Deezer.getAccessToken
Returns access token.

| Field    | Type       | Description
|----------|------------|----------
| appId    | credentials| The id of your application, generated when you created your application on developer page.
| appSecret| credentials| The app secret is available from the Application setting page and should not be shared with anyone or embedded in any code that you will distribute (you should use the client-side flow for these scenarios).
| code     | credentials| The code you received at the previous step.
| output   | Select     | The way you want to output the access_token. If not specifed, this will output the access_token as a string to parse (like in the example below)

## Deezer.getAlbumComments
Return a list of album's comments. Represented by an array of Comment objects.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| albumId    | String     | The Deezer album id.

## Deezer.getAlbumFans
Return a list of album's fans. Represented by an array of User objects.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| albumId    | String     | The Deezer album id.

## Deezer.getAlbumTracks
Return a list of album's tracks. Represented by an array of Track objects.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| albumId    | String     | The Deezer album id.

## Deezer.getArtistTop5Tracks
Get the top 5 tracks of an artist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | The artist's Deezer id.

## Deezer.getArtistAlbums
Return a list of artist's albums. Represented by an array of Album objects.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | The artist's Deezer id.

## Deezer.getArtistComments
Return a list of artist's comments. Represented by an array of Comment objects.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | The artist's Deezer id.

## Deezer.getArtistFans
Return a list of artist's fans. Represented by an array of User objects.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | The artist's Deezer id.

## Deezer.getRelatedArtists
Return a list of related artists. Represented by an array of Artist objects

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | The artist's Deezer id.

## Deezer.getTracks
Return a list of tracks. Represented by an array of Track object.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | The artist's Deezer id.

## Deezer.getArtistPlaylists
Return a list of artist's playlists. Represented by an array of Playlist object.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | The artist's Deezer id.

## Deezer.getTopTracks
Returns the Top tracks.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getTopAlbums
Returns the Top albums.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getTopArtists
Returns the Top artists.

No arguments.

## Deezer.getTopPlaylists
Returns the Top playlists.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getEditorsChoiceAlbums
Return a list of albums selected every week by the Deezer Team.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getEditorsChoice
This method returns four lists : Top track, Top album, Top artist and Top playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getCountryNewReleases
This method returns the new releases per genre for the current country.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getArtistsForGenre
Returns all artists for a genre.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getRadiosForGenre
Returns all radios for a genre

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getUserOptions
Get the user's options.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getPlaylistComments
Return a list of playlist's comments. Represented by an array of Comment objects

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | The playlist's Deezer id.

## Deezer.getPlaylistFans
Return a list of playlist's fans. Represented by an array of User objects.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | The playlist's Deezer id.

## Deezer.getPlaylistTracks
Return a list of playlist's tracks. Represented by an array of Track object.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | The playlist's Deezer id.

## Deezer.getRadioByGenre
Returns a list of radio splitted by genre.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getTop5Radios
Return the top radios (5 radios)

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getRadioFirst40Tracks
Get first 40 tracks in the radio

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getPersonalRadioByGenre
Returns a list of personal radio splitted by genre (as MIX in website)

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.searchAlbums
Search albums.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| searchQuery| String     | Search string.

## Deezer.searchArtists
Search artists.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| searchQuery| String     | Search string.

## Deezer.getUserSearchHistory
Get user search history.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| searchQuery| String     | Search string.

## Deezer.searchPlaylists
Search playlists.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| searchQuery| String     | Search string.

## Deezer.searchRadio
Search radio.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| searchQuery| String     | Search string.

## Deezer.searchTracks
Search tracks.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| searchQuery| String     | Search string.

## Deezer.searchUsers
Search users.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| searchQuery| String     | Search string.

## Deezer.getUserFavoriteAlbums
Return a list of user's favorite albums. Represented by an array of Album object

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getUserFavoriteArtists
Return a list of user's favorite artists. Represented by an array of Artist object

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.

## Deezer.getUserFlowTracks
Returns a list of user's flow tracks, represented by an array of Track object.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserFolder
Return a list of user's Folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserFollowing
Return a list of user's following, represented by an array of User object

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserFollowers
Return a list of user's followers, represented by an array of User object

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserRecentlyPlayedTracks
Returns a list of the recently played tracks.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.addNotificationsInUserFeed
Use this method in post only, to add notifications in user feed.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserPermissions
Return the user's Permissions granted to the application.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserPersonnalSongs
Return a list of user's personnal song, represented by an array of Tracks.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserPlaylist
Return a list of user's public Playlist, represented by an array of Playlist object. Permission is needed to return private playlists.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserRadios
Return a list of user's favorite Radios, represented by an array of Radio object.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getUserFavoriteTracks
Return a list of user's favorite tracks. Represented by an array of Track object.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getAlbumsRecommendations
Return a list of user's recommendations albums.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getArtistsRecommendations
Return a list of user's recommendations artists.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getPlaylistsRecommendations
Return a list of user's recommendations playlists.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getTracksRecommendations
Return a list of user's recommendations tracks.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.getRadiosRecommendations
Return a list of user's recommendations radios.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.

## Deezer.addCommentToAlbum
Add a comment to the album.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| albumId    | String     | User id.
| comment    | String     | The content of the comment.

## Deezer.addCommentToArtist
Add a comment to the artist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| artistId   | String     | Artist id.
| comment    | String     | The content of the comment.

## Deezer.setBookmarkOnEpisode
Sets a bookmark on the episode.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| episodeId  | String     | Artist id.
| offset     | Number     | The offset where the bookmark is set, must be between 0 and 100.

## Deezer.renameFolder
Rename the folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| folderId   | String     | Folder id.
| title      | String     | The new title of the folder.

## Deezer.addPlaylistToFolder
Add a playlist to the folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| folderId   | String     | Folder id.
| playlistId | String     | The playlist id.

## Deezer.addAlbumToFolder
Add an album to the folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| folderId   | String     | Folder id.
| albumId    | String     | The album id.

## Deezer.ratePlaylist
Rate the playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | Playlist id.
| note       | String     | An int [1-5].

## Deezer.updatePlaylist
Update the playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | Playlist id.

## Deezer.markPlaylistAsSeen
Mark the playlist as seen.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | Playlist id.

## Deezer.addCommentToPlaylist
Add a comment to the playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | Playlist id.
| comment    | String     | The content of the comment.

## Deezer.addTrackToPlaylist
Add a track to the playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | Playlist id.
| songs      | String     | A comma separated list of track ids.

## Deezer.orderTracksInPlaylist
Order tracks in the playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | Playlist id.
| order      | String     | A comma separated list of track ids.

## Deezer.updatePersonalTrack
Update a personal track.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| trackId    | String     | Track id.

## Deezer.addAlbumToUserLibrary
Add an album to the user's library.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| albumId    | String     | The id of the album.

## Deezer.addArtistToUserFavorites
Add an artist to the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| artistId   | String     | The id of the artist.

## Deezer.createFolder
Create a folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| title      | String     | The title of the folder.

## Deezer.followUser
Follow user.

| Field        | Type       | Description
|--------------|------------|----------
| accessToken  | credentials| Your access token.
| userId       | String     | User id.
| followingUser| String     | The user id to follow.

## Deezer.createPlaylist
Create a playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| title      | String     | The title of the new playlist.

## Deezer.addPlaylistToUserFavorites
Add a playlist to the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| playlistId | String     | The playlist id.

## Deezer.addPodcastToUserFavorites
Add a podcast to the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| podcastId  | String     | The podcast id.

## Deezer.addRadioToUserFavorites
Add a radio to the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| radioId    | String     | The radio id.

## Deezer.addTrackToUserFavorites
Add a track to the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | User id.
| trackId    | String     | The id of the track.

## Deezer.removeComment
Remove a comment.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| commentId  | String     | Comment id.

## Deezer.removeBookmarkOnEpisode
Removes the bookmark on the episode.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| episodeId  | String     | Episode id.

## Deezer.deleteFolder
Delete the folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| folderId   | String     | Folder id.

## Deezer.removePlaylistFromFolder
Remove a playlist from the folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| folderId   | String     | Folder id.
| playlistId | String     | The playlist id.

## Deezer.removeAlbumFromFolder
Remove an album from the folder.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| folderId   | String     | Folder id.
| albumId    | String     | The album id.

## Deezer.deletePlaylist
Delete the playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | The playlist id.

## Deezer.removeTracksFromPlaylist
Delete the playlist.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| playlistId | String     | The playlist id.
| songs      | String     | A comma separated list of track ids.

## Deezer.deletePersonalTrack
Delete a personal track.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| trackId    | String     | The track id.

## Deezer.removeAlbumFromUserLibrary
Remove an album from the user's library.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | The user id.
| albumId    | String     | The album id.

## Deezer.removeArtistFromUserFavorites
Remove an artist from the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | The user id.
| artistId   | String     | The artist id.

## Deezer.unfollowUser
Unfollow user.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | The user id.
| user       | String     | The user id.

## Deezer.removePlaylistFromUserFavorites
Remove a playlist from the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | The user id.
| playlistId | String     | The playlist id.

## Deezer.removePodcastFromUserFavorites
Remove a podcast from the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | The user id.
| podcastId  | String     | The podcast id.

## Deezer.removeRadioFromUserFavorites
Remove a radio from the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | The user id.
| radioId    | String     | The podcast id.

## Deezer.removeTrackFromUserFavorites
Remove a track from the user's favorites.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your access token.
| userId     | String     | The user id.
| trackId    | String     | The podcast id.

