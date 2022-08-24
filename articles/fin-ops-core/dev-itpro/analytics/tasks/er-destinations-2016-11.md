---
title: ER Konfigurieren Sie Ziele
description: Diese Prozedur zeigt, wie verschiedene Ziele für Ausgabekomponenten für elektronische Berichterstellung (ER) eingerichtet und verwendet werden, wie beispielsweise ein Ordner oder eine Datei.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
ms.openlocfilehash: 3c8d03e9783013183fbe76cb36014fa9e1e1cbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291053"
---
# <a name="er-configure-destinations"></a>ER Konfigurieren Sie Ziele

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie verschiedene Ziele für Ausgabekomponenten für elektronische Berichterstellung (ER) eingerichtet und verwendet werden, wie beispielsweise ein Ordner oder eine Datei. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF. Deutschland ist das Land/die Region der primären Adresse der juristischen Person, Sie können jedoch jede beliebige juristische Person für diese Prozedur verwenden. 

Das Format, das in diesem Beispiel verwendet wird, ist "ISO20022 Kreditübertragung", aber Sie können jedes beliebige Format verwenden, das Sie bereits importiert haben. Beachten Sie, dass diese Prozedur ein Beispiel für die Einstellungen zu einer einzelnen Datei und einem einzelnen Ziel ist. Weitere Informationen über die Zielverwaltung für die elektronische Berichterstellung können Sie in der Hilfe von Dynamics 365 Finance finden.

1. Wechseln Sie zu "Organisationsverwaltung" > "Elektronische Berichterstellung" > "Ziel für elektronische Berichterstellung".
2. Klicken Sie auf "Neu", um einen neuen Satz von Zielen für ein Format zu erstellen.
3. Wählen Sie im Feld "Referenz" ein Format aus, für das Sie Ziele konfigurieren möchten.
    * Wenn Sie keinen Wert auszuwählen haben, bedeutet dies, dass Sie keine Formatkonfigurationen für die elektronische Berichterstellung importiert haben. Sie müssen eine Formatkonfiguration importieren, bevor Sie Ziele einrichten.  
4. Klicken Sie auf "Neu", um ein neues "Dateiziel" zu erstellen.
    * Beachten Sie, dass Sie ein "Dateiziel" für jede Ausgabekomponente des gleichen Formats erstellen können, wie beispielsweise ein Ordner oder eine Datei. Sie können Ziele in den Einstellungen getrennt voneinander aktivieren und deaktivieren.  
5. Geben Sie im Feld "Name" den benutzerfreundlichen Namen der Ausgabekomponente ein.
    * Es wird empfohlen, dass Sie aussagekräftige Namen verwenden, wie "Zahlungsdatei" oder "Kontrollbericht". Diese Namen werden Benutzern bei der Konfigurationsausführungszeit zusammen mit den Zieleinstellungen vorgestellt.  
6. Im "Dateiname" wählen Sie eine Datei oder einen Ordner aus, die/der für das Format spezifisch ist.
7. Klicken Sie auf "Einstellungen".
8. Wählen Sie "Ja" im Feld "Aktiviert" aus.
    * Das Kontrollkästchen "Aktiviert" auf jeder Registerkarte aktiviert und deaktiviert jedes Ziel getrennt. In diesem Beispiel aktivieren Sie das Senden einer Ausgabedatei zu einem E-Mail-Empfänger, wenn die Datei generiert ist.  
9. Klicken Sie auf Bearbeiten, um E-Mail-Empfänger einzurichten.
10. Klicken Sie auf Hinzufügen.
11. Klicken Sie auf "Verwaltungs-E-Mail ausdrucken".
12. Wählen Sie im Feld "E-Mail-Quelle" eine Option aus.
    * Sie können verschiedene E-Mail-Quelltypen wie Debitor oder ein Kreditortyp auswählen. Dadurch wird der Typ des Arguments angegeben, der durch die E-Mail-Quellkontoformel zurückgegeben wird. In der E-Mail-Quellkontoformel, die in einem folgenden Schritt beschrieben wird, binden Sie eine E-Mail-Quelle. Wählen Sie "Händler" aus, wenn Ihre Formel ein Händlerkonto zurückgibt. Verwenden Sie "Händler", wenn Sie das Konfigurationsbeispiel für die "Kreditübertragung (ISO 20022)" verwenden.  
13. Klicken Sie auf "E-Mail-Quelle binden".
14. In der "Formel" geben Sie einen dokumentspezifischen Verweis auf einen Parteityp, denn Sie vorher gewählt haben ein.
    * Anstelle es einzugeben, können Sie einen Datenquellknoten finden, der das Parteikonto darstellt, und klicken Sie auf die Schaltfläche "Datenquelle hinzufügen", um die Formel zu aktualisieren. Beispiel: Wenn Sie die Konfiguration "Kreditübertragung (ISO 20022)" verwenden, lautet der Knoten, der ein Händlerkonto darstellt, '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID. Andernfalls geben Sie einen beliebigen Zeichenfolgenwert ein, wie "DE-001", um eine Formel zu speichern.  
15. Klicken Sie auf "Speichern".
16. Schließen Sie die Seite.
17. Klicken Sie auf "Bearbeiten", um die Kontaktdetails für Partei zu konfigurieren.
18. Wählen Sie "Ja" im Feld "Primärkontakt" aus.
    * Sie können verschiedene Optionen nutzen, um anzugeben, welcher Kontakttyp der Partei als E-Mail-Adresse für dieses Ziel verwendet werden soll. Wir verwenden in diesem Beispiel den Primärkontakt.  
19. Klicken Sie auf "OK".
20. Klicken Sie auf "OK".
21. Geben Sie im Feld "Betreff" einen Wert ein.
22. Klicken Sie auf "OK".



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
