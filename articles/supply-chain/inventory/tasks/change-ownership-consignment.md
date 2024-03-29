---
title: Besitz des Lagerbestands auf Grundlage des Produktionsbedarfs ändern
description: Dieses Verfahren zeigt, wie Sie den Eigentümer des Lieferungsbestandes vom Kreditor auf Ihre juristische Person ändern, wenn ein Bedarf für den Bestand in der Produktion vorhanden ist.
author: yufeihuang
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e735a9003f2859ed173f399525297506ec458e8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565830"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Besitz des Lagerbestands auf Grundlage des Produktionsbedarfs ändern

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie Sie den Eigentümer des Lieferungsbestandes vom Kreditor auf Ihre juristische Person ändern, wenn ein Bedarf für den Bestand in der Produktion vorhanden ist. Diese Besitzänderung wird ausgeführt, indem eine Bestandsbesitz-Änderungserfassung erstellt und gebucht wird. Die Besitzänderungs-Erfassungspositionen kann manuell erstellt werden, oder, wie in dieser Aufzeichnung, basierend auf einem vorhandenen Produktionsbedarf durchgeführt werden Normalerweise wird diese Aufgabe von einem Fertigungsbereichsvorgesetzten ausgeführt. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Wenn Sie Ihren eigenen Daten nutzen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind: es wurden ein Lagererfassungsname für die Bestandsbesitzänderung, physisch erfasste verfügbare Artikel im Besitz des Kreditors und mindestens eine Produktionsauftragsposition für Rohstoff eingerichtet. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.

> [!NOTE]
> Ausgehende Lieferungsprozesse werden standardmäßig nicht unterstützt und die automatische Besitzerfassungsverarbeitung wird nicht unterstützt.

## <a name="create-an-inventory-ownership-journal"></a>Erstellen einer Bestandsbesitz-Erfassung
1. Wechseln Sie zu "Lagerverwaltung" > "Journaleinträge" > "Artikel" > "Bestandseigentümeränderung".
2. Klicken Sie auf "Neu".
    * Die Bestandseigentümer-Journaländerung wird verwendet, um den Eigentümer des Lieferungsbestandes vom Kreditor auf die aktuelle juristische Person zu ändern. Diese Besitzänderung wird über die Freigabe des verfügbaren Lagerbestands im Besitz des Kreditors und den Empfang des Bestands in der aktuellen juristischen Person durchgeführt.  
3. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
    * Sie können nur Lagerjournalnamen auswählen, die einen Erfassungstyp "Besitzänderung" haben.  
4. Klicken Sie auf "OK".
5. Klicken Sie auf Funktionen.
6. Klicken Sie auf "Erfassungspositionen aus Produktionsaufträgen erstellen".
    * Sie können den Eigentumsübertragungsprozess starten, indem Sie alle Produktionsauftragspositionen abfragen, die ggf. einen Verbrauch des Rohmaterials haben.  
7. In den Lagerabgangstatus wählen Sie eine Option, um das Feld einzubeziehen.
    * Mit dieser Option können Sie nach dem Abgangsstatus von Lagerbuchungen filtern. Beispielsweise können Sie Erfassungspositionen für Bestand erstellen, der den Status "Entnommen" und "Physisch reserviert" hat.  
8. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
    * In diesem Abschnitt können Sie zusätzliche Filter anwenden. So können z. B. ein bestimmtes Rohmaterialdatum auswählen.  
9. Klicken Sie auf "OK".

## <a name="post-the-inventory-ownership-change-journal"></a>Buchen der Bestandseigentümer-Journaländerung
1. Klicken Sie auf "Buchen".
    * Wenn die Erfassung gebucht ist, wird der Bestand im Besitz des Kreditors über eine "Besitzänderungs"-Referenz freigegeben. Anschließend wird der Bestand über eine Lagerbuchung als verfügbar empfangen, die mit einem Produktzugang für Bestellung aktualisiert wird. Beachten Sie, dass nur Buchungen, die der gebuchten Erfassung zugeordnet sind, erstellt werden. Es werden keine voraussichtlichen Lagerbuchung erstellt.  
2. Klicken Sie auf "OK".
3. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]