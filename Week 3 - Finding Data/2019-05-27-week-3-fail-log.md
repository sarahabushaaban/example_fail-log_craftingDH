# Module 2 Exercises
<ul>
<li>The Dream Case</li>
<li>Wget</li>
<li>Writing a program to extract data from a webpage</li>
<li>Encoding transcribed text</li>
<li>Collecting data from Twitter</li>
<li>Coverting images to text with Tesseract</li>
</ul>

### The Dream Case

<ul>
<li>I faced far more difficulties in this first exercise than I could&rsquo;ve imagined for something that looked fairly straightforward. I wasn&rsquo;t sure whether I was to lodge my history into the dhbox-work-today file, but I did initially.</li>
<li>Then, I came into some confusion about whether I was meant to format my file as markdown, or to leave it in HTML, but ultimately decided to leave it in HTML because it appeared to be a suitable format.</li>
</ul>

### Wget

<ul>
<li>-r : Recursive retrieval; retrieves links from the websites, but also links that exist within those links&hellip; therefore, it can accumulate a lot, too much links, not specific enough. </li>
<li>--no-parent/-np : limits search to those links within the website domain (e.g. activehistory.ca/papers/(hierarchy) )</li>
<li>-l 2: LIMITS links (out of hierarchy) to only 2 follow links</li>
<li>-w 10: tells the server to WAIT 10 seconds between requests. Milligan uses 2 seconds. </li>
<li>--limit-rate=20k: LIMITS maximum speed to 20kb/s. Up to 200 kb/s is ok for small files, according to Milligan, but better to use 20 kb/s to go easy on the server. </li>
<li><strong>What does that spell?</strong>
<ul>
<li>wget -r --no-parent -w 2 --limit-rate=20k http://activehistory.ca/papers/ - this is the command I input.</li>
</ul>
</li>
<li>When done, information appeared on the screen, signalling that total &ldquo;wall clock time&rdquo; was 18 minutes and 22 seconds, which I assume is how long it has been since I input the command, and it says it downloaded 182 files in 6 minutes and 3 seconds.</li>
<li>Used nano urls.py to open new Python file titled &lsquo;urls&rsquo;</li>
<li>Pasted this script, to extract the URLs from the specified range of 80 pages from the war diaries, and put them into a text file:<br />urls = ''; *URLS <br />f=open('urls.txt','w') <br />for x in range(8029, 8110): **the specified 80 pages**<br /> urls = 'http://data2.collectionscanada.ca/e/e061/e00151%d.jpg\n' % (x)<br /> f.write(urls)<br />f.close</li>
<li>Then, input command($) wget -i urls.txt -r --no-parent -nd -w 2 --limit-rate=100k to download urls from urls.txt</li>
<li>$ls to make sure the files were actually downloaded</li>
</ul>

### Writing a program to extract data from a webpage

<ul>
<li>Pay critical attention to closing &lt;&gt; all tags</li>
<li>Use Firefox, not Safari or Google Chrome to view xml file</li>
</ul>

### Collecting data from twitter

### Converting images to text with Tesseract

<ul>
<li>$ mkdir ocr-test: Created a new directory, ocr-test</li>
<li>$ sudo apt-get install tesseract-ocr: installed Tesseract into DH Box</li>
<li>$ sudo apt-get update: updated package lists for outdated packages</li>
<li>$ convert -density 300 ~/war-diary/e001518087.jpg -depth 8 -strip -background white -alpha off e001518087.tiff: converted first file to TIFF with ImageMagick&rsquo;s convert command</li>
<li>$ tesseract e001518087.tiff output.txt: extracted text</li>
<li>Installed packages to RStudio, Magick, Magrittr and Tesseract</li>
<li>$ sudo apt-get install libcurl4-gnutls-dev: installed RCurl</li>
<li>$ sudo apt-get install libmagick++-dev: installed libmagick library</li>
<li>$ sudo apt-get install libtesseract-dev: installed libtesseract library</li>
<li>$ sudo apt-get install libleptonica-dev: installed libleptonic library</li>
<li>$ sudo apt-get install tesseract-ocr-eng: installed English Tesseract library</li>
<li>$ sudo apt-get install libpoppler-cpp-dev: installed popper cpp library</li>
<li>RStudio -&gt; run install.packages lines in script, then library lines to load libraries, then run each line until image_ocr(); run the last line write.table() to export OCR to text file</li>
<li>output.txt and R.txt downloaded</li>
</ul>

## Comments and Concerns

<ul>
<li>Via Rail&rsquo;s wifi is not the best. Maybe doing readings on the train could work sometimes - less likely if there are any images in the links. My patience will definitely be tested doing the exercises &amp; using the VPN on this signal. </li>
</ul>
