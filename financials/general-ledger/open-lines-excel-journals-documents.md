---
title: "Veröffentlicht Sie Erfassungspositionen und Dokumente von Excel"
description: "In diesem Thema wird erläutert, wie Positionen für allgemeine Erfassungen aus Microsoft Excel schließt und veröffentlicht. Er umfasst Informationen zu verschiedenen Vorlagen, die Sie verwenden können, abhängig vom Buchungstyp ein, den Sie eingeben."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Veröffentlicht Sie Erfassungspositionen und Dokumente von Excel

In diesem Thema wird erläutert, wie Positionen für allgemeine Erfassungen aus Microsoft Excel schließt und veröffentlicht. Er umfasst Informationen zu verschiedenen Vorlagen, die Sie verwenden können, abhängig vom Buchungstyp ein, den Sie eingeben.

Benutzer können Positionen für Finanzerfassungen aus Microsoft Excel eingeben und veröffentlichen. Nachdem ein Benutzer eine Erfassung erstellt, die zeigt ** offene Positionen in Excel ** Schaltfläche die Vorlagen an, die zur Verfügung stehen. Vorlagen sind so entworfen, dass bestimmte Szenarien zu unterstützen, jedoch nicht alle der Kontenart in Kombination die Erfassung unterstützt wird. In der folgenden Tabelle werden die Vorlagen, die verfügbar sind und die Kontenart an, die sie unterstützt wird.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | ** Unterstützte Kontenart **                                                                                             | ** Enthält Informationen zum Zugreifen ** Vorlage                                                          |
| Sachkontoerfassungspositionen     | Konto: Sachkonto, Debitor, Kreditor, Bank-Gegenkonto: Sachkonto, Debitor, Kreditor, Bank-Intercompany wird unterstützt.       | Allgemeine Erfassung                                                                         |
| Rechnungsbuch         | Konto: Kreditoren-Gegenkonto: Sachkonto-Intercompany wird nicht unterstützt.                                                    | Kreditorenrechnungsbuch                                                                     |
| Rechnungserfassung          | Konten: Kreditoren-Gegenkonto: Sachkonto-Intercompany wird unterstützt.                                                      | Kreditorenrechnungserfassung                                                                      |
| Kreditorenrechnung           |                                                                                                                         | Kreditorenrechnung                                                                          |
| Debitorenrechnungserfassung | Konto: Debitoren-Gegenkonto: Sachkonto-Intercompany wird unterstützt.                                                     | Allgemeine Erfassung                                                                         |
| Freitextrechnung        |                                                                                                                         | ** Auf der Freitextrechnung auf ** ** Seite geöffnet in Excel ** (das Microsoft Office-Symbol). |
| Anlagenerfassung     | Anlage dem Sachkonto, an die Bank, für den Debitor oder Kreditor. Intercompany ist nicht unterstützt.                                               | Anlagenerfassung                                                                     |
| Kreditorenzahlungserfassung   | Konto: Kreditoren-Gegenkonto: Sachkonto, Bank-Intercompany wird unterstützt.                                                 | Kreditorenzahlungserfassung                                                                  |
| Debitorzahlungserfassung | Konto: Debitoren-Gegenkonto: Sachkonto, Bank-Intercompany wird unterstützt.                                               | Debitorzahlungserfassung                                                                |
| Projektausgabenerfassung  | Konto: Projekt, Sachkonten, Debitoren-, Kreditoren-Gegenkonto: Projekt, Sachkonten, Debitoren-, Kreditoren-Intercompany wird unterstützt. | Ausgaben der allgemeinen Erfassung unter (Projektverwaltung und- verrechnung)                       |

Wenn die Positionen veröffentlicht werden, sie werden geprüft, um sicherzustellen, dass sie mit den Regeln entsprechen, die den in Finanzerfassungen eingerichtet werden. Nachdem die veröffentlicht Positionen sind, können Benutzer die Belege von Microsoft Dynamics 365 für Arbeitsgänge bearbeiten oder buchen. 

Um Finanzdimensionen einer Vorlage hinzugefügt werden soll, sind zusätzliche Änderungen erforderlich. Weitere Informationen finden Sie [fügen Sie Dimensionen der Microsoft Excel-Vorlage] Entwickler-itpro hinzufügen "\ \ Finanz-Dimensionen \ Hinzugefügte-Dimension-ExcelVorlagen). Nachdem sich mit Dimensionen befassen Entität hinzugefügt wurden, werden sie im Excel-Designer verfügbar und können zur Vorlage hinzugefügt werden.




