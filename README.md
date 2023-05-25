# Configuring PlexDownloader:

To configure PlexDownloader, follow these steps:

1. Edit the `user.ini` file with information relevant to your installation.

2. If you are downloading or syncing remotely, you must enter your MyPlex information and enable MyPlex.

3. Start by running the command: `python plexdl.py`.

To find your movie/music/tv/photo section ID, follow these instructions:

- Visit your Plex Web and navigate to the category you want to sync. For example: [http://192.168.3.5/web/index.html#!/server/.../section/2](http://192.168.3.5/web/index.html#!/server/.../section/2)
- The ID you need is the number at the end of the URL, such as `2`.
- Alternatively, you can find your content section ID by visiting [http://localhost:32400/library/sections/](http://localhost:32400/library/sections/).

## User.Ini Options

The `user.ini` file contains the following options:

**[general]**

- `sleeptime`: Time in seconds that you want to wait between checking for new content. The default is 600 seconds (10 minutes).
- `plexurl`: Enter your IP here, making sure there is no "/" at the end of the IP. For example: `http://127.0.0.1:32400`

**[webui]**

- `status`: Enable or disable the web manager for sync items.
- `port`: Port number for the web manager. The default is `8585`, but you can change it to any port you prefer.

**[myplex]**

- `status`: Enable or disable MyPlex. The default is `disable`.
- `username`: Your MyPlex email.
- `password`: Your MyPlex password.

**[tvshows]**

- `active`: Enable or disable the TV shows category.
- `plexid`: Your TV show section Plex ID.
- `tvfile`: List of TV shows you want to sync. Each TV show should be on a separate line, matching the name as it appears in Plex.
- `tvtype`: Specify the type of TV show syncing: `episode`, `recent`, or `all`. Selecting `recent` will download the most current season, while `all` will download every season.
- `tvlocation`: Download location for your synced TV shows. For example: `/Users/plexdl/Downloads/TV Shows/`.
- `fullsync`: Enable or disable full sync. When enabled, it will download everything it finds, following the `tvtype` setting.
- `autodelete`: Enable or disable automatic deletion of old episodes.
- `folderstructure`: Specify the folder structure for TV shows. Choose between `default` or `server`. The `server` option uses the Plex server naming convention, such as `/Season X/Show s1e1 - desc.mkv`.

**[movies]**

- `active`: Enable or disable the movies category.
- `plexid`: Your movie section Plex ID.
- `moviefile`: List of wanted movies you want to sync. Each movie should be on a separate line, formatted as `Movie (year)`. For example: `Avatar (2009)`.
- `movielocation`: Download location for your synced movies. For example: `/Users/plexdl/Downloads/Movies/`.
- `fullsync`: Enable or disable full sync. When enabled, it will download everything it finds.

**[music]**

- `active`: Enable or disable the music category.
- `plexid`: Your music section Plex ID.
- `musicfile`: List of wanted music. Include only artists, with one artist per line in the file.

- `musiclocation`: Download location for your synced music files. For example: `/Users/plexdl/Downloads/Music/`.

- `fullsync`: Enable or disable full sync. When enabled, it will download everything it finds.

**[pictures]**

- `active`: Enable or disable the pictures category.

- `plexid`: Your pictures section Plex ID.

- `picturefile`: List of wanted pictures. Include only albums, with one album per line in the file.

- `picturelocation`: Download location for your synced pictures. For example: `/Users/plexdl/Downloads/Pictures/`.

- `fullsync`: Enable or disable full sync. When enabled, it will download everything it finds.

**EXAMPLES:**

Here are some examples of how to format the text files for different categories:

**[tvshows.txt]**

```
Warehouse 13
Eureka
```

**[movies.txt]**

```
Avatar (2009)
```

**[music.txt]**

```
The Beatles
```

**[pictures.txt]**

```
Family Trip To France
```

Make sure to save the `user.ini` file with your desired configurations before running the PlexDownloader.
