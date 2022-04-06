go into your huds `resource/clientscheme.res` file and add `#base "shadows.res"` to the top of the file<br>
then, create a new file called `shadows.res` and put it next to your `clientscheme.res`<br>
then, add the following text to the inside of the `shadows.res` file:

```
Scheme
{
  Fonts
  {
    ShadowsFont
    {
      "1"
      {
        "name"			"A font that does not exist"
        "tall"			"20"
        "additive"		"0"
        "antialias"		"1"
        "shadow"		"1"
      }
    }
  }
}
```
then, go into your autoexec (if you use mastercomfig it will be in the `user` folder) and paste the following in:

```
r_shadows 1
r_shadowrendertotexture 1
cl_blobbyshadows 0
r_shadowmaxrendered 12
```

then, start up tf2.
