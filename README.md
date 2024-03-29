# compact-json
A modified JSON Format to make data more compact (For small data without repetition, this data may increase, but for data with repetition, this will be the feasible solution

# A Normal JSON File Structure
```
{
    "users":[
        {
            "id":0,
            "name":"Tanvir Sourov",
            "work":"Socian",
            "email":"tanvir@socian.xyz",
            "dob":"1994",
            "address":"Dhaka",
            "city":"Dhaka",
            "optedin":true
        },
        {
            "id":1,
            "name":"Tareq Al Muntasir",
            "work":"Technolive",
            "email":"tareq@technolive.co",
            "dob":"1994",
            "address":"Dhaka",
            "city":"Dhaka",
            "optedin":false
        }
    ],
    "images":[
        {
            "id":1,
            "name":"abc.png",
            "url":"/abc.png"
        },
        {
            "id":2,
            "name":"def.png",
            "url":"/def.png"
        },
        {
            "id":3,
            "name":"ghi.png",
            "url":"/ghi.png"
        }
    ],
    "coordinates":{
        "x":35.12,
        "y":-21.49
    },
    "price":"$59,395",
    "others":[
        {
            "premium":"good",
            "bonus":"satisfactory",
            "gender":"male",
            "organization":"abc ltd",
            "location":"bangladesh",
            "population":"160 million",
            "age":24,
            "priority":"yes",
            "is_admin":1
        },
        {
            "premium":"bad",
            "bonus":"satisfactory",
            "gender":"female",
            "organization":"def ltd",
            "location":"bangladesh",
            "population":"160 million",
            "age":25,
            "priority":"no",
            "is_admin":0
        }
    ],
    "books":[
        {
            "author":"Mr X",
            "name":"Compact JSON",
            "page":1,
            "brand":"Socian Ltd",
            "value":"yes",
            "easy":"yes"
        },
        {
            "author":"Mr Y",
            "name":"Compact JSON 2",
            "page":1,
            "brand":"Technolive",
            "value":"yes",
            "easy":"yes"
        }
    ]
}
```

# CJSON or Compact JSON File Structure
```
{
    "v_a_l_u_e":[
        "users",
        "id",
        "name",
        "work",
        "email",
        "dob",
        "address",
        "city",
        "optedin",
        "images",
        "url",
        "coordinates",
        "price",
        "others",
        "premium",
        "bonus",
        "gender",
        "organization",
        "location",
        "population",
        "age",
        "priority",
        "is_admin",
        "books",
        "author",
        "page",
        "brand",
        "value",
        "easy"
    ],
    "a":[
        {
            "b":0,
            "c":"Adam Carter",
            "d":"Unilogic",
            "e":"adam.carter@unilogic.com",
            "f":"1978",
            "g":"83 Warner Street",
            "h":"Boston",
            "i":true
        },
        {
            "b":1,
            "c":"Leanne Brier",
            "d":"Connic",
            "e":"leanne.brier@connic.org",
            "f":"13/05/1987",
            "g":"9 Coleman Avenue",
            "h":"Toronto",
            "i":false
        }
    ],
    "j":[
        {
            "b":1,
            "c":"abc.png",
            "k":"/abc.png"
        },
        {
            "b":2,
            "c":"def.png",
            "k":"/def.png"
        },
        {
            "b":3,
            "c":"ghi.png",
            "k":"/ghi.png"
        }
    ],
    "l":{
        "x":35.12,
        "y":-21.49
    },
    "m":"$59,395",
    "n":[
        {
            "o":"good",
            "p":"satisfactory",
            "q":"male",
            "r":"abc ltd",
            "s":"bangladesh",
            "t":"160 million",
            "u":24,
            "v":"yes",
            "w":1
        },
        {
            "o":"bad",
            "p":"satisfactory",
            "q":"female",
            "r":"def ltd",
            "s":"bangladesh",
            "t":"160 million",
            "u":25,
            "v":"no",
            "w":0
        }
    ],
    "x":[
        {
            "y":"Mr X",
            "c":"Compact JSON",
            "z":1,
            "a1":"Socian Ltd",
            "b1":"yes",
            "c1":"yes"
        },
        {
            "y":"Mr Y",
            "c":"Compact JSON 2",
            "z":1,
            "a1":"Technolive",
            "b1":"yes",
            "c1":"yes"
        }
    ]
}
```

As a result, the JSON file gets compressed and data is reduced. Also, the server side response sending and receiving becomes less data consuming.

A parser corresponding to this architecture can be used to parse the CJSON.

The value of the "v_a_l_u_e" array will be replaced by the following characters:

## a, b, c, d, e, ... , y, z, a1, b1, c1, ... ,y1, z1, a2, b2, c2, ... ,y2, z2, ... ... ...
