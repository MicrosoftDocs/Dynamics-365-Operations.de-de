---
title: Einrichtungsoptionen für die Automatisierung von Lieferantenrechnungen (Vorschau)
description: In diesem Artikel werden die Optionen beschrieben, die zum Einrichten und Konfigurieren der Automatisierung von Lieferantenrechnungen verfügbar sind.
author: sunfzam
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86ad68b3dc08bf2c57ab5f9bc6c65bc37c0901e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874840"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Einrichtungsoptionen zur Automatisierung von Kreditorenrechnungen

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Optionen beschrieben, die zum Einrichten und Konfigurieren der Automatisierung von Lieferantenrechnungen verfügbar sind. Die Funktionen zur Rechnungsautomatisierung verwenden die folgenden Arten von Einrichtungsparametern:

- Parameter für die automatische Anwendung von Vorauszahlungen in importierten Rechnungen.
- Parameter zum Übermitteln importierter Lieferantenrechnungen an das Workflow-System und Abgleichen der gebuchten Produktzugangspositionen mit ausstehenden Lieferantenrechnungspositionen.
- Parameter für die Verarbeitung der Automatisierung von Hintergrundaufgaben. Das Prozessautomatisierungsframework wird verwendet, um importierte Lieferantenrechnungen an das Workflow-System zu übermitteln. Dies wird auch dazu verwendet, um gebuchte Produktbelegzeilen automatisch mit ausstehenden Kreditorenrechnungszeilen abzugleichen und eine Validierung der Rechnungsübereinstimmung für manuelle Rechnungen durchzuführen, die automatisch mit Produktbelegzeilen abgeglichen wurden. Verschiedene Geschäftsprozesse verwenden dieses Framework, um zu definieren, wie oft der ausgewählte Prozess ausgeführt wird. Die verfügbaren Frequenzen für die Hintergrundprozesse **Produktzugangspositionen mit Rechnungspositionen abgleichen** und **Kreditorenrechnungen an Workflow einreichen** umfassen **Stunde** und **Täglich**.

Um Informationen zu einer Hintergrundaufgabe einzurichten oder anzuzeigen, gehen Sie zu **Systemadministration \> Setup \> Prozessautomatisierungen** und wählen Sie die Registerkarte **Hintergrundaufgabe**.

Um eine berührungslose Automatisierung des Importprozesses durch Buchung von Kreditorenrechnungen zu erreichen, müssen Sie einen Kreditorenrechnungsworkflow einrichten. Um einen Workflow einzurichten gehen Sie zu **Kreditorenkonten > Setup > Kreditorenkontenworkflows**. Um sicherzustellen, dass die Rechnung ohne manuellen Eingriff von Anfang bis Ende verarbeitet werden kann, müssen Sie eine automatisierte Buchungsaufgabe in Ihre Workflow-Konfiguration aufnehmen.

## <a name="parameters-for-automatically-applying-prepayments-in-imported-invoices"></a>Parameter für die automatische Anwendung von Vorauszahlungen in importierten Rechnungen

- **Automatisch Vorauszahlung für importierte Rechnungen anwenden** – Wenn diese Option auf **Ja** eingestellt ist, sucht das System beim Importieren von Kreditorenrechnungen automatisch vorhandene Vorauszahlungen zu einer entsprechenden Bestellung. Wenn anwendbare Vorauszahlungen gefunden werden, wird eine zusätzliche Zeile hinzugefügt, um die Vorauszahlungen in den importierten Kreditorenrechnungen anzuwenden.
- **Blockieren Sie den Folgeautomatisierungsprozess für den Fall, dass der Antrag auf Vorauszahlung fehlschlägt** – Wenn diese Option auf **Jaw** eingestellt ist, werden Rechnungen gesperrt, wenn eine Vorauszahlung nicht möglich ist. Wie andere automatisierte Prozesse, z. B. der Quittungsabgleich und die Übermittlung an einen Workflow-Prozess, nimmt der Rechnungsautomatisierungsprozess gesperrte Rechnungen erst dann auf, wenn die Vorauszahlung manuell angewendet wird. 

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parameter zum Senden importierter Kreditorenrechnungen an das Workflow-System

Spezielle Parameter werden zum Einreichen importierter Kreditorenrechnungen an das Workflow-System verwendet. Zusätzlich werden einige Parameter verwendet, um gebuchte Produktzugangspositionen automatisch mit ausstehenden Kreditorenrechnungspositionen abzugleichen. Auf der Registerkarte **Automatisierung von Kreditorenrechnungen** der Seite **Kreditorenkontoparameter** sind die Parameter, die Sie einstellen müssen, in die folgenden Abschnitte unterteilt:

- Workflow für Kreditorenrechnungen
- Produktzugänge automatisch abgleichen

Folgende Parameter sind verfügbar:

- **Importierte Rechnungen automatisch an den Workflow senden** – Wenn Sie diese Option auf **Ja** setzen, werden importierte Rechnungen automatisch an das Workflow-System gesendet. Wenn diese Option auf **Nein** gesetzt ist, müssen Rechnungen manuell eingereicht werden. Durch Setzen dieser Option auf **Ja** aktivieren Sie einen berührungslosen Prozess aus den Importergebnissen durch Buchung.

    Sie können diese Option nur auf **Ja** einstellen, wenn ein aktiver Kreditorenrechnungsworkflow für Ihre juristische Person eingerichtet ist. Um einen Workflow einzurichten, gehen Sie zu **Kreditorenkonten \> Setup \> Kreditorenkontenworkflow**.

- **Abgleichen von Produktzugängen vor dem automatischen Absenden den Rechnungspositionen** – Wenn Sie diese Option auf **Ja** setzen, kann die importierte Rechnung nicht automatisch an das Workflow-System übergeben werden, bis die abgeglichene Produktzugangsmenge der Rechnungsmenge entspricht. Durch Setzen dieser Option auf **Ja** aktivieren Sie den automatischen Abgleich gebuchter Produktzugänge mit Rechnungspositionen, für die eine dreiseitige Abgleichsrichtlinie definiert ist. Dieser Prozess wird ausgeführt, bis die abgeglichene Produktzugangsmenge der Rechnungsmenge entspricht. Zu diesem Zeitpunkt wird die Rechnung automatisch an das Workflow-System gesendet.

    Die Option **Produktbelege vor automatischer Übermittlung mit Rechnungspositionen abgleichen** ist nur verfügbar, wenn die Option **Rechnungsabgleichprüfung aktivieren** ausgewählt ist. Wenn diese Option ausgewählt ist, wird die Option **Produktzugänge automatisch Rechnungspositionen zuordnen** automatisch ausgewählt.

- **Die berechneten Summen müssen den importierten Summen für die automatische Übermittlung des Workflows entsprechen** – Wenn Sie diese Option auf **Ja** setzen, kann die Rechnung nicht automatisch an das Workflow-System gesendet werden, bis die für die Rechnung berechneten Summen den importierten Summen entsprechen. Wenn diese Option auf **Nein** gesetzt ist, kann die Rechnung automatisch an das Workflow-System gesendet werden. Sie kann jedoch erst gebucht werden, wenn die berechneten Summen so korrigiert wurden, dass sie mit den importierten Summen übereinstimmen. Wenn Sie den Rechnungsbetrag oder den Umsatzsteuerbetrag nicht importieren, sollte diese Option auf **Nein** gesetzt sein.
- **Produktzugänge automatisch Rechnungspositionen zuordnen** – Wenn Sie diese Option auf **Ja** setzen, kann die Hintergrundverarbeitung verwendet werden, um einen automatischen Abgleich von gebuchten Produktzugängen mit Rechnungspositionen durchzuführen, für die eine dreiseitige Abgleichsrichtlinie definiert ist. Dieser Prozess wird ausgeführt, bis die abgeglichene Produktzugangsmenge der Rechnungsmenge entspricht oder bis der Wert des Feldes **Anzahl der versuchten automatischen Abgleiche** erreicht ist. Der Prozess kann ausgeführt werden, bis die Rechnung an das Workflow-System gesendet wurde.

    Diese Option steht nur zur Verfügung, wenn die Option **Rechnungsabgleichprüfung aktivieren** ausgewählt wurde.

    Wenn Sie die Option **Abgleich von Produktzugängen mit Rechnungspositionen vor dem automatischen Abgleich** auf **Ja** setzen, kann diese Option nicht auf **Nein** gesetzt werden. Um diese Option auf **Nein** zu setzen, müssen Sie zuerst die Option **Produktzugänge vor dem automatischen Abgleich den Rechnungspositionen zuordnen** auf **Nein** setzen.

- **Anzahl der versuchten automatischen Abgleiche** – Wählen Sie aus, wie oft das System versuchen soll, Produktzugänge mit einer Rechnungsposition abzugleichen, bevor es zu dem Schluss kommt, dass der Prozess fehlgeschlagen ist. Wenn die angegebene Anzahl von Versuchen erreicht ist, wird die Rechnung aus der Automatisierungsverarbeitung entfernt.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
