# Overpass-turbo-queries

Just copy the query and paste in the Overpass-turbo query building tool to search for needed stuff.
[Overpass-turbo](https://overpass-turbo.eu/)

## Contents

1. Hiking queries
    1. [Wilderness huts](#Wilderness-huts)
        1. [Wilderness huts](#Wilderness-huts)
        2. [Simple huts](#Simple-huts)
    2. [Lean-to's](#Lean-tos)
    3. [Tent sites](#Tent-sites)
    4. [Shower](#Shower)

___

## Hiking queries

### Wilderness huts

Wilderness hut: has fireplace or stove, free rent, fully closed (foor and walls).
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

Simple hut: no fireplace or stove, fully closed (roof and walls).
![Example of simple hut](https://media.voog.com/0000/0030/9870/photos/Kautsi%20metsaonn-7.jpg)
![Example of simple hut](https://media.voog.com/0000/0030/9870/photos/Kautsi%20metsaonn-8.jpg)

Simple query

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

___

### Lean-to's

Lean-to: not fully closed, at least one wall open.
![Example of lean-to](https://media.voog.com/0000/0030/9870/photos/Kurisoo%20l%C3%B5kkekoht.jpg)

Simple query

```Overpass QL
nwr["amenity"="shelter"]["shelter_type"="lean_to"]({{bbox}});
out center;
```

___

### Tent sites

Backcountry camp site: no facilities, may not have toilet, generally has fireplace and picnic table.
![Example of tent site](https://media.voog.com/0000/0030/9870/photos/J%C3%B5eharu%20TA.jpg)

Simple query

```Overpass QL
nwr["tourism"="camp_site"]({{bbox}});
out center;
```

Free tent site query

```Overpass QL
nwr["tourism"="camp_site"]["fee"="no"]({{bbox}});
out center;
```

Free tent site with toilet query

```Overpass QL
nwr["tourism"="camp_site"]["fee"="no"]["toilets"="yes"]({{bbox}});
out center;
```

Free tent site with toilet and shower query - those are rarity usually in a lot of places...

```Overpass QL
nwr["tourism"="camp_site"]["fee"="no"]["toilets"="yes"]["shower"="yes"]({{bbox}});
out center;
```

[Back up](#Contents)

___

### Shower

Shower: may be paid with hot water and may be simple rinse shower at the beach without hot water or possibility to properly wash.
![Shower symbol](https://upload.wikimedia.org/wikipedia/commons/e/e3/PL_road_sign_D-26d.svg)

Simple query

```Overpass QL
nwr["amenity"="shower"]({{bbox}});
out center;
```

Paid shower query

```Overpass QL
nwr["amenity"="shower"]["fee"="yes"]({{bbox}});
out center;
```

[Back up](#Contents)

___
