# yt-dl-thing


yt-dlp for dummies.
I used to use gui for downloading playlists - both audio and video but , for some reason gui isn't working on mx linux 21(now). I don't know how to fix it so I spent last 2 hours finding right commands(I am not a tech guy). I just wanted some easy solution but there isn't, so this might help some. There are good tutorials everywhere on how to install yt-dlp. so i am skipping that part.

type yt-dlp -U first to update it.


To download YouTube VIDEO playlist with best audio - with its own folder with correct title, replace 1080p with desired resolution. This will also add numbers to downloaded files so thats really useful. ( replace URL with youtube playlist link within "") There is only one URL to replace so it wouldn't be confusing.

yt-dlp -o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "URL" -f 'bv*[height=1080]+ba'


To download YouTube AUDIO playlist with OPUS file format. - with its own folder with correct title. files will be numbered correctly within its own folded titled as youtube playlist name. There is one URL to replace so it wont be confusing.

yt-dlp -o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "URL" -f 'ba' -x --audio-format opus


single video from youtube.

yt-dlp "URL" -f 'bv*[height=1080]+ba'


single audio from youtube video.

yt-dlp "URL" -f 'ba' -x --audio-format opus


Example. To download entire playlist within its own folder.


yt-dlp -o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "https://youtube.com/playlist?list=PLKbmcnUUQMlnJXD8XCtq-f3GCCf29qeaY" -f 'bv*[height=1080]+ba'




Note : Files are downloaded to default directory, Dont know how to change it but thats alright. Private videos will be neglected in download process. Commands are tested on debian and mx linux 21. The old gui method was so simple, this command line stuff is difficult to understand.
