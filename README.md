# amazon_movies_korean_titles
Switch out English titles for Korean movies on Amazon video to Korean titles

I wrote up a rough draft that goes through Amazon Video search results and switches out the English-translated Korean movie titles with the original Korean titles. 
I wasn't able to find a decent source where I could reference the translated titles back to the original Korean ones, so this just queries wikipedia with the hopes that a wiki for the movie exists and the entry has the Hangul title in it. Only works for about half the video search results at best. Load it as a local chrome extension, go to amazon, search "korean movies" and it should do its thing. 

Things that dont't work: 
* Pagination. Switching pages on the search results doesn't do a page reload, so the code won't trigger. Need to figure out a way to wait for amazon's xhr request for the next page data to finish and retrigger my code.
* If the Korean title has numbers in it, they'll get dropped. Need to fix the regex that grabs the Korean out of the wiki search result.
