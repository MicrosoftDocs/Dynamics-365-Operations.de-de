---
title: Periodische Aufgaben des Kundenkreditmanagements
description: In diesem Thema werden die regelmäßigen Aufgaben beschrieben, die für die Verwaltung der Kreditlimits für Debitoren erforderlich sind.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 398fcd9d45ce0ddfb1f7189e0712f9dac2db012f
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753506"
---
# <a name="periodic-credit-management-tasks"></a>Periodische Kreditverwaltungsaufgaben

[!include [banner](../includes/banner.md)]

In diesem Thema werden die regelmäßigen Aufgaben beschrieben, die für die Verwaltung der Kreditlimits für Debitoren erforderlich sind.

## <a name="update-risk-scores"></a>Risikobewertungen aktualisieren

Wenn sich Unternehmen entwickeln und sich die Umstände ändern, können sich auch die Kreditrisiken für einen bestimmten Debitor ändern. Um ein angemessenes Kreditlimit für Ihre Debitoren aufrechtzuerhalten, müssen Sie die Kriterien für jede Risikobewertung regelmäßig überprüfen und die Bewertungen für jeden Debitor aktualisieren. Sie können die folgenden Ergebnisse über die Seite **Risikobewertungen aktualisieren** (**Kredit und Inkasso \>Periodische Aufgaben \>Kreditmanagement \> Risikobewertungen aktualisieren**) aktualisieren. Alle benutzerdefinierten Berechnungen werden ebenfalls verarbeitet.

- **Durchschnittliche Zahlungstage** – Dies ist die durchschnittliche Anzahl von Tagen, die ein Debitor benötigt, um Rechnungen zu bezahlen.
- **Debitor seit** – Dieser Wert gibt die Anzahl der Jahre an, in denen ein Debitor Debitor Ihrer Organisation war.
- **Im Geschäft seit** – Dies ist die Anzahl der Jahre, die ein Debitor im Geschäft war. Es verwendet den Wert des Felds **Geschäftsbeginn** auf der Seite **Debitoren**.
- **Dauer der ausstehenden Verkäufe in Tagen** – Diese Bewertung basiert auf dem Debitorenkontensaldo, den Umsatzerlösen und der Anzahl der Tage in den letzten 12 Monaten.
- **Durchschnittlicher Saldo** – Diese Bewertung basiert auf dem Debitorenkontensaldo der letzten 12 Monate.
- **Kreditmanagement-Gruppe**, **Kontostatus** und **Land** – Diese Bewertungen verwenden Informationen des Debitors.

## <a name="update-customer-balance-statistics"></a>Debitorenbilanzstatistik aktualisieren

Sie können den Prozess **Debitorenbilanzstatistik** ausführen, um die Berechnung der Bilanzstatistik zu aktualisieren, die auf der Seite **Bilanzstatistik-Abfrage** angezeigt wird. Diese Informationen werden verwendet, um die Risikobewertung und die Werte zu berechnen, die in den Infoboxen auf der Seite **Kunde** angezeigt werden.

Wenn Sie den Prozess ausführen, werden die Debitorenbilanzstatistiken für einen einzelnen Debitor aktualisiert. Um einen Batchauftrag für die Ausführung des Prozesses für mehrere Debitoren einzurichten, können Sie die Seite **Bilanzstatistik berechnen** (**Kreditmanagement \> Periodische Aufgaben \>Bilanzstatistik berechnen**) verwenden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
