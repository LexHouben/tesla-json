# Tesla Supercharger Europe JSON

This repository contains up-to-date data of all known Tesla Supercharger locations in the Netherlands, including address, GPS coordinates, pricing details, number of stalls, and additional metadata.

## 📂 File Structure

- `all_superchargers.json`: Main data file containing all supercharger locations and their attributes.
- `parse_all_superchargers.py`: Python script used to generate and update the JSON file from raw data.

## 📦 Data Structure

The main JSON file (`all_superchargers.json`) contains two top-level keys:
- `meta`: Contains metadata such as generation date, version, and statistics.
- `locations`: An array of objects, each representing a single supercharger location.

**Example:**
```json
{
  "meta": {
    "jsonfiledate": "2025-08-06T15:37:48.232333",
    "chargerCount": 72,
    "sourceDir": "html",
    "generator": "parse_all_superchargers.py",
    "version": "1.0",
    "successCount": 72,
    "errorCount": 0
  },
  "locations": [
    {
      "filedate": "2025-07-16T19:27:37.633638",
      "name": "Harderwijk, Netherlands",
      "address": "Boekhorstlaan 4, 3847 LP Harderwijk, NL",
      "gps": {
        "lat": 52.335916,
        "lon": 5.643857
      },
      "stalls": 16,
      "maxPowerKw": 250,
      "pricing": [
        {
          "chargingLabel": "Oplaadkosten voor eigenaar van een Tesla",
          "idleFee": "€1.00/min",
          "idleLabel": "Idle fees (tot)",
          "pricingDetails": [
            {
              "label": "00:00 - 04:00",
              "rate": "€ 0,23/kWh"
            }
            // ...
          ]
        }
        // ...
      ]
    }
    // ...
  ]
}
