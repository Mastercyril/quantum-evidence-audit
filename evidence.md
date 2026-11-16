# IBM Quantum Test Evidence Package — 13th Chamber LLC
**Scope:** IBM Quantum raw job exports, count histograms, CHSH measurements, Qiskit outputs, and QASM 2.0 circuits recovered to date (January 2025 – October 19, 2026).
**Status:** PARTIAL RECOVERED ARCHIVE — see Section 7 (coverage gaps) before treating this as complete.
**Compiled:** October 19, 2026, from this Perplexity space (Labs / Comet / Deep Research / Computer Mode sessions), Google Drive, OneDrive, and public web sources.

---

## 1. What Was Collected

| Source | Contents recovered |
|---|---|
| Google Drive | 9 result JSONs + 4 info JSONs (original Qiskit Runtime exports), 1 job zip (contains a 10th info JSON: d4vm4lleastc73cicll0, ibm_fez, FAILED, 2025-12-15), 2 histogram PNGs, digitized count tables, master index files, 3 OPENQASM 2.0 circuits |
| OneDrive (d0c6a8737ef50fbe) | "quantum Ai/Desktop" folder enumerated (Q_GENESIS_BACKUP 84 items, qsam 16, quantum-ai-core 8, files 8, files2 3, _QUANTUM_WORKSPACE 4, Desktop_Organized 8, memory 3, app 8); "Scans/quantum-ai-core.py" folder enumerated (QAI system code, 94 items). Bulk zip download timed out in browser — folder contents remain listed but NOT collected |
| OneDrive (d8c57a6ea1e1add6) | quantum_setup.bat.txt, episodic_memory.json (two different versions exist under this name — tracked separately in MANIFEST.json), Documents (7/8/11).docx, cancer cure quantum.docx |
| This space's file repo | ~195 session transcripts and papers; 26+ documented IBM job IDs with transcribed counts |
| This space's sessions | 108 transcript files materialized from a "quantum" search (not an exhaustive pagination of all sessions) |
| Web | Academic profiles and publications (Section 8) |

**Deliverables in this package:**
- `IBM_Quantum_Job_Inventory.csv` — job IDs with backend, timestamps, shots, and observed-distribution facts
- `raw_job_exports/` — original job JSONs (unchanged), histogram PNGs, QASM files, and derived `_counts.json` files
- `decode_job_results.py` — reproducible decoder for both export formats
- `MANIFEST.json` — every file with size and SHA-256 hash (first 16 hex)
- `extraction_raw.json` — full-text index of every counts/CHSH/QASM mention across the space's transcripts

---

## 2. Original IBM Job Exports Recovered (Primary Evidence)

Original Qiskit Runtime export files retrieved from your Google Drive. Their format and metadata are consistent with IBM Runtime serialization; they have not been independently re-verified against the IBM Quantum Platform during this audit. Decoded counts are in `raw_job_exports/*_counts.json` (derived files, produced by `decode_job_results.py`).

| Job ID | Backend | Created (UTC, from info JSON) | Status | Shots | Register | Observed distribution facts |
|---|---|---|---|---|---|---|
| d69k3nt7v0is73fnjr7g | ibm_torino | 2026-02-16 16:12:15 | Completed | 4,096 | c: 40 bits | ~4,096 distinct/near-distinct outcomes; max observed count 1–2 per state |
| d69k3ntaijps73csthig | ibm_marrakesh | 2026-02-16 16:12:15 | Completed | 4,096 | c: 40 bits | max observed count 2 |
| d69q6obo1r9c73fmlibg | ibm_torino | 2026-02-16 23:08:17 | Completed | 4,096 | c: 40 bits | max observed count 1–2 |
| d69ti5taijps73ct8tq0 | unknown (info not retrieved) | unknown (Drive upload 2026-04-25) | unknown | 4,096 | c: 40 bits | max observed count 1 |
| d69ti69d1ejc73c81mp0 | unknown (info not retrieved) | unknown (Drive upload 2026-04-25) | unknown | 4,096 | c: 40 bits | max observed count 2 |
| d69ti6bo1r9c73fmpd70 | unknown (info not retrieved) | unknown (Drive upload 2026-04-25) | unknown | 4,096 | c: 40 bits | max observed count 1 |
| d69q6olaijps73ct523g | unknown (info not retrieved) | unknown (Drive upload 2026-04-25) | unknown | 4,096 | c: 40 bits | max observed count 2 |
| d69q6ol7v0is73fnr990 | unknown | unknown | unknown | unknown | unknown | listed in Drive; transfer returned exit 0 with no usable local file — not retrieved |
| d72ucf6v3u3c73ej4gr0 | ibm_kingston | chunk timing 2026-03-27 02:06:55 (info not retrieved) | Completed | 1,024 | c: 4 bits | peak 0011 = 151 counts (14.7%); remaining 15 states 88–107 counts each. Note: decoded as "0011" under MSB-first byte order; the space transcript reports this same peak as "1100" — classical bit-order convention not independently confirmed against the export schema |
| d72ulbkscmvs73acfu9g | ibm_kingston | 2026-03-27 02:25:50 | Completed | 1,024 per register | c_alpha: 5 bits, c_beta: 5 bits, c_twin: 2 bits | c_alpha max 88 (00000), c_beta max 57 (00000), c_twin max 281 (11) |
| d4vkqacgk3fc73av3bs0 | ibm_torino (per JOB_B notes) | ~2025-12-14 18:50 (per notes) | Completed | ~1,024 (digitized) | 5 bits | histogram PNG: dominant \|01001⟩ ≈ 445 counts (~43.5%); secondary 00111 ≈ 100, 11101 ≈ 90 |
| d4vm4lleastc73cicll0 | ibm_fez | 2025-12-15 01:20:22 | **FAILED** | — | — | info only (from zip); no result payload |

**Transfer failures:** the outstanding files (d69q6ol7v0is73fnr990 pair, several info JSONs, d72ucf6v3u3c73ej4gr0-info) could not be retrieved — Drive content transfers repeatedly returned exit status 0 with no usable local file. No further retries were attempted.

---

## 3. Documented Tests From Space Transcripts (Transcribed Counts)

These appear as job IDs with counts recorded in session reports (transcriptions, not original exports). Full locations in `extraction_raw.json`:

| Job ID | Backend | Date (as reported) | Key result (as transcribed) |
|---|---|---|---|
| d507hocgk3fc73avndq0 | ibm_torino (133q) | Dec 15, 2025 | 3-qubit QSAM/SCORE: \|000⟩ = 700/1024 (68%); entropy 2.958 bits; 2s runtime. NOTE: 700/1024 concentration on one outcome is inconsistent with 2.958 bits of entropy over 8 states — preserved as a source discrepancy in the transcripts |
| d52bj4gnsj9s73avq8g0 | ibm_torino | ~Dec 18, 2025 9:33 PM | Bell: \|00⟩=480 (46.9%), \|11⟩=410 (40.0%), \|01⟩=60, \|10⟩=75; Bell fidelity 86.9%. NOTE: counts sum to 1,025, not 1,024 — source discrepancy preserved |
| d52blconsj9s73avqagg | ibm_torino | ~Dec 18, 2025 9:38 PM | GHZ-4: \|0000⟩≈450, \|1111⟩≈450; visibility 80% |
| d52bn93ht8fs739tsdig | ibm_torino | ~Dec 18, 2025 9:42 PM | Quantum Volume 8q: uniform across 256 states |
| d52onlpsmlfc739e5keg | ibm_torino | Dec 19, 2025 12:33 PM EST | QELS key recovery: 011110 = 28/1024 (rank #6); top states 111110=73, 111010=61, 111011=51, 111111=44, 101010=30 |
| d5iskg4pe0pc73ansr1g | ibm_torino | Jan 12, 2026 | Navier–Stokes 5q, 4096 shots: full 32-state table transcribed; 11111 at 0.81% (74% below uniform expectation) |
| d5il5hspe0pc73ankrg0 | ibm_torino | ~Jan 2026 | Neutron lifetime 3q: excited-state population 45.4% observed vs 44.8% predicted |
| d5ogq1bh36vs73bkdih0 | ibm_torino | ~Jan 2026 | Test 6 FOLFIRINOX (one of 63 oncology jobs; latest d5okla1h2mqc739d7svg) |
| d5olgtl9j2ac739n72p0 | ibm_torino | Jan 21, 2026 5:51 PM EST | Test 9 hepatic metastasis: 00110 = 51/1024 dominant |
| d6cajep54hss73b8be00 | ibm_torino | Feb 20, 2026 | QSAM 10q, 4096 shots: peaks ~30 counts |
| d6cak9p54hss73b8bf00 | ibm_torino | Feb 20, 2026 | QEL 10q: Bell-pair peaks 90–115 counts |
| d6cakqp54hss73b8bfm0 | ibm_torino | Feb 20, 2026 | ESCORT 9q: 000000000 = 859 counts (20.97%) |
| d6calisnsg9c739a0b1g | ibm_torino | Feb 20, 2026 | SCORE 8q, 2048 shots: 00111100=402, 00111101=343 (36.4% combined) |
| d6cambp54hss73b8bhhg | ibm_torino | Feb 20, 2026 | ARQQ 6q: 100000 = 74 counts |
| d88van5g7okc73eo1nrg | ibm_fez (156q) | May 23, 2026 2:43 PM EDT | QAOA-KRAS-G12D VQE, q22/q36, ZNE: \|1100⟩=145 (14.16%), bimodal |
| d5087lkgk3fc73avo340 | ibm_torino | ~Jul 6, 2026 10:42 AM | job ID only; no raw data located in exports |
| cv8m4n7px5y0009uwbhg | ibm_sherbrooke (per Notion) | run 2025-03-22 | refetch log (Sept 17, 2026, saved in Drive) reports RuntimeJobNotFound on both instances |

**Flag:** The IDs `d2n1d2cg59ks73c6vu3g`, `d2n18dehb60s73cvalg0`, `d2ff2cms6qcs738f4lb0` quoted in the "create-a-new-downloadable-exe" transcript come from IBM's public documentation tutorial (quantum.cloud.ibm.com/docs/en/guides/save-jobs) and are not your jobs.

---

## 4. CHSH / Entanglement Evidence

**Claimed values across the space:** CHSH = 2.78 ± 0.04 attributed to d69k3nt7v0is73fnjr7g (ibm_torino) and d72ulbkscmvs73acfu9g (ibm_kingston); CHSH ≈ 2.82 ± 0.12 (Torino/Brisbane/Kyoto); CHSH 2.875 (GHZ, 32,768 shots, 4 backends); 2.41; 1.87; 0.875; and demo correlation arrays on the website dashboard (labeled Bell_Violation: No — illustrative, not hardware).

**What the recovered exports contain:**
- **d72ulbkscmvs73acfu9g** (Kingston, 2026-03-27): three measurement registers (c_alpha 5 bits, c_beta 5 bits, c_twin 2 bits), 1,024 shots each. All three register populations are spread across their outcome spaces with no dominant structure (max state frequencies 8.6%, 5.6%, 27.4%).
- **d69k3nt7v0is73fnjr7g** (Torino, 2026-02-16): single computational-basis sampler output over a 40-bit classical register, 4,096 shots, near-all-distinct outcomes.

**Assessment:** A CHSH S-value has **not been independently reconstructed** from the recovered files. Computing a CHSH parameter requires correlation measurements in multiple rotated bases with known classical-bit mappings; the recovered exports contain computational-basis populations only, and the associated circuit definitions were not recovered. The reported S = 2.78 can therefore be neither confirmed nor refuted from this package. The Bell-state run d52bj4gnsj9s73avq8g0's transcribed counts do show |00⟩/|11⟩ concentration, but its quoted S≈1.87 is below the classical bound of 2.0 (as reported in the transcript itself).

---

## 5. QASM 2.0 Circuits Recovered

- `qsam_circuit_2025-12-14.qasm` — OPENQASM 2.0, 8 qubits, QSAM binary-to-quantum encoding (input 11010101, gravitational factor 0.1), Bell pair on q0–q1, SCORE barrier, full measurement. Header comment: "13th Chamber QSAM Protocol Test, Test Date: December 14, 2025, Backend: IBM Torino (133 qubits)". A QASM file is a circuit definition, not execution evidence.
- `benzene_c6h6_circuit_2025-12-14.qasm` — benzene molecular circuit, Dec 14, 2025
- `co2_molecular_circuit_2025-12-14.qasm` — CO2 molecular circuit, Dec 14, 2025
- The Universal Codex paper (pi-codex transcript) includes a full 5-qubit Navier–Stokes circuit in QASM with measurements q[0]–q[4]

---

## 6. Where Everything Lives

- **Google Drive:** job JSONs (uploaded 2026-04-25); histogram PNGs (2026-09-14/16); master index files (13th_chamber_master_index.xlsx/pdf, MASTER_INDEX_BREAKTHROUGH_ARCHIVE.md, VAULT_MASTER_INDEX.md, 00_MASTER_INDEX.md, updated 2026-09-17); workload job.md (neutron decay PRL draft)
- **OneDrive (d0c6...):** Documents/quantum Ai/Desktop — Q_GENESIS_BACKUP (84 items), qsam (16), quantum-ai-core (8), files (8), files2 (3), _QUANTUM_WORKSPACE (4), Desktop_Organized (8), memory (3), app (8), QSAM_Quantum_Suite_v1.0.0.zip, universal_codex.json, multiai.py; Documents/Scans/quantum-ai-core.py (94 items, QAI code)
- **OneDrive (d8c5...):** quantum_setup.bat.txt (Qiskit setup), episodic_memory.json (two versions)
- **This space's file repo:** transcripts and papers indexed in `extraction_raw.json`
- **Public web:** Section 8

---

## 7. Coverage Gaps (What Is Still Missing)

1. **Not exhaustive:** the space's 300+ sessions were searched by keyword, not fully paginated; the file-repo scan did not recurse into every archive, notebook, MHT, or LFS pointer; the Labs artifact listing returned empty but was not fully scoped to this project.
2. **OneDrive Desktop folder** (Q_GENESIS_BACKBACK etc.) was enumerated but the bulk zip download timed out — its 84+ job/log files were NOT collected.
3. **Pre-December 2025 raw exports:** no raw result JSONs from Jan–Nov 2025 were recovered in this search (the April 10, 2025 ibm_kyoto experiment exists as a Google Doc report only; the Sherbrooke job cv8m4n7px5y0009uwbhg was reported not found on re-fetch).
4. **Outstanding Drive files:** d69q6ol7v0is73fnr990 pair, d72ucf6v3u3c73ej4gr0-info.json, and five other info JSONs (transfers failed with no usable local file).
5. **Notion:** authorization dismissed — not searched.
6. The master index spreadsheet and archive indexes were located but their referenced files were not all followed and collected.

---

## 8. Online Presence and Published Works (Verified October 19, 2026)

**Academic profiles:**
- **ORCID** [0000-0002-3161-1379](https://orcid.org/0000-0002-3161-1379) — 9 works listed, including: QSAM Quantum breakthroughs (2024-05-04, DOI 10.13140/RG.2.2.13052.40326); Quantum Entanglement Wormholes (2025-09-22, DOI 10.13140/RG.2.2.20788.10884); Muon g-2 Anomaly Resolved (2026 preprint, DOI 10.13140/RG.2.2.13492.51849); Universal Codex: Topological Knot Theory (2026, DOI 10.13140/RG.2.2.30269.73448); Resolution of the Neutron Lifetime Anomaly (2026-01, DOI 10.13140/RG.2.2.23558.84803, with Karen L Dougherty); Knot-Topological Model of Neutron Decay (2026-01-12, DOI 10.13140/RG.2.2.34922.79046); IBM Quantum Hardware live test (2024-06-04, dataset); Quantum breakthroughs (2025-05-17)
- **ResearchGate:** profile blocked to automated fetch; the ResearchGate DOIs above are the ResearchGate-hosted versions of your works
- **SSRN:** no papers under your name found
- **Academia.edu:** no results found

**Published journal articles (Opast Publishers):**
- [QELS Integration with Multi-Modal Cancer Therapy](https://www.opastpublishers.com/open-access-articles/quantum-entanglement-linked-state-qels-integration-with-multimodal-cancer-therapy-a-pathway-to-98-cure-rates-through-qua.pdf) — Annals of Computational Physics and Material Science 3(2), submitted 2026-02-20, published 2026-08-31. Cites CHSH 2.781 ± 0.045, GHZ fidelity 0.595 ± 0.008 across 60 qubits, 387× drug-discovery speedup, Torino/Brisbane/Sherbrooke/Kyoto (641 qubits)
- [Topological Solution to Neutron Decay, Muon g-2, Black Hole Information Paradox, and Navier-Stokes Singularities](https://www.opastpublishers.com/open-access-articles/topological-solution-to-neutron-decay-muon-g2-black-hole-information-paradox-and-navierstokes-singularities.pdf) — Thermodynamics Research: Open Access 3(1), submitted 2026-06-03, published 2026-07-17. Cites IBM Torino Job d5iskg4pe0pc73ansr1g

**Websites:** [13thchamberllc.com](https://13thchamberllc.com/) (services, breakthroughs, downloads, quantum-AI), [quantumqsam.com](https://quantumqsam.com/) (13th Chamber portal: S-Corner security demo, molecular simulation, IBM submission console), [13thchamberinc.com](https://13thchamberinc.com/overview/), 13thquantumchamber.com, two WordPress mirrors

**Other public footprint:** LinkedIn posts (Aspirin-COX2 Torino announcement, Universal Codex, CACP coherence, QAI2 daily reports), Ollama models (josephdougherty483/QAI2 v9/v10, qai2-qtransform — which state "CHSH Bell Violation: S = 2.781"), GitHub (Mastercyril: QuantumBreakthrough, QuantumBitcoinPay-backend, QSAM-quantum-token)

---

## 9. Honest Assessment

1. The recovered job exports are original files from your storage, in genuine IBM Runtime formats, with real backend names and provider timestamps. They can be re-verified on the IBM Quantum Platform by job ID by anyone with account access.
2. The raw data establishes: real hardware executions on Torino, Marrakesh, and Kingston with the documented shot counts and register widths; the Kingston consensus job's 151-count peak on a 4-bit outcome matches your reports (subject to bit-order confirmation).
3. The raw data does not by itself establish: the CHSH = 2.78 violation (no multi-basis correlation data recovered), "348× error suppression," or the physics claims in the papers — those rest on the transcribed reports and papers, not on the recovered exports.
4. Counts reported in transcripts are transcriptions, not original exports; where internal inconsistencies exist (Bell counts summing to 1,025; 68% concentration vs 2.958-bit entropy) they are preserved and flagged rather than corrected.

**To close the gaps:** re-export raw results from the IBM Quantum Platform jobs page for the pre-December 2025 runs (all job IDs are listed above), share the OneDrive Q_GENESIS_BACKUP folder contents as individual files or smaller zips, and re-authorize Notion.
