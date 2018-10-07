# Hướng dẫn cài đặt
# docker-overpass-api

# 1. Tải file dữ liệu osm dưới dạng nén bz2

```
curl -o planet.osm.bz2 https://download.geofabrik.de/asia/vietnam-latest.osm.bz2
```

# 2. Build

```
sudo docker build -t overpass-api.0.7.53 .
```

# 3. Run

```
docker run -d -p 8888:80 overpass-api.0.7.53
```

Đợi đến khi server start xong

Hiện thị server đang start
```
docker ls -all
```

# 4. Test
Dùng postman:<br/>
http://localhost:8888/api/interpreter<br/>
Method post<br/>
Data body dạng text:
```
[out:json][timeout:25];
(
  way["name"="Nguyễn Văn Linh"](16.026098131077337,108.17988395690917,16.099257728555084,108.27481269836426);
);
out body;
```

# Kết quả test:
{
  "version": 0.6,
  "generator": "Overpass API 0.7.55.4 3079d8ea",
  "osm3s": {
    "timestamp_osm_base": "2018-09-26T03:08:02Z",
    "copyright": "The data included in this document is from www.openstreetmap.org. The data is made available under ODbL."
  },
  "elements": [

{
  "type": "way",
  "id": 295128790,
  "nodes": [
    2988146945,
    2988146970,
    3514086537,
    2988146975,
    2988146980,
    2988146978,
    2988146977,
    2988146981,
    3068684710,
    4660405967,
    3068684711,
    3068684712,
    4660405966,
    2988146972,
    2623083098,
    2990909264,
    2988146962
  ],
  "tags": {
    "highway": "primary",
    "name": "Nguyễn Văn Linh",
    "oneway": "yes"
  }
},
{
  "type": "way",
  "id": 295128791,
  "nodes": [
    2988146956,
    4791168346,
    2988146967,
    4660405960,
    4660405961,
    4660405957,
    4660405964,
    4660405959,
    4660405963,
    4660405958,
    4660405962,
    2988146960,
    2988146953,
    4025302513,
    3070108202,
    2990909265,
    2988146958,
    3068684702,
    2988146949,
    3068684701,
    2988146988,
    3514086535
  ],
  "tags": {
    "highway": "primary",
    "name": "Nguyễn Văn Linh",
    "oneway": "yes"
  }
},
{
  "type": "way",
  "id": 295394151,
  "nodes": [
    2991011681,
    2991011685,
    3514073882,
    2991011695,
    2991011700,
    2991011702
  ],
  "tags": {
    "highway": "primary",
    "name": "Nguyễn Văn Linh",
    "oneway": "yes"
  }
},
{
  "type": "way",
  "id": 295394152,
  "nodes": [
    2991011708,
    2991011705,
    2991011698,
    2991011691,
    2991011689
  ],
  "tags": {
    "highway": "primary",
    "name": "Nguyễn Văn Linh",
    "oneway": "yes"
  }
},
{
  "type": "way",
  "id": 295449625,
  "nodes": [
    1333341472,
    2991819252,
    2991819251,
    2991819249,
    3071486516,
    3754565325,
    3754570967,
    1616276760,
    3754596962,
    1333333032,
    2991819236,
    3514033913,
    420248763,
    2991819233,
    2991816831,
    2991816830,
    2991816828,
    2991816823,
    3761464410,
    2991816820,
    2991816818,
    2991816817,
    2991816816
  ],
  "tags": {
    "highway": "primary",
    "name": "Nguyễn Văn Linh",
    "oneway": "yes"
  }
},
{
  "type": "way",
  "id": 295449627,
  "nodes": [
    2991816808,
    2991816811,
    1334198744,
    1334198766,
    2991816819,
    2991816821,
    2991816824,
    2991816826,
    2991816827,
    2991816829,
    3514033911,
    2991816832,
    3514033912,
    420249033,
    2991819237,
    3754596961,
    2991819238,
    3754570968,
    3514082735,
    1333362006,
    3514082737,
    2991819244,
    2991819245,
    2991819243,
    2991819242
  ],
  "tags": {
    "highway": "primary",
    "name": "Nguyễn Văn Linh",
    "oneway": "yes"
  }
}

  ]
}
