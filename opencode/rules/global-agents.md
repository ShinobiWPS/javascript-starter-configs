## Fix At The Source

- Prefer fixing problems in the layer that owns the behavior, contract, or data.
- Do not patch downstream layers to compensate for upstream mistakes by default.
- When backend data, menu structure, route targets, labels, or permissions are wrong, fix the backend/source-of-truth first.
- Do not add frontend remapping, normalization, fallback routing, or UI overrides for backend contract issues unless the user explicitly requests a temporary workaround.
- If the correct fix belongs to another layer, stop and explain that before implementing anything locally.
- If a workaround is unavoidable, mark it as temporary and explain why the source-layer fix is not being made.
