---
title: "atctools: R Package for ATC Code Matching and Validation"
summary: "An R package designed for facilitating Anatomical Therapeutic Chemical (ATC) matching and ensuring the integrity of ATC data in pharmaceutical datasets."
tags:
  - Science
  - R
  - Pharmacology
date: '2024-12-01T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  focal_point: Smart

url_code: 'https://github.com/vljlangen/atctools'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
slides: ""
---

**atctools** is an R package created by Ville Langén that facilitates Anatomical Therapeutic Chemical (ATC) matching and ensures the integrity of ATC data in pharmaceutical datasets. This specialized tool is essential for pharmaceutical research, drug safety studies, and healthcare data analysis.

## Overview

The atctools package provides comprehensive tools for working with ATC codes, which are used worldwide to classify drugs according to the organ or system on which they act and their therapeutic, pharmacological, and chemical properties. The package bridges the gap between drug names and their standardized ATC classifications.

## Key Features

### 🔍 **ATC Matching Functions**

**Advanced drug name matching** using sophisticated algorithms including Levenshtein distance for fuzzy matching, ensuring accurate identification even with spelling variations or formatting differences.

### 🏷️ **ATC Code Matching** 

**Direct ATC-to-drug name matching** for reverse lookups and data verification workflows.

### ✅ **ATC Data Integrity Checks**

**Comprehensive validation tools** to verify the structure and validity of ATC codes using authoritative reference lists.

## Core Functions

### drug_match()

Matches drug names to ATC codes **without stripping** trailing characters like "mg", "g", etc.

**Usage:**
```r
library(atctools)

output_data <- drug_match(example_drug_data, "drug_name", example_reference_data)
output_data
```

**Key Features:**
- Preserves original drug name formatting
- Uses fuzzy matching algorithms for robust identification
- Includes confidence scoring through `drug_name_flag`

### drug_match_strip()

Matches drug names to ATC codes **with trailing characters stripped** for cleaner matching.

**Usage:**
```r
output_data_stripped <- drug_match_strip(example_drug_data_with_mg, "drug_name", example_reference_data)
output_data_stripped
```

**Perfect for:**
- Drug names with dosage information (e.g., "paracetamol 500mg")
- Standardizing drug nomenclature
- Handling varied formatting in clinical datasets

### atc2drug()

Matches ATC codes back to drug names directly with **no fuzzy matching** for precise lookups.

**Usage:**
```r
output_data_atc2drug <- atc2drug(example_atc_data, "ATC_code", example_reference_data)
output_data_atc2drug
```

**Use Cases:**
- Reverse lookups from ATC to drug names
- Data verification and validation
- Creating drug dictionaries from ATC classifications

## 🔍 ATC Validation Functions

### validate_atc()

Checks if ATC codes follow the **correct structural format** (length, character pattern).

**Usage:**
```r
validate_output <- validate_atc(example_atc_data_for_validation, "atc_1")
validate_output
```

**Validation Criteria:**
- Proper ATC code length and structure
- Character pattern verification
- Format compliance with WHO ATC standards

### validate_atc_by_reference()

Checks if ATC codes **exist in a given reference list** (e.g., WHO ATC index or validated datasets).

**Usage:**
```r
validate_by_ref_output <- validate_atc_by_reference(example_atc_data_for_validation, "atc_2", example_reference_data)
validate_by_ref_output
```

### Combined Validation Workflow

**Comprehensive validation** using both format and reference checking:

```r
output_combined <- example_atc_data_for_validation %>%
  validate_atc("atc_1") %>%
  validate_atc_by_reference("atc_2", example_reference_data)

output_combined
```

**Output Flags:**
- `atc_1_invalid`: Flag for invalid format (1 = invalid, 0 = valid)
- `atc_2_invalid`: Flag for "not found in reference list" (1 = not found, 0 = found)

## Understanding drug_name_flag

The `drug_name_flag` column provides **matching confidence** in outputs from `drug_match()` and `drug_match_strip()`:

- **0**: First 3 characters of drug name match the first 3 of matched ATC code ✅
- **1**: Mismatch detected between drug name and ATC prefix ⚠️

This flag helps identify potential matching errors and enables quality control in large datasets.

## Example Datasets

atctools includes comprehensive example datasets for testing and learning:

### **example_drug_data**
Drug names without dosage information for clean matching scenarios.

### **example_drug_data_with_mg** 
Drug names with trailing dosage units (e.g., "paracetamol 500mg") for strip matching.

### **example_atc_data**
ATC codes for testing `atc2drug()` – includes valid, invalid, and NA values.

### **example_reference_data**
Reference dataset for drug name ↔ ATC code matching workflows.

### **example_atc_data_for_validation** ✨ New!
Contains ATC codes across multiple columns for testing both structural and reference-based validation.

## Installation

Install the development version directly from GitHub:

```r
# install.packages("devtools")
devtools::install_github("vljlangen/atctools")
```

## Use Cases

Perfect for:
- **Pharmaceutical researchers** standardizing drug classifications
- **Clinical data scientists** validating medication datasets
- **Epidemiologists** conducting drug utilization studies
- **Healthcare analysts** ensuring data quality in EHR systems
- **Regulatory affairs** professionals working with drug databases
- **Pharmacovigilance** teams processing adverse event data

## Key Updates & Features

### ✅ **New Validation Functions**
- `validate_atc()` checks format validity against WHO standards
- `validate_atc_by_reference()` verifies presence in reference datasets

### 🧪 **Enhanced Testing**
- New `example_atc_data_for_validation` dataset
- Comprehensive validation workflow examples

### 🔁 **Improved Documentation**
- Updated function examples with real-world scenarios
- Clear validation workflow documentation

### 🧹 **Performance Improvements**
- Enhanced `atc2drug()` function with better column detection
- Optimized matching algorithms for large datasets

## Why atctools?

Working with ATC codes manually is error-prone and time-consuming. atctools solves this by:

- **Automating matching** between drug names and ATC codes
- **Ensuring data quality** through comprehensive validation
- **Handling edge cases** intelligently (dosage units, spelling variations)
- **Providing confidence metrics** for quality control
- **Supporting research workflows** with robust, tested functions

## Technical Details

- **Built for**: R statistical computing environment
- **Specialty**: Pharmaceutical and healthcare data analysis
- **Dependencies**: Minimal dependencies for maximum compatibility
- **License**: Open source (check repository for specific license)
- **Maintained**: Actively developed with regular updates

## Development & Support

atctools is open source and welcomes contributions from the pharmaceutical data science community. Bug reports, feature requests, and pull requests are encouraged on the [GitHub repository](https://github.com/vljlangen/atctools).

**Questions or issues?** Feel free to reach out through the project's GitHub issues page.

Transform your pharmaceutical data workflows from manual, error-prone processes into automated, validated pipelines with atctools! 