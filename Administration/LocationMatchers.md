# Location Matchers

Location Matchers define rules for matching location identifiers during data imports. This feature ensures that imported data from various sources is correctly associated with locations in Atlas despite variations in naming or coding.

**Permission:** `Pages.Administration.LocationMatchers`

## Overview

The Location Matchers page manages rules that map external location identifiers to Atlas location records. This is essential when importing data from production accounting systems, SCADA, or other sources that may use different location naming conventions.

## Key Features

* Create matching rules for location identification
* Support multiple identifier formats per location
* Handle variations in location naming
* Fuzzy matching capabilities
* Priority-based matching rules
* Test matchers before applying to imports
* Track matching success rates
* Manage exceptions and unmatched records

## Use Cases

* Map lease-well combinations to location IDs
* Handle API numbers and government identifiers
* Match customer location names to internal codes
* Support multiple naming conventions from different data sources
* Resolve duplicate or ambiguous location identifiers

## Creating Matchers

1. Identify the external identifier format
2. Create a matching rule or pattern
3. Link to the corresponding Atlas location
4. Test the matcher with sample data
5. Apply to import processes
6. Monitor and refine as needed

