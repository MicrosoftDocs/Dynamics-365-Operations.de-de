---
title: Einen Zahlungszeitplan auf die Rechnungserfassung anwenden
description: In diesem Artikel wird beschrieben, wie Sie dem Kreditor-Rechnungs-Journal eine Zahlung hinzufügen können.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f3ae08ea46be66dd8bf26f7f91bd73f6c5b9192f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863129"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Einen Zahlungszeitplan auf die Rechnungserfassung anwenden

[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 Finance Release 10.0.25 wird jetzt ein Zahlungszeitplan auf dem **Kreditorenrechnungsjournal** unterstützt.

Um diese Funktion nutzen zu können, müssen Sie die Funktion **Zahlungsausgangs Buch.-Blatt** in der Funktionsverwaltung aktivieren.

Nachdem die Funktion aktiviert wurde, wird der Seite **Erfassungen Buch.-Blatt** ein neues Feld **Zahlungszeitplan** hinzugefügt. Wenn Sie eine Buchungsblattzeile erstellen und die Zahlungsbedingungen für den Kreditor gepflegt sind und die Zahlungsbedingungen im Zahlungsplan ausgewählt sind, wird das Feld **Zahlungsplan** auf der Seite **Rechnungsblatt** aktualisiert.

Sie können den Zahlungsplan, der verwendet wird, entsprechend Ihren geschäftlichen Anforderungen ändern. Bei der Buchung des Journals für Lieferantenrechnungen werden offene Transaktionen des Kreditors gemäß dem Zahlungsplan erstellt.

 - Um mehrere offene Transaktionen von Kreditoren zu überprüfen, die aus dem Zahlungsplan generiert wurden, gehen Sie zu **Kreditoren \> Rechnungen \> Offene Rechnungen von Kreditoren**, und geben Sie die Rechnungsnummer oder das Kreditorenkonto ein.
 - Um den Zahlungsplan zu überprüfen oder zu konfigurieren, gehen Sie zu **Kreditoren \> Zahlungseinrichtung \> Zahlungsplan**.
 - Um die Zahlungsbedingungen zu konfigurieren und einen Zahlungsplan zuzuweisen, gehen Sie zu **Kreditoren a. LL \> Zahlungseinrichtung \> Zahlungsbedingungen**.
 - Um die Zahlungsbedingungen für einen Kreditor zu pflegen, gehen Sie zu **Kreditoren \> Alle Kreditor**, wählen das Kreditorenkonto aus und legen dann auf der Registerkarte **Zahlung** das Feld **Zahlungsbedingungen** fest.

Die Funktion Zahlungsplan ist auch im Prozess **Register für Lieferantenrechnungen** verfügbar. Wenn im Erfassungsjournal des Rechnungsregisters ein Zahlungsplan ausgewählt ist, werden bei der Buchung des Rechnungsregisters **nicht** mehrere Zahlungszeilen des Kreditors erzeugt. Die Zahlungszeilen des Kreditors werden generiert, wenn die Rechnung genehmigt wird.

## <a name="limitation"></a>Begrenzung

Für eine ausstehende Kreditor-Rechnung, wenn der Zahlungsplan auf dem Rechnungskopf steht, gibt es eine erweiterte Seite, auf der Benutzer die Zahlungszeilen bearbeiten können. (Zum Beispiel können Benutzer das Fälligkeitsdatum und den Wert für jede Zahlungszeile bearbeiten.) Zahlungszeilen, die aus dem Zahlungsausgangs Buch.-Blatt generiert werden, haben den Wert aus dem Zahlungsplan.

Diese Funktionalität wird in einer zukünftigen Version für das **Lieferantenrechnungsjournal** und **Ausstehende Rechnungen** verfügbar sein.
