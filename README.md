# Overpass-turbo-queries

Just copy the query and paste in the Overpass-turbo query building tool to search for needed stuff.
[Overpass-turbo](https://overpass-turbo.eu/)

## Contents

1. Hiking queries
    1. [Wilderness huts](#Wilderness-huts)
        1. [Wilderness huts](#Wilderness-huts)
        2. [Simple huts](#Simple-huts)

___

## Hiking queries

### Wilderness huts

Wilderness hut
![Example of wilderness hut](https://media.voog.com/0000/0030/9870/photos/Liipsaare%20metsaonn6.jpg)
![Example of wilderness hut](https://media.voog.com/0000/0030/9870/photos/Liipsaare%20metsaonn5.jpg)

#### Simple query

```Overpass QL
nwr["tourism"="wilderness_hut"]({{bbox}});
out center;
```

#### Free wilderness huts

```Overpass QL
nwr["tourism"="wilderness_hut"]["fee"="no"]({{bbox}});
out center;
```

[Back up](#Contents)

### Simple huts

Simple hut
![Example of simple hut](https://media.voog.com/0000/0030/9870/photos/Kautsi%20metsaonn-7.jpg)
![Example of simple hut](https://media.voog.com/0000/0030/9870/photos/Kautsi%20metsaonn-8.jpg)

```Overpass QL
nwr["amenity"="shelter"]["shelter_type"="basic_hut"]({{bbox}});
out center;
```

Free simple huts

```Overpass QL
nwr["amenity"="shelter"]["shelter_type"="basic_hut"]["fee"="no"]({{bbox}});
out center;
```

[Back up](#Contents)
