# Chapter 4: State

## GitHub Pages
Link hasil deployment: [React State](https://fatahpratam.github.io/tutorial-react-state/)

## Youtube Tutorial
- Link: [Full Stack React Developer Course with Appwrite](https://www.youtube.com/watch?v=Bvwq_S0n2pk)
- Creator: [HiteshCodeLab](https://www.youtube.com/@HiteshCodeLab)

## Mempelajari lebih lanjut tentang jsx
- Variable Injection -> Caranya dengan membuat kurung kurawal {}

- Dapat menambah event listener langsung di jsx seperti HTML biasa.

## Apa itu state
- Objek React bawaan yang digunakan untuk menampung data atau informasi tentang komponen.
- State dari suatu komponen dapat berubah seiring waktu dan ketika nilai state berubah, maka komponen akan dirender ulang.

## Cara menggunakan state
- Panggil method useState dengan nilai yang ingin di simpan.
- Destructure array yang dikembalikan oleh useState dengan pola ['Nama variabel', 'Nama fungsi pengubah' ];
- Untuk mendapatkan nilai variabel cukup memanggil 'Nama variabel'.
- Untuk mengubah nilai variabel cukup memanggil 'Nama fungsi pengubah'.

## Batching
- Strategi pengelompokan beberapa pembaruan state sebelum memicu render ulang komponen.
- Optimalisasi ini sangat penting karena setiap render ulang dapat menjadi mahal secara komputasi, terutama pada komponen yang kompleks dengan pohon DOM virtual yang besar.
- Karena batching, salah satu setCounter aja yang akan dijalankan:
const [counter, setCounter] = useState(15);
setCounter(counter + 1);
setCounter(counter + 1);

- Untuk mengatasinya, gunakanlah callback:
setCounter(prevCounter => prevCounter + 1);
setCounter(prevCounter => prevCounter + 1);
