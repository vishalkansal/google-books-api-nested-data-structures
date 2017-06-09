
    
# Arrays and Hashes in API Data

APIs or Application Programming Interfaces are used to get and send data between apps. Think of them as a secret developer access to apps that most non-technical users would never be able to access. APIs are useful because they provide us with data and functionality that we can integrate into our own programming.

![Coldplay](https://s3.amazonaws.com/upperline/curriculum-assets/ruby/coldplay.jpg)

In this lab, we've set up a call to the Spotify API that returns a big hash (filled with more hashes and arrays) all related to the current top tracks by Coldplay in the US. We then save this to a variable called `top_tracks`. Here's the code that pulls that data from the API for us.

```ruby
#import the gems we need to pull data from an API
require 'httparty'
require 'json'

# In these two lines we get the data from Spotify and save to the variable called top_tracks.

response = HTTParty.get('https://api.spotify.com/v1/artists/4gzpq5DPGxSnKTe4SA8HAU/top-tracks?country=US')
top_tracks = JSON.parse(response.body)
```
## Instructions

Fork and clone this lab, and run `bundle install` in the command line.

Open up the `api-challenge.rb` in your text editor and run `ruby api-challenge.rb` to see the nested hash that is returned in `top_tracks`. Then see how far you can get at parsing through this crazy nested hash of data to write code that will answer the questions in the file. There are easy, medium and hard challenges... Good luck!

**Note:** You may want to use `pp` (stands for pretty print) instead of `print` or `puts` - it makes the data structures much easier to see as you're working with them!


PLATFORMS
  ruby

DEPENDENCIES
  httparty
  json

BUNDLED WITH
   1.14.6
