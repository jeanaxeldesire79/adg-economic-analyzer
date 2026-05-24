# Changelog — ADG Economic Analyzer

All notable changes to the Economic Analyzer will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/).

## [2.0.1] — 2026-05-24

### Changed
- Production release with live data integration from World Bank + UNDP
- Updated data source endpoints to production API routes
- Enhanced error handling with graceful degradation
- Improved responsive layout for mobile devices
- Optimized chart rendering for large datasets (44K+ data points)

## [1.0.0] — 2026-05-23

### Added
- Initial release of the ECOWAS Economic Analyzer
- Interactive charting for 88+ economic indicators across 15 ECOWAS countries
- Country selector with full ECOWAS member state list
- Indicator browser with search and filtering
- Year range selector (1960–2023)
- Data table view with export functionality
- Responsive dark theme design
- Offline/error state handling with graceful degradation
- Data sourced from World Bank API and Google Drive CSV import

### Technical
- Single-file HTML application (no build step required)
- Vanilla JavaScript with async API calls via `Promise.all`
- CSS custom properties for theming
- Mobile-responsive layout
- Backend: Python FastAPI → PostgreSQL (datasci_db)
- API: `/api/data/economic/*` endpoints
