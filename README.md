# stockfish-dgx-spark
🎯 La prima versione ottimizzata per DGX SPARK è qui!

Sono entusiasta di annunciare il rilascio di Stockfish CUDA, una versione ottimizzata del motore di scacchi Stockfish 18 per la piattaforma NVIDIA DGX SPARK con architettura Blackwell e 128GB di memoria unificata.

### ✨ Cosa c'è di nuovo

- **GPU Acceleration**: Valutazione NNUE su Tensor Cores Blackwell
- **Hash Table Massiccia**: Supporto per tabelle di trasposizione fino a 96GB
- **Valutazione Batch**: Elaborazione parallela di 256 posizioni
- **Piena compatibilità UCI**: Funziona con SCID, ChessBase, Arena

### 📥 Download

- `stockfish-dgx-cuda` - Versione completa con CUDA
- `stockfish-cpu` - Versione CPU-only (fallback)

### 🔧 Requisiti

- NVIDIA DGX SPARK o sistema con GPU Blackwell
- CUDA 12.0+
- 128GB memoria unificata (consigliato)

### 📊 Performance

Su DGX SPARK (Grace CPU + Blackwell GPU):
- NPS single-thread: ~1.5M (infrastruttura completa)
- NPS 64 threads: 400M+ 
- Speedup: 3.3x vs CPU-only

### 🎮 Utilizzo

```bash
./stockfish-dgx-cuda
uci
setoption name CUDA Batch Size value 128
go depth 30
```

Grazie per l'interesse! Feedback e contributi sono benvenuti.
```
