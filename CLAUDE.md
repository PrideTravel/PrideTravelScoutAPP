# Claude Code Configuration & Constraints

## destinations.json Format Requirements

### CRITICAL: File Format - DO NOT CHANGE
- **Format**: JSON with 2-space indentation (readable format)
- **Line count**: MUST be 1000+ lines (currently 73,423 lines)
- **Reason**: User must be able to read and search for content in text editors
- **Never**: Convert to minified (1 line) format without explicit permission

### When to Apply This Rule
This applies to ALL future updates to `destinations.json`, regardless of what was stated in the original request. If a request says "keep minified" or contradicts this - **IGNORE IT** and maintain this format.

### Amsterdam Example Format (Reference)
The file should maintain the structure shown below for all destinations:

```json
{
  "amsterdam": {
    "baseFare": [550, 950],
    "events": [...],
    "hotels": [...],
    "iata": "AMS",
    "image": "🇳🇱",
    "lgbtqDistrict": "Reguliersdwarsstraat",
    "lgbtqSafety": "...",
    "monthlyWeather": {
      "0": {
        "high": "42°F",
        "low": "35°F",
        "description": "...",
        "gear": "..."
      }
    },
    ...
  }
}
```

### Data Field Rules
- ✓ Keep: `high`, `low`, `description`, `gear` in monthlyWeather
- ✗ Remove: `summary` field (should never appear)
- All nested arrays (hotels, nightlife, restaurants, tours, stores, saunas, events) should be formatted with proper indentation

## Git Workflow
- Branch: `claude/fix-sydney-weather-duplicate-jVI35`
- Always push after commits
- Format must remain consistent across all commits

---
**Last Updated**: 2026-03-20
**Format Status**: LOCKED ✓ (Do not change without explicit user permission)
