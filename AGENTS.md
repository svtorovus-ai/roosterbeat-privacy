# RoosterBeat Privacy — правила

## 1. Роль repo

Це disclosure/privacy publication, не source application.

Application source:
`svtorovus-ai/RoosterBeat`.

Package:
`ua.grey.roosterbeat`.

## 2. Policy має відповідати коду

Перед зміною claims звірити фактичні:
- Android manifests mobile/wear;
- services;
- network use;
- sensors;
- notification listener;
- AccessibilityService;
- analytics SDK;
- data storage;
- Wearable Data Layer.

Не писати "не збирає", якщо код уже робить інакше.
Не писати "збирає", якщо це лише permission, який не читається.

## 3. Sensitive areas

Особливо уважно:
- accelerometer/gyroscope/rotation/gravity sensors;
- notification access;
- media session;
- foreground services;
- AccessibilityService rotary/bezel;
- device-to-device Wearable API.

## 4. Accessibility disclosure

Current scope описує bezel rotary input.

Якщо AccessibilityService починає:
- retrieve window content;
- inspect text;
- perform UI actions;
- expand event types;

policy/disclosure треба переглянути.

## 5. Notification listener disclosure

Current stated purpose: playback/media detection.

Якщо source починає читати notification content, package names/history, transmitting it — policy must change.

## 6. Network claims

Не робити абсолютних тверджень про "немає Internet" без перевірки source.

Wearable Data Layer і відкриття Play Store треба описувати точно.

Якщо з'явиться:
- analytics;
- crash reporting;
- updater;
- backend;
- telemetry;

оновити policy.

## 7. Version/date

При material privacy change:
- update effective date;
- keep UA/EN meaning aligned;
- avoid contradictory sections.

## 8. Play Console consistency

Privacy page, Data Safety form і prominent disclosures повинні не суперечити одне одному.

Code change involving permission/data category має викликати privacy review.

## 9. Не комітити private data

Policy може містити public developer contacts, але не:
- signing secrets;
- API tokens;
- private account identifiers;
- debug logs.

## 10. Пов'язаний release

Privacy text має відповідати production-signed RoosterBeat release, а не лише dev branch.

Перед Play submission звір current Gradle/manifests.
