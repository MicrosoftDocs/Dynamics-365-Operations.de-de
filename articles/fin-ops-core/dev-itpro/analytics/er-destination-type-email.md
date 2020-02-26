---
title: E-Mail-ER-Zieltyp
description: Dieses Thema enthält Informationen zum Konfigurieren eines E-Mail-Ziels für jede ORDNER- oder DATEI-Komponente eines ER-Formats (Electronic Reporting), das zum Generieren ausgehender Dokumente konfiguriert ist.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019786"
---
# <a name="EmailDestinationType">E-Mail-Ziel</a>

[!include [banner](../includes/banner.md)]

Sie können ein E-Mail-Ziel für jede ORDNER- oder DATEI-Komponente eines ER-Formats konfigurieren, das zum Generieren ausgehender Dokumente konfiguriert ist. Basierend auf der Zieleinstellung wird ein generiertes Dokument als Anhang einer E-Mail zugestellt.

Legen Sie **Aktiviert** auf **Ja** fest, um eine Ausgabedatei per E-Mail zu senden. Wenn diese Option aktiviert ist, können Sie den E-Mail-Betreff und -Text bearbeiten und die E-Mail-Empfänger angeben. Sie können für die E-Mail und den E-Mail-Betreff konstante Texte einrichten, oder Sie können ER-[Formeln](er-formula-language.md) verwenden, um E-Mail-Texte dynamisch zu erstellen. 

Sie könnne E-Mail-Adressen für ER auf zwei Arten konfigurieren. Die Konfiguration kann auf dieselbe Weise abgeschlossen werden wie es auch für die Druckverwaltungsfunktion geschieht. Sie können auch eine E-Mail-Adresse auflösen, indem Sie einen direkten Verweis auf die ER-Konfiguration über eine Formel erstellen.

[![E-Mail-Ziel aktivieren](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-Mail-Adressen-Arten

Wenn Sie **Bearbeiten** in den Feldern **An** oder **CC** auswählen, wird das Dialogfeld für **E-Mail an** angezeigt. Sie können dann den Typ der E-Mail-Adresse auswählen, den Sie verwenden möchten. Die E-Mail-Typen **Konfigurations-E-Mail** und **Druckverwaltung** werden derzeit unterstützt.

[![E-Mail-Typ auswählen](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Druckverwaltung

Wenn Sie den E-Mail-Typ **Druckverwaltung** auswählen, können Sie feste E-Mail-Adressen im Feld **An** eingeben. 

[![Feste E-Mail-Adressen konfigurieren](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Um keine festen E-Mail-Adressen zu verwenden, müssen Sie die E-Mail-Herkunftsart für ein Ziel auswählen. Folgende Werte werden unterstützt: **Kunde**, **Lieferant**, **Interessent**, **Kontakt**, **Konkurrent**, **Arbeitskraft**, **Bewerber**, **Künftiger Kreditor** und **Unzulässiger Lieferant**. Nachdem Sie einen E-Mail-Quelltyp ausgewählt haben, verwenden Sie die Schaltfläche neben dem Feld **E-Mail-Quellkonto**, um das Formular **Formel-Designer** zu öffnen. Mit diesem Formular können Sie eine Formel anhängen, die zur Laufzeit das **Parteikonto** des ausgewählten Quellentyps vom verarbeiteten Dokument an das E-Mail-Ziel zurückgibt.

[![E-Mail-Quellkonto konfigurieren](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formeln sind für die ER-Konfiguration spezifisch sind. Im Feld **Formel** geben Sie einen dokumentspezifischen Verweis auf einen Debitoren- oder Händlerparteityp ein. Anstelle ihn einzugeben, können Sie den Datenquellknoten suchen, der das Debitoren- oder Kreditorenkonto darstellt, und dann auf **Datenquelle hinzufügen** klicken, um die Formel zu aktualisieren. Beispiel: Wenn Sie die Konfiguration **Kreditübertragung (ISO 20022)** verwenden, lautet der Knoten, der ein Debitorenkonto darstellt, `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Wenn Sie einen Zeichenfolgenwert eingeben, beispielsweise `"DE-001"`, und eine Formel speichern, wird eine E-Mail an die Kontaktperson des Kreditors, **DE-001**, gesendet.


[![ER-Formel-Designer-Seite](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![E-Mail-Quellkonto konfigurieren](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Konfigurations-E-Mail

Verwenden Sie diesen E-Mail-Typ, wenn die Konfiguration, die Sie verwenden, einen Knoten in den Datenquellen hat, die eine **E-Mail-Adresse** zurückgeben. Sie können Datenquellen und Funktionen im Formeldesigner verwenden, um eine ordnungsgemäße formatierte E-Mail-Adresse abzurufen. Beispiel: Wenn Sie die Konfiguration **Kreditübertragung (ISO 20022)** verwenden, lautet der Knoten, der eine E-Mail-Adresse der Kontaktperson des Kreditors darstellt, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Quelle der E-Mail-Adresse konfigurieren](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)
- [Formeldesigner in der elektronischen Berichterstellung (EB)](general-electronic-reporting-formula-designer.md)
