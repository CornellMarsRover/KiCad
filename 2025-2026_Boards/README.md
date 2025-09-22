import pypandoc

# Content for the markdown file
content = """# 2025-2026 Boards

This repository contains PCB designs for boards created in KiCad during the 2025-2026 design cycle.

## Overview

- **Design Tool:** KiCad  
- **Timeframe:** 2025–2026  
- **Purpose:** Centralized documentation and tracking of PCB projects made this year.

## Board Projects

- [ ] Board 1 – Description and specs TBD  
- [ ] Board 2 – Description and specs TBD  
- [ ] Board 3 – Description and specs TBD  

## Notes

All designs should follow standard design rules and best practices for manufacturability and testing. Updates will be logged as the boards progress from schematic to layout to fabrication.
"""

# Save as markdown
output_path = "/mnt/data/2025-2026_boards.md"
pypandoc.convert_text(content, 'md', format='md', outputfile=output_path, extra_args=['--standalone'])

print(f"Markdown file created at: {output_path}")
