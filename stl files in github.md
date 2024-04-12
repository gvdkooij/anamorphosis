De meest simpele stl die je kan bedenken
Met slechts één face van drie vertices



```stl
solid 
  facet 
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
 endsolid
```

En nu met de normal krijgt hij een beetje glans
```stl
solid 
  facet normal 0 -1 0
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
 endsolid
```







Maar nu wordt het wat complexer, want hij moet natuurlijk wel vanaf allebei de kanten zichtbaar zijn.

```stl
solid 
  facet 
      vertex 0 0 0
       vertex 100 0 0
      vertex 0 0 100
    endfacet
  facet 
      vertex 0 0 0
      vertex 0 0 100
       vertex 100 0 0
    endfacet
 endsolid
```

Nu gaan we een lichaam opbouwen

1, Eerste vlak

```stl
solid 
  facet 
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
 endsolid
```

2. Tweede vlak

```stl
solid 
  facet 
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
  facet 
    vertex 0 0 0
    vertex 0 0 100
    vertex 0 100 0
  endfacet
 endsolid
```

3. Derde vlak

 ```stl
solid 
  facet 
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
  facet 
    vertex 0 0 0
    vertex 0 0 100
    vertex 0 100 0
  endfacet
    facet 
    vertex 0 0 0
    vertex 0 100 0
    vertex 100 0 0

  endfacet
 endsolid
```

En het vierde vlak

 ```stl
solid 
  facet 
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
  facet 
    vertex 0 0 0
    vertex 0 0 100
    vertex 0 100 0
  endfacet
    facet 
    vertex 0 0 0
    vertex 0 100 0
    vertex 100 0 0

  endfacet
    facet 
    vertex 0 0 100
     vertex 100 0 0
    vertex 0 100 0
  
  endfacet
 endsolid
```

En nu deze met normal

1, Eerste vlak

```stl
solid 
  facet normal 0 -1 0
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
 endsolid
```




2. Tweede vlak

```stl
solid 
  facet normal 0 -1 0
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
  facet normal -1 0 0
    vertex 0 0 0
    vertex 0 0 100
    vertex 0 100 0
  endfacet
 endsolid
```

3. Derde vlak

 ```stl
solid 
  facet normal 0 -1 0
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
  facet normal -1 0 0
    vertex 0 0 0
    vertex 0 0 100
    vertex 0 100 0
  endfacet
    facet normal 0 0 -1
    vertex 0 0 0
    vertex 0 100 0
    vertex 100 0 0

  endfacet
 endsolid
```

En het vierde vlak

 ```stl
solid 
  facet normal 0 -1 0
    vertex 0 0 0
    vertex 100 0 0
    vertex 0 0 100
  endfacet
  facet normal -1 0 0
    vertex 0 0 0
    vertex 0 0 100
    vertex 0 100 0
  endfacet
    facet normal 0 0 -1
    vertex 0 0 0
    vertex 0 100 0
    vertex 100 0 0

  endfacet
    facet normal 1 1 1 
    vertex 0 0 100
     vertex 100 0 0
    vertex 0 100 0
  
  endfacet
 endsolid
```


