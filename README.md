# Overpass-turbo-queries

Just copy the query and paste in the Overpass-turbo query building tool to search for needed stuff.
[Overpass-turbo](https://overpass-turbo.eu/)

## Contencts

1. Hiking queries
    1. [Wilderness huts](#Wilderness-huts)

___

## Hiking queries

### Wilderness huts

![Example of wilderness hut](https://media.voog.com/0000/0030/9870/photos/Liipsaare%20metsaonn6.jpg)
![Example of wilderness hut](https://media.voog.com/0000/0030/9870/photos/Liipsaare%20metsaonn5.jpg)

#### Simple query

`
nwr["tourism"="wilderness_hut"]({{bbox}});
out center;  
`

#### Free wilderness huts

`
nwr["tourism"="wilderness_hut"]["fee"="no"]({{bbox}});
out center;
`
