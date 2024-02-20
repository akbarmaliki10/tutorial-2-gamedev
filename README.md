# Jawaban Latihan
## Playtest
- Apa saja pesan log yang dicetak pada panel Output?
```
--- Debugging process started ---
Godot Engine v3.5.3.stable.official.6c814135b - https://godotengine.org
OpenGL ES 3.0 Renderer: NVIDIA GeForce RTX 3060/PCIe/SSE2
Async. shader compilation: OFF
 
Platform initialized
--- Debugging process stopped ---
```
- Coba gerakkan landasan ke batas area bawah, lalu gerakkan kembali ke atas hingga hampir menyentuh batas atas. Apa saja pesan log yang dicetak pada panel Output?
```
--- Debugging process started ---
Godot Engine v3.5.3.stable.official.6c814135b - https://godotengine.org
OpenGL ES 3.0 Renderer: NVIDIA GeForce RTX 3060/PCIe/SSE2
Async. shader compilation: OFF
 
Platform initialized
Reached objective!
Reached objective!
--- Debugging process stopped ---
```
- Buka scene MainLevel dengan tampilan workspace 2D. Apakah lokasi scene ObjectiveArea memiliki kaitan dengan pesan log yang dicetak pada panel Output pada percobaan sebelumnya?
```
Lokasi scene ObjectiveArea tentu saja memiliki kaitan dengan pesan log yang dicetak pada panel output. Ketika node BlueShip mengenai/entered ObjectiveArea yang didefinisikan dengan fungsi "_on_ObjectiveArea_body_entered" maka akan tercetak ReachedObjective pada panel output
```
## Memanipulasi Node dan Scene
- Scene BlueShip dan StonePlatform sama-sama memiliki sebuah child node bertipe Sprite. Apa fungsi dari node bertipe Sprite?
```
Fungsi node bertipe sprite adalah memunculkan texture 2D, tekstur yang ditampilkan dapat berupa region dari tekstur atlas yang lebih besar atau sebuah frame yang terbuat dari sprite sheet animation(Sumber: godot docs).
```
- Root node dari scene BlueShip dan StonePlatform menggunakan tipe yang berbeda. BlueShip menggunakan tipe RigidBody2D, sedangkan StonePlatform menggunakan tipe StaticBody2D. Apa perbedaan dari masing-masing tipe node?
```
StaticBody2D merupakan sebuah body yang tidak seharusnya bergerak yang biasanya cocok untuk objek statis seperti tembok atau platform. Sedangkan RigidBody2D merupakan sebuah body yang mengimplementasikan/dikendalikan oleh 2D physics engine dimana kita tidak langsung mengontrol bodynya dengan tombol/etc tetapi kita mengaplikasikan hukum fisika terhadap body tersebut.
```
- Ubah nilai atribut Mass dan Weight pada tipe RigidBody2D secara bebas di scene BlueShip, lalu coba jalankan scene MainLevel. Apa yang terjadi?
```
Setelah saya coba mengubah atribut mass dan weight pada node BlueShip tidak terjadi apa-apa. Namun, ketika mengubah gravity scale maka body akan menjadi lebih cepat turun.
```
- Ubah nilai atribut Disabled pada tipe CollisionShape2D di scene StonePlatform, lalu coba jalankan scene MainLevel. Apa yang terjadi?
```
Yang terjadi adalah text "Reached Objective!" tidak pernah tercetak pada panel output ketika BlueShip masuk kedalam area objective karena fungsi body_entered akan mendeteksi node/objek yang memiliki collision shape masuk kedalam area mereka.
```
- Pada scene MainLevel, coba manipulasi atribut Position, Rotation, dan Scale milik node BlueShip secara bebas. Apa yang terjadi pada visualisasi BlueShip di Viewport?
```
Visualisasi BlueShip akan bergerak di sumbu x dan y, selain itu BlueShip akan berotasi sesuai dengan derajat yang kita mau.
```
- Pada scene MainLevel, perhatikan nilai atribut Position node PlatformBlue, StonePlatform, dan StonePlatform2. Mengapa nilai Position node StonePlatform dan StonePlatform2 tidak sesuai dengan posisinya di dalam scene (menurut Inspector) namun visualisasinya berada di posisi yang tepat?
```
Karena positionnya relative dengan node parentnya yaitu MainLevel.
```