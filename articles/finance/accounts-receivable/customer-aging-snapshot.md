---
title: Fälligkeitsmomentaufnahmen für Debitoren
description: Dieser Artikel enthält Informationen zu Fälligkeitsmomentaufnahmen für Debitoren. Eine Fälligkeitsmomentaufnahme berechnet Saldenrückblicke für eine Gruppe von Debitoren zu einem bestimmten Zeitpunkt.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: e4ccc8ac9b5374ca0713167a17b8704727c687fd
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775235"
---
# <a name="customer-aging-snapshots"></a>Fälligkeitsmomentaufnahmen für Debitoren

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Fälligkeitsmomentaufnahmen für Debitoren. Eine Fälligkeitsmomentaufnahme berechnet Saldenrückblicke für eine Gruppe von Debitoren zu einem bestimmten Zeitpunkt. Sie können Fälligkeitsmomentaufnahme entweder für alle Debitoren oder für die Debitoren in einem Debitorenpool erstellen.

Informationen aus Fälligkeitsmomentaufnahmen werden auf der Listenseite **Saldenrückblick** und auf der Seite **Inkassi** angezeigt. Sie müssen zuerst eine Fälligkeitsmomentaufnahme erstellen, bevor Sie die Listenseite **Saldenrückblick** verwenden können. Auf der Listenseite sind nur Informationen für Debitoren aufgeführt, für die eine Fälligkeitsmomentaufnahme erstellt wurde.

Der Arbeitsbereich **Debitorenkredit und Inkasso** zeigt die Fälligkeit für Debitoren ebenfalls an. Weitere Informationen finden Sie unter [Power BI-Inhalt zur Kredit- und Inkassoverwaltung](credit-collections-power-bi.md).

> [!NOTE]
> Um die Zeit zum Erstellen einer Fälligkeitsmomentaufnahme für Debitoren zu verkürzen, aktivieren Sie folgende Funktionen im Arbeitsbereich **Funktionsverwaltung**: 
> - **Leistungsverbesserung bei der Debitorenfälligeit** 
> - **Erweiterung der Debitorenfälligkeitsleistung mit Debitorenpools**  
>Wenn beide Funktionen aktiviert sind, können **Debitorenpools** beim Erstellen der Fälligkeitsmomentaufnahme verwendet werden. 

Wenn Sie eine Fälligkeitsmomentaufnahme für Debitoren erstellen, geben Sie in die folgenden Felder Informationen dazu ein:

- **Zahlungsfristdefinition**: Wählen Sie die Zahlungsfristdefinition für die Fälligkeitsmomentaufnahme aus. Sie können eine Fälligkeitsmomentaufnahme für jede Zahlungsfristdefinition haben. Der Fälligkeitsmomentaufnahme und die Zahlungsfristdefinition müssen separat erstellt werden.
- **Poolkennung**: Dieses Feld ist optional. Sie können einen Pool verwenden, um die Gruppe von Debitoren festzulegen, die in der Fälligkeitsmomentaufnahme verarbeitet werden sollen. Wenn Sie in diesem Feld einen Debitorenpool auswählen, wird die Fälligkeitsmomentaufnahme nur auf die Debitorenkonten erstellt, die Teil des Debitorenpools sind. Der ausgewählte Debitorenpool muss den Typ **Fälligkeitsmomentaufnahme** haben. Wenn Sie dieses Feld leer lassen, wird für alle Debitorenkonten eine Fälligkeitsmomentaufnahme erstellt.


- **Kriterien**: Die Fälligkeitsmomentaufnahme wird ausgehend von dem von Ihnen ausgewählten Datum fällig:

    - **Buchungsdatum**: Jede Buchung wird ausgehend von ihrem Buchungsdatum fällig.
    - **Fälligkeitsdatum**: Jede Buchung wird ausgehend von ihrem Fälligkeitsdatum fällig.
    - **Dokumentdatum**: Jede Buchung wird ausgehend von ihrem Dokumentdatum fällig.

- **Fälligkeit per**: Wählen Sie das Datum aus, das im Feld **Aktuelles Datum** für die Fälligkeitsmomentaufnahme verwendet werden soll. Zahlungsfristen werden dann auf der Grundlage dieses Datums berechnet. 

    - **Heutiges Datum**: Wählen Sie das Systemdatum aus. Wählen Sie diese Option, wenn die Verarbeitung als sich wiederholender Batch erfolgen soll. Jedes Mal, wenn der Batch ausgeführt wird, wird das Systemdatum dieser Ausführung verwendet.
    - **Gewähltes Datum**: Wählen Sie ein Datum aus, das Sie selbst festlegen. Wenn Sie diese Option auswählen, müssen Sie ein Fälligkeitsdatum eingeben.

   Angenommen die aktuelle Zahlungsfrist beträgt 30 Tage. Wenn Sie in diesem Feld das **heutige Datum** ausgewählt haben, beginnt die aktuelle Zahlungsfrist am heutigen Datum und umfasst dann die vorherigen 29 Tage. Wenn Sie in diesem Feld ein **gewählten Datum** ausgewählt und ein Datum angegeben haben, beginnt die aktuelle Zahlungsfrist am festgelegten Datum und umfasst dann die vorherigen 29 Tage.

- **Inkassostatus aktualisieren**: Setzen Sie diese Option auf **Ja**, um den Inkassostatus auf der Seite **Inkassi** von **Zahlungszusage** auf **Zahlungszusage nicht eingehalten** zu aktualisieren, wenn das Fälligkeitsdatum nach dem Datum im Feld **Datum Zahlungszusage** liegt. Setzen Sie diese Option auf **Nein** um den Inkassostatus im Feld **Inkasso** unverändert zu lassen.
- **Inklusive Debitoren ohne Saldo**: Setzen Sie diese Option auf **Ja**, um alle Debitoren einzubeziehen, unabhängig von ihrem Saldo. Wenn Sie alle Debitoren einbeziehen, sollten Sie die Funktion **Leistungsverbesserung bei der Debitorenfälligeit** und **Erweiterung der Debitorenfälligkeitsleistung mit Debitorenpools** verwenden. Setzen Sie diese Option auf **Nein**, um nur Debitoren einbeziehen, die ein Saldo haben. Diese Einstellung wird bei der Beschleunigung der Leistung helfen, da Debitoren ohne Saldo übersprungen werden.
- **Kreditlimitberechnungen während der Fälligkeit umgehen**: Wenn diese Option auf **Ja** eingestellt ist, berechnet der Fälligkeitsprozess den Betrag der **Lieferscheinzwischensumme**, der **Offenen Auftragszwischensumme** und des **Verfügbaren Kredits** für jeden Debitor. Diese Salden werden auf der Seite **Saldenrückblick** in der FactBox unter **Kreditlimit** angezeigt. Stellen Sie diese Option für eine schnellere Leistung während des Fälligkeitsprozesses auf **Ja** ein. Stellen Sie sie auf **Nein**, um die Salden neu zu berechnen, wenn der Fälligkeitsprozess ausgeführt wird. 
- **Unternehmensbereich**: Wählen Sie auf der Registerkarte **Unternehmensbereich** die juristischen Personen (Unternehmen) aus, die in den Fälligkeitsmomentaufnahme aufgenommen werden sollen. Es können nur juristische Personen ausgewählt werden, bei denen zentralisierte Zahlungen eingerichtet wurden. Transaktionen der ausgewählten juristischen Personen werden dann in die Fälligkeitsfristen für Debitoren einbezogen, die in allen diesen juristischen Personen dieselbe Parteikennung haben. Währungsbeträge werden in die Buchhaltungswährung der juristischen Person umgerechnet, bei der Sie zum Zeitpunkt der Erstellung der Fälligkeitsmomentaufnahme angemeldet sind.

Sie sollten diesen Prozess so planen, dass er als Batch ausgeführt wird.

> [!NOTE]
> Um die Batchleistung beim Erstellen von Fälligkeitsmomentaufnahmen zu verbessern, geben Sie in das Feld **Maximale Anzahl an Stapelverarbeitungsaufgaben** im Inforegister **Inkassostandards** unter der Registerkarte **Inkassi** der Seite **Debitorenparameter** eine Zahl ein. Im Feld **Fällige Debitorensalden** sollten Sie mit einem Wert zwischen **12** und **20** beginnen und ihn dann anpassen, um die Verarbeitung für Ihre Situation zu optimieren. Wir empfehlen, diesen Wert auf nicht größer als **30** einzustellen, da sich dies auf die Leistung auswirkt. 

