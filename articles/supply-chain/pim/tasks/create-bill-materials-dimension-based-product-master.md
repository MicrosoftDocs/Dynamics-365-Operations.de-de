---
title: Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen
description: Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f86625821f8a01a6d4949f9dca538a279f52ce9c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565587"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen

[!include [banner](../../includes/banner.md)]

Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben. Die ersten 4 Aufzeichnungen richten Daten ein, die benötigt werden, um diese Prozedur abzuschließen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Aufgabe wird normalerweise vom Produktdesigner ausgeführt.

## <a name="select-the-product"></a>Wählen Sie das Produkt aus

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * Suchen Sie den freigegebenen Produktmaster mit dimensionsbasierter Konfigurationstechnologie, die Sie im ersten Aufgabenleitfaden in dieser Sequenz erstellt haben.  
1. Wählen Sie im Aktivitätsbereich **Techniker**.
1. Wählen Sie **Stücklisten-Versionen**.

## <a name="create-new-bom-and-bom-version"></a>Erstellen Sie neue Stückliste und Stücklistenversion

1. Wählen Sie **Neu** aus.
1. Wählen Sie **Stückliste und Stückliste Version**.
1. Geben Sie im Feld **Name** einen Wert ein.
    * Festlegen eines Standorts  
    * In dieser Prozedur legen wir keinen bestimmten Standort für die Stückliste fest.  
1. Wählen Sie **OK**.
1. Wählen Sie **Neu** aus.
    * In dieser Prozedur fügen wir vier Positionen der Stückliste hinzu. Zwei Positionen stellen Kabeloptionen dar und zwei Positionen stellen Gehäuseoptionen dar.  
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie Artikelnummer "A0001", HDMI 6'-Kabel, aus.  
1. Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die in Anleitung 4 erstellte Kabelkonfigurationsgruppe in dieser Sequenz.  
1. Wählen Sie **Neu** aus.
    * Wählen Sie Artikelnummer "A0002", HDMI 12'-Kabel, aus.  
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
1. Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie erneut die Kabelkonfigurationsgruppe.  
1. Wählen Sie **Neu** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie Artikelnummer "D0002 Gehäuse" aus.  
1. Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Gehäusekonfigurationsgruppe für diese Stückliste-Zeile.  
1. Wählen Sie **Neu** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie Artikelnummer "M0007 StandardCabinet" als letzte Stücklistenposition aus.  
1. Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Gehäusekonfigurationsgruppe für die letzte Zeile der Stückliste aus.  

## <a name="approve-and-activate"></a>Genehmigen und aktivieren

1. Schließen Sie die Seite.
1. Wählen Sie **Genehmigen**.
1. Geben Sie im Feld **Genehmigt von** einen Wert ein oder wählen Sie ihn aus.
1. Wählen Sie *Ja* im Feld **Wollen Sie die Stückliste auch genehmigen?**.
1. Wählen Sie **OK**.
1. Wählen Sie **Aktivieren** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]