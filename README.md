# mjpg-opencv-video-broadcasting
broadcasting opencv output video with mjpg streamer in python

<html>
<body>
<p>For use this project need to install mjpg-streamer and run it on linux terminal </p>
<p>Following this steps </p>
<h2>1. Install build dependencies</h2>
<p><pre>  sudo apt-get install libjpeg8-dev imagemagick libv4l-dev</pre></p>
<h2>2.Add missing videodev.h</h2>
<p><pre>  sudo ln -s /usr/include/linux/videodev2.h /usr/include/linux/videodev.h</pre></p>
<h2>3.Unzip the MJPG-Streamer source code</h2>
<p><pre>  unzip mjpg-streamer-code-182.zip</pre></p>
<h2>4.Build MJPG-Streamer</h2>
<p><pre>  cd mjpg-streamer-code-182/mjpg-streamer</pre></p>
<p><pre>  make mjpg_streamer input_file.so output_http.so</pre></p>
<h2>5.Install MJPG-Streamer</h2>
<p><pre>  sudo cp mjpg_streamer /usr/local/bin</pre></p>
<p><pre>  sudo cp output_http.so input_file.so /usr/local/lib/</pre></p>
<p><pre>  sudo cp -R www /usr/local/www</pre></p>
<h2>6.Run This Code</h2>
<p><pre>  python main.py</pre></p>
<h2>7.Start MJPG-Streamer</h2>
<p><pre>  LD_LIBRARY_PATH=/usr/local/lib mjpg_streamer -i "input_file.so -f /path/to/your/save/jpg/file -n pic.jpg" -o "output_http.so -w /usr/local/www"</pre></p>
<p><pre>  Example : </pre></p>
<p><pre>  LD_LIBRARY_PATH=/usr/local/lib/ mjpg_streamer -i "input_file.so -f /home/mazyar/Desktop -n out.jpg" -o "output_http.so -w /usr/local/www"</pre></p>
<h2>8.Watch the Stream!</h2>
<p>Now you can connect with your web browser and watch the stream live. If you want to watch</p>
<p>from within the same Raspberry Pi you can enter http://localhost:8080 in the browser's </p>
<p>address bar. If you want to watch from another computer in your network use </p>
<p>http://IP-address:8080.</p>
<h4>Lets Enjoy !!! </h4>
<body>
</html>
