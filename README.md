# SM Drums — Deeply Sampled Free Drums (normalized mirror)

A normalized mirror of **SM Drums / Deeply Sampled Free Drums**, a free drum
sample library by Scott McLean (drums), Tod Stillwell and Suleiman Ali:
3,614 stereo samples from one acoustic kit, renamed to one convention and paired
with an Opus twin.

## Why this repository exists

This is a good-will mirror that makes the pack easy to fetch in one place and in
one naming scheme. It is **not the authors' repository**. The authors' own
download at <https://smmdrums.wordpress.com/> remains the canonical source.

## Licence

The authors publish **no licence document**. The upstream repository contains no
`LICENSE` file and no licence text accompanies the pack. This mirror does not
claim the pack is in the public domain and does not relicense it. The only grant
is this announcement:

> ALL of the content on this website is for FREE royalty free use by anyone for anything.

Source: <https://www.kvraudio.com/forum/viewtopic.php?p=6072198>

This mirror is made in reliance on that announcement and will be removed
immediately on request. See [NOTICE.md](NOTICE.md) for the full notice.

## Credits

- **Scott McLean** — drums; engineered and recorded all drum and cymbal samples.
- **Tod Stillwell** — edited the SMDrum samples; co-authored the Sforzando user guide.
- **Suleiman Ali** — created the SM Drums web site.
- **D. Smolken** — SFZ programming in Sforzando; co-authored the Sforzando user guide.

## Links

- Author's site: <https://smmdrums.wordpress.com/>
- Announcement: <https://www.kvraudio.com/forum/viewtopic.php?p=6072198>
- Upstream repository: <https://github.com/sfzinstruments/SMDrums>

## What is here

- **3,614 samples** in `source/`, all stereo 24-bit WAV at 44.1 kHz.
- **3,664,135,760 bytes (3.66 GB)** of source audio, copied byte-for-byte from upstream.
- **3,614 Opus twins** in `opus/`, 48 kHz, 160 kbit/s VBR, totalling **272,571,224 bytes (272.6 MB)**.
- `MAPPING.csv` — one row per sample with the original path, byte counts, duration and format.
- `NOTICE.md` — the licence position for this pack.

## Naming

Every file follows:

```
<pack>_<piece>_<articulation>_<perspective>_vl<NN>_rr<N>[_<take>].<codec>
```

- `pack` is `smdrums`.
- `piece` is the drum struck.
- `articulation` is how it was struck.
- `perspective` is `main`: the pack ships a single stereo perspective.
- `vl<NN>` is the source's dynamic layer, zero-padded, with `vl01` the softest.
- `rr<N>` is the source's round robin. `rr1` where the source has no round robin.

Pieces used in this pack: `kick1`, `snare1`, `snare2`, `snare3`, `snare4`, `snare5`, `tom1`, `tom2`, `tom3`, `tom4`, `hihat`, `crash1`, `crash2`, `crash3`, `crash4`, `china1`, `ride1`, `ride2`, `other`.

Articulations used in this pack: `hit`, `mute`, `rimshot`, `sidestick`, `tight`, `loose`, `open`, `footsplash`, `foot`, `half`, `closed`, `edge`, `bell`, `bow`.

## Mapping table

The full original → new table is below, and the same data with byte counts,
duration and format columns is in [`MAPPING.csv`](MAPPING.csv).

### Mapping notes

- **Snares.** The pack ships five snare instruments, each with its own key on
  the author's snare bus, so each gets its own piece:
  - the hybrid snares `Snare HyB 1/2/3` are `SNARE1KEY`/`SNARE2KEY`/`SNARE3KEY`
    and become `snare1`/`snare2`/`snare3`;
  - `Snare65` has its own keys (`SNR65RKEY` regular, `SNR65NRKEY` no-ring) and
    becomes `snare4` — regular as `hit`, no-ring as `mute`;
  - `Snare67` no-ring has its own key (`SNR67NRKEY`) and becomes `snare5`
    `mute`. It is **not** `snare2`: `SNR67NRKEY` and `SNARE2KEY` are different
    drums.

  `NR` (no ring) is mapped to `mute` throughout. The manual notes that HyB1/2/3
  sound very similar and are intended to be alternated; they remain separate
  pieces here because the author assigns them separate keys.
- **Rimshots and sidestick.** The hybrid's rimshot maps to `snare1` `rimshot`.
  The generic `RimShot_Stereo` and `SideStick_Stereo` sets are not tied to a
  numbered snare by the source, so they map to `other`.
- **Hi-hat.** `01 Hat Tight 1` → `tight`, `02 Hat, Loose` → `loose`,
  `03 Hat, Open` → `open`, `04 Hat, Foot, Open` → `footsplash`,
  `05 Hat, Foot` → `foot`, and `Hi-Hat Clsd#2` → `closed`. The
  `06 Hat,Closed-Open` set is a closed-to-open articulation; it maps to `half`
  because the closed list has no swell term and `open` is taken by `03`.
  `Hi-Hat Clsd#2` is present in the pack but is not referenced by any SFZ in it.
- **Rides.** The non-bell rides are named `…_Cnt_Tip` (centre, tip) in their leaf
  names, while the SFZ control labels call the corresponding key "Edge". They map
  to `bow`: the leaf names describe a centre/tip strike on the ride body, and
  `bow` is the closed-list term for that region, pairing with `bell`. The `L`/`R`
  in the leaf names is the physical cymbal, not a perspective or a take.
- **Crashes.** The leaf names say `edge`, which maps to `edge`; crash numbering is
  by ascending size (13, 15, 16, 17 inches).
- **Toms.** The source's own numbering is kept (`Tom1` → `tom1`), although the
  author's bus maps `Tom4` to the floor tom and `Tom1` to the hi tom.

<details>
<summary>Full original → new mapping (3,614 rows)</summary>

| new name | original path |
| --- | --- |
| `smdrums_china1_hit_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR1/01_China_RR1.wav` |
| `smdrums_china1_hit_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR2/01_China_RR2.wav` |
| `smdrums_china1_hit_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR3/01_China_RR3.wav` |
| `smdrums_china1_hit_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR4/01_China_RR4.wav` |
| `smdrums_china1_hit_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR1/02_China_RR1.wav` |
| `smdrums_china1_hit_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR2/02_China_RR2.wav` |
| `smdrums_china1_hit_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR3/02_China_RR3.wav` |
| `smdrums_china1_hit_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR4/02_China_RR4.wav` |
| `smdrums_china1_hit_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR1/03_China_RR1.wav` |
| `smdrums_china1_hit_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR2/03_China_RR2.wav` |
| `smdrums_china1_hit_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR3/03_China_RR3.wav` |
| `smdrums_china1_hit_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR4/03_China_RR4.wav` |
| `smdrums_china1_hit_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR1/04_China_RR1.wav` |
| `smdrums_china1_hit_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR2/04_China_RR2.wav` |
| `smdrums_china1_hit_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR3/04_China_RR3.wav` |
| `smdrums_china1_hit_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR4/04_China_RR4.wav` |
| `smdrums_china1_hit_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR1/05_China_RR1.wav` |
| `smdrums_china1_hit_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR2/05_China_RR2.wav` |
| `smdrums_china1_hit_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR3/05_China_RR3.wav` |
| `smdrums_china1_hit_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/China Cymbal (Samples)/RR4/05_China_RR4.wav` |
| `smdrums_crash1_edge_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/01_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/01_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/01_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/01_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/02_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/02_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/02_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/02_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/03_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/03_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/03_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/03_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/04_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/04_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/04_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/04_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/05_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/05_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/05_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/05_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/06_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/06_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/06_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/06_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/07_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/07_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/07_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/07_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/08_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/08_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/08_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/08_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/09_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/09_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/09_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/09_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/10_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/10_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/10_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/10_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/11_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/11_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/11_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/11_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/12_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/12_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/12_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/12_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/13_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/13_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/13_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/13_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/14_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/14_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/14_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/14_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/15_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/15_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/15_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/15_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/16_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/16_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/16_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/16_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/17_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/17_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/17_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/17_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/18_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/18_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/18_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/18_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/19_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/19_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/19_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/19_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/20_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/20_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/20_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/20_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/21_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/21_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/21_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/21_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash1_edge_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR1/22_Crash_13in_R_edge_RR1.wav` |
| `smdrums_crash1_edge_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR2/22_Crash_13in_R_edge_RR2.wav` |
| `smdrums_crash1_edge_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR3/22_Crash_13in_R_edge_RR3.wav` |
| `smdrums_crash1_edge_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 13 (Samples)/RR4/22_Crash_13in_R_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/01_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/01_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/01_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/01_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/02_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/02_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/02_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/02_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/03_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/03_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/03_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/03_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/04_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/04_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/04_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/04_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/05_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/05_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/05_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/05_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/06_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/06_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/06_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/06_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/07_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/07_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/07_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/07_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/08_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/08_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/08_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/08_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/09_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/09_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/09_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/09_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/10_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/10_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/10_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/10_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/11_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/11_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/11_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/11_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/12_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/12_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/12_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/12_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/13_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/13_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/13_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/13_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/14_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/14_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/14_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/14_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/15_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/15_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/15_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/15_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/16_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/16_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/16_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/16_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/17_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/17_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/17_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/17_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/18_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/18_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/18_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/18_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/19_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/19_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/19_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/19_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/20_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/20_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/20_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/20_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/21_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/21_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/21_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/21_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash2_edge_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR1/22_Crash_15in_L_edge_RR1.wav` |
| `smdrums_crash2_edge_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR2/22_Crash_15in_L_edge_RR2.wav` |
| `smdrums_crash2_edge_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR3/22_Crash_15in_L_edge_RR3.wav` |
| `smdrums_crash2_edge_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 15 (Samples)/RR4/22_Crash_15in_L_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/01_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/01_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/01_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/01_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/02_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/02_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/02_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/02_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/03_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/03_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/03_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/03_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/04_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/04_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/04_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/04_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/05_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/05_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/05_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/05_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/06_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/06_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/06_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/06_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/07_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/07_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/07_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/07_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/08_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/08_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/08_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/08_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/09_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/09_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/09_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/09_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/10_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/10_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/10_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/10_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/11_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/11_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/11_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/11_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/12_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/12_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/12_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/12_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/13_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/13_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/13_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/13_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/14_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/14_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/14_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/14_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/15_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/15_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/15_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/15_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/16_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/16_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/16_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/16_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/17_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/17_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/17_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/17_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/18_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/18_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/18_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/18_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/19_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/19_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/19_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/19_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/20_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/20_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/20_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/20_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/21_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/21_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/21_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/21_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash3_edge_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR1/22_Crash_16in_R_edge_RR1.wav` |
| `smdrums_crash3_edge_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR2/22_Crash_16in_R_edge_RR2.wav` |
| `smdrums_crash3_edge_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR3/22_Crash_16in_R_edge_RR3.wav` |
| `smdrums_crash3_edge_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 16 (Samples)/RR4/22_Crash_16in_R_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/01_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/01_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/01_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/01_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/02_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/02_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/02_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/02_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/03_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/03_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/03_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/03_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/04_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/04_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/04_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/04_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/05_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/05_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/05_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/05_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/06_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/06_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/06_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/06_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/07_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/07_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/07_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/07_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/08_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/08_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/08_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/08_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/09_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/09_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/09_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/09_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/10_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/10_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/10_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/10_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/11_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/11_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/11_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/11_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/12_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/12_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/12_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/12_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/13_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/13_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/13_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/13_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/14_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/14_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/14_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/14_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/15_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/15_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/15_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/15_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/16_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/16_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/16_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/16_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/17_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/17_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/17_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/17_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/18_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/18_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/18_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/18_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/19_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/19_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/19_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/19_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/20_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/20_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/20_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/20_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/21_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/21_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/21_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/21_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/22_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/22_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/22_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/22_Crash_17in_L_edge_RR4.wav` |
| `smdrums_crash4_edge_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR1/23_Crash_17in_L_edge_RR1.wav` |
| `smdrums_crash4_edge_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR2/23_Crash_17in_L_edge_RR2.wav` |
| `smdrums_crash4_edge_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR3/23_Crash_17in_L_edge_RR3.wav` |
| `smdrums_crash4_edge_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Crash (Samples)/Crash 17 (Samples)/RR4/23_Crash_17in_L_edge_RR4.wav` |
| `smdrums_hihat_closed_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/01_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/01_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/01_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/01_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/02_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/02_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/02_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/02_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/03_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/03_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/03_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/03_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/04_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/04_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/04_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/04_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/05_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/05_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/05_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/05_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/06_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/06_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/06_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/06_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/07_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/07_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/07_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/07_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/08_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/08_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/08_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/08_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/09_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/09_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/09_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/09_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/10_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/10_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/10_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/10_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/11_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/11_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/11_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/11_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/12_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/12_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/12_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/12_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/13_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/13_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/13_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/13_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/14_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/14_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/14_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/14_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/15_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/15_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/15_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/15_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/16_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/16_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/16_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/16_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/17_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/17_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/17_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/17_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/18_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/18_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/18_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/18_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/19_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/19_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/19_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/19_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/20_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/20_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/20_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/20_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/21_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/21_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/21_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/21_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/22_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/22_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/22_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/22_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/23_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/23_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/23_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/23_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl24_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/24_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl24_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/24_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl24_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/24_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl24_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/24_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl25_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/25_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl25_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/25_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl25_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/25_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl25_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/25_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl26_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/26_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl26_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/26_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl26_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/26_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl26_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/26_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl27_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/27_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl27_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/27_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl27_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/27_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl27_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/27_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl28_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/28_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl28_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/28_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl28_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/28_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl28_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/28_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl29_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/29_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl29_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/29_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl29_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/29_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl29_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/29_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl30_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/30_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl30_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/30_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl30_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/30_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl30_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/30_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl31_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/31_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl31_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/31_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl31_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/31_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl31_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/31_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl32_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/32_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl32_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/32_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl32_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/32_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl32_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/32_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl33_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/33_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl33_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/33_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl33_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/33_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl33_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/33_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl34_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/34_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl34_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/34_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl34_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/34_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl34_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/34_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl35_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/35_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl35_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/35_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl35_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/35_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl35_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/35_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl36_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/36_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl36_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/36_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl36_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/36_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl36_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/36_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl37_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/37_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl37_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/37_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl37_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/37_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl37_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/37_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl38_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/38_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl38_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/38_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl38_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/38_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl38_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/38_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl39_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/39_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl39_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/39_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl39_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/39_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl39_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/39_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl40_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/40_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl40_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/40_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl40_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/40_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl40_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/40_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl41_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/41_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl41_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/41_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl41_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/41_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl41_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/41_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl42_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/42_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl42_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/42_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl42_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/42_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl42_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/42_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl43_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/43_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl43_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/43_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl43_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/43_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl43_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/43_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl44_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/44_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl44_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/44_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl44_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/44_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl44_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/44_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl45_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/45_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl45_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/45_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl45_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/45_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl45_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/45_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl46_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/46_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl46_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/46_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl46_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/46_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl46_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/46_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl47_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/47_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl47_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/47_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl47_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/47_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl47_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/47_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl48_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/48_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl48_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/48_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl48_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/48_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl48_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/48_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl49_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/49_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl49_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/49_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl49_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/49_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl49_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/49_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl50_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/50_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl50_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/50_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl50_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/50_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl50_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/50_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl51_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/51_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl51_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/51_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl51_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/51_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl51_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/51_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl52_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/52_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl52_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/52_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl52_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/52_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl52_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/52_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl53_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/53_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl53_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/53_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl53_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/53_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl53_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/53_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl54_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/54_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl54_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/54_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl54_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/54_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl54_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/54_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl55_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/55_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl55_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/55_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl55_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/55_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl55_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/55_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl56_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/56_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl56_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/56_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl56_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/56_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl56_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/56_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl57_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/57_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl57_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/57_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl57_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/57_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl57_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/57_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl58_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/58_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl58_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/58_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl58_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/58_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl58_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/58_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl59_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/59_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl59_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/59_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl59_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/59_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl59_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/59_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl60_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/60_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl60_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/60_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl60_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/60_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl60_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/60_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl61_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/61_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl61_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/61_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl61_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/61_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl61_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/61_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl62_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/62_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl62_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/62_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl62_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/62_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl62_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/62_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl63_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/63_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl63_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/63_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl63_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/63_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl63_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/63_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_closed_main_vl64_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR1/64_Hat_Clsd#2__RR1.wav` |
| `smdrums_hihat_closed_main_vl64_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR2/64_Hat_Clsd#2__RR2.wav` |
| `smdrums_hihat_closed_main_vl64_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR3/64_Hat_Clsd#2__RR3.wav` |
| `smdrums_hihat_closed_main_vl64_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat Clsd#2 (Samples)/RR4/64_Hat_Clsd#2__RR4.wav` |
| `smdrums_hihat_foot_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/01_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/01_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/01_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/01_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl01_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/01_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl01_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/01_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl01_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/01_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl01_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/01_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/02_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/02_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/02_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/02_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl02_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/02_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl02_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/02_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl02_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/02_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl02_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/02_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/03_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/03_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/03_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/03_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl03_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/03_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl03_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/03_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl03_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/03_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl03_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/03_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/04_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/04_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/04_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/04_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl04_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/04_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl04_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/04_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl04_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/04_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl04_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/04_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/05_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/05_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/05_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/05_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl05_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/05_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl05_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/05_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl05_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/05_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl05_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/05_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/06_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/06_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/06_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/06_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl06_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/06_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl06_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/06_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl06_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/06_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl06_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/06_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/07_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/07_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/07_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/07_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl07_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/07_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl07_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/07_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl07_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/07_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl07_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/07_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/08_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/08_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/08_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/08_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl08_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/08_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl08_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/08_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl08_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/08_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl08_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/08_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/09_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/09_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/09_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/09_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl09_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/09_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl09_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/09_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl09_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/09_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl09_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/09_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/10_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/10_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/10_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/10_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl10_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/10_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl10_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/10_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl10_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/10_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl10_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/10_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/11_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/11_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/11_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/11_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl11_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/11_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl11_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/11_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl11_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/11_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl11_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/11_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/12_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/12_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/12_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/12_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl12_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/12_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl12_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/12_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl12_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/12_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl12_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/12_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/13_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/13_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/13_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/13_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl13_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/13_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl13_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/13_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl13_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/13_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl13_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/13_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/14_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/14_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/14_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/14_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl14_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/14_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl14_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/14_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl14_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/14_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl14_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/14_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/15_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/15_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/15_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/15_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl15_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/15_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl15_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/15_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl15_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/15_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl15_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/15_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/16_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/16_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/16_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/16_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl16_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/16_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl16_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/16_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl16_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/16_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl16_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/16_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/17_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/17_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/17_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/17_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl17_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/17_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl17_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/17_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl17_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/17_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl17_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/17_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/18_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/18_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/18_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/18_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl18_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/18_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl18_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/18_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl18_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/18_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl18_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/18_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/19_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/19_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/19_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/19_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl19_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/19_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl19_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/19_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl19_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/19_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl19_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/19_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/20_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/20_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/20_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/20_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl20_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/20_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl20_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/20_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl20_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/20_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl20_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/20_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/21_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/21_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/21_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/21_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl21_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/21_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl21_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/21_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl21_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/21_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl21_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/21_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/22_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/22_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/22_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/22_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl22_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/22_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl22_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/22_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl22_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/22_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl22_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/22_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/23_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/23_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/23_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/23_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl23_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/23_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl23_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/23_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl23_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/23_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl23_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/23_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl24_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/24_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl24_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/24_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl24_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/24_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl24_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/24_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl24_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/24_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl24_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/24_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl24_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/24_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl24_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/24_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl25_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/25_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl25_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/25_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl25_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/25_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl25_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/25_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl25_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/25_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl25_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/25_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl25_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/25_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl25_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/25_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl26_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/26_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl26_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/26_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl26_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/26_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl26_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/26_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl26_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/26_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl26_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/26_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl26_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/26_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl26_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/26_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl27_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/27_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl27_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/27_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl27_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/27_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl27_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/27_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl27_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/27_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl27_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/27_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl27_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/27_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl27_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/27_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl28_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/28_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl28_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/28_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl28_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/28_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl28_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/28_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl28_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/28_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl28_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/28_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl28_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/28_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl28_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/28_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl29_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/29_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl29_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/29_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl29_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/29_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl29_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/29_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl29_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/29_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl29_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/29_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl29_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/29_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl29_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/29_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl30_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/30_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl30_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/30_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl30_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/30_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl30_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/30_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl30_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/30_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl30_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/30_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl30_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/30_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl30_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/30_Hat_Foot_RR8.wav` |
| `smdrums_hihat_foot_main_vl31_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR1/31_Hat_Foot_RR1.wav` |
| `smdrums_hihat_foot_main_vl31_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR2/31_Hat_Foot_RR2.wav` |
| `smdrums_hihat_foot_main_vl31_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR3/31_Hat_Foot_RR3.wav` |
| `smdrums_hihat_foot_main_vl31_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR4/31_Hat_Foot_RR4.wav` |
| `smdrums_hihat_foot_main_vl31_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR5/31_Hat_Foot_RR5.wav` |
| `smdrums_hihat_foot_main_vl31_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR6/31_Hat_Foot_RR6.wav` |
| `smdrums_hihat_foot_main_vl31_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR7/31_Hat_Foot_RR7.wav` |
| `smdrums_hihat_foot_main_vl31_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/05 Hat, Foot/RR8/31_Hat_Foot_RR8.wav` |
| `smdrums_hihat_footsplash_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/01_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/01_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/01_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/01_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/02_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/02_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/02_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/02_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/03_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/03_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/03_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/03_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/04_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/04_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/04_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/04_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/05_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/05_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/05_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/05_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/06_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/06_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/06_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/06_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/07_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/07_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/07_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/07_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/08_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/08_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/08_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/08_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/09_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/09_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/09_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/09_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/10_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/10_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/10_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/10_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/11_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/11_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/11_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/11_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/12_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/12_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/12_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/12_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/13_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/13_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/13_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/13_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_footsplash_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR1/14_Hat_Foot_Open_RR1.wav` |
| `smdrums_hihat_footsplash_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR2/14_Hat_Foot_Open_RR2.wav` |
| `smdrums_hihat_footsplash_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR3/14_Hat_Foot_Open_RR3.wav` |
| `smdrums_hihat_footsplash_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/04 Hat, Foot, Open/RR4/14_Hat_Foot_Open_RR4.wav` |
| `smdrums_hihat_half_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/01_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/01_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/01_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/01_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl01_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/01_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl01_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/01_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl01_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/01_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl01_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/01_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/02_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/02_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/02_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/02_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl02_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/02_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl02_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/02_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl02_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/02_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl02_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/02_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/03_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/03_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/03_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/03_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl03_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/03_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl03_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/03_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl03_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/03_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl03_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/03_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/04_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/04_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/04_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/04_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl04_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/04_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl04_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/04_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl04_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/04_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl04_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/04_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/05_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/05_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/05_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/05_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl05_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/05_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl05_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/05_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl05_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/05_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl05_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/05_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/06_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/06_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/06_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/06_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl06_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/06_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl06_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/06_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl06_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/06_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl06_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/06_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/07_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/07_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/07_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/07_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl07_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/07_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl07_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/07_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl07_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/07_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl07_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/07_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/08_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/08_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/08_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/08_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl08_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/08_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl08_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/08_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl08_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/08_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl08_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/08_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/09_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/09_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/09_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/09_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl09_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/09_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl09_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/09_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl09_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/09_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl09_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/09_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/10_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/10_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/10_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/10_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl10_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/10_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl10_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/10_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl10_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/10_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl10_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/10_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/11_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/11_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/11_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/11_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl11_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/11_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl11_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/11_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl11_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/11_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl11_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/11_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_half_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR1/12_Hat_Clsd_Opn_RR1.wav` |
| `smdrums_hihat_half_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR2/12_Hat_Clsd_Opn_RR2.wav` |
| `smdrums_hihat_half_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR3/12_Hat_Clsd_Opn_RR3.wav` |
| `smdrums_hihat_half_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR4/12_Hat_Clsd_Opn_RR4.wav` |
| `smdrums_hihat_half_main_vl12_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR5/12_Hat_Clsd_Opn_RR5.wav` |
| `smdrums_hihat_half_main_vl12_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR6/12_Hat_Clsd_Opn_RR6.wav` |
| `smdrums_hihat_half_main_vl12_rr7.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR7/12_Hat_Clsd_Opn_RR7.wav` |
| `smdrums_hihat_half_main_vl12_rr8.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/06 Hat,Closed-Open/RR8/12_Hat_Clsd_Opn_RR8.wav` |
| `smdrums_hihat_loose_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/01_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/01_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/01_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/01_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl01_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/01_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl01_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/01_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/02_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/02_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/02_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/02_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl02_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/02_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl02_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/02_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/03_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/03_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/03_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/03_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl03_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/03_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl03_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/03_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/04_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/04_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/04_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/04_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl04_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/04_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl04_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/04_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/05_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/05_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/05_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/05_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl05_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/05_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl05_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/05_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/06_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/06_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/06_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/06_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl06_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/06_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl06_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/06_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/07_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/07_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/07_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/07_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl07_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/07_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl07_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/07_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/08_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/08_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/08_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/08_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl08_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/08_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl08_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/08_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/09_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/09_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/09_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/09_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl09_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/09_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl09_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/09_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/10_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/10_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/10_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/10_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl10_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/10_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl10_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/10_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/11_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/11_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/11_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/11_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl11_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/11_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl11_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/11_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/12_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/12_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/12_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/12_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl12_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/12_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl12_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/12_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/13_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/13_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/13_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/13_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl13_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/13_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl13_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/13_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/14_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/14_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/14_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/14_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl14_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/14_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl14_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/14_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/15_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/15_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/15_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/15_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl15_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/15_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl15_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/15_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/16_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/16_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/16_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/16_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl16_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/16_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl16_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/16_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/17_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/17_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/17_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/17_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl17_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/17_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl17_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/17_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/18_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/18_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/18_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/18_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl18_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/18_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl18_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/18_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/19_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/19_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/19_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/19_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl19_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/19_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl19_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/19_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/20_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/20_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/20_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/20_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl20_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/20_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl20_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/20_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/21_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/21_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/21_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/21_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl21_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/21_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl21_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/21_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/22_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/22_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/22_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/22_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl22_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/22_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl22_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/22_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/23_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/23_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/23_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/23_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl23_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/23_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl23_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/23_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl24_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/24_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl24_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/24_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl24_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/24_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl24_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/24_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl24_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/24_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl24_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/24_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl25_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/25_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl25_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/25_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl25_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/25_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl25_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/25_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl25_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/25_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl25_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/25_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl26_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/26_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl26_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/26_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl26_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/26_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl26_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/26_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl26_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/26_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl26_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/26_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl27_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/27_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl27_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/27_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl27_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/27_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl27_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/27_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl27_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/27_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl27_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/27_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl28_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/28_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl28_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/28_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl28_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/28_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl28_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/28_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl28_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/28_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl28_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/28_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl29_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/29_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl29_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/29_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl29_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/29_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl29_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/29_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl29_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/29_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl29_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/29_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl30_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/30_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl30_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/30_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl30_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/30_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl30_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/30_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl30_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/30_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl30_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/30_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl31_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/31_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl31_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/31_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl31_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/31_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl31_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/31_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl31_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/31_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl31_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/31_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl32_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/32_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl32_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/32_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl32_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/32_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl32_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/32_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl32_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/32_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl32_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/32_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl33_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/33_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl33_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/33_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl33_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/33_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl33_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/33_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl33_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/33_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl33_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/33_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl34_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/34_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl34_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/34_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl34_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/34_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl34_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/34_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl34_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/34_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl34_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/34_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl35_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/35_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl35_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/35_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl35_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/35_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl35_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/35_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl35_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/35_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl35_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/35_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl36_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/36_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl36_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/36_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl36_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/36_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl36_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/36_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl36_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/36_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl36_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/36_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl37_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/37_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl37_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/37_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl37_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/37_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl37_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/37_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl37_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/37_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl37_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/37_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl38_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/38_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl38_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/38_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl38_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/38_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl38_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/38_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl38_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/38_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl38_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/38_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl39_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/39_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl39_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/39_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl39_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/39_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl39_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/39_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl39_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/39_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl39_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/39_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_loose_main_vl40_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR1/40_Hat_Loose_Cnt_RR1.wav` |
| `smdrums_hihat_loose_main_vl40_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR2/40_Hat_Loose_Cnt_RR2.wav` |
| `smdrums_hihat_loose_main_vl40_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR3/40_Hat_Loose_Cnt_RR3.wav` |
| `smdrums_hihat_loose_main_vl40_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR4/40_Hat_Loose_Cnt_RR4.wav` |
| `smdrums_hihat_loose_main_vl40_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR5/40_Hat_Loose_Cnt_RR5.wav` |
| `smdrums_hihat_loose_main_vl40_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/02 Hat, Loose/RR6/40_Hat_Loose_Cnt_RR6.wav` |
| `smdrums_hihat_open_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/01_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/01_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/01_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/01_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/02_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/02_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/02_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/02_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/03_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/03_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/03_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/03_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/04_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/04_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/04_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/04_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/05_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/05_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/05_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/05_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/06_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/06_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/06_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/06_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/07_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/07_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/07_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/07_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/08_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/08_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/08_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/08_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/09_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/09_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/09_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/09_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/10_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/10_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/10_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/10_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/11_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/11_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/11_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/11_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/12_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/12_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/12_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/12_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/13_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/13_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/13_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/13_Hat_Open_RR4.wav` |
| `smdrums_hihat_open_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR1/14_Hat_Open_RR1.wav` |
| `smdrums_hihat_open_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR2/14_Hat_Open_RR2.wav` |
| `smdrums_hihat_open_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR3/14_Hat_Open_RR3.wav` |
| `smdrums_hihat_open_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/03 Hat, Open/RR4/14_Hat_Open_RR4.wav` |
| `smdrums_hihat_tight_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/01_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/01_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/01_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/01_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl01_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/01_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl01_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/01_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/02_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/02_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/02_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/02_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl02_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/02_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl02_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/02_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/03_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/03_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/03_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/03_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl03_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/03_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl03_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/03_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/04_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/04_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/04_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/04_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl04_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/04_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl04_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/04_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/05_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/05_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/05_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/05_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl05_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/05_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl05_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/05_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/06_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/06_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/06_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/06_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl06_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/06_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl06_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/06_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/07_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/07_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/07_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/07_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl07_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/07_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl07_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/07_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/08_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/08_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/08_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/08_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl08_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/08_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl08_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/08_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/09_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/09_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/09_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/09_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl09_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/09_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl09_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/09_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/10_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/10_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/10_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/10_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl10_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/10_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl10_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/10_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/11_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/11_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/11_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/11_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl11_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/11_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl11_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/11_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/12_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/12_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/12_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/12_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl12_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/12_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl12_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/12_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/13_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/13_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/13_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/13_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl13_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/13_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl13_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/13_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/14_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/14_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/14_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/14_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl14_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/14_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl14_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/14_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/15_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/15_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/15_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/15_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl15_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/15_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl15_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/15_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/16_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/16_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/16_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/16_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl16_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/16_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl16_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/16_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/17_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/17_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/17_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/17_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl17_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/17_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl17_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/17_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/18_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/18_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/18_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/18_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl18_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/18_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl18_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/18_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/19_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/19_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/19_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/19_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl19_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/19_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl19_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/19_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/20_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/20_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/20_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/20_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl20_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/20_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl20_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/20_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/21_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/21_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/21_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/21_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl21_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/21_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl21_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/21_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/22_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/22_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/22_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/22_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl22_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/22_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl22_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/22_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/23_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/23_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/23_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/23_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl23_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/23_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl23_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/23_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl24_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/24_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl24_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/24_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl24_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/24_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl24_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/24_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl24_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/24_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl24_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/24_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl25_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/25_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl25_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/25_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl25_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/25_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl25_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/25_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl25_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/25_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl25_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/25_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl26_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/26_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl26_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/26_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl26_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/26_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl26_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/26_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl26_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/26_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl26_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/26_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl27_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/27_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl27_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/27_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl27_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/27_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl27_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/27_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl27_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/27_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl27_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/27_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl28_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/28_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl28_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/28_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl28_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/28_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl28_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/28_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl28_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/28_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl28_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/28_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl29_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/29_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl29_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/29_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl29_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/29_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl29_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/29_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl29_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/29_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl29_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/29_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl30_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/30_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl30_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/30_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl30_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/30_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl30_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/30_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl30_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/30_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl30_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/30_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl31_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/31_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl31_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/31_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl31_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/31_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl31_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/31_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl31_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/31_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl31_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/31_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl32_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/32_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl32_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/32_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl32_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/32_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl32_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/32_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl32_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/32_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl32_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/32_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl33_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/33_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl33_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/33_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl33_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/33_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl33_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/33_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl33_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/33_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl33_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/33_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl34_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/34_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl34_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/34_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl34_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/34_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl34_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/34_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl34_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/34_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl34_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/34_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl35_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/35_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl35_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/35_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl35_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/35_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl35_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/35_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl35_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/35_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl35_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/35_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl36_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/36_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl36_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/36_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl36_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/36_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl36_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/36_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl36_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/36_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl36_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/36_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl37_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/37_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl37_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/37_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl37_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/37_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl37_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/37_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl37_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/37_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl37_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/37_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl38_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/38_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl38_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/38_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl38_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/38_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl38_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/38_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl38_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/38_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl38_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/38_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl39_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/39_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl39_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/39_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl39_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/39_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl39_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/39_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl39_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/39_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl39_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/39_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl40_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/40_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl40_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/40_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl40_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/40_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl40_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/40_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl40_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/40_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl40_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/40_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl41_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/41_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl41_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/41_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl41_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/41_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl41_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/41_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl41_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/41_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl41_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/41_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl42_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/42_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl42_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/42_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl42_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/42_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl42_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/42_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl42_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/42_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl42_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/42_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl43_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/43_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl43_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/43_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl43_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/43_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl43_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/43_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl43_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/43_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl43_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/43_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl44_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/44_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl44_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/44_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl44_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/44_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl44_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/44_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl44_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/44_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl44_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/44_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl45_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/45_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl45_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/45_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl45_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/45_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl45_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/45_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl45_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/45_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl45_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/45_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl46_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/46_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl46_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/46_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl46_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/46_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl46_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/46_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl46_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/46_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl46_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/46_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl47_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/47_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl47_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/47_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl47_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/47_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl47_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/47_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl47_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/47_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl47_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/47_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl48_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/48_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl48_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/48_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl48_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/48_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl48_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/48_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl48_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/48_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl48_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/48_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_hihat_tight_main_vl49_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR1/49_Hat_Tight_Cnt_RR1.wav` |
| `smdrums_hihat_tight_main_vl49_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR2/49_Hat_Tight_Cnt_RR2.wav` |
| `smdrums_hihat_tight_main_vl49_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR3/49_Hat_Tight_Cnt_RR3.wav` |
| `smdrums_hihat_tight_main_vl49_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR4/49_Hat_Tight_Cnt_RR4.wav` |
| `smdrums_hihat_tight_main_vl49_rr5.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR5/49_Hat_Tight_Cnt_RR5.wav` |
| `smdrums_hihat_tight_main_vl49_rr6.wav` | `Samples/SMD Cymbals Stereo (Samples)/Hi-Hat (Samples)/01 Hat Tight 1/RR6/49_Hat_Tight_Cnt_RR6.wav` |
| `smdrums_kick1_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/01_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/01_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/01_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/01_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl01_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/01_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl01_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/01_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl01_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/01_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl01_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/01_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/02_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/02_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/02_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/02_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl02_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/02_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl02_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/02_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl02_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/02_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl02_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/02_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/03_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/03_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/03_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/03_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl03_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/03_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl03_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/03_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl03_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/03_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl03_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/03_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/04_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/04_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/04_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/04_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl04_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/04_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl04_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/04_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl04_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/04_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl04_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/04_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/05_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/05_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/05_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/05_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl05_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/05_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl05_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/05_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl05_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/05_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl05_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/05_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/06_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/06_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/06_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/06_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl06_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/06_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl06_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/06_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl06_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/06_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl06_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/06_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/07_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/07_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/07_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/07_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl07_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/07_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl07_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/07_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl07_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/07_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl07_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/07_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/08_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/08_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/08_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/08_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl08_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/08_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl08_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/08_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl08_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/08_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl08_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/08_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/09_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/09_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/09_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/09_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl09_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/09_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl09_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/09_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl09_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/09_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl09_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/09_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/10_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/10_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/10_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/10_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl10_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/10_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl10_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/10_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl10_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/10_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl10_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/10_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/11_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/11_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl11_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/11_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl11_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/11_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl11_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/11_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl11_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/11_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl11_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/11_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl11_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/11_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/12_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/12_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl12_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/12_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl12_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/12_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl12_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/12_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl12_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/12_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl12_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/12_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl12_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/12_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/13_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/13_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl13_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/13_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl13_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/13_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl13_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/13_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl13_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/13_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl13_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/13_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl13_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/13_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/14_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/14_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl14_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/14_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl14_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/14_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl14_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/14_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl14_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/14_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl14_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/14_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl14_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/14_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/15_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/15_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl15_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/15_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl15_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/15_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl15_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/15_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl15_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/15_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl15_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/15_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl15_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/15_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/16_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/16_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl16_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/16_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl16_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/16_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl16_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/16_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl16_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/16_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl16_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/16_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl16_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/16_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/17_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/17_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl17_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/17_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl17_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/17_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl17_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/17_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl17_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/17_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl17_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/17_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl17_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/17_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/18_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/18_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl18_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/18_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl18_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/18_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl18_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/18_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl18_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/18_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl18_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/18_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl18_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/18_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/19_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/19_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl19_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/19_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl19_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/19_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl19_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/19_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl19_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/19_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl19_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/19_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl19_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/19_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/20_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/20_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl20_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/20_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl20_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/20_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl20_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/20_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl20_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/20_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl20_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/20_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl20_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/20_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/21_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/21_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl21_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/21_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl21_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/21_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl21_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/21_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl21_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/21_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl21_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/21_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl21_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/21_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/22_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/22_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl22_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/22_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl22_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/22_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl22_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/22_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl22_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/22_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl22_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/22_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl22_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/22_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/23_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/23_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl23_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/23_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl23_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/23_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl23_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/23_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl23_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/23_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl23_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/23_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl23_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/23_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/24_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/24_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl24_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/24_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl24_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/24_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl24_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/24_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl24_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/24_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl24_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/24_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl24_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/24_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/25_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/25_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl25_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/25_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl25_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/25_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl25_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/25_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl25_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/25_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl25_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/25_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl25_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/25_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/26_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/26_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl26_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/26_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl26_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/26_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl26_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/26_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl26_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/26_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl26_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/26_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl26_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/26_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/27_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/27_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl27_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/27_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl27_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/27_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl27_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/27_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl27_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/27_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl27_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/27_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl27_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/27_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/28_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/28_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl28_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/28_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl28_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/28_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl28_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/28_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl28_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/28_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl28_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/28_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl28_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/28_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/29_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/29_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl29_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/29_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl29_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/29_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl29_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/29_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl29_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/29_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl29_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/29_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl29_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/29_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/30_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/30_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl30_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/30_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl30_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/30_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl30_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/30_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl30_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/30_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl30_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/30_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl30_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/30_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/31_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/31_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl31_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/31_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl31_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/31_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl31_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/31_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl31_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/31_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl31_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/31_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl31_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/31_Kik_Stereo_RR8.wav` |
| `smdrums_kick1_hit_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR1/32_Kik_Stereo_RR1.wav` |
| `smdrums_kick1_hit_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR2/32_Kik_Stereo_RR2.wav` |
| `smdrums_kick1_hit_main_vl32_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR3/32_Kik_Stereo_RR3.wav` |
| `smdrums_kick1_hit_main_vl32_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR4/32_Kik_Stereo_RR4.wav` |
| `smdrums_kick1_hit_main_vl32_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR5/32_Kik_Stereo_RR5.wav` |
| `smdrums_kick1_hit_main_vl32_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR6/32_Kik_Stereo_RR6.wav` |
| `smdrums_kick1_hit_main_vl32_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR7/32_Kik_Stereo_RR7.wav` |
| `smdrums_kick1_hit_main_vl32_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Kik_Stereo/RR8/32_Kik_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/01_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/01_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/01_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/01_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl01_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/01_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl01_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/01_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl01_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/01_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl01_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/01_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/02_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/02_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/02_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/02_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl02_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/02_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl02_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/02_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl02_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/02_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl02_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/02_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/03_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/03_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/03_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/03_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl03_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/03_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl03_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/03_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl03_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/03_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl03_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/03_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/04_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/04_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/04_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/04_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl04_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/04_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl04_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/04_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl04_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/04_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl04_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/04_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/05_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/05_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/05_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/05_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl05_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/05_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl05_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/05_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl05_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/05_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl05_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/05_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/06_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/06_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/06_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/06_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl06_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/06_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl06_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/06_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl06_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/06_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl06_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/06_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/07_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/07_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/07_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/07_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl07_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/07_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl07_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/07_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl07_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/07_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl07_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/07_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/08_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/08_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/08_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/08_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl08_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/08_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl08_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/08_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl08_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/08_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl08_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/08_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/09_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/09_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/09_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/09_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl09_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/09_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl09_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/09_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl09_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/09_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl09_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/09_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/10_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/10_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/10_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/10_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl10_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/10_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl10_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/10_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl10_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/10_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl10_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/10_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/11_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/11_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl11_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/11_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl11_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/11_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl11_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/11_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl11_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/11_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl11_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/11_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl11_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/11_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/12_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/12_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl12_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/12_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl12_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/12_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl12_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/12_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl12_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/12_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl12_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/12_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl12_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/12_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/13_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/13_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl13_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/13_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl13_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/13_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl13_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/13_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl13_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/13_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl13_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/13_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl13_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/13_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/14_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/14_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl14_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/14_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl14_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/14_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl14_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/14_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl14_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/14_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl14_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/14_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl14_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/14_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/15_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/15_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl15_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/15_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl15_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/15_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl15_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/15_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl15_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/15_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl15_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/15_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl15_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/15_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/16_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/16_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl16_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/16_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl16_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/16_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl16_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/16_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl16_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/16_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl16_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/16_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl16_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/16_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/17_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/17_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl17_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/17_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl17_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/17_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl17_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/17_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl17_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/17_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl17_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/17_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl17_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/17_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/18_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/18_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl18_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/18_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl18_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/18_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl18_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/18_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl18_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/18_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl18_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/18_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl18_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/18_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/19_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/19_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl19_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/19_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl19_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/19_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl19_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/19_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl19_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/19_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl19_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/19_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl19_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/19_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/20_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/20_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl20_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/20_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl20_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/20_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl20_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/20_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl20_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/20_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl20_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/20_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl20_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/20_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/21_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/21_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl21_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/21_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl21_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/21_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl21_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/21_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl21_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/21_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl21_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/21_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl21_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/21_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/22_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/22_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl22_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/22_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl22_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/22_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl22_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/22_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl22_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/22_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl22_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/22_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl22_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/22_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/23_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/23_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl23_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/23_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl23_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/23_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl23_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/23_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl23_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/23_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl23_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/23_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl23_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/23_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/24_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/24_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl24_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/24_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl24_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/24_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl24_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/24_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl24_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/24_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl24_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/24_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl24_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/24_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/25_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/25_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl25_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/25_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl25_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/25_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl25_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/25_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl25_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/25_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl25_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/25_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl25_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/25_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/26_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/26_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl26_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/26_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl26_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/26_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl26_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/26_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl26_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/26_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl26_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/26_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl26_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/26_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/27_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/27_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl27_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/27_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl27_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/27_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl27_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/27_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl27_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/27_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl27_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/27_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl27_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/27_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/28_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/28_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl28_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/28_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl28_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/28_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl28_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/28_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl28_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/28_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl28_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/28_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl28_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/28_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/29_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/29_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl29_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/29_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl29_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/29_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl29_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/29_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl29_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/29_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl29_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/29_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl29_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/29_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/30_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/30_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl30_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/30_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl30_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/30_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl30_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/30_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl30_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/30_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl30_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/30_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl30_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/30_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/31_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/31_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl31_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/31_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl31_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/31_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl31_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/31_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl31_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/31_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl31_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/31_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl31_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/31_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/32_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/32_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl32_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/32_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl32_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/32_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl32_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/32_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl32_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/32_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl32_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/32_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl32_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/32_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl33_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/33_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl33_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/33_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl33_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/33_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl33_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/33_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl33_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/33_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl33_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/33_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl33_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/33_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl33_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/33_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_hit_main_vl34_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR1/34_Snare65_Reg_Stereo_RR1.wav` |
| `smdrums_snare4_hit_main_vl34_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR2/34_Snare65_Reg_Stereo_RR2.wav` |
| `smdrums_snare4_hit_main_vl34_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR3/34_Snare65_Reg_Stereo_RR3.wav` |
| `smdrums_snare4_hit_main_vl34_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR4/34_Snare65_Reg_Stereo_RR4.wav` |
| `smdrums_snare4_hit_main_vl34_rr5.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR5/34_Snare65_Reg_Stereo_RR5.wav` |
| `smdrums_snare4_hit_main_vl34_rr6.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR6/34_Snare65_Reg_Stereo_RR6.wav` |
| `smdrums_snare4_hit_main_vl34_rr7.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR7/34_Snare65_Reg_Stereo_RR7.wav` |
| `smdrums_snare4_hit_main_vl34_rr8.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_Reg_Stereo/RR8/34_Snare65_Reg_Stereo_RR8.wav` |
| `smdrums_snare4_mute_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/01_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/01_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/02_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/02_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/03_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/03_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/04_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/04_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/05_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/05_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/06_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/06_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/07_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/07_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/08_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/08_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/09_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/09_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/10_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/10_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/11_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/11_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/12_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/12_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/13_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/13_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/14_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/14_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/15_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/15_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/16_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/16_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/17_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/17_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/18_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/18_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/19_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/19_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/20_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/20_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/21_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/21_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/22_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/22_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/23_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/23_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/24_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/24_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/25_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/25_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/26_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/26_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/27_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/27_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/28_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/28_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/29_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/29_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/30_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/30_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/31_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/31_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_snare4_mute_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR1/32_Snare65_NR_Stereo_RR1.wav` |
| `smdrums_snare4_mute_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare65_NR_Stereo/RR2/32_Snare65_NR_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/01_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/01_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/01_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/01_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/02_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/02_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/02_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/02_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/03_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/03_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/03_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/03_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/04_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/04_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/04_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/04_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/05_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/05_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/05_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/05_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/06_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/06_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/06_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/06_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/07_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/07_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/07_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/07_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/08_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/08_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/08_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/08_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/09_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/09_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/09_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/09_RimShot_Stereo_RR4.wav` |
| `smdrums_other_rimshot_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR1/10_RimShot_Stereo_RR1.wav` |
| `smdrums_other_rimshot_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR2/10_RimShot_Stereo_RR2.wav` |
| `smdrums_other_rimshot_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR3/10_RimShot_Stereo_RR3.wav` |
| `smdrums_other_rimshot_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/RimShot_Stereo/RR4/10_RimShot_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/01_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/01_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/01_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/01_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl01_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/01_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl01_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/01_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl01_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/01_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl01_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/01_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/02_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/02_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/02_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/02_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl02_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/02_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl02_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/02_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl02_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/02_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl02_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/02_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/03_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/03_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/03_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/03_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl03_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/03_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl03_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/03_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl03_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/03_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl03_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/03_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/04_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/04_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/04_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/04_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl04_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/04_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl04_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/04_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl04_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/04_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl04_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/04_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/05_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/05_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/05_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/05_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl05_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/05_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl05_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/05_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl05_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/05_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl05_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/05_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/06_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/06_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/06_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/06_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl06_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/06_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl06_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/06_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl06_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/06_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl06_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/06_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/07_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/07_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/07_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/07_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl07_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/07_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl07_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/07_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl07_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/07_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl07_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/07_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/08_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/08_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/08_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/08_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl08_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/08_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl08_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/08_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl08_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/08_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl08_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/08_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/09_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/09_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/09_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/09_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl09_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/09_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl09_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/09_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl09_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/09_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl09_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/09_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/10_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/10_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/10_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/10_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl10_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/10_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl10_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/10_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl10_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/10_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl10_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/10_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/11_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/11_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl11_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/11_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl11_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/11_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl11_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/11_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl11_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/11_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl11_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/11_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl11_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/11_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/12_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/12_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl12_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/12_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl12_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/12_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl12_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/12_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl12_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/12_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl12_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/12_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl12_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/12_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/13_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/13_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl13_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/13_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl13_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/13_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl13_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/13_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl13_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/13_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl13_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/13_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl13_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/13_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/14_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/14_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl14_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/14_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl14_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/14_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl14_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/14_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl14_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/14_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl14_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/14_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl14_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/14_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/15_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/15_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl15_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/15_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl15_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/15_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl15_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/15_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl15_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/15_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl15_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/15_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl15_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/15_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/16_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/16_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl16_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/16_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl16_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/16_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl16_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/16_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl16_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/16_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl16_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/16_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl16_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/16_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/17_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/17_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl17_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/17_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl17_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/17_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl17_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/17_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl17_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/17_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl17_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/17_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl17_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/17_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/18_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/18_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl18_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/18_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl18_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/18_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl18_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/18_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl18_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/18_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl18_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/18_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl18_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/18_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/19_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/19_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl19_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/19_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl19_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/19_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl19_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/19_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl19_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/19_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl19_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/19_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl19_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/19_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/20_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/20_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl20_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/20_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl20_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/20_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl20_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/20_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl20_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/20_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl20_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/20_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl20_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/20_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/21_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/21_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl21_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/21_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl21_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/21_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl21_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/21_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl21_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/21_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl21_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/21_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl21_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/21_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/22_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/22_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl22_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/22_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl22_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/22_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl22_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/22_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl22_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/22_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl22_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/22_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl22_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/22_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/23_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/23_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl23_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/23_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl23_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/23_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl23_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/23_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl23_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/23_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl23_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/23_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl23_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/23_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/24_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/24_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl24_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/24_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl24_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/24_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl24_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/24_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl24_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/24_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl24_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/24_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl24_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/24_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/25_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/25_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl25_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/25_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl25_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/25_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl25_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/25_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl25_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/25_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl25_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/25_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl25_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/25_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/26_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/26_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl26_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/26_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl26_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/26_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl26_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/26_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl26_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/26_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl26_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/26_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl26_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/26_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/27_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/27_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl27_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/27_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl27_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/27_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl27_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/27_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl27_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/27_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl27_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/27_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl27_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/27_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/28_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/28_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl28_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/28_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl28_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/28_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl28_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/28_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl28_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/28_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl28_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/28_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl28_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/28_SideStick_Stereo_RR8.wav` |
| `smdrums_other_sidestick_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR1/29_SideStick_Stereo_RR1.wav` |
| `smdrums_other_sidestick_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR2/29_SideStick_Stereo_RR2.wav` |
| `smdrums_other_sidestick_main_vl29_rr3.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR3/29_SideStick_Stereo_RR3.wav` |
| `smdrums_other_sidestick_main_vl29_rr4.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR4/29_SideStick_Stereo_RR4.wav` |
| `smdrums_other_sidestick_main_vl29_rr5.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR5/29_SideStick_Stereo_RR5.wav` |
| `smdrums_other_sidestick_main_vl29_rr6.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR6/29_SideStick_Stereo_RR6.wav` |
| `smdrums_other_sidestick_main_vl29_rr7.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR7/29_SideStick_Stereo_RR7.wav` |
| `smdrums_other_sidestick_main_vl29_rr8.wav` | `Samples/SMDrum Stereo (Samples)/SideStick_Stereo/RR8/29_SideStick_Stereo_RR8.wav` |
| `smdrums_ride1_bell_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/01_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/01_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/01_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/01_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/02_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/02_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/02_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/02_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/03_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/03_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/03_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/03_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/04_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/04_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/04_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/04_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/05_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/05_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/05_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/05_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/06_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/06_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/06_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/06_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/07_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/07_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/07_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/07_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/08_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/08_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/08_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/08_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/09_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/09_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/09_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/09_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/10_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/10_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/10_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/10_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/11_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/11_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/11_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/11_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/12_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/12_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/12_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/12_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/13_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/13_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/13_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/13_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/14_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/14_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/14_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/14_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/15_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/15_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/15_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/15_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/16_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/16_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/16_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/16_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/17_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/17_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/17_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/17_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/18_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/18_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/18_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/18_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/19_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/19_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/19_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/19_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/20_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/20_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/20_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/20_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/21_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/21_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/21_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/21_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/22_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/22_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/22_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/22_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/23_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/23_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/23_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/23_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bell_main_vl24_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR1/24_Ride_Bell_17in_L_Tip_RR1.wav` |
| `smdrums_ride1_bell_main_vl24_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR2/24_Ride_Bell_17in_L_Tip_RR2.wav` |
| `smdrums_ride1_bell_main_vl24_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR3/24_Ride_Bell_17in_L_Tip_RR3.wav` |
| `smdrums_ride1_bell_main_vl24_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 Bell (Samples)/RR4/24_Ride_Bell_17in_L_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/01_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/01_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/01_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/01_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/02_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/02_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/02_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/02_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/03_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/03_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/03_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/03_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/04_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/04_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/04_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/04_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/05_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/05_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/05_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/05_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/06_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/06_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/06_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/06_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/07_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/07_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/07_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/07_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/08_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/08_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/08_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/08_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/09_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/09_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/09_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/09_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/10_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/10_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/10_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/10_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/11_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/11_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/11_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/11_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/12_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/12_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/12_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/12_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/13_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/13_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/13_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/13_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/14_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/14_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/14_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/14_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/15_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/15_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/15_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/15_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/16_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/16_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/16_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/16_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/17_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/17_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/17_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/17_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/18_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/18_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/18_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/18_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/19_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/19_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/19_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/19_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/20_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/20_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/20_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/20_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/21_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/21_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/21_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/21_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/22_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/22_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/22_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/22_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/23_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/23_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/23_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/23_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl24_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/24_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl24_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/24_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl24_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/24_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl24_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/24_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride1_bow_main_vl25_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR1/25_Ride_17in_L_Cnt_Tip_RR1.wav` |
| `smdrums_ride1_bow_main_vl25_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR2/25_Ride_17in_L_Cnt_Tip_RR2.wav` |
| `smdrums_ride1_bow_main_vl25_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR3/25_Ride_17in_L_Cnt_Tip_RR3.wav` |
| `smdrums_ride1_bow_main_vl25_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 17 (Samples)/RR4/25_Ride_17in_L_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/01_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/01_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/01_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/01_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/02_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/02_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/02_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/02_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/03_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/03_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/03_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/03_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/04_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/04_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/04_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/04_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/05_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/05_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/05_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/05_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/06_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/06_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/06_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/06_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/07_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/07_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/07_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/07_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/08_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/08_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/08_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/08_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/09_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/09_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/09_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/09_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/10_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/10_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/10_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/10_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/11_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/11_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/11_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/11_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/12_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/12_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/12_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/12_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/13_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/13_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/13_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/13_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/14_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/14_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/14_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/14_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/15_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/15_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/15_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/15_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/16_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/16_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/16_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/16_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/17_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/17_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/17_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/17_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/18_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/18_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/18_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/18_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/19_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/19_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/19_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/19_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/20_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/20_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/20_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/20_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/21_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/21_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/21_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/21_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/22_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/22_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/22_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/22_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bell_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR1/23_Ride_Bell_20in_R_Tip_RR1.wav` |
| `smdrums_ride2_bell_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR2/23_Ride_Bell_20in_R_Tip_RR2.wav` |
| `smdrums_ride2_bell_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR3/23_Ride_Bell_20in_R_Tip_RR3.wav` |
| `smdrums_ride2_bell_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 Bell (Samples)/RR4/23_Ride_Bell_20in_R_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl01_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/01_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl01_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/01_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl01_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/01_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl01_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/01_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl02_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/02_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl02_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/02_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl02_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/02_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl02_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/02_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl03_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/03_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl03_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/03_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl03_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/03_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl03_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/03_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl04_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/04_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl04_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/04_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl04_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/04_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl04_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/04_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl05_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/05_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl05_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/05_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl05_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/05_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl05_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/05_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl06_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/06_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl06_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/06_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl06_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/06_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl06_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/06_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl07_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/07_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl07_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/07_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl07_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/07_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl07_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/07_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl08_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/08_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl08_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/08_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl08_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/08_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl08_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/08_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl09_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/09_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl09_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/09_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl09_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/09_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl09_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/09_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl10_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/10_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl10_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/10_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl10_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/10_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl10_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/10_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl11_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/11_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl11_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/11_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl11_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/11_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl11_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/11_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl12_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/12_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl12_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/12_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl12_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/12_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl12_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/12_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl13_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/13_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl13_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/13_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl13_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/13_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl13_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/13_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl14_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/14_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl14_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/14_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl14_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/14_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl14_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/14_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl15_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/15_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl15_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/15_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl15_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/15_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl15_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/15_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl16_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/16_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl16_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/16_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl16_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/16_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl16_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/16_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl17_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/17_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl17_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/17_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl17_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/17_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl17_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/17_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl18_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/18_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl18_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/18_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl18_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/18_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl18_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/18_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl19_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/19_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl19_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/19_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl19_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/19_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl19_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/19_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl20_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/20_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl20_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/20_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl20_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/20_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl20_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/20_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl21_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/21_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl21_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/21_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl21_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/21_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl21_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/21_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl22_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/22_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl22_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/22_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl22_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/22_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl22_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/22_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_ride2_bow_main_vl23_rr1.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR1/23_Ride_20in_R_Cnt_Tip_RR1.wav` |
| `smdrums_ride2_bow_main_vl23_rr2.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR2/23_Ride_20in_R_Cnt_Tip_RR2.wav` |
| `smdrums_ride2_bow_main_vl23_rr3.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR3/23_Ride_20in_R_Cnt_Tip_RR3.wav` |
| `smdrums_ride2_bow_main_vl23_rr4.wav` | `Samples/SMD Cymbals Stereo (Samples)/Ride (Samples)/Ride 20 (Samples)/RR4/23_Ride_20in_R_Cnt_Tip_RR4.wav` |
| `smdrums_snare1_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/01_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/01_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/02_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/02_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/03_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/03_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/04_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/04_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/05_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/05_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/06_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/06_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/07_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/07_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/08_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/08_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/09_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/09_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/10_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/10_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/11_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/11_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/12_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/12_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/13_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/13_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/14_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/14_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/15_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/15_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/16_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/16_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/17_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/17_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/18_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/18_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/19_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/19_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/20_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/20_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/21_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/21_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/22_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/22_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/23_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/23_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/24_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/24_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/25_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/25_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/26_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/26_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/27_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/27_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/28_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/28_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/29_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/29_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/30_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/30_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/31_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/31_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_hit_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR1/32_Snr65NR_Ster_HB_RR1.wav` |
| `smdrums_snare1_hit_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB1 (Samples)/RR2/32_Snr65NR_Ster_HB_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/01_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/01_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/02_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/02_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/03_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/03_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/04_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/04_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/05_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/05_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/06_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/06_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/07_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/07_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/08_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/08_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/09_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/09_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/10_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/10_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/11_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/11_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/12_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/12_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/13_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/13_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/14_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/14_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/15_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/15_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/16_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/16_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/17_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/17_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/18_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/18_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/19_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/19_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/20_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/20_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/21_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/21_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/22_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/22_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/23_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/23_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/24_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/24_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/25_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/25_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/26_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/26_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/27_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/27_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/28_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/28_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/29_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/29_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/30_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/30_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/31_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/31_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare1_rimshot_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR1/32_RimShot_Str_HyB1_RR1.wav` |
| `smdrums_snare1_rimshot_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD RimShot_Str_HyB1 (Samples)/RR2/32_RimShot_Str_HyB1_RR2.wav` |
| `smdrums_snare2_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/01_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/01_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/02_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/02_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/03_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/03_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/04_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/04_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/05_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/05_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/06_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/06_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/07_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/07_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/08_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/08_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/09_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/09_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/10_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/10_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/11_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/11_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/12_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/12_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/13_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/13_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/14_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/14_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/15_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/15_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/16_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/16_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/17_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/17_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/18_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/18_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/19_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/19_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/20_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/20_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/21_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/21_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/22_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/22_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/23_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/23_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/24_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/24_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/25_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/25_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/26_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/26_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/27_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/27_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/28_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/28_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/29_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/29_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/30_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/30_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/31_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/31_Snr_HyB2_RR2.wav` |
| `smdrums_snare2_hit_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR1/32_Snr_HyB2_RR1.wav` |
| `smdrums_snare2_hit_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB2 (Samples)/RR2/32_Snr_HyB2_RR2.wav` |
| `smdrums_snare5_mute_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/01_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/01_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/02_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/02_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/03_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/03_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/04_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/04_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/05_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/05_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/06_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/06_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/07_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/07_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/08_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/08_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/09_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/09_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/10_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/10_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/11_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/11_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/12_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/12_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/13_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/13_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/14_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/14_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/15_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/15_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/16_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/16_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/17_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/17_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/18_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/18_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/19_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/19_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/20_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/20_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/21_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/21_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/22_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/22_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/23_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/23_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/24_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/24_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/25_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/25_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/26_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/26_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/27_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/27_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/28_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/28_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/29_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/29_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/30_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/30_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/31_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/31_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare5_mute_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR1/32_Snare67_NR_Stereo_RR1.wav` |
| `smdrums_snare5_mute_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Snare67_NR_Stereo/RR2/32_Snare67_NR_Stereo_RR2.wav` |
| `smdrums_snare3_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/01_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/01_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/02_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/02_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/03_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/03_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/04_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/04_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/05_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/05_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/06_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/06_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/07_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/07_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/08_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/08_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/09_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/09_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/10_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/10_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/11_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/11_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/12_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/12_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/13_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/13_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/14_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/14_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/15_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/15_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/16_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/16_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/17_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/17_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/18_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/18_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/19_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/19_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/20_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/20_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/21_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/21_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/22_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/22_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/23_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/23_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/24_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/24_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/25_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/25_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/26_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/26_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/27_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/27_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/28_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/28_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/29_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/29_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/30_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/30_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl31_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/31_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl31_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/31_Snr_HyB3_RR2.wav` |
| `smdrums_snare3_hit_main_vl32_rr1.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR1/32_Snr_HyB3_RR1.wav` |
| `smdrums_snare3_hit_main_vl32_rr2.wav` | `Samples/SMDrum Stereo (Samples)/SMD_Snr_Str_HyB3 (Samples)/RR2/32_Snr_HyB3_RR2.wav` |
| `smdrums_tom1_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/01_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/01_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/01_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/01_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/02_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/02_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/02_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/02_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/03_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/03_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/03_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/03_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/04_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/04_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/04_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/04_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/05_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/05_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/05_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/05_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/06_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/06_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/06_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/06_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/07_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/07_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/07_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/07_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/08_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/08_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/08_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/08_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/09_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/09_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/09_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/09_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/10_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/10_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/10_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/10_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/11_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/11_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl11_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/11_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl11_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/11_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/12_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/12_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl12_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/12_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl12_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/12_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/13_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/13_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl13_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/13_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl13_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/13_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/14_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/14_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl14_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/14_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl14_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/14_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/15_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/15_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl15_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/15_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl15_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/15_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/16_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/16_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl16_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/16_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl16_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/16_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/17_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/17_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl17_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/17_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl17_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/17_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/18_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/18_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl18_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/18_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl18_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/18_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/19_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/19_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl19_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/19_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl19_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/19_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/20_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/20_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl20_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/20_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl20_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/20_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/21_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/21_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl21_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/21_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl21_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/21_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/22_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/22_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl22_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/22_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl22_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/22_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/23_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/23_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl23_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/23_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl23_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/23_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/24_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/24_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl24_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/24_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl24_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/24_Tom1_Stereo_RR4.wav` |
| `smdrums_tom1_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR1/25_Tom1_Stereo_RR1.wav` |
| `smdrums_tom1_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR2/25_Tom1_Stereo_RR2.wav` |
| `smdrums_tom1_hit_main_vl25_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR3/25_Tom1_Stereo_RR3.wav` |
| `smdrums_tom1_hit_main_vl25_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom1/RR4/25_Tom1_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/01_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/01_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/01_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/01_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/02_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/02_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/02_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/02_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/03_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/03_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/03_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/03_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/04_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/04_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/04_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/04_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/05_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/05_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/05_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/05_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/06_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/06_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/06_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/06_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/07_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/07_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/07_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/07_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/08_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/08_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/08_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/08_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/09_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/09_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/09_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/09_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/10_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/10_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/10_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/10_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/11_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/11_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl11_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/11_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl11_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/11_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/12_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/12_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl12_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/12_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl12_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/12_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/13_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/13_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl13_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/13_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl13_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/13_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/14_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/14_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl14_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/14_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl14_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/14_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/15_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/15_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl15_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/15_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl15_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/15_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/16_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/16_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl16_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/16_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl16_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/16_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/17_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/17_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl17_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/17_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl17_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/17_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/18_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/18_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl18_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/18_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl18_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/18_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/19_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/19_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl19_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/19_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl19_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/19_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/20_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/20_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl20_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/20_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl20_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/20_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/21_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/21_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl21_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/21_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl21_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/21_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/22_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/22_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl22_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/22_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl22_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/22_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/23_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/23_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl23_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/23_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl23_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/23_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/24_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/24_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl24_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/24_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl24_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/24_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/25_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/25_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl25_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/25_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl25_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/25_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/26_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/26_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl26_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/26_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl26_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/26_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl27_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/27_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl27_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/27_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl27_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/27_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl27_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/27_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl28_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/28_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl28_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/28_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl28_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/28_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl28_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/28_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl29_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/29_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl29_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/29_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl29_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/29_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl29_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/29_Tom2_Stereo_RR4.wav` |
| `smdrums_tom2_hit_main_vl30_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR1/30_Tom2_Stereo_RR1.wav` |
| `smdrums_tom2_hit_main_vl30_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR2/30_Tom2_Stereo_RR2.wav` |
| `smdrums_tom2_hit_main_vl30_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR3/30_Tom2_Stereo_RR3.wav` |
| `smdrums_tom2_hit_main_vl30_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom2/RR4/30_Tom2_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/01_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/01_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/01_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/01_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/02_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/02_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/02_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/02_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/03_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/03_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/03_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/03_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/04_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/04_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/04_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/04_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/05_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/05_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/05_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/05_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/06_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/06_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/06_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/06_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/07_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/07_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/07_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/07_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/08_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/08_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/08_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/08_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/09_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/09_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/09_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/09_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/10_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/10_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/10_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/10_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/11_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/11_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl11_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/11_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl11_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/11_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/12_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/12_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl12_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/12_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl12_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/12_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/13_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/13_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl13_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/13_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl13_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/13_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/14_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/14_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl14_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/14_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl14_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/14_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/15_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/15_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl15_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/15_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl15_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/15_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/16_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/16_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl16_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/16_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl16_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/16_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/17_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/17_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl17_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/17_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl17_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/17_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/18_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/18_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl18_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/18_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl18_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/18_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/19_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/19_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl19_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/19_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl19_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/19_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/20_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/20_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl20_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/20_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl20_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/20_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/21_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/21_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl21_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/21_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl21_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/21_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/22_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/22_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl22_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/22_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl22_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/22_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/23_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/23_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl23_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/23_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl23_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/23_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/24_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/24_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl24_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/24_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl24_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/24_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/25_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/25_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl25_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/25_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl25_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/25_Tom3_Stereo_RR4.wav` |
| `smdrums_tom3_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR1/26_Tom3_Stereo_RR1.wav` |
| `smdrums_tom3_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR2/26_Tom3_Stereo_RR2.wav` |
| `smdrums_tom3_hit_main_vl26_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR3/26_Tom3_Stereo_RR3.wav` |
| `smdrums_tom3_hit_main_vl26_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom3/RR4/26_Tom3_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl01_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/01_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl01_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/01_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl01_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/01_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl01_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/01_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl02_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/02_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl02_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/02_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl02_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/02_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl02_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/02_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl03_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/03_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl03_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/03_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl03_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/03_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl03_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/03_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl04_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/04_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl04_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/04_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl04_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/04_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl04_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/04_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl05_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/05_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl05_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/05_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl05_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/05_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl05_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/05_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl06_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/06_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl06_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/06_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl06_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/06_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl06_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/06_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl07_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/07_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl07_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/07_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl07_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/07_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl07_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/07_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl08_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/08_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl08_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/08_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl08_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/08_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl08_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/08_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl09_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/09_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl09_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/09_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl09_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/09_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl09_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/09_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl10_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/10_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl10_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/10_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl10_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/10_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl10_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/10_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl11_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/11_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl11_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/11_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl11_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/11_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl11_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/11_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl12_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/12_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl12_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/12_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl12_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/12_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl12_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/12_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl13_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/13_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl13_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/13_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl13_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/13_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl13_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/13_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl14_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/14_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl14_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/14_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl14_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/14_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl14_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/14_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl15_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/15_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl15_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/15_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl15_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/15_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl15_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/15_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl16_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/16_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl16_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/16_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl16_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/16_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl16_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/16_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl17_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/17_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl17_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/17_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl17_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/17_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl17_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/17_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl18_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/18_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl18_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/18_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl18_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/18_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl18_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/18_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl19_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/19_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl19_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/19_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl19_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/19_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl19_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/19_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl20_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/20_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl20_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/20_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl20_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/20_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl20_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/20_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl21_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/21_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl21_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/21_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl21_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/21_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl21_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/21_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl22_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/22_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl22_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/22_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl22_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/22_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl22_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/22_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl23_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/23_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl23_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/23_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl23_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/23_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl23_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/23_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl24_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/24_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl24_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/24_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl24_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/24_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl24_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/24_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl25_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/25_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl25_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/25_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl25_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/25_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl25_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/25_Tom4_Stereo_RR4.wav` |
| `smdrums_tom4_hit_main_vl26_rr1.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR1/26_Tom4_Stereo_RR1.wav` |
| `smdrums_tom4_hit_main_vl26_rr2.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR2/26_Tom4_Stereo_RR2.wav` |
| `smdrums_tom4_hit_main_vl26_rr3.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR3/26_Tom4_Stereo_RR3.wav` |
| `smdrums_tom4_hit_main_vl26_rr4.wav` | `Samples/SMDrum Stereo (Samples)/Toms_Stereo/Tom4/RR4/26_Tom4_Stereo_RR4.wav` |

</details>

## How it was made

Source samples were copied and renamed only; they were never resampled,
normalized or trimmed, and each copy is byte-identical to its upstream file.
Each Opus twin was encoded with:

```sh
opusenc --bitrate 160 --vbr --comp 10 --framesize 20 "<source>" "opus/<stem>.opus"
```

using opus-tools 0.2 (libopus 1.6.1). `opusenc` resamples to 48 kHz; that is the
only alteration, and it affects only the Opus twin, never the source file.

## Removal

Ask for removal at <https://github.com/michalslonina/drum-samples-smdrums/issues>
(or contact `michalslonina` on GitHub); removal is immediate.
