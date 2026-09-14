# Nairobi Flood Eye

Nairobi Flood Eye adapts God's Eye View into a resident-facing flood preparedness map for Nairobi. The first increment adds a Nairobi location preset and a safety-focused welcome screen. It does **not** calculate flood risk, show live flood conditions, recommend evacuation routes, or issue alerts.

## Product direction

The next release should combine official Kenya Meteorological Department warnings with a map of validated flood-prone areas, shelters, clinics, and roads. Every operational layer needs a named source, observation or issue time, validity period, geographic coverage, and a visible unavailable/stale state. The map must never turn an unverified report into an official warning.

Build in this order:

1. **Official warning card:** ingest a machine-readable official source if available; otherwise link to the [KMD warnings page](https://meteo.go.ke/weather-warnings/) and explicitly label the app's status as unavailable. Show issue and expiry times in East Africa Time.
2. **Preparedness guide:** short, accessible steps in English and Kiswahili, including what to do before heavy rain and when a road is submerged. Review wording with a Kenyan disaster-response partner.
3. **Verified places:** shelters, health facilities, and flood-prone locations with provenance and last verification dates. Do not infer safety from map position alone.
4. **Reports and closures:** community submissions enter a moderation queue; show unverified and confirmed reports differently, with expiry to avoid stale closure markers.
5. **Routing and response view:** only offer routes after validating road status and destination availability. A separate operator view could support triage, resource allocation, and incident history.

Other useful applications of the 3D globe include watershed and drainage visualization, rainfall-scenario playback for education, infrastructure exposure analysis, school and clinic continuity planning, and post-flood damage assessment. Scenario playback must be labeled as a simulation, not a forecast.

## Data and licensing

The upstream code is MIT licensed. Bundled third-party datasets, imagery, and 3D models have separate terms; review each before public or commercial deployment. The upstream [LICENSE](../LICENSE) and [DATA_SOURCES.md](../DATA_SOURCES.md) describe those restrictions. The KMD [warnings page](https://meteo.go.ke/weather-warnings/) and [NDOC](https://ndoc.go.ke/) are the initial authoritative public links. This prototype does not scrape or republish their warnings.
