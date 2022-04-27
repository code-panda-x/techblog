---
title: "Flask Api"
date: 2022-04-15T11:21:13-05:00
draft: true
---

## API in clask
### Naive appraoch

`jsonify` converts obj to json
`request.get_json` gets json obj from POST requests

```
from flask import Flask, jsonify, request
app = Flask(__name__)

# Main page
@app.route('/')
def hello_world():
    return "Hello World"

# Get request
@app.route('/hi', methods=["GET"])
def hi_there():
    retJson = {
        'name': 'Max'
    }
    return jsonify(retJson)

# Post request
@app.route('/add', methods=["POST"])
def add_two():
    dataDict = request.get_json()
    return jsonify(dataDict)



if __name__ == "__main__":
    app.run(host="127.0.0.1", port=5000)
    #app.run(debug=True) - Internal Server Error, display the bug so we can debug
```

### Using flask_restful
REST API:
1. Resource: what we offer
2. Path
   
```
from flask import Flask, jsonify, request
from flask_restful import Api, Resource


app = Flask(__name__)
api = Api(app)

class Add(Resource):
    def post(self):
        retMap = {
            'Message': ret,
            'Status Code': 200
        }
        return jsonify(retMap)

api.add_resource(Add, "/add")

if __name__=="__main__":
    app.run(debug=True)
```

## Web app vs Web server

Typically
Web app return: page (render)

Web server return: Json

## Json format
```
{
    "num" : 3,
    "string" : "abc",
    "boolean" : 1,
    "array": [1,2,3,"abc"],
    "arrOfObj":[
        {
            "obj1": 1
        }
        {
            "obj2": 2
        }
    ],
    "nestedarr":[
        {
            "somearr":[
                {

                }
            ]
        }
    ]
}
```

