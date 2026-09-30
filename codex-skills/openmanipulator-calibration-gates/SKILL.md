---
name: openmanipulator-calibration-gates
description: Change or assess OpenMANIPULATOR-X calibration, controller, vision-to-motion, or physical test workflows. Use when motor direction, HOME, limits, gamepad, Cartesian control, or real motion is involved.
---

# OpenMANIPULATOR calibration gates

Read the current controller, calibration records, and wiring notes before making changes. Keep encoder RAW values, mathematical joint angles, and FK/IK coordinates distinct. Do not infer direction, HOME, or physical reachability from geometry or old measurements.

Preserve independent firmware and PC safety limits, torque gate, dead-man behavior, and watchdog where present. A software XYZ envelope does not prove mechanical safety. Detection and camera mapping do not authorize automatic motion.

Validate logic offline with meaningful tests, then report exactly which gates remain: sketch compilation, board upload, read-only calibration, and supported physical movement. For initial physical trials, use the user's established conservative speed and one selected motor or direction at a time unless the user specifies a different safe protocol. Ask for measured endpoints rather than inventing them.

When publishing code, inspect the exact staged files and exclude calibration data, telemetry, secrets, and generated results unless requested. Report local and remote commit IDs separately.
