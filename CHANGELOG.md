# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.1] - 2026-02-19

### Fixed
- Navigation anchors for "Servicios", "Proyectos", and "Nosotros" were broken in multilingual routes.
- Developer image in `About.astro` was pointing to a template placeholder.
- Missing `codeUrl` and `previewUrl` props in `CardProject.astro`.
- SEO image names for projects.
- Syntax errors in Astro components (`About.astro`, `Experience.astro`).
- Multilingual navigation links in `common.json` (English version).

### Added
- `codeUrl` and `previewUrl` fields to `common.json` for proper project linking.
- New SEO-friendly image placeholders for projects.

## [Unreleased]

### Added
- Initial project setup.
