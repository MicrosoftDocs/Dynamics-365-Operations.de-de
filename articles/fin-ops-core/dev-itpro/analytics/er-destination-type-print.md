---
title: Drucker-ER-Zieltyps
description: Dieses Thema enthält Informationen zum Konfigurieren eines Druckerziels für jede ORDNER- oder DATEI-Komponente eines ER-Formats (Electronic Reporting), das zum Generieren ausgehender Dokumente in PDF- oder Microsoft Office-Formaten (Excel\Word) konfiguriert ist.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: b7a279dcb30e7681ae654ab17d898a5364391d57
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679605"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Druckerziel

[!include [banner](../includes/banner.md)]

Sie können ein generiertes Dokument direkt an einen Netzwerkdrucker senden und drucken.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, müssen Sie den Dokumentweiterleitungsagenten installieren und konfigurieren und anschließend die Netzwerkdrucker registrieren. Weitere Informationen finden Sie unter [Installieren des Dokumentweiterleitungsagenten, um Netzwerkdruck zu aktivieren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Druckerziel verfügbar machen

Damit das **Drucker**-Ziel in der aktuellen Instanz von Microsoft Dynamics 365 Finance verfügbar ist, gehen Sie zum Arbeitsbereich **Funktionsverwaltung**, und aktivieren Sie die folgenden Funktionen in dieser Reihenfolge:

1. Ausgehende Dokumente der elektronischen Berichterstattung aus Microsoft Office-Formaten in PDF konvertieren
2. Dokumentweiterleitungsagent als Ziel der elektronischen Berichterstellung für ausgehende Dokumente

[![Aktivieren der ER-Druckerzielfunktion in der Funktionsverwaltung](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Anwendbarkeit

Das **Drucker**-Ziel kann nur für Dateikomponenten konfiguriert werden, die zum Generieren von Ausgaben im druckbaren PDF-Format (PDF Merger- oder PDF-Dateiformatelemente) oder Microsoft Office Excel-/Word-Format (Excel-Datei) verwendet werden. Wenn die Ausgabe im PDF-Format erstellt wird, wird sie an einen Drucker gesendet. Wenn die Ausgabe im Microsoft Office-Format generiert wird, wird es automatisch in das PDF-Format konvertiert und dann an einen Drucker gesendet.

### <a name="limitations"></a>Einschränkungen

Diese Funktion ist eine Vorschau-Funktion und unterliegt den angegebenen Nutzungsbedingungen, die in [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365-Vorschauen](https://go.microsoft.com/fwlink/?linkid=2105274) beschrieben sind.

Das **Drucker**-Ziel ist nur für Cloud-Bereitstellungen implementiert.

### <a name="use-the-printer-destination"></a>Druckerziel verwenden

1. Setzen Sie die Option **Aktiviert** auf **Ja**, um ein generiertes Dokument an einen Drucker zu senden.
2. Im Feld **Druckername** wählen Sie den gewünschten Netzwerkdrucker aus.
3. Setzen Sie die Option **Im Druckarchiv speichern?** auf **Ja**, um die generierte Ausgabe im Druckarchiv zu speichern, damit sie für weitere Ausdrucke zur Verfügung steht. Um später auf die archivierte Ausgabe zuzugreifen, gehen Sie zu **Organisationsverwaltung** \> **Abfragen und Berichte** \> **Berichtarchiv**.

[![Verwenden des Druckerziels](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Die Option für **In PDF konvertieren** muss nicht aktiviert sein, wenn Sie das **Drucker**-Ziel konfigurieren. Die PDF-Konvertierung für Druckzwecke erfolgt auch dann, wenn die Option deaktiviert ist.

Um eine bestimmte [Seitenausrichtung](electronic-reporting-destinations.md#SelectPdfPageOrientation) zu verwenden, wenn Sie ein ausgehendes Dokument im Excel-Format drucken, müssen Sie die Möglichkeit **In PDF konvertieren** aktivieren. Wenn Sie die Option **In PDF konvertieren** auf **Ja** einstellen, wird das Feld **Seitenausrichtung** verfügbar. In dem Feld **Seitenausrichtung** können Sie eine Seitenausrichtung auswählen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)
