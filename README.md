# BsaHw3

## Flights: 

```

GET: /api/flights/

GET: /api/flights/:id

DELETE: /api/flights/:id

POST: /api/flights/
BODY: {
  number: string,
  destinationTime: string,
  destination: string,
  depatureTime: string,
  depature: string
}

PUT: /api/flights/:id
BODY: {
  destinationTime: string,
  destination: string,
  depatureTime: string,
  depature: string
}

```

## Tickets:

```

GET: /api/tickets/
GET: /api/tickets/:id
DELETE: /api/tickets/:id

POST: /api/tickets/
BODY: {
  flightid: number,
  price: number
}

PUT: /api/tickets/:id
BODY: {
  flightid: number
  price: number
}

GET: /api/tickets?flightid=:flightid

```

## Departure

```
GET: /api/depatures/
GET: /api/depatures/:id
DELETE: /api/depatures/:id

POST: /api/depatures/
BODY: {
  flightid: number,
  date: string,
  crewid: number,
  planeid: number
}

PUT: /api/depatures/:id
BODY: {
  flightid: number,
  date: string,
  crewid: number,
  planeid: number
}

GET: /api/depatures?flightid=:flightid
GET: /api/depatures?flightid=:crewid
GET: /api/depatures?flightid=:planeid

```

## AirHostesses

```
GET: /api/airhostesses/
GET: /api/airhostesses/:id
DELETE: /api/airhostesses/:id

POST: /api/airhostesses/
BODY: {
  id: number,
  firstname: string,
  lastname: string,
  birthdate: string
}

PUT: /api/airhostesses/:id
BODY: {
  firstname: string,
  lastname: string,
  birthdate: string
}

GET: /api/arhostesses/:id/crews
```

## Pilots

```
GET: /api/pilot/
GET: /api/pilot/:id
DELETE: /api/pilot/:id

POST: /api/pilot/
BODY: {
  firstname: string,
  lastname: string,
  birthdate: string,
  experience: number
}

PUT: /api/pilot/:id
BODY: {
  firstname: string,
  lastname: string,
  birthdate: string,
  experience: number
}

GET: /api/pilots/:id/crews
```

## Crews

```
GET: /api/crews/
GET: /api/crews/:id
DELETE: /api/crews/:id

POST: /api/crew/
BODY: {
   pilotid: number,
   airhostesses: number[]
}

PUT: /api/crew/:id
BODY: {
  pilotid: number,
  airhostesids: number[]
}

GET: /api/crew?pilotid=:pilotid
GET: /api/crew?airhostesid=:airhostesid
```

## Planes

```
GET: /api/planes/
GET: /api/planes/:id
DELETE: /api/planes/:id

POST: /api/planes/
BODY: {
   name: string,
   planetypeid: number,
   manufactureddate: string,
   servicelife: number
}

PUT: /api/planes/:id
BODY: {
  name: string,
  planetypeid: number,
  manufactureddate: string,
  servicelife: number
}

GET: /api/planes?planetypeid=:planetypeid
```

## PlaneTypes

```
GET: /api/planetypes/
GET: /api/planetypes/:id
DELETE: /api/planetypes/:id

POST: /api/planetypes/
BODY: {
   model: string,
   capacity: number,
   carrying: number
}

PUT: /api/planetypes/:id
BODY: {
  model: string,
   capacity: number,
   carrying: number
}
```
