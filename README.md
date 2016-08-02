# Curlese

This is my first open-source project, so be nice!

Ever had the documentation tell you to hit an endpoint with something like:

curl -X POST \
  -H "X-Parse-Application-Id: ${APPLICATION_ID}" \
  -H "X-Parse-REST-API-Key: ${REST_API_KEY}" \
  -H "Content-Type: application/json" \
  -d '{"score":1337,"playerName":"Me","cheatMode":false}' \
  https://api.service.com/1/classes/Score


But your end native-side code looks something like:

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

(Ruby example)

?

Work with REST endpoints in multiple languages and multiple platforms and fed up of the syntactic gymnastics needed to map curl commands to your native language? Well, this library is for you. Write once in inlined curl, and generate out to native code!

SIMPLIFY YOUR PLUMBING! LEARN CURL ONCE AND TAKE ANYWHERE!


 

