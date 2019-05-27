---
title: Verwalten der Lagerortarbeitskräfte
description: In diesem Artikel wird beschrieben, wie Sie Dynamics 365 for Finance and Operations verwenden können, um die Arbeit zu steuern und zu überwachen, die von Mitarbeitern an Ihren Lagerorten ausgeführt wird.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5a35d0a52d6f5bf995ce54f10eab92147b0e76a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572557"
---
# <a name="manage-warehouse-workers"></a>Verwalten der Lagerortarbeitskräfte

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 for Finance and Operations verwenden können, um die Arbeit zu steuern und zu überwachen, die von Mitarbeitern an Ihren Lagerorten ausgeführt wird.

Wenn Sie die Funktionen in der Lagerortverwaltung verwenden, werden alle Arbeitsgänge der Lagerarbeiter als *Arbeit* bezeichnet. Arbeit, wie die Entnahme, das Umlagern und das Zählen des verfügbaren Lagerbestands wird mithilfe von mobilen Geräten erfasst. Bevor ein Lagerarbeiter Arbeit ausführen kann, muss er einer Arbeitskraft in der Personalverwaltung zugeordnet werden. Jedes **Arbeitskraftkonto** kann mehrere Lagerortarbeitsbenutzer haben, die ihm zugeordnet sind. Diese Arbeitsbenutzer können in verschiedenen Lagerorten arbeiten und verschiedene Zugriffsebenen auf unterschiedliche Menüs des mobilen Geräts haben. Sie können die Lagerortarbeitsbenutzer als mehrere Anmeldungen für die ausgewählte Arbeitskraft betrachten. Jeder Arbeitsbenutzer hat einen Standardlagerort, und bestimmte Workflows werden durch die Menüartikel, die diesem Arbeitsbenutzer verfügbar sind, offengelegt. 

Um einen neuen Arbeitsbenutzer zu erstellen, klicken Sie auf der Seite **Arbeitskräfte**, auf der Registerkarte **Allgemeines** im Abschnitt **Lagerorte** auf **Arbeitskraft**. Sie müssen eine Benutzerkennung, einen Benutzernamen, einen Standardlagerort und einen Menünamen angeben. Dieses Menü wird geladen, wenn sich der Benutzer beim Portal für mobile Geräte für den Lagerort anmeldet. Dort können Sie definieren, auf welche Menüelemente der Benutzer Zugriff hat. 

Als Teil der Einrichtung für jeden Arbeitsbenutzer können Sie auch spezielle Prozessworkflows definieren. Sie können beispielsweise das Feld **Ist ein Supervisor der permanenten Inventur** verwenden, um anzugeben, ob der Benutzer Anpassungen an Zykluszählungsabweichungen während eines Zählvorgangs vornehmen kann oder ob diese Anpassungen zuerst von einer anderen Person geprüft werden müssen.

## <a name="defining-labor-standards"></a>Definieren von Arbeitsstandards
Auf der Seite **Arbeitsstandards** können die Berechnungsmethoden definieren, die das System verwendet, um die geschätzte Zeit zu berechnen, die für eine bestimmte Art von Arbeit erforderlich sein soll. Diese Definition kann auf einer allgemeinen Ebene oder auf einer bestimmten Ebene festgelegt werden. So können Sie beispielsweise die Zeit definieren, die erforderlich sein soll, um eine Auftragsentnahme pro Gewicht für eine bestimmte Einheitsdefinition zu verarbeiten, wenn eine bestimmte Entnahme verwendet wird. Gleichzeitig können Sie die Uhrzeit erfassen, auf Basis einer anderen Berechnungsmethode, für den Einlagerungsvorgang des verfügbaren Lagerbestands, der entnommen wird. 

Um die Arbeitsstandards zu aktivieren, die Sie definiert haben, müssen Sie die Option **Arbeitsstandards zulassen** für jeden Lagerort auswählen, in dem Arbeitsstandards verwendet werden.

## <a name="monitoring-and-controlling-warehouse-work"></a>Überwachen und Steuern von Lagerarbeit
Auf der Seite **Alle Arbeit** können Sie alle Arbeit überwachen und verwalten, die geplant, in Bearbeitung und abgeschlossen ist. Von dieser Seite können Sie verschiedene Prozesse aktualisieren, wie Lagerortbenutzerzuweisungen und Arbeitspriorität. Sie können auch Detailinformationen anzeigen, die der Arbeitskopfzeile und den Arbeitspositionen zugeordnet sind, um ein Verständnis der erwarteten oder abgeschlossenen Arbeitsprozesse zu erhalten. 

Wenn Sie die Option **Arbeitsstandards** aktivieren, können Sie die berechnete geschätzten Zeit für die Arbeit anzeigen. Wenn die Arbeit verarbeitet wird, wird die tatsächliche Zeit dann auch für jeden Arbeitsvorgang angezeigt. Auf diese Weise können Sie die geschätzten Zeitberechnungen mit der tatsächlichen Zeit vergleichen. 

Darüber hinaus können Sie die geschätzte Zeit in den Regeln für die automatische Aufteilung der Arbeit während der Arbeitserstellung verwenden. Auf diese Weise können Sie für Arbeit einen Lastenausgleich durchführen, auf Grundlage der erwarteten Zeitspanne, um die Aufgaben abzuschließen. 

Eine Analyse der Zeit, die benötigt wird, um Arbeitsaufgaben zu verarbeiten, kann Verbesserungen in der Effizienz der Lagerarbeiter fördern. Die folgenden Berichte sind verfügbar, um Sie bei dieser Analyse zu unterstützen:

-   **Arbeit nach Benutzer** – Dieser Bericht zeigt die Arbeitskraftproduktivität, auf der Grundlage der tatsächlichen Zeiten im Vergleich mit erwarteten Zeiten.
-   **Arbeit nach Arbeitstransaktionstyp** – Sie können diesen Bericht verwenden, um Unwirtschaftlichkeiten in bestimmten Lagerortprozessen zu untersuchen. Beispielsweise stellen Sie fest, dass Entnahmen für Umlagerungsaufträge diese Woche länger als in den Vorwochen dauern. Sie können diese Informationen dann für weitere Untersuchungen verwenden.




