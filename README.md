# YouTube-dl
系統:Centos 6.8<br/>
必要軟體:YouTube-dl . ffmpeg . Apache . php . python<br>

<h1>Step1: 安裝 Python</h1>
YouTube-dl需要Python2.6,2.7,3.2+<br>
<code>yum install python -y</code><br>

<h1>Step2: 安裝必要軟體</h1>
<h3>2-1 Youtube-dl</h3>
到這邊<a href="https://rg3.github.io/youtube-dl/download.html">YouTube-dl</a> 下載YouTube-dl<br>
<code>sudo wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/bin/youtube-dl</code><br>
<code>sudo chmod a+rx /usr/bin/youtube-dl</code><br>
測試YouTube-dl是否正常運作<br>
<code>youtube-dl</code><br>
正常會回傳<br>
  Usage: youtube-dl [OPTIONS] URL [URL...]  
  
youtube-dl: error: You must provide at least one URL.  
    Type youtube-dl --help to see a list of all options.      
<h3>2-2 ffmpeg</h3>
從本專案中下載ffmpeg安裝腳本<a href="https://raw.githubusercontent.com/Kutinging/YouTube-dl/master/ffmpeg/latest-ffmpeg-centos6.sh">ffmpeg</a><br>
<code>sudo wget https://raw.githubusercontent.com/Kutinging/YouTube-dl/master/ffmpeg/latest-ffmpeg-centos6.sh</code><br>
<code>sudo chmod +x latest-ffmpeg-centos6.sh</code>  
<code>sudo ./latest-ffmpeg-centos6.sh</code>  
安裝完後到安裝的目錄底下查看bin資料夾  
裡面包含ffmpeg,ffprobe等等檔案  
將所有檔案複製到/bin/  
<code>cp ffmpeg ffprobe ffserver lame vsyasm x264 yasm ytasm /bin/</code>  
