# Nova Blog Updates

This project was one that wasn't quite abandoned but also wasn't anything I particularly felt need to update since I'm so inconsistent with blogging. However I wanted to pick it back up since I want a place to post essays I write on my interests. Looking into the code, I remembered my philosophy behind building this platform, but also saw some glaring issues in the original implementation. It was very fragile, and I feel accurately represented how junior I was when I originally made it. 

I've now updated the repo to be a bit better written, and will probably be updating more often.

As for what specifically was wrong, the html parsing was funky, we were esentially taking whole html files breaking them in half, and then stitching them back together. I have implemented a slot system now with layouts and base pages, reducing repeated html and making the text replication much more reliable.

I also updated the method with which it is published to github pages to more closely reflect documentation. 

You can see the [diff here](https://github.com/madaley1/nova-blog/commit/11cde3e235ffd1cd62e929853aa6e0784c576b2f), don't worry about the failing checks, its because its not the github pages repo, which is required for them to pass.