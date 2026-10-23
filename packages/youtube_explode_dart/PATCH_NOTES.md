# Parche local para SonicBoost

Este paquete está vendorizado dentro del repo (no es una dependencia externa)
para poder mantenerlo sincronizado con las correcciones activas del proyecto
original de Hexer10 (https://github.com/Hexer10/youtube_explode_dart),
que sí sigue mantenido, en vez de depender de un fork congelado.

Base: Hexer10/youtube_explode_dart v3.1.0 (2026-05-09)

Cambios agregados sobre la base, portados desde anandnet/youtube_explode_dart
para conservar compatibilidad con SonicBoost/Harmony Music:
- `AudioOnlyStreamInfo.loudnessDb` (double) — usado para normalización de volumen.
- `AudioOnlyStreamInfo.duration` (int?, ms) — usado como fallback de duración.

Archivos tocados respecto a la base de Hexer10:
- lib/src/reverse_engineering/models/stream_info_provider.dart
- lib/src/reverse_engineering/player/player_response.dart
- lib/src/videos/streams/stream_client.dart
- lib/src/videos/streams/types/audio_only_stream_info.dart
- lib/src/videos/streams/types/audio_only_stream_info.g.dart

Para actualizar en el futuro: descargar la última versión de Hexer10/youtube_explode_dart
y reaplicar estos 5 cambios (son pequeños y mecánicos, ver diffs en el historial de este repo).
