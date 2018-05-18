---
title: "Veröffentlicht von Erfassungspositionen und Dokumente aus Excel"
description: "In diesem Thema wird erläutert, wie Positionen für allgemeine Erfassungen aus Microsoft Excel veröffentlicht. Es umfasst Informationen zu verschiedenen Vorlagen, die Sie verwenden können, abhängig vom Buchungstyp, den Sie eingeben."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a2da864254efda2621e1b157413a16d251020786
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Veröffentlicht von Erfassungspositionen und Dokumente aus Excel

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Positionen für allgemeine Erfassungen aus Microsoft Excel veröffentlicht. Es umfasst Informationen zu verschiedenen Vorlagen, die Sie verwenden können, abhängig vom Buchungstyp, den Sie eingeben.

Benutzer können Positionen für Finanzerfassungen aus Microsoft Excel eingeben und veröffentlichen. Nachdem ein Benutzer eine Erfassung erstellt, die zeigt **Positionen in Excel öffnen**-Schaltfläche die Vorlagen an, die zur Verfügung stehen. Vorlagen sind so entworfen, dass bestimmte Szenarien zu unterstützen, jedoch nicht alle der Kontenart in Kombination die Erfassung unterstützt wird. In der folgenden Tabelle werden die Vorlagen, die verfügbar sind und die Kontenart an, die sie unterstützt wird.

|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Vorlage**             | **Unterstützte Kontenarten**                                                                                             | **Informationen zum Zugreifen auf die Vorlage**                                                          |
| Sachkontoerfassungspositionen     | Konto: Sachkonto, Debitor, Kreditor, Bank-Gegenkonto: Sachkonto, Debitor, Kreditor, Bank-Intercompany wird unterstützt.       | Allgemeine Erfassung                                                                         |
| Rechnungsbuch         | Konto: Kreditoren-Gegenkonto: Sachkonto-Intercompany wird nicht unterstützt.                                                    | Kreditorenrechnungsbuch                                                                     |
| Rechnungserfassung          | Konto: Kreditoren-Gegenkonto: Sachkonto-Intercompany wird unterstützt.                                                      | Kreditorenrechnungserfassung                                                                      |
| Kreditorenrechnung           |                                                                                                                         | Kreditorenrechnung                                                                          |
| Debitorenrechnungserfassung | Konto: Debitoren-Gegenkonto: Sachkonto-Intercompany wird unterstützt.                                                     | Allgemeine Erfassung                                                                         |
| Freitextrechnung        |                                                                                                                         | Auf der **Freitextrechnung** Seite klicken Sie auf **In Excel öffnen** (das Microsoft Office-Symbol). |
| Anlagenerfassung     | Anlage zum Sachkonto, Bank, Debitor oder Kreditor. Intercompany wird nicht unterstützt.                                               | Anlagenerfassung                                                                     |
| Kreditorenzahlungserfassung   | Konto: Kreditoren-Gegenkonto: Sachkonto, Bank-Intercompany wird unterstützt.                                                 | Kreditorenzahlungserfassung                                                                  |
| Debitorzahlungserfassung | Konto: Debitoren-Gegenkonto: Sachkonto, Bank-Intercompany wird unterstützt.                                               | Debitorzahlungserfassung                                                                |
| Projektausgabenerfassung  | Konto: Projekt, Sachkonto, Debitor, Kreditor, Bank-Gegenkonto: Projekt, Sachkonto, Debitor, Kreditor-Intercompany wird unterstützt. | Ausgaben der allgemeinen Erfassung unter (Projektverwaltung und- verrechnung)                       |

Wenn die Positionen veröffentlicht werden, sie werden geprüft, um sicherzustellen, dass sie mit den Regeln entsprechen, die den in Finanzerfassungen eingerichtet werden. Nachdem die Positionen veröffentlicht sind, können Benutzer die Belege von Microsoft Dynamics 365 for Finance and Operations bearbeiten oder buchen. 

Um Finanzdimensionen einer Vorlage hinzugefügt werden soll, sind zusätzliche Änderungen erforderlich. Weitere Informationen finden Sie unter [Dimensions zur Microsoft Excel-Vorlage hinzufügen](../../dev-itpro/financial/add-dimensions-excel-templates.md). Nachdem sich mit Dimensionen befassen Entität hinzugefügt wurden, werden sie im Excel-Designer verfügbar und können zur Vorlage hinzugefügt werden.






