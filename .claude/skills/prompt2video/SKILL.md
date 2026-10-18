---
name: prompt2video
description: Tukar prompt teks kepada video. Guna bila pengguna minta buat video, reel, intro, explainer atau animasi dari idea/prompt.
---

# prompt2video

Workflow tukar prompt kepada video (MP4) menggunakan HTML + HyperFrames.

## Langkah

1. **Brief** - Dari prompt pengguna, tetapkan: tujuan, durasi (default 15s), nisbah (9:16 / 16:9 / 1:1), bahasa, gaya visual. Tanya hanya jika benar-benar tidak jelas.
2. **Skrip & storyboard** - Pecahkan kepada babak (3-6), tiap satu: masa mula/tamat, teks atas skrin, visual, transisi. Simpan di `output/<nama>/storyboard.md`.
3. **Komposisi** - Tulis komposisi HTML/GSAP di `output/<nama>/index.html` mengikut storyboard.
4. **Preview & lint** - Guna skill `/hyperframes-cli` untuk lint dan preview; baiki ralat.
5. **Render** - Render ke `output/<nama>/video.mp4`.
6. **Serah** - Beritahu laluan fail, durasi dan resolusi.

## Prasyarat

```bash
npx skills add heygen-com/hyperframes
```

## Peraturan

- Satu folder per video di bawah `output/`.
- Jangan commit fail render besar (`*.mp4`) - ia dalam `.gitignore`.
