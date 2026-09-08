# VirtusChat 💬

> **Vysoce výkonná, decentralizovaná a šifrovaná komunikační platforma postavená na nativní C++ architektuře s hardwarově akcelerovaným rozhraním DirectX 9.**

---

## 📌 O projektu

**VirtusChat** (v klientském rozhraní rovněž *VitusChat*) je komunikační platforma zaměřená na maximální soukromí, špičkový výkon a nulovou latenci.

Na rozdíl od běžných komunikačních nástrojů postavených na těžkých webových rámcích typu Electron přináší VirtusChat **nativní C++ řešení**, které maximálně šetří systémové prostředky, minimalizuje využití paměti RAM a poskytuje okamžitou odezvu i na méně výkonném hardwaru.

---

## ⚡ Architektura & Klíčové technické moduly

- **Nativní UDP Socket Wrapper:** Síťový modul postavený přímo na WinSock2 s implementací protokolů KCP a ENet pro rychlý a spolehlivý přenos dat bez zbytečné latence.
- **AudioEngine & WASAPI:** Nízkoúrovňový zvukový subsystém využívající WASAPI Exclusive mode a Waveform API s integrací kodeku Opus (48 kHz).
- **DirectX 9 Obsidian Engine:** Vlastní na míru navržené grafické jádro s hardware-akcelerovaným vykreslováním a retro DirectX 9 estetikou.
- **Media & ScreenCapture:** Integrovaný systém pro zachytávání obrazovky a distribuci multimédií postavený na knihovnách VLC SDK a FFmpeg.
- **Široká kompatibilita (MSVC v141_xp):** Cílená optimalizace umožňující nativní běh od Windows XP SP3 až po Windows 11.

---

## 🛡️ Bezpečnost & Kryptografické standardy

Bezpečnostní architektura aplikace staví na zásadách **Zero-Knowledge** a end-to-end šifrování (E2EE):

| Komponenta | Použitý standard / Protokol | Stav |
| :--- | :--- | :--- |
| **Šifrování zpráv i hlasu** | AES-GCM-256 + Curve25519 (mbedTLS) | ✔ Prověřeno |
| **Výměna klíčů** | Double Ratchet Protocol | ✔ Ověřeno |
| **Hashování hesel & dat** | Argon2id (klientské Zero-Knowledge hashování) | ✔ Aktivní |
| **Soukromí & Data** | Nulový sběr telemetrie a metadat | ✔ 100% Soukromé |

---

## 👥 Struktura týmu a organizace

Projekt a organizace stojí na provázané spolupráci specializovaných rolí a oddělení, které pokrývají celý životní cyklus vývoje a provozu:

### 👑 Vedení projektu (Project Leadership)
- **Strategické a koordinační řízení:** Směřování vize projektu, správa projektové roadmapy, prioritizace vývojových úkolů a řízení komunitních kanálů.
- **Bezpečnostní dohled & Architektura:** Kontrola kryptografických implementací, revize bezpečnosti zdrojového kódu, dohled nad stabilitou backendu a síťové infrastruktury.

### 💻 Vývojové oddělení (Core Engineering)
- **Klientský a grafický vývoj (C++ / DirectX):** Implementace klientského rozhraní, správa paměti a ladění nativního grafického jádra.
- **Síťové subsystémy & Protokoly:** Tvorba a optimalizace UDP vrstvy, správa soketů, synchronizace stavů a eliminace latence.
- **Multimédia a audio:** Správa kódování hlasového přenosu (Opus), integrace nízkoúrovňového audia a přenosu videa.

### 🧪 Zajištění kvality a testování (Quality Assurance)
- **Zátěžové testování & Penetrační zkoušky:** Prověřování odolnosti sítě a šifrovaných tunelů při vysokém zatížení.
- **Meziplatformní kompatibilita:** Důsledné testování na širokém spektru operačních systémů a konfigurací.

---

## 💾 Podporované platformy

- **Windows:** Nativní desktopová aplikace (.exe) – podpora Windows 7 / 8 / 10 / 11
- **Android:** Mobilní klient (.apk)
- **macOS / Linux / iOS:** Plánováno / ve fázi přípravy a vývoje
- **Webová platforma:** Připravováno

---

## 📜 Zásady & Ochrana soukromí

VirtusChat je vyvíjen s důrazem na absolutní ochranu soukromí uživatelů, otevřenost a technologickou preciznost.
