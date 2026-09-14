# Nairobi Flood Eye design

## Audience and purpose

Residents in Nairobi need a clear path from the map to official warnings and practical preparation. The initial prototype prioritizes orientation and source transparency. It must not imply that an El Niño event is currently forecast or that a flood alert is active.

## First increment

Keep the existing Cesium application and add Nairobi to its location catalogue. Rename the browser page and first-run card to Nairobi Flood Eye. The card links directly to KMD warnings and NDOC and states that the prototype does not issue alerts. Existing global layers remain available for exploration.

## Later data flow

An adapter will normalize each approved warning into source, area, issued time, expiry time, severity, text, and URL. A UI card will render the normalized record and show unavailable or stale states. Geospatial risk, shelter, and incident layers will remain separate, with their own provenance and verification rules. No community report will share the visual treatment of an official warning.

## Validation

Run the existing unit suite and production build. Check that Nairobi appears in the location catalogue, and that all public-safety links and caveats render on the first-run card. No emergency guidance or risk estimate is generated from the 3D view alone.
