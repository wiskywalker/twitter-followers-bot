# twitter-bot
A bot for Twitter. **OPTIONS**: Follow users from query, geocode or list; unfollow who do not follow back (and are not included in *whitelist.txt*); create reports (containing followers, followings, people who do not follow me back and people i do not follow back). 


## Usage

Follow people who tweeted a word (**query**), limited to the **limit** value:
```
python twitter-bot.py -o follow -q {query} -l {limit}
```

Follow people who tweeted in a location (**geocode**), limited to the **limit** value:
```
python twitter-bot.py -o follow -g {geocode} -l {limit}
```

Follow users from a list file:
```
python twitter-bot.py -o follow -i {list_file}
```

Unfollow users from a list file:
```
python twitter-bot.py -o unfollow -i {list_file}
```

Unfollow all the people who do not follow you back and are not included in *whitelist.txt*:
```
python twitter-bot.py -o unfollow-back
```

Show report (followers, followings, people who do not follow me back and people i do not follow back):
```
python twitter-bot.py -o info
```


## Examples

Follow 5 people tweeting 'oscp':

```
python twitter-bot.py -q "oscp" -l 5 -o follow
```
![Screenshot](https://i.imgur.com/KZCVq6D.png)

Follow 7 people tweeting in 40.432,-3.708:

```
python3 twitter-bot.py -g "40.432,-3.708,10km" -l 7 -o follow
```
![Screenshot](https://i.imgur.com/3ZCQ1kk.png)

Follow users in example.lst:
```
python3 twitter-bot.py -o follow -i example.lst
```
![Screenshot](https://i.imgur.com/Y5GndGI.png)

Unfollow users in example.lst:

![Screenshot](https://i.imgur.com/0qDpQYG.png)

Unfollow people who i follow but they do not follow me back add them to a list:

```
python3 twitter-bot.py -o unfollow-back -i list-id
```
![Screenshot](https://i.imgur.com/QBhrXoe.png)

```
python3 twitter-bot.py -o info
```
![Screenshot](https://i.imgur.com/0quGImh.png)


![Screenshot](https://i.imgur.com/KfIXHO4.png)


## Requirements

Python 2.x:
```
pip install tweepy
```

Python 3.x:
```
pip3 install tweepy
```

*Create a twitter account and a twitter app, and fill the **config.py** file with the data you can create in https://developer.twitter.com*

## Note

Tested both in Python2.x (2.7.15rc1) and Python 3.x (3.6.7)