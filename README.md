# LoversLabTest
Minimal working example to test LoversLab semi-automated downloads (via prompt window). For SSE v1.6.1170, no downgrade or CC content required.
* https://drive.google.com/file/d/15GRE1Y-uTAF4sYwpXyQO4y4NWUFf527n/view?usp=sharing

Includes:
* ### Some "sanity check" examples to make sure the process is working in principle:
  * SKSE
  * USSEP
  * MO plugin "sync plugins"
* ### Some stubborn mods hosted on LoversLab, where the download via prompt window fails repeatedly (but often works *eventually*):
  * Ostim Solutions - A Sexlab Solutions Revisited Port b5
    * https://www.loverslab.com/files/file/17441-ostim-solutions-a-sexlab-solutions-revisited-port/
    * the meta file:
      * ```
        [General]
        installed=true
        manualURL=https://www.loverslab.com/files/file/17441-ostim-solutions-a-sexlab-solutions-revisited-port/
        prompt=Please download "Sexlab_Solutions_Revisited_SE_-_Ostim_Beta_5.zip"
        ```
  * Heels Sound 1.5 SSE
    * https://www.loverslab.com/files/file/1795-heels-sound/
    * meta file:
      * ```
        [General]
        installed=true
        manualURL=https://www.loverslab.com/files/file/1795-heels-sound/
        prompt=Please download "Heels Sound 1.5 SSE.7z"
        ```

These links/downloads work fine directly from a browser. In the log, the failure always looks like this:
```
00:01:33.036 [INFO] (Wabbajack.Downloaders.Manual.ManualDownloader) Starting manual download of https://www.loverslab.com/files/file/1795-heels-sound/
00:01:37.957 [DEBUG] (Wabbajack.Networking.Http.ResumableDownloader) Download for 'Heels Sound 1.5 SSE.7z' is starting from 0...
00:01:38.060 [INFO] (Wabbajack.Downloaders.DownloadDispatcher) Finished downloading Heels Sound 1.5 SSE.7z. Hash: SzPhmGIXkog=; Size: 8.4KB/2.9MB
00:01:38.060 [WARN] (Wabbajack.Downloaders.DownloadDispatcher) Initial download of Heels Sound 1.5 SSE.7z failed, trying mirror
00:01:38.060 [INFO] (Wabbajack.Downloaders.DownloadDispatcher) Downloading Heels Sound 1.5 SSE.7z from mirror, hash NfeHXl03zEg=
00:01:38.060 [INFO] (Wabbajack.Downloaders.WabbajackCDNDownloader) Getting file definition for CDN download WabbajackCDNDownloader+State|https://mirror.wabbajack.org/35f7875e5d37cc48
00:03:08.305 [INFO] (Wabbajack.Downloaders.DownloadDispatcher) Finished downloading Heels Sound 1.5 SSE.7z. Hash: AAAAAAAAAAA=; Size: 8.4KB/2.9MB
00:03:08.305 [ERROR] (Wabbajack.Installer.StandardInstaller) Downloaded hash AAAAAAAAAAA= does not match expected hash: NfeHXl03zEg=
```
