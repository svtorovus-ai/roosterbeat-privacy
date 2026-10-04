# RoosterBeat Privacy — guide

## Source relationship

```text
RoosterBeat source
  ├─ mobile manifest/services
  └─ wear manifest/services
          ↓
privacy/data-safety review
          ↓
roosterbeat-privacy publication
          ↓
Google Play listing/disclosure
```

## Current declared behavior

Policy currently states local gesture sensor processing, Wearable Data Layer sync, local calibration settings, media control, notification listener and Wear AccessibilityService for bezel.

These are documentation claims and must be revalidated against source before each material Play release.

## Review checklist

Search RoosterBeat source for:
- INTERNET;
- ACCESS_NETWORK_STATE;
- analytics/crash SDK;
- HTTP clients;
- sensor listeners;
- SharedPreferences/DataStore;
- notification listener;
- AccessibilityService config;
- Wearable DataClient/MessageClient;
- contacts/location/files;
- advertising identifiers.

Then reconcile policy.

## Changes requiring policy review

- new permission;
- new external server;
- crash/analytics SDK;
- account/login;
- cloud backup;
- user-generated content upload;
- broader accessibility;
- notification-content processing;
- sensor persistence;
- new retention behavior.

## Publication acceptance

- effective date current for material change;
- Ukrainian and English sections semantically consistent;
- package id correct;
- no claims contradicted by manifest;
- Google Play Data Safety matches;
- prominent disclosure text matches behavior;
- public page renders.
