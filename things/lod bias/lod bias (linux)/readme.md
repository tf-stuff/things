first grab the requirements<br>
```
sudo apt install gcc-multilib g++-multilib libx11-dev mesa-common-dev
```
then, clone https://gitlab.com/torkel104/libstrangle using git<br>
```
git clone https://gitlab.com/torkel104/libstrangle
```
then, navigate into the new "libstrangle-master" folder<br>
```
cd libstrangle-master
```
then, use the "make" command<br>
```
sudo make install
```
then, go to tf2's launch options and add the text below, with "<somenumber>" replaced with your desired lod bias, between -16 and 16.<br> positive numbers indicate lower textures, negative indicate higher.<br>
```
STRANGLE_PICMIP=<somenumber> strangle %command%
```
and yes, "%command%" is supposed to be there.<br>
different values work on different hardware, so you'll just have to experiment with it yourself<br>

now, go to tf2's properties and disable the steam overlay. this crashes the game on some systems while using libstrangle, so disabling it will mean you have a better chance of having this work.
