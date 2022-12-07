# Twitter-Meme-API-Host
For Getting Memes from Twitter
An API used to scrap memes from Twitter Userid and returns in json.

The Link of the Meme APIs is : http://ms-twitter-memeapi.azurewebsites.net

// At the first ping the api takes times to get the data in order to wakeup the server, after the first successful ping the delay is resolved.

### Default
By default the API grabs a random meme from 

    "memes",
    "Theindianmeme", #IND
    "OldMemeArchive",
    "_sarcasticvijay", #IND 
    "GabbbarSingh", #IND
    "RespectfulMemes",
    "Being_Humor", #IND
    "Cryptic_Miind", #IND
    "WholesomeMeme",
    "sagarcasm", #IND
    "OhWonka",
    #"Lord_Voldemort7",
    "trilochann45", #IND
    "moretylenol",
    "_sarcasticvijay", #IND 
    "whitememejesus",
    "memes_hallabol", #IND
    "IntrovertProbss"



API Link : http://ms-twitter-memeapi.azurewebsites.net

Example Response:

```lua
  {
"count": 1,
"memes": [
{
"post_user": "IntrovertProbss",
"post_media_url": "http://pbs.twimg.com/media/FdMA2GWWYAAjCbN.jpg",
"post_text": "",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1520851980993900548/1b5DfXlR_normal.jpg",
"post_url": "https://t.co/yUly6wClqm",
"post_likes": 787,
"post_retweet": 78
}
]
}
 ```

 ## Custom Endpoints
 
### Specify count (MAX 49)
In order to get multiple memes in a single request from the default userid, specify the count with the following endpoint.

Endpoint: /{count}

Example: http://ms-twitter-memeapi.azurewebsites.net/2

Response:

```lua   
{
"count": 2,
"memes": [
{
"post_user": "WholesomeMeme",
"post_media_url": "http://pbs.twimg.com/media/Fiw-8n7XwAAKQAR.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1411016646815358978/H8kX0hfw_normal.jpg",
"post_url": "https://t.co/IWfJRkK7um",
"post_text": "",
"post_likes": 54877,
"post_retweet": 3508
},
{
"post_user": "RespectfulMemes",
"post_media_url": "http://pbs.twimg.com/media/FicB2BzXwAEbecT.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/800857197697703936/RMfUXdGk_normal.jpg",
"post_url": "https://t.co/efOW0QWY3z",
"post_text": "",
"post_likes": 11594,
"post_retweet": 1272
}
]
}
```    

### Specific Userid
In order to get a random posts from any Userid, specify the subreddit name in the following endpoint.

Endpoint: /{userid}

Example: http://ms-twitter-memeapi.azurewebsites.net/allindiamemes

Response:

```lua
{
"count": 1,
"memes": [
{
"post_user": "allindiamemes",
"post_media_url": "http://pbs.twimg.com/media/FgU2YYkaUAI1Xlu.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1583305417261993984/GJDncE5H_normal.jpg",
"post_url": "https://t.co/3tuDdfIWMh",
"post_text": "Kohli will drop the catch.\nRohit will miss the runout. ",
"post_likes": 197,
"post_retweet": 22
}
]
}
```    

### Specific Userid & Count (MAX 49)
In order to get a custom number of posts from a specific Userid, specify the name of the Userid and the count in the following endpoints.

Endpoint: /{userid}/{count}

Example: http://ms-twitter-memeapi.azurewebsites.net/allindiamemes/5

Response:
```lua
{
"count": 5,
"memes": [
{
"post_user": "allindiamemes",
"post_media_url": "http://pbs.twimg.com/media/Fh2pCADaUAAVCga.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1583305417261993984/GJDncE5H_normal.jpg",
"post_url": "https://t.co/uw7fQz0dvr",
"post_text": "Me to my twitter mutuals ",
"post_likes": 209,
"post_retweet": 47
},
{
"post_user": "allindiamemes",
"post_media_url": "http://pbs.twimg.com/ext_tw_video_thumb/1585927114259587074/pu/img/wbiLSo4LSddmG-ti.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1583305417261993984/GJDncE5H_normal.jpg",
"post_url": "https://t.co/t8TQAnJTRe",
"post_text": "Parag Agrawal walking away from Twitter with $42 million\n\n",
"post_likes": 7172,
"post_retweet": 880
},
{
"post_user": "allindiamemes",
"post_media_url": "http://pbs.twimg.com/media/Fh2pCADaUAAVCga.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1583305417261993984/GJDncE5H_normal.jpg",
"post_url": "https://t.co/uw7fQz0dvr",
"post_text": "Me to my twitter mutuals ",
"post_likes": 209,
"post_retweet": 47
},
{
"post_user": "allindiamemes",
"post_media_url": "http://pbs.twimg.com/media/FjNBSdMaMAA2j6Y.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1583305417261993984/GJDncE5H_normal.jpg",
"post_url": "https://t.co/N2qws5GHtF",
"post_text": "Me playing watchman while my friend is romancing his gf ",
"post_likes": 176,
"post_retweet": 42
},
{
"post_user": "allindiamemes",
"post_media_url": "http://pbs.twimg.com/media/FiA474EakAEQgGG.jpg",
"post_url_profile_url": "http://pbs.twimg.com/profile_images/1583305417261993984/GJDncE5H_normal.jpg",
"post_url": "https://t.co/Z0ONPyMghd",
"post_text": "Waiting for Elon Musk to restore Kangana Ranaut's account ",
"post_likes": 175,
"post_retweet": 52
}
]
}
```
