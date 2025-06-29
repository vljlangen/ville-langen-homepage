---
title: "tablestylizer: R Package for Styling and Formatting Tables"
summary: "An R package that provides functions for styling and formatting tables, making them publication-ready with enhanced visual appeal and clarity."
tags:
  - Science
  - R
date: '2024-12-01T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  focal_point: Smart

url_code: 'https://github.com/vljlangen/tablestylizer'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
slides: ""
---

**tablestylizer** is an R package created by Ville Langén that provides a comprehensive set of functions for styling and formatting tables, making them more suitable for publication in academic papers and reports.

## Overview

The tablestylizer package enhances the visual appeal and clarity of tables generated in R, transforming raw output into polished, publication-ready formats. It's particularly useful for researchers and data analysts who need to present statistical results in a professional manner.

## Key Features

### stylize_tableone() Function

Processes a tableone object to a lean, publication-ready format:

- **Converts rownames to column names** for better structure
- **Transfers percentage symbols** appropriately 
- **Removes unnecessary symbols** that clutter the output
- **Automatic p-value processing** using the `stylize_p()` function when p-value columns are present

### stylize_p() Function

Specialized p-value formatting for improved readability:

- **Rounds to 2 decimal places** whenever feasible
- **Handles small values**: Values less than 0.001 are expressed as `"<0.001"`
- **Smart 0.05 handling**: Avoids outputting exactly `"0.05"` since this may not hold practical meaning when alpha = 0.05
- **Preserves precision**: If rounding would result in `"0.050"`, the original value is retained
- **Exact 0.050 preservation**: Original values of exactly 0.050 are kept without rounding

**Usage Examples:**
```r
stylize_p(0.05795)  # Returns: "0.06"
stylize_p(0.0499)   # Returns: "0.0499"
stylize_p(0.002)    # Returns: "0.002"
stylize_p(0.0005)   # Returns: "<0.001"
```

### stylize1() Function

Stylizes numeric values with custom rules, targeting 1 decimal place:

- **Rounds to 1 decimal place** unless they round to a smaller digit
- **Threshold parameter**: Optional specification for displaying values as `"<threshold"`
- **Scientific notation**: Very large or small values are expressed as powers of 10
- **Intelligent rounding**: Preserves precision when rounding would lose significant information

**Usage Examples:**
```r
stylize1(-0.05)              # Returns: "-0.1"
stylize1(0.002)              # Returns: "0.002"
stylize1(0.0005, 0.001)      # Returns: "<0.001"
```

### stylize2() Function

Similar to `stylize1()`, but targeting 2 decimal places:

- **Rounds to 2 decimal places** with intelligent precision handling
- **Scientific notation**: Very large or small values expressed as powers of 10
- **Threshold parameter**: Optional for `"<threshold"` display
- **Consistent formatting**: Maintains uniform decimal place presentation

**Usage Examples:**
```r
stylize2(-0.05)              # Returns: "-0.10"
stylize2(0.002)              # Returns: "0.002"
stylize2(0.0005, 0.001)      # Returns: "<0.001"
```

## Installation

Install the development version directly from GitHub:

```r
# Install the development version from GitHub
devtools::install_github("vljlangen/tablestylizer")
```

## Use Cases

Perfect for:
- **Academic researchers** preparing statistical tables for publication
- **Data analysts** creating professional reports
- **Biostatisticians** formatting clinical trial results
- **Journal submissions** requiring specific formatting standards
- **Presentations** where clear, readable tables are essential

## Why tablestylizer?

Statistical tables often contain formatting inconsistencies that make them difficult to read and unprofessional in appearance. tablestylizer solves this by:

- **Standardizing number formatting** across all table elements
- **Improving readability** through consistent decimal places and scientific notation
- **Handling edge cases** intelligently (like the 0.05 p-value scenario)
- **Saving time** with automated formatting rules
- **Ensuring publication standards** are met consistently

## Technical Details

- **Built for**: R statistical computing environment
- **Dependencies**: Minimal dependencies for maximum compatibility
- **License**: Open source (check repository for specific license)
- **Maintained**: Actively developed and supported

## Development & Support

tablestylizer is open source and welcomes contributions. Bug reports, feature requests, and pull requests are encouraged on the [GitHub repository](https://github.com/vljlangen/tablestylizer).

**Questions or issues?** Feel free to reach out through the project's GitHub issues page.

Transform your R table formatting from tedious manual work into a streamlined, professional process with tablestylizer! 