---
title: Umlagerungsdokument für eine interne Umlagerung generieren
description: Dieses Verfahren zeigt, wie Umlagerungsdokumente für Warenbewegung innerhalb eines Unternehmens erstellt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba18582a27bbec3639095b589101af09366579e2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208380"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Umlagerungsdokument für eine interne Umlagerung generieren

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie Umlagerungsdokumente für Warenbewegung innerhalb eines Unternehmens erstellt werden. Diese Prozedur ist nur für juristische Personen mit einer primären Adresse in Litauen verfügbar. Diese Prozedur wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Litauen erstellt. Bevor Sie dieses Verfahren ausführen können, müssen Sie das Verfahren „Umlagerungsdokumente für Warenbewegung innerhalb eines Unternehmens erstellen“ ausführen. Diese Prozedur ist für Bestandsbuchhalter vorgesehen. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="create-a-transfer-order"></a>Erstellen eines Umlagerungsauftrags
1. Navigieren zur Lagerverwaltung > Eingehende Aufträge > Umlagerungsauftrag.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Von Lagerort" einen Wert ein, oder wählen Sie einen Wert aus.
4. Geben Sie im Feld "Nach Lagerort" einen Wert ein, oder wählen Sie einen Wert aus.
5. Klicken Sie auf Hinzufügen.
6. Markieren Sie in der Liste die ausgewählte Zeile.
7. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Transportdetails für Umlagerungsauftrag ausfüllen
1. Klicken Sie auf "Speichern".
2. Klicken Sie im Aktivitätsbereich auf Versenden.
3. Klicken Sie auf Transportdetails.
4. Wählen Sie die Option Ja im Feld "Transportdetails drucken" aus.
5. Geben Sie im Feld 'Wahren genehmigt von' einen Wert ein, oder wählen Sie einen Wert aus.
6. Geben Sie im Feld 'Verpackung' einen Wert ein.
7. Geben Sie im Feld "Risikoebene der Auslastung" einen Wert ein.
8. Geben Sie im Feld 'Spediteur' einen Wert ein, oder wählen Sie einen Wert aus.
9. Geben Sie im Feld 'Modell' einen Wert ein, oder wählen Sie einen Wert aus.
10. Geben Sie im Feld "Registrierungsnummer" einen Wert ein.
11. Geben Sie im Feld "Anhängererfassungsnummer" einen Wert ein.
12. Geben Sie im Feld 'Fahrer' einen Wert ein, oder wählen Sie einen Wert aus.
13. Geben Sie im Feld "Fahrername" einen Wert ein.
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Anzeigen des Lieferscheins für nicht gebuchten Umlagerungsauftrag
1. Klicken Sie auf "Lieferschein".
2. Klicken Sie auf "OK".
3. Schließen Sie die Seite.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Anzeigen des Lieferscheins für gebuchten Umlagerungsauftrag
1. Klicken Sie im Aktivitätsbereich auf Umlagerungsauftrag.
2. Klicken Sie im Aktivitätsbereich auf Versenden.
3. Klicken Sie auf "Umlagerungsauftrag versenden".
4. Klicken Sie auf die Registerkarte "Allgemein".
5. Wählen Sie im Feld 'Aktualisieren' eine Option aus.
6. Klicken Sie auf die Registerkarte "Überblick".
7. Geben Sie im Feld "Lieferschein" einen Wert ein.
8. Klicken Sie auf "OK".
9. Klicken Sie im Aktivitätsbereich auf Versenden.
10. Klicken Sie auf "Lieferschein".
11. Klicken Sie auf "OK".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]