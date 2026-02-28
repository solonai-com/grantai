# Changelog

All notable changes to GrantAi will be documented in this file.

## [1.8.5] - 2026-02-27

### Fixed
- JSON-RPC 2.0 notification handling — Claude Desktop connections now work correctly
- Notifications (no `id` field) no longer receive error responses

### Changed
- Docker configs now include `--pull always` to ensure fresh images

## [1.8.4] - 2026-02-26

### Added
- Multi-client support — Claude Code, Cursor, and other MCP clients can share memory simultaneously

### Changed
- SQLite WAL mode handles concurrent access safely
- Removed exclusive instance lock

## [1.8.3] - 2026-02-25

### Security
- Removed all debug logging from production binaries (GHS v4)

## [1.8.2] - 2026-02-25

### Fixed
- Installer cleanup — removes stale files before copying new ones
- Preserves user data during upgrades

## [1.8.1] - 2026-02-24

### Fixed
- Docker image versioning — explicit tags instead of :latest

## [1.8.0] - 2026-02-22

### Added
- Volume-based licensing — device fingerprint tied to data directory
- HTTP transport support for Team/Enterprise plans

### Changed
- Device limits: trial=3, standard=3, professional=5, enterprise=100

---

[Download latest release →](https://solonai.com/grantai/download)
