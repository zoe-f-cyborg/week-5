# Week 5 Journal

<iframe  title="YouTube video player" width="480" height="390" src="http://www.youtube.com/watch?v=TheVideoID?autoplay=1" frameborder="0" allowfullscreen></iframe>

### Readings
- The introductory musical piece was fascinatingly good. I fell down a rabbit hole reading, and listening to “Assemblage Theory.” 
- Looking at the [digital panopticon](https://www.digitalpanopticon.org/search?targ=multipie&e0.type.t.t=root&e0.has_tattoo.tty.x=yes&tf-multipie-start=sentence&tf-multipie-end=tattoo_subjects), I found navigating its search criteria slightly confusing. I tried to search within the “executed” category for a long time before realizing that it wasn’t, as I assumed, but because there [was actually none,](https://www.digitalpanopticon.org/search?e0.type.t.t=root&e0.given.s.s=&e0.surname.s.s=&e0._all.s.s=&e1.type.t.t=executed&e1.date.d.ld=&e1.date.d.lm=&e1.date.d.ly=&e1.date.d.hd=&e1.date.d.hm=&e1.date.d.hy=) as none of the nearly 2500 executed convicts are recorded as having tattoos. 
- [This](https://datasittersclub.github.io/site/dsc4/) article on *The Data-Sitters Club*, from the DH Awards web page, was a good example of the type of literary analysis work topic modelling can assist us with, and as an english minor it intrigued me quite a lot. The author’s suggesting that “the books might be modelling for the reader in a discursive way one of the forms of emotional labor that women are socialized to do in daily life: regulating other people’s emotions for them” emerged from using AntConc to detect instances of “a little” modifying positive or negative terms. 
- I also explored the Queer History Project for a bit, bookmarking [this](https://gizmodo.com/how-90s-cybersex-pioneers-looked-for-action-and-found-c-1831079932) article for later. 


### Audio Mediums
- Audacity— I’ve had this installed on previous machines for small recording projects of my own and I was quite excited to get back into it! 
- Two-Tone— I played around with the provided data and created this short piece: I chose A major because I liked the bouncy feeling the more unusual tonic provided. I played around with some of the different instruments but they mostly just added to the dissonance of it, which I did try to minimize. Instead, I went with 3 lines of melody, 1 bass (for the material) and 2 piano (for the coins). Of the piano lines, I set one to play only the higher notes, using the “filter value” scale, and made its tempo x2, so that it effectively added emphasis to those wealthier (in coin) cities. I kept the bass at a x2 tempo mainly because I just liked the way it sounded— it made the fact that the notes rarely change less of a bug and more of a feature, a gentle *ostinato* supporting the piece. I just wish I could tamper with the notes a little bit to give it more of a feeling of resolution… 

[my sonification](sonification-roman-data.mp3)

### Story Mapping
- To get my gills wet I mucked up a quick silly map of the dour-faced selfies I took across western Europe last summer:

<iframe src=“https://uploads.knightlab.com/storymapjs/3f10e63fc07b3d0e9fe302f2e4b512f2/hello-world/index.html” width = 100% height = "400"></iframe>

- ??? This didn't seem to work. Will return to it. 

#### Using Leaflet
- Copying and pasting the source code, this worked fine, but when I tried to make adjustments by altering the coordinates for “this is the center of our map!” and changing the pixel length of the final display map, it no longer loaded anything. I’m not sure if this is because of something I did to the code without realizing it (the long and lat numbers I entered where a digit shorter than the originals, for example, because that’s all the website I was using counted), or because I “terminated session” in terminal so that I could try again, even though it seemed to still be processing something. 
    - Update: There were a few reasons, I think:
    - 1. I hadn’t navigated back to web-map in terminal when I reopened it— I have to remember to `cd documents/digital-history/week-5/web-map` every time.
    - In the Json code, I had removed the spaces on either end of the coordinates within the brackets, so it read `"coordinates":  [-75.693207, 45.411491]` instead of `"coordinates":  [ -75.693207, 45.411491  ]` like the original code. 
    - With those fixed, it generated a new map beautifully! Now a box of 1000 pixels by 1000 pixels, denoting the location of the YMCA. 

![screencap](ss3.png)

- (this image has the old ottawa map overlay, because I forgot to take a screenshot of the earlier stages)

#### Map Warping
- the begin, I chose a [simple](https://www.bac-lac.gc.ca/eng/CollectionSearch/Pages/record.aspx?app=fonandcol&IdNumber=2163337&new=-8586104077399913864) image of a flat map

- I added many control points.

![image](ss5.png)

- And I rectified it, then added it (https://mapwarper.net/maps/tile/47938/{z}/{x}/{y}.png) to my leaflet map. 

![image](ss6.png)

- It looks good, though I’m… not entirely sure that that *is* where the YMCA is. I decided to add the location of my old high school (Lisgar Collegiate Instatute), grabbing the approximate latitude and longitude from [latlong.net](https://www.latlong.net/convert-address-to-lat-long.html). 

![img](ss8.png)

- It’s certainly quite close, so although I wouldn’t use this map for extremely precise examination, it gives a pretty good general sense of space.

- I wanted to also try out a [more challenging](https://www.bac-lac.gc.ca/eng/CollectionSearch/Pages/record.aspx?app=fonandcol&IdNumber=4140195&new=-8586104062217727912) (and fun) image, this 3d illustration of an arial view of the city, highlighting major businesses

![image](ss11.png)

- That, er, doesn’t look right. It actually looked alright in preview before I added point 8— the canal just didn’t quite line up with itself. Which makes me realize the green-yellow-red of the location points probably indicates something about the accuracy of my choices?? Interesting. 
- I was able to delete point 8 and got a much better image. I fidgeted with it for a while, deleting and adding points, until I settled on a less is more philosophy and kept only 4 points. Final url: https://mapwarper.net/maps/tile/47940/{z}/{x}/{y}.png 

![image](ss15.png)

- The maps still don’t line up as well as I would like, however, so I was excited to move on to stage where I would be able to toggle the overlay on and off. 

#### Overlays and animations
- Following the tutorial, the code definitely worked, though I’m confused why the lumber district map is so small?!?!
- I also created a version using the maps I had rectified, renaming the variables to “simple map” and “business map”

![image of code](ss22.png)

![image of map](ss20.png)

- I was able to add the animation easily— Overall I’ve been quite surprised by how forgiving this system seems to be, as I didn’t have any major roadblocks! 
- I decided to animate the route from Lisgar Collegiate to the YMCA. My points were: 
`-75.689964, 45.420504
-75.691992, 45.419796
-75.687063, 45.414042
-75.693207, 45.411491`
- I added those into the code, creating the final map (which I wish I knew how to export and show here). It lined up with the streets very well, as I hoped it would.

![img](ss23.png)

#### Conclusion
- This project was some fo the most fun I’ve had in this course! The code was surprisingly forgiving and although I wouldn’t have been able to construct it myself, I felt fairly comfortable manipulating it as needed. 
- There is a lot more I could imagine doing with this type of technology, and indeed which has been done: 
- Recently [a friend of mine](https://twitter.com/clairequaclaire/status/1267554737466953733) put out on a poll on twitter asking if I was living on unceceded or treaty land. I assumed unceceded because that’s what they always say before public theatre performances and other events here. But when [I googled it](https://native-land.ca/) I found a website mapping aboriginal communities, languages, and treaties, which suggested that my current location was actually part of the “Crawford Purchase” of 1783. [Nicknamed “the gunshot treaty”](http://www.stoneskingston.ca/indigenous-history/the-crawford-purchase/) its boundaries were supposedly “determined by how far the sound of a gunshot carried.” This struck me as the type of historical data particularly suited to mapping. I was especially interested in how different areas (both of aboriginal territories and treaty boundaries) sometimes overlaid one another— a contradiction which becomes obvious when mapped! 

![img](ss26.png)
