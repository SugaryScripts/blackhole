For those aiming to download videos from MS Teams meetings in which you participated but were not the Organizer, I managed to do so using yt-dlp and ffmpeg. The procedure is quite similar for both tools.
- Open your Browser (I got it to work in Chrome, Edge and Firefox)
- Login to [portal.office.com](http://portal.office.com/)
- Go to where you can play the video you want to download, either via Sharepoint or Streams.
- Hit F12
- Go to the "Network" tab
- Filter: videomanifest
- Hit F5
- Start playing the video
- As soon as the video starts, a result will appear, starting with "videomanifest?provider".
- Right-click on "videomanifest?provider...", and click where it allows you to copy the URL.
(You can now pause the video. Downloading will work even if the video is no longer playing)
- Go to Notepad and Paste the URL. The URL should be around 3,000 characters long
- Hit Ctrl-F (Find), and look for "index&format=dash" (without the quotation marks)
- Delete all the characters that follow "index&format=dash", basically everything from "&altManifestMetadata" to the end of the URL.
- Copy the shortened but still around 1,000 characters long URL.

Now it's time to download your video!
Here are the instructions using YT-DLP
- Open Command Prompt in Administrator mode.
- Go to your YT-DLP folder (ex: d:\yt-dlp)
- Type: yt-dlp "PasteShortenedURLhere" -o FilenameYouWant.mp4

Here are the instructions using FFMPEG
- Open Command Prompt in Administrator mode.
- Go to your FFMPEG folder (ex: d:\ffmpeg)
- Type: ffmpeg -i "PasteShortenedURLhere" -codec copy FilenameYouWant.mp4

The instructions were effective as of August 22, 2024.
[Fetching Title#vt25](https://www.reddit.com/r/sharepoint/comments/nuk8q0/is_there_any_way_to_download_view_only_videos/)