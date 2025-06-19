# 🔬 oriC Prediction Pipeline

This project provides an efficient and partially biologically informed pipeline to predict the **origin of replication (oriC)** in bacterial genomes using patterns like **DnaA boxes**, **AT-rich regions**, **GATC motifs**, and **GC skew analysis**.

---

## 🚀 Features

✅ GC Skew Analysis

Calculates GC skew and identifies minima or local dips in skew values to narrow down potential oriC regions.

✅ K-mer Pattern Discovery

Scans for the most frequently repeated k-mers (e.g., 9-mers) and their reverse complements, allowing Hamming distance-based mismatches.

Focuses on repeats clustered within a defined window size (e.g., 500 bp).

✅ Poly-AT Region Detection

Identifies AT-rich sequences, which are often essential for strand separation during replication initiation.

✅ Refined OriC Selection

Integrates k-mer repeat positions and AT-rich regions to predict a concise oriC region.

Handles circular genome context by considering flanking sequence continuity.

✅ Optional Enhancements

Detection of GATC clusters for SeqA protein binding.

Identification of other replication-related motifs (e.g., IHF sites, DnaA-trios) for further biological insights.

---

## 📦 Usage

Clone the repository and run the pipeline with your input genome file (in FASTA format):

```bash
python ori_pipeline.py example_genome.fasta
