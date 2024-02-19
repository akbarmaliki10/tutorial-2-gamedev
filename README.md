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