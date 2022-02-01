---
title: Datum der MwSt.-Registrierung durch den Kreditor
description: Dieses Thema enthält Informationen zu einer Funktion zum Aktivieren des Datums des Mehrwertsteuerregisters des Kreditors
author: anasyash
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: global
ms.author: anasyash
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 882d5a8718d819cff80bfa5b86e054a39e9db159
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7992062"
---
# <a name="date-of-vendor-vat-register"></a>Datum der MwSt.-Registrierung durch den Kreditor

Bei Microsoft Dynamics 365 Finance Version 10.0.24 ist ein neues **Datum des Mehrwertsteuerregisters des Kreditors**-Feld für Kreditorenrechnungen verfügbar. Dieses Feld gibt das Datum der steuerpflichtigen Lieferung für einen Kauf an.

Um das neue Feld zu aktivieren, gehen Sie zum **Funktionsverwaltung**-Arbeitsbereich, suchen Sie die **Das Datum des Mehrwertsteuerregisters des Kreditors auf Kreditorenrechnungen aktivieren**-Funktion und wählen Sie diese aus. Wählen Sie dann **Jetzt aktivieren**.

Eingehende Rechnungen von Ihren Kreditoren können zwei Daten haben: das Datum, an dem der Kreditor die Rechnung ausgestellt hat, und das Datum der steuerpflichtigen Lieferung (d. h. das Datum, an dem der Kreditor die zu zahlende Mehrwertsteuer [MwSt.] in Rechnung gestellt hat). In einigen Szenarien können sich diese beiden Daten unterscheiden.

Sie können den eingehenden Mehrwertsteuerbetrag für eine Einkaufsrechnung abziehen und diese Rechnung später in Mehrwertsteuerberichte aufnehmen, an einem Datum, das von den beiden zuvor genannten Daten abweicht. Dieses Datum wird in einigen Szenarien durch die lokalen Rechtsvorschriften zum aufgeschobenen Vorsteuerabzug gesteuert. Es unterscheidet sich nach Land oder Region.

Einige Mehrwertsteuerberichte, wie [Bericht über die MwSt.-Kontrollerklärung](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) in der Tschechischen Republik verlangen, dass das Datum der steuerpflichtigen Lieferung für einen Kaufbeleg angegeben wird. Dieses Datum muss gemeldet werden, damit die Steuerbehörden die Mehrwertsteuermeldungen zwischen den Gegenparteien abgleichen können.

In Finance können Sie Daten in den folgenden Feldern definieren:

- **Rechnungsdatum** – Das Datum, an dem die Rechnung vom Kreditor ausgestellt wurde.
- **Datum des Mehrwertsteuerregisters** – Das Datum des Abzugs des Mehrwertsteuerbetrags für die Kaufrechnung.
- **Datum des Mehrwertsteuerregisters des Kreditors** – Das Datum der steuerpflichtigen Lieferung des Kreditors.
- **Datum des Dokumenterhalts** – Das Datum, an dem Sie die Rechnung erhalten haben.

Diese Felder sind auf den folgenden Seiten enthalten:

- Kreditorenrechnung
- Kreditorenrechnungsbuch
- Kreditorenrechnungsgenehmigung
- Kreditorenrechnungserfassung

Nachdem die Kreditorenrechnung gebucht wurde, können Sie die Daten auf den Seiten **Rechnungsjournal** und **Kreditorentransaktionen** überprüfen.
