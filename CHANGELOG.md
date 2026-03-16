# Changelog

All notable changes to GrantAi will be documented in this file.

## [1.8.6] - 2026-03-11

### Fixed
- Document chunking for files over 512 tokens — now uses windowed processing with overlap
- Windows build stability improvements

### Changed
- Auto-trial activation on first run (no license key required for 30-day trial)

## [1.8.5] - 2026-02-27

### Fixed
- Claude Desktop connection stability improved

### Changed
- Docker configs now include `--pull always` to ensure fresh images

## [1.8.4] - 2026-02-26

### Added
- Multi-client support — Claude Code, Cursor, and other MCP clients can share memory simultaneously

## [1.8.3] - 2026-02-25

### Fixed
- Performance and stability improvements

## [1.8.2] - 2026-02-25

### Fixed
- Installer now cleanly upgrades without leftover files
- User data preserved during upgrades

## [1.8.1] - 2026-02-24

### Fixed
- Docker image versioning — explicit tags instead of :latest

## [1.8.0] - 2026-02-22

### Added
- HTTP transport support for Team/Enterprise plans

### Changed
- Increased device limits for all plans

---

[Download latest release →](https://solonai.com/grantai/download)
