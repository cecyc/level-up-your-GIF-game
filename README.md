##Level up your GIF Game 👍

![https://dl.dropboxusercontent.com/u/32684641/meme-hub/level-up.gif](level up!)

Presented at #CSSDevConf 2016.

###Contents

####How do you pronounce GIF?

[JIF is the Format, GIF is the culture](https://medium.com/message/jif-is-the-format-gif-is-the-culture-af8673796c44)

####History of GIFs

[Arrival of a Train](https://www.youtube.com/watch?v=1dgLEDdFddk), by the Lumière Brothers

[Early Kinetoscopes](https://www.youtube.com/watch?v=686Y7bZYavA), by Edison

[Sprinkler Sprinkled](https://www.youtube.com/watch?v=IooPPi1YzkM), by the Lumière Brothers

####What makes a good GIF?

> A good GIF is a simple concept

####What makes a great GIF?

> A great GIF provides an unexpected element

####GIFs in the workplace

A few simple rules for safe workplace GIFs

1. If you wouldn't share it with HR, it doesn't belong in chat
2. Does it enhance the interaction?
3. Do not use `/giphy` lightly

####Common tools

**GIPHY lesser known commands**

Returns #1 rated result for the query

```
/giphy #1 [search term]
```

Returns a yes or no answer based on a question

```
/giphy #magic8ball [question]
```

Returns a random GIF with your weather forecast

```
/giphy #weather [city or zip code]
```

**GIF Keyboard integration**

GIF Keyboard on Slack is an alternate GIF integration that gives you more flexibility.

Returns one result:

```
/gif [query]
```

Returns several results to choose from before posting. The results are only visible to you until you choose which one to share.

```
/gifs [query]
```

####Custom workflows

**Dropbox + Alfred**

1. Host your GIFs in Dropbox Public folder
2. Use custom Alfred workflow to search in folder + bash script to generate sharable Dropbox link.

[Click here for tutorial.](http://destroytoday.com/writings/gif-workflow/)

**Github + CLI**

Free option!

1. Host your GIFs on Github
2. Use shareable Github links for GIFs
3. Set-up aliases and bash script to search and generate sharable URLs

Alias to cd into GIF repo, git add, git commit and git push

```
alias gif-add="cd ~/absolute/path/to/gif-repo && git add . && git commit -m 'adding GIFs' && git push origin master"
```

Alias to search GIF repo from any location

```
alias gif-search="~/absolute/path/to/gif-repo ls | grep"

$ gif-search query
```

Bash script to generate sharable URL

```
#!/bin/bash
base_url="https://raw.githubusercontent.com/USERNAME/repo/branch/"
base_url+=$1
echo $base_url
```

To run the script as an executable from anywhere:

1. Move file to /usr/local/bin
2. Add privileges `chmod +x filename`
