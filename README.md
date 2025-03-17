# F1 Insights Visualizer

A high-impact visualization tool for analyzing Formula 1 telemetry data, focusing on driver performance in wet conditions.

## Overview

F1 Insights Visualizer (previously `quick_viz.py`) creates visually striking, presentation-ready charts that highlight critical driving techniques in challenging race conditions. The tool specializes in comparing drivers who crashed versus those who maintained control, with a focus on:

- **Torque spike analysis**: Identifying sudden power delivery issues that lead to loss of traction
- **Throttle control techniques**: Comparing progressive vs. abrupt throttle application patterns
- **Power delivery patterns**: Analyzing common factors across different crash incidents

## Features

- 16:9 aspect ratio visualizations optimized for presentations
- Color-coded insights with clear visual hierarchy
- Team logo integration for immediate driver recognition
- Intelligent data enhancement when telemetry is limited
- Key insight summaries for quick comprehension
- Modern dark-themed design with emphasis on critical data points

## Requirements

- Python 3.7+
- FastF1 (3.4.0+)
- Matplotlib
- Pandas
- NumPy
- Seaborn

## Installation

```bash
# Create and activate a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install required packages
pip install fastf1 matplotlib pandas numpy seaborn
```

## Usage

```bash
python f1_insights_visualizer.py
```

This will:
1. Create a `cache` directory for FastF1 data
2. Download race data for the Australian GP (with fallback to 2023 data if needed)
3. Generate detailed visualizations in the `crash_analysis_plots/quick_insights` directory
4. Create a summary page with key findings

## Visualizations

The tool generates three main comparison visualizations:

1. **Torque Spikes: Why Cars Crash**
   - Compares Sainz (crash) with Piastri (save) to highlight throttle application differences

2. **Throttle Control: Recovery vs Spin**
   - Contrasts Doohan's single large input (crash) with Antonelli's multiple small adjustments (save)

3. **Power Delivery: Crash Pattern Analysis**
   - Identifies common patterns across multiple crashes (Alonso, Sainz, Doohan)

Each visualization includes detailed speed profiles, throttle application patterns, and torque delivery analysis, with clear annotations highlighting critical moments.

## Customization

You can customize the comparisons by modifying the `KEY_COMPARISONS` list in the script, allowing for different driver pairings and focus areas.

## Credits

- Uses the FastF1 package for accessing Formula 1 telemetry data
- Visualization design by Lucas Qiu
- F1 data provided by the official F1 Fast API

## Recommended Rename

For better clarity about the tool's purpose, we recommend renaming `quick_viz.py` to `f1_insights_visualizer.py`. 