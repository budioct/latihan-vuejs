# Latihan Dengan Vue Js
## App Kulineran

### Setup Project
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

## Running DB with JSON Server
### Getting started
```
npm install -g json-server
```

### Create a db.json file with some data
```
{
  "best-products": [
    {
      "id": 1,
      "kode": "K-01",
      "nama": "Sate Ayam",
      "harga": 16000,
      "is_ready": true,
      "gambar": "sate-ayam.jpg"
    }
    ],
  "keranjangs": [],
  "pesanans": []
}
```

### files db.json exiest on directory db-app-kulineran
```
db.json
```

### running JSON SERVER
```
json-server --watch db.json
```

### Now if you go to http://localhost:3000/best-products, you'll get
```
{
    id: 1,
    kode: "K-01",
    nama: "Sate Ayam",
    harga: 16000,
    is_ready: true,
    gambar: "sate-ayam.jpg"
}
```
