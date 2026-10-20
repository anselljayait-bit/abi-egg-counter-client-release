# ABI Egg Counter Client

Aplikasi sinkronisasi data Egg Counter AI ke server ABI, berjalan otomatis setiap 120 detik.

## Persiapan

- Windows 64-bit dan koneksi internet.
- Credential perangkat dari admin ABI.
- Tidak perlu menginstal Node.js.

## Instalasi

1. Download paket Windows dari menu **Releases**, lalu ekstrak seluruh isinya.
2. Letakkan folder aplikasi sejajar dengan folder `excel`:

   ```text
   releaseB/
   ├── excel/
   │   └── day.csv
   └── abi-egg-counter-client/
       ├── abi-egg-counter-client.exe
       ├── init.cmd
       ├── set-credential.cmd
       └── install-task.cmd
   ```

3. Double-click **init.cmd** untuk membuat konfigurasi awal.
4. Double-click **set-credential.cmd**, lalu masukkan credential ABI.
5. Double-click **install-task.cmd**. Setujui UAC dan masukkan password akun Windows jika diminta, bukan PIN atau credential ABI.

Gunakan akun Windows yang sama untuk seluruh proses. Jangan memisahkan file `.exe` dari file pendampingnya.

## Setelah Instalasi

Aplikasi berjalan di background dan otomatis berjalan kembali setelah PC menyala.

- Status terakhir: `logs/status.json`
- Catatan aktivitas: folder `logs`
- Tanpa internet, data tetap mengantre dan akan dicoba kirim kembali.

## Menghentikan Auto-Start

Double-click **uninstall-task.cmd**.

**Penting:** Jangan membagikan credential atau menghapus data aplikasi di `%LOCALAPPDATA%\ABI\EggCounterSync`.
