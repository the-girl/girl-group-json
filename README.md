# girl group json

[json-server](https://github.com/typicode/json-server)

## 00 준비하기
```sh
$ npm install
```

## 01 실행하기
```sh
$ npm run serve
```

## 02 Routes

### Plural routes
```
GET /groups
GET /groups/1
GET /idols
GET /idols/1
```

### Singular routes
```
GET /profile
```

### Filter
```
GET /idols?name=나연
GET /idols?id=3&id=4
```

### Paginate
```
GET /idols?_page=2
GET /idols?_page=2&_limit=5
```

### Sort
```
GET /idols?_sort=height&_order=asc
GET /groups/2/idols?_sort=height&_order=asc
GET /idols?_sort=height,weight&_order=desc,asc
```

### Slice
```
GET /idols?_start=6&_end=12
GET /idols?_start=6&_limit=3
```

##### Operators
```
GET /idols?height_gte=160&height_lte=165
GET /idols?groupId_ne=1
GET /idols?birth_like=-03-
```

### Full-text search
```
GET /idols?q=999
```

### Relationships
```
GET /groups?_embed=idols
GET /groups/1?_embed=idols

GET /idols?_expand=group
GET /idols/2?_expand=group

GET /groups/2/idols
```

### Database
```
GET /db
```

### Homepage
```
GET /
```
