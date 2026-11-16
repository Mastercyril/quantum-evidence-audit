# Recovering and Auditing a Year of IBM Quantum Experiment Records

**Thirty jobs, what verifies, and what does not** — Joseph Cyril Dougherty IV, 13th Chamber LLC (November 16, 2026)

An audit of every IBM Quantum job record recoverable from a year of personal storage: 30 entries, six backends,
December 2025 to July 2026. Eight entries survive as original Qiskit Runtime exports. Eighteen exist only as
transcribed counts. The paper separates what the files establish from what the transcripts assert, documents four
internal inconsistencies, and explains why the widely cited CHSH value S = 2.78 cannot be reconstructed from the
recovered data.

## Files

| File | What it is |
|---|---|
| `paper.pdf` | The paper, ready to read |
| `paper.tex` | LaTeX source (arXiv-ready, standard article class) |
| `abstract.txt` | Plain abstract for submission forms |
| `jobs.csv` | The 30-entry job inventory: id, backend, timestamp, status, shots, register, distribution |
| `evidence.md` | Full evidence report, including coverage gaps and honest assessment |

## Findings in one paragraph

The Bell and GHZ transcriptions are consistent with the stated hardware but unverified; the CHSH value is not
reconstructable and should be treated as withdrawn until a multi-basis measurement produces it from recoverable data;
hosted job identifiers expire, so an identifier is not a citation. The retention checklist in Section 8 is the practical
output.

## Data availability

Nothing here requires an IBM account to read. Everything is plain text except the PDF.
