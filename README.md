# VHDL Counter Rollover Bug

This repository demonstrates a common bug in VHDL code involving counters and rollover conditions.  The `buggy_counter` entity is a simple counter that increments on each rising clock edge, resetting to 0 when it reaches 15. However, there's a subtle error in how the rollover is handled, leading to unexpected behavior.  The solution demonstrates the proper way to address this issue.

## Bug Description
The primary issue lies in the `elsif rising_edge(clk)` section.  The counter's rollover condition is correctly handled when `internal_count` reaches 15. However, in some cases, the counter's behavior at the boundary might not be completely correct, potentially resulting in a delay or skipping a count.

## Bug Solution
The solution includes a corrected `buggy_counter` entity that accurately manages the rollover condition. This improved version uses a more robust approach to ensure the counter behaves predictably at all times.