---
title: Vorauszahlung für Kreditorenrechnungen automatisch anwenden
description: In diesem Thema wird die Möglichkeit beschrieben, Vorauszahlungen automatisch auf Kreditorenrechnungen anzuwenden.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5b07c1d4c2189184b2ad29d46ec2aef0ee03c1c0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985361"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automatisch auf Kreditorenrechnungen anwenden

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Möglichkeit beschrieben, Vorauszahlungen automatisch auf Kreditorenrechnungen anzuwenden. Zu einer Bestellung kann im Rahmen eines Kaufvertrages eine Vorauszahlung erstellt werden. Nachdem eine Kreditorenrechnung eingegangen ist, kann die Vorauszahlung verwendet werden, um die Verbindlichkeiten aus der Kreditorenrechnung zu begleichen. Die neue Funktion ermöglicht es dem System, automatisch Bestellnummern auf einer Kreditorenrechnung zu verwenden, um beim Importieren der Kreditorenrechnung entsprechende Vorauszahlungen zu suchen.

Wenn Vorauszahlungen gefunden werden und angewendet werden können, werden Positionen zu den vorhandenen Rechnungspositionen hinzugefügt, um die Vorauszahlungen zu übernehmen. Die Vorauszahlungszeilen werden beim Rechnungsabgleich nie berücksichtigt.

Die folgenden Punkte beschreiben, wie Vorauszahlungen bei verschiedenen Einkaufsprozessen verwendet werden:

- **Eine Kreditorenrechnung pro Bestellung** – Die Vorauszahlung der Bestellung wird auf die Lieferantenrechnung verrechnet.
- **Eine Kreditorenrechnung für mehrere Bestellungen** – Die Vorauszahlungen aller Bestellungen werden auf die Lieferantenrechnung verrechnet.
- **Mehrere Kreditorenrechnungen pro Bestellung** – Die Vorauszahlung der Bestellung wird auf die erste importierte Lieferantenrechnung verrechnet. Wenn der Vorauszahlungsbetrag den Rechnungsbetrag übersteigt, schlägt der Vorauszahlungsantrag fehl und Sie müssen die Vorauszahlung manuell anwenden.
- **Mehrere Kreditorenrechnungen für mehrere Bestellungen** – Die Vorauszahlungen der Bestellungen werden auf die erste relevante Rechnung verrechnet. Wenn der Vorauszahlungsbetrag den Rechnungsbetrag übersteigt, schlägt der Vorauszahlungsantrag fehl und Sie müssen die Vorauszahlungen manuell anwenden. Wenn Vorauszahlungen, die nach Vorauszahlungen verbleiben, auf die erste Rechnung angewendet werden, können sie auf die folgenden Rechnungen angewendet werden.

Wenn das System versucht, eine Vorauszahlung anzuwenden, die Anwendung jedoch fehlschlägt, hängt das Verhalten von der Einstellung der Option **Folgeautomatisierungsprozess für den Fall nlovkirtrn, dass der Antrag auf Vorauszahlung fehlschlägt**:

- **Ja** – Die Fehlermeldung „Automatische Beantragung der Vorauszahlung: fehlgeschlagen“ wird in die Automatisierungshistorie aufgenommen und die Rechnung verbleibt in der Liste der offenen Kreditorenrechnungen. Die Rechnung bleibt gesperrt, bis Sie die Vorauszahlung manuell vornehmen.

    Um Vorauszahlungen manuell anzuwenden, rufen Sie die ausstehende Kreditorenrechnung auf. Stellen Sie auf der **Rechnungsdetails**-Seite die Option **In die automatisierte Verarbeitung einbeziehen** für die gesperrte Rechnung auf **Nein**. Sie können die Vorauszahlung nun manuell anwenden. Nachdem die Vorauszahlung verrechnet wurde, stellen Sie die Option **In die automatisierte Verarbeitung einbeziehen** zurück auf **Ja**, damit die Rechnung automatisch verarbeitet werden kann.

    Sie können die automatische Beantragung der Vorauszahlung auch umgehen, indem Sie die Option **In die automatisierte Verarbeitung einbeziehen** auf **Nein** und dann wieder auf **Ja** stellen. Sie erhalten folgende Meldung: „Für die Bestellung ist bereits eine Vorauszahlung vorhanden. Möchten Sie sie für die ausgewählte Kreditorenrechnung ignorieren?“ Wählen Sie **Ja** aus. Die Meldung „Antrag der Vorauszahlung manuell umgangen“ wird in der Automatisierungshistorie hinzugefügt und die Kreditorenrechnung wird nicht gesperrt, wenn der automatisierte Prozess erneut ausgeführt wird.

- **Nein** – Folgeautomatisierungsprozesse werden fortgesetzt. Sie können die Vorauszahlung noch während der Abrechnung anwenden.
