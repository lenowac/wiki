# Replace "alt+f4" with "win+w"

...or choose anything else, "win+q" is quite popular as well.

1. Get [Autohotkey](https://www.autohotkey.com/)
2. win+r, enter: `%AppData%\Microsoft\Windows\Start Menu\Programs\Startup`
3. create "win+w.ahk"
4. paste this in there:

```
#w::Send !{F4}
return
```

<br/>

if you are interested in more, here's a quick symbol rundown:

```
# = windows key
^ = ctrl key
! = alt
+ = shift
<^>! = alt gr
```

[or go read the whole thing](https://www.autohotkey.com/docs/Hotkeys.htm#Symbols)

<br/><br/>

now enjoy not crippiling your hand every time you want to close a window
