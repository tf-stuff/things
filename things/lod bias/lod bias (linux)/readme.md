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

<h2>troubleshooting</h2>

game should launch, if issues exist try adding `STRANGLE_NODLSYM=1` before the `STRANGLE_PICMIP=` or disable steam overlay.<br>
if the game launches but no bias has been applied, try setting `mat_mipmaptextures` to 1 and `mat_filtertextures` to 1 OR try setting `mat_filtertextures` to 0
