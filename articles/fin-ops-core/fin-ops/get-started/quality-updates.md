---
title: Proaktive Qualitätsupdates
description: Dieser Artikel enthält Informationen zur proaktiven Bereitstellung von Qualitätsupdates.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7d8de017c54a13a9935d74d33a57813922c9f823
ms.sourcegitcommit: 8aee31d6dffabe13969dd5b9de4e0bf95f53e67e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887129"
---
# <a name="proactive-quality-updates"></a>Proaktive Qualitätsupdates

[!include[banner](../includes/banner.md)]

In den letzten Jahren hat Microsoft kontinuierliche Fortschritte bei dem gemacht, was wir als [One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md) bezeichnen. Die Prämisse von One Version ist einfach: Je näher wir dem Ziel kommen, dass alle Kunden die gleiche Softwareversion zu haben, desto höher ist die Qualität, die wir liefern können. Wir finden und beheben Probleme einmal und geben diese Lösungen schneller an mehr Kunden weiter.

Die Ergebnisse bestätigen diese Prämisse: geringere Vorfallzahlen bei unseren Produkten. Wenn Kunden nicht dieselbe Version verwenden, stellen wir regelmäßig fest, dass sie Problemen haben, für die bereits eine Lösung vorliegt. Wir haben bereits große Fortschritte mit Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations und Dynamics 365 Commerce gemacht und dank der jüngsten technischen Fortschritte ist es jetzt möglich, den nächsten Schritt zu tun. Die folgenden Informationen beschreiben, was wir tun werden, was wir bereits getan haben, um die Voraussetzungen zu schaffen, und wie und wann wir die neuen Funktionen störungsfrei einführen werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

- Proaktive Qualitätsupdates (PQU) werden monatlich angewendet.
- Ausnahmen für proaktive Qualitätsaktualisierungen werden nur für Kunden zugelassen, die von der US-amerikanischen Food and Drug Administration (FDA) reguliert werden.
- Proaktive Qualitätsupdates führen niemals zu einem Downgrade der Umgebung oder einem automatischen Upgrade von einer Service-Update-Version auf eine andere. 
- Microsoft legt fest, wie proaktive Qualitätsupdates für regulierte Umgebungen und für staatliche und staatliche Cloud-Kunden verwaltet werden.
- Benachrichtigungen zu proaktiven Qualitätsaktualisierungen werden im [Microsoft 365 Nachrichtencenter](https://admin.microsoft.com/AdminPortal/) gebucht.
- Fünf Tage bevor ein proaktives Qualitätsupdate auf eine Umgebung angewendet wird, werden Kunden benachrichtigt, dass das Update durchgeführt wird.
- Kunden können proaktive Qualitätsupdates nicht stornieren oder verschieben.
- Proaktive Qualitätsupdates werden während dem regionsspezifischen [geplanten Wartungsfenster](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) installiert.
- Qualitätsupdates sind so konzipiert, dass sie ein geringes Risiko von Problemen oder Regressionen aufweisen, und dies wird von Microsoft-Daten unterstützt.
- Microsoft empfiehlt gezielte Tests für bestimmte Probleme oder bestimmte Hotfixes, die mit einem proaktiven Qualitätsupdate zusammenhängen.
- ALLE Sandboxes, mit Ausnahme derjenigen, für die aus regulatorischen Gründen eine zeitgebundene Ausnahme gilt, werden bis zum 7. Januar 2023 integriert.
- Das Produktions-Onboarding für proaktive Qualitätsupdates beginnt am 21. Januar 2023. 
- Das Produktions-Onboarding beginnt nur für Lifecycle Services-Projekte, die über Sandbox(en) verfügen und bisher proaktive Qualitätsupdates in regelmäßigen Abständen für alle unterstützten Service-Update-Versionen erhalten. Dies gilt nur für Kundenumgebungen, denen aus regulatorischen oder anderen rechtlichen Gründen keine Ausnahmen gewährt wurden.
- Einen vollständigen Zeitplan proaktiver Qualitätsupdates für Sandbox- und Produktionsumgebungen im Laufe des Jahres 2023 finden Sie unten.
- Bei jedem Service-Update läuft mindestens ein PQU-Release-Train oder soll beginnen. Sobald Ihre Umgebungen in den PQU-Prozess aufgenommen wurden, erhalten Sie möglicherweise ein vorab geplantes proaktives Qualitätsupdate für alle, wenn Sie zu einem Dienstupdate einer neueren Version wechseln. Bitte überprüfen Sie den Zeitplan, um festzustellen, wann eine PQU für ein Service-Update geplant ist, wenn Sie ein Upgrade auf eine neuere Version des Service-Updates planen. 

> [!Note]
> Standard-Leistungstest (Tier4), Premium-Leistungstest (Tier5) Sandboxen und Produktionsumgebungen erhalten PQUs am Wochenende. 

## <a name="focus-on-quality-updates"></a>Schwerpunkt Qualitätsupdates

Wir bieten derzeit pro Jahr sieben [Dienstupdates](public-preview-releases.md) an. Version 10.0.29 ist zum Beispiel ein Dienstupdate. Bis vor Kurzem gab es acht Updates pro Jahr. Wir haben jedoch ein Update abgeschafft, da Kundenfeedback nahelegte, dass unsere Kunden Änderungen gegen Ende des Kalenderjahres lieber vermeiden möchten.

Wir werden die Intervalle der Dienstupdates nicht ändern. Stattdessen konzentrieren wir uns bei unserem nächsten Schritt auf dem Weg zu One Vision auf *Qualitätsupdates*. Qualitätsupdates sind kumulative Builds von Hotfixes. Sie enthalten keine neuen Funktionen. Unsere gesamte Kunden-Community ist zu jedem Zeitpunkt auf die drei oder vier neuesten Dienstupdates verteilt. Es kann jedoch ein, dass innerhalb der Gruppe für ein bestimmtes Dienstupdate Dutzende verschiedener Qualitätsupdateversionen verwendet werden, je nach den Daten, an denen die Personen bereitgestellt wurden. Im nächsten Schritt werden wir Qualitätsupdates proaktiv bereitstellen. Wir verwenden dieses Modell bereits für unsere Dataverse-basierten Anwendungen und konnten die erwarteten Ergebnisse im Hinblick auf verbesserte Qualität und weniger Supportfälle erreichen.

Natürlich könnte eine Reduzierung von Fehlern die Notwendigkeit von Qualitätsupdates verringern oder vollständig eliminieren. Es laufen mehrere Initiativen, um die Fehler zu reduzieren, für die Qualitätsupdates notwendig sind. Selbst wenn die Nutzlasten im Qualitätsupdate reduziert werden, verbessert die Konsistenz im gesamten Kundenstamm die Supportfähigkeit, bringt Kunden schneller Verbesserungen und verringert die Häufigkeit, mit der Kunden auf Probleme stoßen, für die bereits Lösungen vorliegen.

## <a name="making-proactive-distribution-possible"></a>Proaktive Bereitstellung möglich machen

Es wurden bereits mehrere Fortschritte umgesetzt, die eine proaktive Bereitstellung von Qualitätsupdates ermöglichen:

- **Aktualisierung nahezu ohne Downtime**: Um häufigere Umgebungen zu fördern, ist es wichtig, dass die Auswirkungen auf die Verfügbarkeit der Umgebung reduziert werden, um Vereinbarungen zum Servicelevel (SLAs) für Dynamics 365 aufrechtzuerhalten. Die Aktualisierung nahezu ohne Downtime wurde ursprünglich eingeführt, um das monatliche Betriebssystem-Patching zu verbessern, indem ein Cluster-Failover verwendet wird, um das aktualisierte Image mit minimaler Unterbrechung zu aktivieren. Der Mechanismus zum Anwenden von Updates wird verbessert, sodass er noch weniger störend ist, und er deckt dann sowohl das Betriebssystem-Patching als auch die Bereitstellung hochwertiger Updates ab.

    Bei interaktiven Benutzern wird eine aktive Sitzung möglicherweise unterbrochen, und die Wiederholung erfolgt in der jetzt aktualisierten Umgebung. Mit der Einführung von [prioritätsbasierten Stapelplanung](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), wird die Stapelplanung und -verarbeitung sofort nach dem Update wiederhergestellt und fortgesetzt. Für Kunden wird eine prioritätsbasierte Stapelplanung eingerichtet, bevor sie an der proaktiven Verteilung von Qualitätsupdates für ihre Produktionsumgebungen teilnehmen.

- **Nutzungsschwache Zeiten**: Nutzungsschwache Zeiten sind für jede Azure-Region festgelegt und während der Dark Hour-Periode werden Aktualisierungen nahezu ohne Downtime werden in diesem Zeitraum durchgeführt.

## <a name="the-proactive-update-process"></a>Der proaktive Updateprozess

Die Bereitstellung proaktiver Qualitätsupdates folgt einem sicheren Bereitstellungsprozess (SDP). Die Besonderheiten des SDP werden sich weiterentwickeln, aber Qualitätsupdates werden zunächst in Sandbox-Umgebungen bereitgestellt. Wenn der Prozentsatz der erfolgreich bereitgestellten Sandboxes zunimmt, beginnt die Bereitstellung in Produktionsumgebungen. Überwachungssysteme überwachen Systemtelemetrie- und Live-Website-Vorfälle und stoppen die Einführung einer bestimmten Version, wenn eine Regression erkannt wird. Kunden können die Qualitätsupdates weiterhin vor der proaktiven Bereitstellung abrufen, wenn sie dies wünschen.

Aktuelle Versionsverwaltungsdaten zeigen, dass weniger als 3 Prozent der Regressionen in Qualitätsupdates eingeführt werden. Mit einem verstärkten Fokus auf die Eliminierung von Regressionen und einem verbesserten SDP werden die potenziellen Auswirkungen von Regressionen erheblich geringer sein als die Gewinne bei der Qualität, die durch eine schnellere Bereitstellung von Fixes für Kunden auf breiter Basis erzielt werden.

## <a name="process-changes"></a>Änderungen verarbeiten

Vor der Aktivierung der proaktiven Bereitstellung von Qualitätsupdates wird eine Reihe von Prozessänderungen implementiert:

- **Schema**: Tools stellen sicher, dass hochwertige Update-Builds nur Schemaänderungen enthalten, die angewendet werden können, während der Dienst online ist. Dieser Ansatz trägt dazu bei, die Möglichkeit zu bewahren, das Update nahezu ohne Ausfallzeit anzuwenden.
- **Verstärkte Änderungsprüfung**: Derzeit gibt es bereits einen zusätzlichen Prozessschritt, um Änderungen für die Aufnahme in ein Qualitätsupdate zu genehmigen. Die Prüfung im zusätzlichen Schritt wird verstärkt, um das Potenzial für Regressionen zu verringern. Breaking Changes sind in Qualitätsupdates nicht zulässig, und die verstärkte Änderungsprüfung wird dazu beitragen, dass wir dieses Ziel erreichen.
- **Sichtbarkeit**: Benachrichtigungen für bevorstehende proaktive Qualitätsupdates werden über das Admin Center, Lifecycle Services (LCS) und andere verfügbare Kanäle gesendet. Darüber hinaus haben Supportteams und Vorfallleiter Einblick darin, wo Qualitätsupdates proaktiv bereitgestellt wurden.

    > [!NOTE]
    > Das Microsoft Communications-Team untersucht eine anhaltende Verschlechterung der E-Mail-Tools, die die Zustellung von E-Mail-Benachrichtigungen verhindert. Bitte beobachten Sie die weiter Microsoft 365 Message Center für Onboarding- und Benachrichtigungsnachrichten.

- **Fail Safe via Flighting** - Flighting wird verwendet, um Codeänderungen zu schützen, wo immer dies in einem Qualitätsupdate-Fehlerbehebung möglich ist, oder die bestehende Funktion Flighting zu verwenden, die für die Korrektur relevant ist. Wenn nach einer proaktiven Bereitstellung ein Fallback oder das Ausschalten einer Änderung erforderlich ist, kann dies über das Flighting-System erfolgen, um weitere Fehler zu vermeiden.
- **Sandbox-Synchronisierungskennzeichnung** – Ein gestaffeltes Update auf eine isolierte Sandbox nach Wahl zusammen mit der Produktion wird derzeit nicht unterstützt. Alle Tier-2- und Tier-3-Sandboxes erhalten proaktive Updates mindestens 7 Tage vor der Produktionsumgebung in einem Lifecycle Services-Projekt. Dies gilt wieder nur für Kundenumgebungen, denen aus regulatorischen oder anderen rechtlichen Gründen keine Ausnahmen gewährt wurden.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Wie sieht die Rollout-Roadmap für Qualitätsupdates aus?

Die Verteilung von proaktiven Qualitätsupdates für Sandbox-Umgebungen begann September 2022 für Azure Public Cloud-Kunden. Bis zum 1. Januar 2023 werden wir das Onboarding von 99 % der Sandboxes für proaktive Qualitätsupdates abschließen.

Ausnahmen vom proaktiv aktualisierten Bereitstellungsprozess sind nur für FDA-regulierte Kunden zulässig. Wir arbeiten noch daran, wie regulierte Umgebungen und staatliche Cloud-Kunden verwaltet werden sollen. 

Da Kunden regelmäßig kleinere Nutzlasten erhalten, erwarten wir, dass es einfacher wird, auf dem Laufenden zu bleiben. Wir werden die Häufigkeit der Update-Bereitstellung anpassen, wenn wir den Prozess nachweislich ohne Unterbrechung ausführen können. Dieser Prozess funktioniert für unsere Dataverse-Plattform und -Anwendungen bereits effektiv und liefert die erwarteten Verbesserungen der Servicequalität. Wir machen den gleichen Schritt nach vorne unbedingt auch für Finanz- und Betriebsanwendungen.


## <a name="when-will-quality-updates-start-for-production-environments"></a>Wann beginnen Qualitätsupdates für Produktionsumgebungen?
In den ersten Monaten des Jahres 2023, beginnend am 15. Januar, werden wir mit dem Onboarding von Produktionsumgebungen für proaktive Updates beginnen und den Prozentsatz der Produktionsumgebungen, die proaktive Updates erhalten, schrittweise erhöhen. Wir zielen nur auf eine Produktionsumgebung in einem Lifecycle Services-Projekt ab, in der die Sandbox-Umgebungen bereits integriert sind, um proaktive Updates zu erhalten. Vor einem Update werden Kunden mit integrierten Produktionsumgebungen über das Message Center oder das Lifecycle Services-Banner benachrichtigt. Einen vollständigen Zeitplan proaktiver Qualitätsupdates für Sandbox- und Produktionsumgebungen im Laufe des Jahres 2023 finden Sie unten.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Wie sieht der Zeitplan für das Update der proaktiven Sandboxqualität aus?
Informationen zu den nutzungsschwachen Zeiten für jede Region finden Sie unter [Welche Wartungsfenster sind nach Region geplant?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Version des proaktiven Qualitätsupdates: 10.0.29
**Anwendungsversion: 10.0.1326.70**  
**Entsprechender aktueller KB-Artikel: 750332**

| Station | Regionen | Abgeschlossener Zeitplan | Kommender Sandbox-Zeitplan|
|---|---|---|---|
| Station 1 | Kanada, Mitte, Kanada, Osten, Frankreich, Mitte, Indien, Mitte, Norwegen, Osten, Schweiz, Westen | 14. Oktober bis 17. Oktober 2022, 2. November bis 5. November 2022, 13. November bis 16. November 2022, 5. Dezember bis 8. Dezember 2022 | 2. Januar bis 5. Januar 2023 |
| Station 2 | Frankreich, Süden, Indien, Süden, Norwegen, Westen, Schweiz, Norden, Südafrika, Norden, Australien Osten, Vereinigtes Königreich, Süden, VAE, Norden, Japan, Osten, Australien, Südosten, Südostasien | 15. Oktober bis 18. Oktober 2022, 2. November bis 5. November 2022, 13. November bis 16. November 2022, 5. Dezember bis 8. Dezember 2022 | 2. Januar bis 5. Januar 2023 |
| Station 3 | Ostasien, Vereinigtes Königreich, Westen, Japan, Westen, Brasilien, Süden, Westeuropa, USA, Osten, VAE, Mitte | 16. Oktober bis 19. Oktober 2022, 2. November bis 5. November 2022, 13. November bis 16. November 2022, 5. Dezember bis 8. Dezember 2022 | 2. Januar bis 5. Januar 2023 |
| Station 4 | Nordeuropa, USA, Mitte, USA, Westen | 17. Oktober bis 20. Oktober 2022, 2. November bis 5. November 2022, 15. November bis 18. November 2022, 5. Dezember bis 8. Dezember 2022 | 2. Januar bis 5. Januar 2023 |
| Station 5 | DoD, Community-Cloud der Regierung, China | Nicht geplant | Nicht geplant |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> Version des proaktiven Qualitätsupdates: 10.0.30
**App-Version: 10.0.1362.77**
**Entsprechender aktueller KB-Artikel: 767597**

| Station | Regionen | Abgeschlossener Zeitplan | Kommender Sandbox-Zeitplan |
|---|---|---|---|
| Station 1 | Kanada, Mitte, Kanada, Osten, Frankreich, Mitte, Indien, Mitte, Norwegen, Osten, Schweiz, Westen | 1. Dezember bis 4. Dezember 2022 |  13. Dezember bis 16. Dezember 2022 | 
| Station 2 | Frankreich, Süden, Indien, Süden, Norwegen, Westen, Schweiz, Norden, Südafrika, Norden, Australien Osten, Vereinigtes Königreich, Süden, VAE, Norden, Japan, Osten, Australien, Südosten, Südostasien | 2. Dezember bis 5. Dezember 2022 |  13. Dezember bis 16. Dezember 2022 | 
| Station 3 | Ostasien, Vereinigtes Königreich, Westen, Japan, Westen, Brasilien, Süden, Nordeuropa, USA, Osten, VAE, Mitte | 3. Dezember bis 6. Dezember 2022 |  13. Dezember bis 16. Dezember 2022 | 
| Station 4 | Westeuropa, USA, Mitte, USA, Westen | 4. Dezember bis 7. Dezember 2022 |  13. Dezember bis 16. Dezember 2022 | 
| Station 5 | DoD, Community-Cloud der Regierung, China | Nicht geplant | Nicht geplant |

### <a name="proactive-quality-update-calendar-year-2023-schedule"></a><a name="schedule"></a> Proaktive Qualitätsaktualisierung Zeitplan für das Kalenderjahr 2023

#### <a name="stations-to-region-mapping"></a><a name="Stations-Regions"></a> Zuordnung von Stationen zu Regionen

| Stationen | Regionen |
|---|---|
| Station 1 | TBD |
| Station 2 | Kanada, Mitte, Kanada, Osten, Frankreich, Mitte, Indien, Mitte, Norwegen, Osten, Schweiz, Westen |
| Station 3 | Frankreich, Süden, Indien, Süden, Norwegen, Westen, Schweiz, Norden, Südafrika, Norden, Australien Osten, Vereinigtes Königreich, Süden, VAE, Norden, Japan, Osten, Australien, Südosten, Südostasien |
| Station 4 | Ostasien, Vereinigtes Königreich, Westen, Japan, Westen, Brasilien, Süden, Nordeuropa, USA, Osten, VAE, Mitte |
| Station 5 | Westeuropa, USA, Mitte, USA, Westen |
| Station 6 | DoD, Community-Cloud der Regierung, China |


> [!IMPORTANT]
> Dies ist ein Zeitplan auf hohem Niveau für das Jahr 2023. Einen konkreteren Zeitplan finden Sie im folgenden Beispiel für Januar 10.0.30 Release-2. Der genaue Fahrplan und die App-Version werden 7 Tage vor dem Start eines Qualitätsupdatezuges aktualisiert.

> [!Note]
> Nur die integrierten Produktionsumgebungen erhalten das Update für 10.0.30 Release-2-Train, integrierte Umgebungen erhalten eine explizite Kommunikation.

| Qualitätsupdate trainieren | Freigabe eingestellt | Trainingsdauer |
|---|---|---|
| 10.0.30 Version-2 | 16. Dezember 2022 | 2. Januar bis 29. Januar 2023 |
| 10.0.30 Version-3 | 13. Januar 2023 | 30. Januar bis 25. Februar 2023 |
| 10.0.30 Version-4 | 24. Februar 2023 | 6. März bis 8. April 2023 |
| 10.0.31 Version-1 | 3. Februar 2023 | 13. Februar 2023 bis 18. März 2023|
| 10.0.31 Version-2 | 3. März 2023 | 13. März bis 15. April 2023|
| 10.0.31 Version-3 | 14. April 2023 | 24. April 2023 bis 27. Mai 2023|
| 10.0.32 Version-1 | 31. März 2023 | 10. April 2023 bis 13. Mai 2023|
| 10.0.32 Version-2 | 28. April 2023 | 8. Mai 2023 bis 10. Juni 2023|
| 10.0.32 Version-3 | 26. Mai 2023 | 5. Juni 2023 bis 8. Juli 2023|
| 10.0.33 Version-1 | 28. April 2023 | 8. Mai 2023 bis 10. Juni 2023|
| 10.0.33 Version-2 | 26. Mai 2023 | 5. Juni 2023 bis 8. Juli 2023|
| 10.0.33 Version-3 | 14. Juli 2023 | 24. Juli 2023 bis 26. August 2023|
| 10.0.34 Version-1 | 23. Juni 2023 | 3. Juli 2023 bis 5. August 2023|
| 10.0.34 Version-2 | 21. Juli 2023 | 31. Juli bis 2. September 2023|
| 10.0.34 Version-3 | 1. September 2023 | 11. September bis 14. Oktober 2023|
| 10.0.35 Version-1 | 28. Juli 2023 | 7. August 2023 bis 9. September 2023|
| 10.0.35 Version-2 | 25. August 2023 | 4. September 2023 bis 7. Oktober 2023|
| 10.0.35 Version-3 | 20. Oktober 2023 | 30 Oktober 2023 bis 16. Dezember 2023|
| 10.0.36 Version-1 | 29. September 2023 | 9. Oktober 2023 bis 11. November 2023|
| 10.0.36 Version-2 | 27. Oktober 2023 | 6. November 2023 bis 16. Dezember 2023|
| 10.0.36 Version-3 | 12. Januar 2024 | 22. Januar 2023 bis 24. Februar 2024|
| 10.0.37 Version-1 | 3. November 2023 | 13. November 2023 bis 6. Januar 2024|
| 10.0.37 Version-2 | 30. Dezember 2023 | 8. Januar 2024 bis 10. Februar 2024|
| 10.0.37 Version-3 | 27. Januar 2024 | 5. Februar 2024 bis 9. März 2024|
| 10.0.37 Version-4 | 23. Februar 2024 | 4. März 2024 bis 6. April 2024|

### <a name="proactive-quality-update-upcoming-10030-release-2-train-schedule"></a><a name="schedule"></a> Proaktives Qualitätsupdate in Kürze 10.0.30 Release-2-Zugfahrplan
**Anwendungsversion: 10.0.1362.99**

| Stationen | Kommender Sandbox-Zeitplan | Anstehender Produktionsplan |
|---|---|---|
| Station 1 | NA | NA |
| Station 2 | 2. Januar bis 5. Januar 2023 | 21. Januar bis 22. Januar 2023 |
| Station 3 | 3. Januar bis 6. Januar 2023 | 28. Januar bis 29. Januar 2023 |
| Station 4 | 9. Januar bis 12. Januar 2023 | NA |
| Station 5 | 16. Januar bis 19. Januar 2023 | NA |
| Station 6 | NA | NA |

> [!IMPORTANT] 
> Fünf Tage im Voraus aktualisiert Microsoft den vorhergehenden Zeitplan und sendet eine Benachrichtigung für die Gruppe von Umgebungen, die diese Qualitätsupdates erhalten sollen. Der vorstehende Zeitplan gilt nur für Umgebungen, die über ein bevorstehendes Update benachrichtigt wurden. Informationen zu den nutzungsschwachen Zeiten für jede Region finden Sie unter [Welche Wartungsfenster sind nach Region geplant?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> Für jede Regionsgruppe bzw. *Station*, wo derzeit ein Qualitätsupdate bereitgestellt werden soll, zeigt der Zeitplan eine Spanne von vier Tagen. Qualitätsupdates beginnen nur mit Sandbox-Umgebungen. Wenn der Prozentsatz der erfolgreich bereitgestellten Sandboxes zunimmt, beginnt die Bereitstellung in Produktionsumgebungen mit einer vorherigen Benachrichtigung an Kunden.
> 
> Qualitätsupdates werden immer fortlaufend erfolgen, was es uns ermöglicht, eine Reihe von Umgebungen pro Zeitplan anzuvisieren und alle Sätze bis zum Ende des vierten Tages für eine Station abzuschließen. Dies bedeutet jedoch nicht, dass ein Umgebungsupdate vier Tage dauert. Es bedeutet lediglich, dass wir nicht im Voraus bestimmen können, welche Umgebungen an einem bestimmten Tag innerhalb des Zeitraums von vier Tagen aktualisiert werden. Alle Updates werden während der dunklen Stunden mit nahezu null Ausfallzeiten durchgeführt. Updates werden definitiv innerhalb des Fensters der dunklen Stunden einer bestimmten Region enden.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Wie werden die dunklen Stunden für Kunden gehandhabt, die über eine Finanz- und Betriebs-App-Instanz verfügen, aber in mehreren Zeitzonen aktiv sind? 
Es gibt keine speziellen Zeitpläne außerhalb der nutzungsschwachen Zeiten, in denen eine Instanz von Finanz- und Betriebs-Apps vorhanden ist, da wir planen, Qualitätsupdates auf minimal störende Weise mit [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean) einzuführen.

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Wie sieht die aktuelle Bereitstellungskadenz für proaktive Qualitätsupdates aus?
Proaktive Qualitätsupdates (PQUs) werden derzeit für jede unterstützte Version eines Service-Updates einmal im Monat versendet. Für ausgewählte Sandbox-Umgebungen wird nur ein Update pro Monat gepusht, es sei denn, Kunden wechseln zu einer neuen Service-Update-Version. In diesem Fall erhalten sie möglicherweise eine vorgeplante PQU als Teil eines bestehenden Zuges für das neue Service-Update. Nachdem die weltweite Bereitstellung im Jahr 2023 abgeschlossen ist, wird die Häufigkeit dieser Updates zunehmen. Sie werden immer mindestens einen Monat im Voraus benachrichtigt, wenn sich der Versandrhythmus ändert.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Wie stellt Microsoft die Qualität dieser Updates sicher?
Microsoft ist bestrebt, die Release-Pipeline effizient genug zu halten, um kleine Nutzlasten bereitzustellen, um die Validierungskosten niedrig zu halten. Jeder Fix in einem Qualitätsupdate durchläuft einen strengen und sicheren Bereitstellungsprozess, der dazu beiträgt, die Qualität und Zuverlässigkeit zu verbessern und dadurch die Auswirkungen auf den Kunden zu reduzieren. Die Bereitstellung erfolgt schrittweise zuerst in Sandbox-Umgebungen, gefolgt von der Produktion. Gestaffelte Bereitstellungen ermöglichen eine ordnungsgemäße Überwachung, um festzustellen, ob eine weitere Bereitstellung sicher ist. Wir stoppen die Einführung, wenn Probleme bei jeder bereitgestellten Kundengruppe festgestellt werden, und stellen sicher, dass jeder Schritt der Einführung genügend Zeit hat, damit Probleme auftauchen. Für jedes anstehende Qualitätsupdate bieten wir durch Aktualisierungen der öffentlichen Dokumentation und E-Mails Einblick in den Zeitplan, damit Kunden vorausplanen können.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Können Kunden ein Qualitätsupdate verzögern, verschieben oder anhalten?
Nein Das Hauptziel von Qualitätsupdates besteht darin, sicherzustellen, dass sich Grundlagen wie Sicherheit, Datenschutz, Zuverlässigkeit, Verfügbarkeit und Leistung für unsere Kunden kontinuierlich verbessern. Durch das Verzögern oder Anhalten eines Updates werden Sicherheit, Verfügbarkeit und Zuverlässigkeit gefährdet.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Woher weiß ich, welcher Satz von Änderungen in eine Qualitätsupdate-Nutzlast eingeflossen sind?
Führen Sie die folgenden Schritte aus, um die Liste der Änderungen zu identifizieren, die in eine Qualitätsupdate-Nutzlast einfließen. 

Verwenden Sie das Qualitätsupdate-Training 10.0.28 und die zugehörige App-Version 10.0.1265.89.

1. Melden Sie sich in Lifecycle Services an und öffnen Sie die Seite **Umgebungsdetails** für Ihre Sandbox. 
2. Wählen Sie im Abschnitt **Verfügbare Updates** die Option **Updates ansehen** für das neueste Qualitätsupdate-Build. 
3. Exportieren Sie den Build in eine CSV- oder Microsoft Excel-Datei.
4. Filtern Sie in der exportierten Datei nach der **Buildversion**, die kleiner oder gleich der Buildnummer 10.0.1265.89 ist, und wählen Sie sie aus. Sie sollten jetzt in der Lage sein, die Deltanutzlast anzuzeigen.
 
> [!NOTE]
> Der Export in eine CSV- oder Excel-Datei muss erfolgen, bevor die Umgebung aktualisiert wird. Andernfalls können Sie eine Umgebung mit einer ähnlichen Konfiguration verwenden, in der das Update nicht installiert ist, und die obigen Schritte ausführen.

[![Beispiel einer Umgebung mit Qualitätsupdate.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Wie ist der Prozess, wenn nach einem Qualitätsupdate ein kritisches Problem gefunden wird?
Ein kritisches Problem oder eine Regression sind ein oder mehrere Ereignisse, die normalerweise dazu führen, dass mehrere Kunden eine verschlechterte Erfahrung mit einem oder mehreren unserer Dienste haben. Diese Probleme können zu ungeplanten Ausfallzeiten führen, einschließlich Nichtverfügbarkeit, Leistungseinbußen und Störungen des Dienstmanagements. Wenn es aufgrund solcher Regressionen zu einer breiten Kundenauswirkung kommt, stoppen wir die Einführung eines Qualitätsupdates, bis wir das Problem kommunizieren und beheben können. In der Regel enthält das nächste Qualitätsupdate die erforderliche Korrektur, um die Einführung fortzusetzen.

Wenn eine einzelne Kundenumgebung betroffen ist, wenden Sie sich an den Microsoft-Support, um ein Ticket zu eröffnen. Basierend auf der Begründung werden wir die Einführung des Qualitätsupdates in allen anderen Umgebungen in diesem Projekt stoppen, bis das Problem behoben ist.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Können Kunden weiterhin manuell Hotfix-Updates von Lifecycle Services anwenden?
Ja. Um sicherzustellen, dass Hotfixes dauerhaft gleich funktionieren, können Hotfix-Updates weiterhin auf Kundenumgebungen in Lifecycle Services angewendet werden. Es ist jedoch wichtig zu beachten, dass Hotfixes, die als Teil eines Qualitätsupdates bereitgestellt werden, den Standard-SDP durchlaufen, bevor das Update bereitgestellt wird. Dadurch wird das Risiko von Regressionen aufgrund höherer Qualität reduziert. Wir empfehlen, dass Sie sich für eine Qualitätsaktualisierung entscheiden, anstatt Hotfixes manuell anzuwenden, um die Zuverlässigkeit zu erhöhen.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Können Kunden ein Qualitätsupdate vor dem Zeitplan proaktiv selbst installieren?
Ja. Sie können ein Qualitätsupdate proaktiv installieren. Microsoft überspringt das Update, wenn die aktuelle Build-Version der Umgebung gleich oder höher als das betreffende Qualitätsupdate ist.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Wenn für eine Umgebung innerhalb einer Woche ein geplantes monatliches Service-Update ansteht, erhält sie dann immer noch Qualitätsupdates?
- Qualitätsupdates werden nicht auf Produktionsumgebungen angewendet, wenn ein bevorstehendes Dienstupdate innerhalb einer Woche nach dem geplanten Zeitpunkt des Qualitätsupdates geplant ist.
- Wenn eine Sandbox-Umgebung dieselbe oder eine höhere Build-Version als das bevorstehende Qualitätsupdate hat, wird sie übersprungen.
- Wenn eine Produktionsumgebung dieselbe oder eine höhere Build-Version als das bevorstehende Qualitätsupdate hat, wird sie übersprungen.
- Wenn eine Sandbox aufgrund eines Qualitätsupdates oder eines manuellen Updates für die Produktion die gleiche oder eine höhere Build-Version hat, erhält die Produktion dennoch die geplante Version des monatlichen Dienstupdates. Wenn Sie nicht möchten, dass die geplante Produktionsumgebung auf die Dienstaktualisierungsversion aktualisiert wird, können Sie die Dienstaktualisierung von Lifecycle Services aus anhalten. 
- Wir empfehlen, dass Sie den neuesten Qualitätsupdate-Build verwenden, um Ihre Änderungen für ein bevorstehendes Service-Update für bessere Stabilität und Ergebnisse zu testen.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Wenn eine Umgebung eine bevorstehende geplante Aktion und ein geplantes Qualitätsupdate im selben Wartungsfenster hat, erhält sie dann trotzdem das Qualitätsupdate?
Wenn es Konflikte mit einer vorab geplanten Aktion gibt, beispielsweise einer Point-in-Time-Wiederherstellung (PITR), wird das Qualitätsupdate auf das Nächste verfügbare Wartungsfenster innerhalb des viertägigen Fensters verschoben. Weitere Informationen zum Zeitplan finden Sie unter [Wie sieht der Zeitplan für proaktive Qualitätsupdates aus?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kann eine Umgebung in ihren vorherigen Zustand zurückversetzt werden, wenn es Probleme gibt, nachdem ein Qualitätsupdate angewendet wurde?
Nachdem ein Qualitätsupdate angewendet wurde, gibt es unter keinen Umständen ein Rollback. Es sind nur Patch-Forward-Optionen verfügbar, um Probleme zu mindern.

## <a name="what-about-fda-regulation-and-gxp"></a>Was ist mit der FDA-Verordnung und GxP?
Der Plan für Kunden, die der FDA-Validierung und -Regulierung unterliegen, befindet sich noch in der Entwicklung. Erwarten Sie bald weitere Updates in diesem Bereich. Vorerst sind alle diese Kunden von Qualitätsaktualisierungen ausgenommen. Um sicherzustellen, dass ein Kunde unter die FDA-Vorschriften fällt, besuchen Sie bitte [Microsoft Azure GxP-Angebot](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Welche Versionen von Dienstupdates werden für diese Qualitätsupdates unterstützt?
Kunden mit allen unterstützten Versionen des Dienstupdates sind für diese Qualitätsupdates qualifiziert. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Die Bereitstellung von Finanz- und Betriebs-Apps mit Retail-Komponenten erfordert neben der erneuten Bereitstellung von MPOS in der Regel zusätzliche Arbeit. Wie wirken sich diese Qualitätsupdates auf das Retail SDK aus? 
Da sich die Art der Hotfixes selbst in der Nutzlast der Qualitätsupdates nicht ändert, erwarten wir derzeit keine zusätzlichen Auswirkungen, die sich zu diesem Zeitpunkt speziell auf Retail-Komponenten beziehen.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Gibt es Auswirkungen auf Cloud Hosted Environments (CHE)? 
CHE-Umgebungen sind nicht für Qualitätsupdates geeignet, da sie außerhalb des Zuständigkeitsbereichs von Microsoft liegen.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Gibt es Integrationsprobleme mit Microsoft Dataverse? 
Es sind keine Integrationsprobleme für Qualitätsupdates mit Dataverse bekannt.

