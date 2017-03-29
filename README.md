# nchan-heroku
One-button deploy [NCHAN][1] to Heroku. Clicking the deploy button will create a Heroku app with the [nchan-buildpack][0] preconfigured for you!

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

This will run NCHAN with a publisher route at `/pub` and a subscriber route at `/sub`. See example pub/sub usage:

~~~sh
# start a subscriber connection
curl <your url>/sub?id=foobar   # id query parameter is the channel

# somewhere else:
curl <your-url>/pub?id=foobar -X POST --data 'hello'
# then, see the message delivered to your open connection!
~~~

[0]: https://github.com/andjosh/nchan-buildpack
[1]: https://github.com/slact/nchan
