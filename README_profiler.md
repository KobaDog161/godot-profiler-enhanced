# Godot Profiler Zoom Patch

Install this addon in a Godot project and enable **Godot Profiler Zoom Patch** in the editor plugins list.

This addon packages patched Godot 4.6.2 editor profiler source files:

- Mouse wheel over the profiler graph zooms the X axis, expanding the frame timeline.
- Ctrl + mouse wheel over the graph zooms the Y axis, expanding function time.
- Middle/right mouse drag keeps horizontal panning while zoomed.
- Double-clicking a profiler function opens its script at the recorded line.
- Left-clicking a profiler function toggles graph plotting; right-clicking opens **Copy** without changing the graph selection.
- Right-clicking a profiler function highlights its callers in light green and its callees in light red until another function is right-clicked.
- Expanding a profiler function shows per-line timing gathered by GDScript while profiling is active.
- The profiler toolbar includes a threshold input in milliseconds to hide line deltas with an average time less than or equal to that value.
- The profiler toolbar includes **Group by script** to show script nodes with their functions as children.

The built-in profiler and the GDScript VM are part of Godot C++ code, so this addon cannot hot-patch an already compiled editor. Use the dock to copy the patched files into a Godot 4.6.2 source checkout, then rebuild the editor.

The addon writes backups beside the original files using the `.codex_zoom_backup` suffix before replacing them.
