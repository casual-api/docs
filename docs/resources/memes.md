# Memes
You can fetch latest memes from Casual API. These memes are taken from popular subreddits and
the database is updated on daily basis so all memes are "fresh and spicy".

## Meme Object

|     Field     |  Type    |                     Description                           |
|:-------------:|:--------:|:---------------------------------------------------------:|
|     `id`      | string   |          The ID of this meme. This is a Reddit post ID.   |
|     `url`     | string   |               The image URL of meme.                      |
|     `nsfw`    | boolean? |          Whether this meme is marked as NSFW.             |
|    `author`   | string   |          The Reddit user that posted this meme.           |
|   `subreddit` | string   | The [subreddit](#meme-subreddits) that this meme is from. |


## Meme Subreddits
These are the subreddits that the memes are taken from. The name field represents the
value of ``subreddit`` field on the [meme object](#meme-object)

|    Name      |                  Description                                        |
|:------------:|:-------------------------------------------------------------------:|
|  `dankmemes` | The [r/dankmemes](https://www.reddit.com/r/dankmemes) subreddit.    |
|  `memes`     | The [r/memes](https://www.reddit.com/r/dankmemes) subreddit.        |

## Endpoints
Following endpoints are used for fetching memes.

### List Random Memes
<span class="http-request">GET</span> <span class="http-path">/memes</span>

Fetch a list of random memes. Use this endpoint to cache a specific set of memes
and periodically update your cache.

Returns the list of [meme objects](#meme-object)

#### Query String Parameters
!!! note ""

    All query string parameters are optional.

|     Field      |  Type    |                     Description                             |  Default  |
|:--------------:|:--------:|:-----------------------------------------------------------:|:---------:|
|    `limit`     | integer  |          The number of memes to fetch (1-100)               |     10    |
| `include_nsfw` | boolean  |             Whether to include NSFW marked memes.           |    true   |
|   `subreddit`  | string   | The [subreddit](#meme-subreddits) to return posts of.       |   random  |

### Get Random Meme
<span class="http-request">GET</span> <span class="http-path">/memes/random</span>

Fetches a random meme. Returns a [meme object](#meme-object)
