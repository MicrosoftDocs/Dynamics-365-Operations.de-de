---
title: Releaseprozess und Releaseverlauf der Planungsoptimierung
description: Dieses Thema enthält Informationen zum Releaseprozess und zum Releaseverlauf für Planungsoptimierung.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 673543ff2c9abefbca0529f35ce20bb26156acc4
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469700"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Releaseprozess und Releaseverlauf der Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Microsoft aktualisiert die Planungsoptimierung monatlich. Je nach geschäftlichen Anforderungen veröffentlichen wir jedoch gelegentlich zusätzliche Updates zwischen den geplanten Releases.

Jedes Release wird in den einzelnen Regionen veröffentlicht, in denen die Planungsoptimierung verfügbar ist. Der Prozess dauert in der Regel drei Tage.

Während die Planungsoptimierung aktualisiert wird, läuft die Produktprogrammplanung möglicherweise etwas langsamer als gewöhnlich.

Umgebungen, die die Planungsoptimierung verwenden, erhalten automatisch die neueste Version. Es ist keine Benutzeraktion erforderlich: Der Dienst wird automatisch aktualisiert. Allerdings werden Breaking-Change-Funktionalitäten niemals automatisch in Umgebungen übertragen. Standardmäßig sind alle Änderungen, die als erheblich betrachtet werden, deaktiviert und müssen explizit mit der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert werden. Daher werden diese Änderungen in Umgebungen erst angezeigt, wenn Sie sie aktivieren.

Da keine Benachrichtigungen angezeigt werden, wenn die Planungsoptimierung in Ihrer Umgebung aktualisiert wird, können Sie die Versionshinweise in der folgenden Tabelle überprüfen, um festzustellen, wann Änderungen veröffentlicht wurden und welche Funktionen sie eingeführt haben. Diese Tabelle zeigt die Änderungen, die für die Planungsoptimierung freigegeben wurden, ob diese Änderungen einer Funktion aus der Funktionsverwaltung zugeordnet sind und das Datum des Release.

| Änderungen | Funktionsverwaltungsdetails | Erscheinungsdaten |
|---|---|---|
| <p>Allgemeine Leistungs-, Qualitäts- und Stabilitätsverbesserungen.<p>[Von Planungsoptimierung zentralisierte Kalenderpflege](../supply-chain-calendars-master-planning.md)<p>[Vorschläge für die Planungsoptimierung zur Optimierung des bestehenden Vorrats](../action-messages.md)<p>[Unterstützung für die Planungsoptimierung zur Vergabe von Unteraufträgen](../../production-control/manage-subcontract-work-production.md) | Es ist keine Funktionsverwaltung erforderlich. | 7.-11. März 2022 |
| <p>Unterstützung der Planungspriorität für Produktionsaufträge hinzugefügt. | Verfügbar mit Version 10.0.25 als Teil der Funktion mit dem Namen *Prioritätsgesteuerte MRP-Unterstützung für Planungsoptimierung*. | 12.-18. November 2021 |
| <p>Allgemeine Leistungs-, Qualitäts- und Stabilitätsverbesserungen. | Es ist keine Funktionsverwaltung erforderlich. | 12.-18. November 2021 |
| <p>Unterstützung für Prozesszeitberechnungsformeln, Produktionsroute mit Überlappung und Produktionsvorgangsnummer bei Bedarfstransaktionen hinzugefügt.</p><p>Verbesserte Fehlermeldungen für die Produktionsplanung in Bezug auf Zeitüberschreitung, Kapazität konnte nicht gefunden werden und zyklische Route.</p><p>Verbesserte Konsistenz bei der Berechnung von Zugangsdaten und Ausgabedaten sowohl für Bestellvorschläge als auch für feste Bestellungen.</p><p>Allgemeine Leistungs-, Qualitäts- und Stabilitätsverbesserungen. | Funktionsname: *Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung* | 22.-27. Oktober 2021 |
| <p>Unterstützung für die Berücksichtigung des Ausschussprozentsatzes bei der Berechnung der Verarbeitungszeit hinzugefügt.</p><p>Unterstützung für Vorgangsnummer und Materialverbrauch während der Planung hinzugefügt. | Funktionsname: *Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung* | 5.-7. Oktober 2021 |
| <p>Unterstützung für Produktionsrouten-Auftragstypen hinzugefügt: **Warten davor**, **Warten danach** und **Transportzeit**.</p><p>Allgemeine Leistungs-, Qualitäts- und Stabilitätsverbesserungen. | Funktionsname: *Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung* | 25.-30. September 2021 |
| <p>Hinzugefügte Unterstützung für Produktprogrammpläne, bei der die **Planungsmethode** auf *Grobterminierung* festgelegt ist.</p><p>Beachten Sie auf der Seite **Arbeitsplangruppen** die Einstellungen für die Kontrollkästchen **Aktivierung**, **Arbeitszeit** und **Kapazität** bei Zeilen mit einem **Arbeitsplan/Einzelvorgangstyp** von *Setup* oder *Prozess*. </p><p>Allgemeine Leistungs-, Qualitäts- und Stabilitätsverbesserungen. | <p>Die Grobterminierung ist in der Funktionsverwaltung ab Version 10.0.20 verfügbar.</p><p>Funktionsname: *Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung*</p>  | 09. bis 17. September 2021 |
| Allgemeine Leistungs-, Qualitäts- und Stabilitätsverbesserungen. | Es ist keine Funktionsverwaltung erforderlich. | 25.-30. August 2021 |
| <p>Das Feld **Vorlaufzeit** wurde zu geplanten Aufträgen hinzugefügt.</p><p>Allgemeine Leistungs-, Qualitäts- und Stabilitätsverbesserungen.</p> | Es ist keine Funktionsverwaltung erforderlich. | 12.-17. August 2021 |
| <p>Anforderungen an den Ressourcentyp für die Terminierung mit unendlicher Kapazität hinzugefügt.</p><p>Verbesserte Ressourceneffizienz und Kalendereffizienz für unendliche Kapazitätsterminierung.</p><p>Weitere Informationen finden Sie unter [Zeitplanung mit unbegrenzter Kapazität](infinite-capacity-planning.md). | <p>Verfügbar in der Funktionsverwaltung ab Version 10.0.20.</p><p>Funktionsname: *Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung*</p> | 6.-12. Juli 2021 |
| Allgemeine Qualitätsverbesserungen. | Es ist keine Funktionsverwaltung erforderlich. | 6.-12. Juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
