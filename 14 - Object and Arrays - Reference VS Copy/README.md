# Object dan Arrays - Reference vs Copy

Perubahan data variable, array, dan Object sekaligus menyimpan data di variable.

## Pelajaran

1. ```string, number, boolean``` variable yg berasal dari var original(pertama) tidak akan berubah bila variable original diubah.
2. ```array``` variable array yg berasal dari var array original (pertama) akan tetap berubah bila var original diubah, jadi harus disimpan dulu seperti pke ```[...data]``` utk mendapatkan data yg tak berubah.
3. ```object``` variable object yg berasal dari var object original (pertama) akan tetap berubah bila var original diubah, jadi harus disimpan dulu.
4. untuk menyimpan data Object bisa pake ```object.assign({}, data)``` dan utk menambah data ditambah object dibelakang ```object.assign({}, data, {key: value, key: value ...})```. tapi sayangnya hanya satu level object yg bisa tersimpan (key value parent), data key child akan tetap berubah bila data Object original berubah.
5. mengakali untuk menyimpan data object lebih dari satu level bisa menggunakan ```JSON.parse(JSON.stringify(data))```, jadi key parent, child diakali dg merubah menjadi string dan dirubah kembali ke object. bisa juga dg menggunakan library lodash dg method ```.cloneDeep()```.