# Value Stream Map Builder (hrs)

A lightweight, interactive web-based tool for building and optimizing value stream maps with hourly-based metrics. Perfect for lean process analysis and identifying opportunities to reduce queue times and improve process efficiency.

## Features

✨ **Key Capabilities:**

- **Interactive Process Step Builder** - Easily add, configure, and remove process steps
- **Real-time Metrics Dashboard** - View total non-value-add time, value-add time, and process efficiency instantly
- **Visual VSM Timeline** - Automatically generated value stream map visualization showing process flow and lead times
- **Process Efficiency Calculation** - Track the percentage of time spent in actual value-adding activities
- **Save/Load Functionality** - Export and import your value stream maps as `.vsm` files
- **PNG Export** - Generate shareable images of your complete value stream maps with metrics
- **Local Storage** - Auto-saves your work to browser local storage
- **Professional UI** - Clean, responsive design with a comprehensive color-coded legend

## Getting Started

### Usage

1. **Open the Tool** - Open `vsm.html` in any modern web browser
2. **Add Process Steps** - Click "+ Add Process Step" to create a new process box
3. **Configure Each Step:**
   - Enter a descriptive step name (e.g., "OCPG Service Now")
   - Set the **Process Cycle Time** (actual time spent working on the item)
   - Set the **Queue Inventory Time** (waiting time between processes)
4. **View Metrics** - The dashboard automatically calculates:
   - Total Non-Value-Add Time (Queue Hours in red)
   - Total Value-Add Time (Process Hours in green)
   - Process Efficiency % (Value-Add / Total Time)
5. **Visualize** - See your value stream map rendered below with the timeline diagram
6. **Save or Export:**
   - Save as `.vsm` file to download and share
   - Load a previously saved `.vsm` file
   - Export the visualization as a PNG image

### Default Example

The tool comes with a default example showing typical process steps:
- OCPG Service Now
- OCPG PRT Tool fillout
- QMS File Handling
- SP Manual process

## Metrics Explained

| Metric | Definition |
|--------|-----------|
| **Process Cycle Time (CT)** | The actual hours spent performing value-adding work at each step |
| **Queue Inventory Time (Inv)** | The hours the item waits between process steps (non-value-add) |
| **Process Efficiency** | Percentage of total time that adds value: `(Value-Add Time / Total Time) × 100` |

The visualization uses:
- 🔴 **Red** for non-value-add (queue) hours
- 🟢 **Green** for value-add (process) hours

## File Format

Saved `.vsm` files use JSON format:

```json
[
  {
    "name": "Process Step Name",
    "ct": 0.15,
    "inv": 0.2
  }
]
