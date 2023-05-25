# Configuring PlexDownloader

To configure PlexDownloader, follow these steps:

1. Edit the `user.ini` file with the relevant information for your installation.

2. If you are downloading/syncing remotely, you need to enter your MyPlex information and enable MyPlex.

3. Start by running the command: `python plexdl.py`.

To find the ID of your movie/music/tv/photo section, follow these steps:

1. Visit your Plex Web by going to: [http://192.168.3.5/web/index.html#!/server/.../section/2](http://192.168.3.5/web/index.html#!/server/.../section/2).

2. The ID you need is the number at the end of the URL. In the above example, the ID is 2.

You can also find your content section ID by visiting: [http://localhost:32400/library/sections/](http://localhost:32400/library/sections/).

## User.Ini Options

The `user.ini` file contains the following options:

### [general]

- `sleeptime`: This option specifies the time in seconds that you want to wait between checking for new content. The default value is 600 seconds (10 minutes).

- `plexurl`: Enter your IP address here, making sure not to include a "/" at the end of the IP. For example: `http://127.0.0.1:32400`.

### [webui]

- `status`: This option enables or disables the web manager for syncing items.

- `port`: This option sets the port number for the web manager. The default port is 8585, but you can change it to any desired port.

### [myplex]

- `status`: This option enables or disables MyPlex. The default is disabled.

- `username`: Enter your MyPlex email address here.

- `password`: Enter your MyPlex password here.

### [tvshows]

- `active`: This option activates or deactivates the TV shows category for scanning.

- `plexid`: Enter the Plex ID for your TV show section.

- `tvfile`: Specify the file name containing the list of TV shows you want to sync. Each TV show should be listed on a separate line, exactly as it appears in Plex.

- `tvtype`: Choose between `episode`, `recent`, or `all`. `recent` will download the most current season, while `all` will download every season.

- `tvlocation`: Set the download location for your synced TV shows. For example: `/Users/plexdl/Downloads/TV Shows/` or `C:/Downloads/TV Shows/`.

- `fullsync`: Enable or disable full sync. When enabled, it will download everything it finds, following the `tvtype` setting.

- `autodelete`: Enable or disable automatic deletion of old episodes.

- `folderstructure`: Choose between `default` or `server`. `server` uses the Plex server naming convention, such as `/Season X/Show s1e1 - desc.mkv`.

### [movies]

- `active`: This option activates or deactivates the movies category for scanning.

- `plexid`: Enter the Plex ID for your movie section.

- `moviefile`: Specify the file name containing the list of movies you want to sync. Each movie should be listed on a separate line in the format: `Movie (year)`, for example: `Avatar (2009)`.

- `movielocation`: Set the download location for your synced movies. For example: `/Users/plexdl/Downloads/Movies/` or `C:/Downloads/Movies/`.

- `fullsync`: Enableor disable full sync. When enabled, it will download everything it finds.

### [music]

- `active`: This option activates or deactivates the music category for scanning.

- `plexid`: Enter the Plex ID for your music section.

- `musicfile`: Specify the file name containing the list of music you want to sync. Include only artists, with one artist per line.

- `musiclocation`: Set the download location for your synced music. For example: `/Users/plexdl/Downloads/Music/`.

- `fullsync`: Enable or disable full sync. When enabled, it will download everything it finds.

### [pictures]

- `active`: This option activates or deactivates the pictures category for scanning.

- `plexid`: Enter the Plex ID for your pictures section.

- `picturefile`: Specify the file name containing the list of pictures you want to sync. Include only albums, with one album per line.

- `picturelocation`: Set the download location for your synced pictures. For example: `/Users/plexdl/Downloads/Pictures/`.

- `fullsync`: Enable or disable full sync. When enabled, it will download everything it finds.

## EXAMPLES:

[tvshows.txt]

```
Warehouse 13
Eureka
```

[movies.txt]

```
Avatar (2009)
```

[music.txt]

```
The Beatles
```

[pictures.txt]

```
Family Trip To France
```
