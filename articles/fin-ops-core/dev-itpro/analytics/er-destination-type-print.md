---
title: Drucker-ER-Zieltyps
description: In diesem Thema wird erläutert, wie für jede FOLDER- oder FILE-Komponente eines EB-Formats (elektronische Berichterstellung) ein Druckerziel konfiguriert werden kann.
author: NickSelin
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2513fc4f86519c71602089cd46e9757813b1a708
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388287"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Druckziel

[!include [banner](../includes/banner.md)]

Sie können ein generiertes Dokument direkt an einen Netzwerkdrucker senden und drucken.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, müssen Sie den Dokumentweiterleitungsagenten installieren und konfigurieren und anschließend die Netzwerkdrucker registrieren. Weitere Informationen finden Sie unter [Installieren des Dokumentweiterleitungsagenten, um Netzwerkdruck zu aktivieren](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Druckerziel verfügbar machen

Damit das **Drucker**-Ziel in der aktuellen Instanz von Microsoft Dynamics 365 Finance verfügbar ist, gehen Sie zum Arbeitsbereich **Funktionsverwaltung**, und aktivieren Sie die folgenden Funktionen in dieser Reihenfolge:

1. Ausgehende Dokumente der elektronischen Berichterstattung aus Microsoft Office-Formaten in PDF konvertieren
2. Dokumentweiterleitungsagent als Ziel der elektronischen Berichterstellung für ausgehende Dokumente

[![Aktivieren der EB-Druckerzielfunktion in der Funktionsverwaltung.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Anwendbarkeit

#### <a name="pdf-printing"></a>PDF-Druck

In Versionen von Finance vor Version 10.0.18 kann das Ziel **Drucker** nur für Dateikomponenten konfiguriert werden, die zur Erzeugung von Ausgaben im druckbaren PDF-Format (**PDF Merger** oder **PDF-Datei** Formatelemente) oder Microsoft Office Excel und Word-Format (**Excel-Datei** Formatelement) verwendet werden. Wenn die Ausgabe im PDF-Format erstellt wird, wird sie an einen Drucker gesendet. Wenn die Ausgabe im Office-Format mit dem Formatelement **Excel-Datei** erstellt wird, wird sie automatisch in das PDF-Format konvertiert und an einen Drucker gesendet.

Ab Version 10.0.18 können Sie jedoch das **Drucker**-Ziel für das **Gemeinsame Datei**-Formatelement konfigurieren. Dieses Formatelement wird meist verwendet, um Ausgaben im TXT- oder XML-Format zu erzeugen. Sie können ein ER-Format konfigurieren, das das Formatelement **Gemeinsame Datei** als Stammformatelement und das Formatelement **Binärer Inhalt** als einziges verschachteltes Element darunter enthält. In diesem Fall erzeugt das Formatelement **Gemeinsame Datei** eine Ausgabe in dem Format, das durch die Bindung angegeben wird, die Sie für das Formatelement **Binärer Inhalt** konfigurieren. Sie können diese Bindung beispielsweise so konfigurieren, dass dieses Element mit dem Inhalt eines [Dokumentenmanagement](../../fin-ops/organization-administration/configure-document-management.md) Anhangs im PDF- oder Office-Format (Excel oder Word) [ausgefüllt](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) wird. Sie können die Ausgabe über das konfigurierte **Drucker**-Ziel ausdrucken. 

> [!NOTE]
> Wenn Sie das Formatelement **Common\\File** auswählen, um das **Drucker**-Ziel zu konfigurieren, gibt es keine Möglichkeit, zur Entwurfszeit zu garantieren, dass das ausgewählte Element eine Ausgabe im PDF-Format oder eine Ausgabe, die in das PDF-Format konvertiert werden kann, erzeugt. Daher erhalten Sie die folgende Warnmeldung: „Bitte vergewissern Sie sich, dass die Ausgabe, die von der ausgewählten Formatkomponente erzeugt wird, in PDF konvertiert werden kann. Andernfalls deaktivieren Sie die Option „In PDF konvertieren“. Sie müssen Maßnahmen ergreifen, um Laufzeitprobleme zu vermeiden, wenn eine nicht-PDF- oder nicht-PDF-konvertierbare Ausgabe für den Druck zur Laufzeit bereitgestellt wird. Wenn Sie eine Ausgabe im Office-Format (Excel oder Word) erwarten, muss die Option **In PDF konvertieren** aktiviert sein.
>
> Ab Version 10.0.26 müssen Sie, um die Option **In PDF konvertieren** zu verwenden, **PDF** für den Parameter **Dokumentenroutingtyp** des konfigurierten **Druckers** auswählen.

#### <a name="zpl-printing"></a>ZPL-Drucken

Ab Version 10.0.26 können Sie das Ziel **Drucker** für das Formatelement **Common\\File** konfigurieren, indem Sie **ZPL** für den Parameter **Dokumentenroutingtyp** auswählen. In diesem Fall wird die Option **In PDF konvertieren** zur Laufzeit ignoriert und die TXT- oder XML-Ausgabe wird direkt an einen ausgewählten Drucker gesendet, indem der Zebra Programming Language (ZPL)-Vertrag des [Document Routing Agent (DRA)](install-document-routing-agent.md) verwendet wird. Verwenden Sie diese Funktion für ein ER-Format, das ein ZPL II Etikettenlayout darstellt, um verschiedene Etiketten zu drucken.

[![Festlegen des Parameters Dokument-Routing-Typ im Dialogfeld Zieleinstellungen.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Weitere Informationen zu dieser Funktion finden Sie unter [Entwerfen Sie eine neue ER-Lösung zum Drucken von ZPL-Etiketten](er-design-zpl-labels.md).

### <a name="limitations"></a>Einschränkungen

Das **Drucker**-Ziel ist nur für Cloud-Bereitstellungen implementiert.

### <a name="use-the-printer-destination"></a>Druckerziel verwenden

1. Setzen Sie die Option **Aktiviert** auf **Ja**, um ein generiertes Dokument an einen Drucker zu senden.
2. Im Feld **Druckername** wählen Sie den gewünschten Netzwerkdrucker aus.
3. Setzen Sie die Option **Im Druckarchiv speichern?** auf **Ja**, um die generierte Ausgabe im Druckarchiv zu speichern, damit sie für weitere Ausdrucke zur Verfügung steht. Um später auf die archivierte Ausgabe zuzugreifen, gehen Sie zu **Organisationsverwaltung** \> **Abfragen und Berichte** \> **Berichtarchiv**.

[![Verwenden des Druckerziels.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Die Option für **In PDF konvertieren** muss nicht aktiviert sein, wenn Sie das **Drucker**-Ziel konfigurieren. Die PDF-Konvertierung für Druckzwecke erfolgt auch dann, wenn die Option deaktiviert ist.

Um eine bestimmte [Seitenausrichtung](electronic-reporting-destinations.md#SelectPdfPageOrientation) zu verwenden, wenn Sie ein ausgehendes Dokument im Excel-Format drucken, müssen Sie die Möglichkeit **In PDF konvertieren** aktivieren. Wenn Sie die Option **In PDF konvertieren** auf **Ja** einstellen, wird das Feld **Seitenausrichtung** verfügbar. In dem Feld **Seitenausrichtung** können Sie eine Seitenausrichtung auswählen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
