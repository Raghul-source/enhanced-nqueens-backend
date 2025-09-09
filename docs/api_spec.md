**# API Specification – Enhanced N-Queens Backend**



**Base URL: `/api/v1`**



---



**## 1. Create Board**

\*\*POST /boards\*\*



\### Request (JSON)

```json

{

&nbsp; "size": 8,

&nbsp; "mode": "predefined",

&nbsp; "regions": null

}

size → board dimension (N x N)



mode → "predefined" or "custom"



regions → optional mapping for custom boards



Response

json

Copy code

{

&nbsp; "board\_id": "abc123",

&nbsp; "size": 8,

&nbsp; "mode": "predefined"

}

**2. Get Board by ID**

GET /boards/{board\_id}



Response

json

Copy code

{

&nbsp; "board\_id": "abc123",

&nbsp; "size": 8,

&nbsp; "regions": {

&nbsp;   "color1": \[\[0,0],\[0,1]],

&nbsp;   "color2": \[\[1,0],\[1,1]]

&nbsp; }

}

**3. Solve Board**

POST /boards/{board\_id}/solve



Response

json

Copy code

{

&nbsp; "board\_id": "abc123",

&nbsp; "solutions": \[

&nbsp;   \[\[0,4],\[1,2],\[2,0],\[3,6],\[4,1],\[5,7],\[6,5],\[7,3]],

&nbsp;   \[\[0,3],\[1,1],\[2,6],\[3,2],\[4,7],\[5,5],\[6,0],\[7,4]]

&nbsp; ]

}

**4. Fetch Solutions by Board ID**

GET /boards/{board\_id}/solutions



Response

json

Copy code

{

&nbsp; "board\_id": "abc123",

&nbsp; "solutions": \[

&nbsp;   \[\[0,4],\[1,2],\[2,0],\[3,6],\[4,1],\[5,7],\[6,5],\[7,3]]

&nbsp; ]

}

**5. Error Handling**

400 Bad Request → invalid input



404 Not Found → board\_id not found



500 Internal Server Error → unexpected server error

