# Curlese

This is my first open-source project, so be nice!

Ever had the documentation tell you to hit an endpoint with something like:

```bash
curl -X POST \
  -H "X-Parse-Application-Id: ${APPLICATION_ID}" \
  -H "X-Parse-REST-API-Key: ${REST_API_KEY}" \
  -H "Content-Type: application/json" \
  -d '{"score":1337,"playerName":"Me","cheatMode":false}' \
  https://api.parse.com/1/classes/Score
```

But your end native-side code looks something like:

```ruby
payload = "{\"score\": \"" + 1337 + "\"}"
           "\", \"playerName\": \"" + \"Me\" + 
            #{}"\", \"cheatMode\": \"" + false + "\"}"

request = RestClient::Request.new(
  	:method => :post,
    :url => 'https://api.service.com/1/classes/Score',
    :headers => {'X-Parse-Application-Id' => APPLICATION_ID,
    			 'X-Parse-REST-API-Key' => 'REST_API_KEY',
    			 'Content-Type' => 'application/json'},
    :payload => payload)
  	response = request.execute
```

Work with REST endpoints in multiple languages and multiple platforms and fed up of the syntactic gymnastics needed to map curl commands to your native language? Well, this library is for you. Write once in inlined curl, and generate out to native code!

SIMPLIFY YOUR PLUMBING! LEARN CURL ONCE AND TAKE ANYWHERE!

Roadmap
1. One language, one curl testcase
2. Multiple languages, one curl testcase
3. Multiple languages, multiple curl testcases

Curl Testcases
* Simple GET
* Simple POST
* -H
* -d
* -X

1. 
'''
```bash
curl -X POST \
  -H "X-Parse-Application-Id: ${APPLICATION_ID}" \
  -H "X-Parse-REST-API-Key: ${REST_API_KEY}" \
  -H "Content-Type: application/json" \
  -d '{"score":1337,"playerName":"Me","cheatMode":false}' \
  https://api.parse.com/1/classes/Score
```
* In Ruby (with [rest-client][https://rubygems.org/gems/rest-client/versions/1.8.0])
* In Obj-C
* In Java/Android



 

