---
title: Quaternion
description: Quaternions are used to represent rotations.
icon: polytoria/Quaternion
---
# Quaternion

:polytoria-Quaternion: Quaternions are used to represent rotations.
## Constructors

| Name | Description |
| --- | --- |
| `New`(`float` x, `float` y, `float` z, `float` w) | Constructs new Quaternion with given x,y,z,w components. |

## Properties

| Name | Description |
| --- | --- |
| `float` x | X component of the Quaternion. Don't modify this directly unless you know quaternions inside out. |
| `float` y | Y component of the Quaternion. Don't modify this directly unless you know quaternions inside out. |
| `float` z | Z component of the Quaternion. Don't modify this directly unless you know quaternions inside out. |
| `float` w | W component of the Quaternion. Don't modify this directly unless you know quaternions inside out. |
| `Vector3` eulerAngles | Returns or sets the euler angle representation of the rotation. |
| `Quaternion` normalized | Returns this quaternion with a magnitude of 1. |
| `Quaternion` identity | The identity rotation (read-only). This quaternion corresponds to "no rotation". |
| `Quaternion` Identity | The identity rotation (read-only). This quaternion corresponds to "no rotation". |

## Methods

| Name | Description |
| --- | --- |
| `void` Set(`float` newX, `float` newY, `float` newZ, `float` newW) | Set x, y, z and w components of an existing Quaternion. |
| `void` SetFromToRotation(`Vector3` fromDirection, `Vector3` toDirection) | Creates a rotation which rotates from `fromDirection` to `toDirection`. |
| `void` SetLookRotation(`Vector3` view, `Vector3` up = Vector3.up) | Creates a rotation with the specified `forward` and `upwards` directions. |
| `void` ToAngleAxis(out `float` angle, out `Vector3` axis) | Converts a rotation to angle-axis format. |
| `string` ToString() | Returns a formatted string for this quaternion. |

## Static Methods

| Name | Description |
| --- | --- |
| Quaternion.Angle(`Quaternion` a, `Quaternion` b) | Returns the angle in degrees between two rotations `a` and `b`. |
| Quaternion.AngleAxis(`float` angle, `Vector3` axis) | Creates a rotation which rotates `angle` degrees around `axis`. |
| Quaternion.Dot(`Quaternion` a, `Quaternion` b) | The dot product between two rotations. |
| Quaternion.Euler(`float` x, `float` y, `float` z) | Returns a rotation that rotates z degrees around the z axis, x degrees around the x axis, and y degrees around the y axis. |
| Quaternion.FromToRotation(`Vector3` fromDirection, `Vector3` toDirection) | Creates a rotation which rotates from `fromDirection` to `toDirection`. |
| Quaternion.Inverse(`Quaternion` rotation) | Returns the Inverse of `rotation`. |
| Quaternion.Lerp(`Quaternion` a, `Quaternion` b, `float` t) | Interpolates between `a` and `b` by `t` and normalizes the result. |
| Quaternion.LerpUnclamped(`Quaternion` a, `Quaternion` b, `float` t) | Interpolates between `a` and `b` by `t` and normalizes the result. The parameter `t` is not clamped. |
| Quaternion.LookRotation(`Vector3` forward, `Vector3` upwards = Vector3.up) | Creates a rotation with the specified `forward` and `upwards` directions. |
| Quaternion.Normalize(`Quaternion` q) | Converts this quaternion to one with the same orientation but with a magnitude of 1. |
| Quaternion.RotateTowards(`Quaternion` from, `Quaternion` to, `float` maxDegreesDelta) | Rotates a rotation `from` towards `to`. |
| Quaternion.Slerp(`Quaternion` a, `Quaternion` b, `float` t) | Spherically interpolates between `a` and `b` by `t`. The parameter `t` is clamped to the range [0, 1]. |
| Quaternion.SlerpUnclamped(`Quaternion` a, `Quaternion` b, `float` t) | Spherically interpolates between `a` and `b` by `t`. The parameter `t` is not clamped. |
