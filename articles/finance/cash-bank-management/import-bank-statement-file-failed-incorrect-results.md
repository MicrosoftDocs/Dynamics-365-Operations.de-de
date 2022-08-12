---
title: Bankauszugsdatei-Importproblembehandlung
description: In diesem Artikel wird erläutert, wie Sie durch geringfügige Unterschiede in der Bankauszugdatei verursachte Probleme beheben.
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151759"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Bankauszugsdatei-Importproblembehandlung

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Diese Funktionalität wird im September 2022 außer Betrieb genommen, neue Benutzer sollten die elektronische Berichterstattung verwenden.

Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 Finance unterstützt wird. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.

## <a name="what-is-the-error"></a>Wie lautet der Fehler?

Nachdem Sie versuchen, eine Bankauszugsdatei zu importieren, wechseln Sie zur Einzelvorgangshistorie der Datenverwaltung und den darin enthaltenen Ausführungsdetails, um den Fehler zu suchen. Der Fehler kann auf einen Kontoauszug, ein Saldo oder eine Auszugszeile verweisen. Es ist allerdings unwahrscheinlich, genügend Informationen zu erhalten, um das Feld oder das Element zu identifizieren, das das Problem verursacht.

> [!NOTE]
> Importierte Bankauszüge können sich nur für einen bestimmten Zeitpunkt überschneiden.  Wenn ein Auszug beispielsweise am 1. Januar 2021 um 12:00 AM endet, kann das Anfangsdatum für den nächsten Auszug 12:00 AM am 1. Januar 2021 um 12:00:00 AM sein.

## <a name="what-are-the-differences"></a>Wie lauten die Unterschiede:
Vergleichen Sie die Bankdateilayoutdefinition mit der Finance-Importdefinition, und achten Sie auf eventuelle Unterschiede in den Feldern und den Elementen. Vergleichen Sie die Bankauszugdatei mit der jeweiligen Finance-Datei. In den Dateien ISO20022 sollten sämtliche Abweichungen einfach sein anzuzeigen.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Zeitzonendifferenzen in importierten Bankauszügen
Die Datums- und Zeitwerte in der Importdatei können von den Datums- und Zeitwerten abweichen, die in Finanzen und Betrieb angezeigt werden. Um diese Abweichung zu verhindern, können Sie auf der Seite **Datenquellen konfigurieren** eine Zeitzoneneinstellung einstellen. Weitere Informationen zur Eingabe einer Zeitzoneneinstellung finden Sie unter [Einrichten des erweiterten Bankabstimmungsimportprozesses](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Umwandlungen
In der Regel muss die Änderung bei einer von drei Umwandlungen vorgenommen werden. Jede Umwandlung ist für einen bestimmten Standard geschrieben.

| Ressourcenname                                         | Dateiname                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Debuggingumwandlungen
### <a name="adjust-the-bai2-and-mt940-files"></a>Anpassen der Dateien BAI2 und MT940

Die Dateien BAI2 und MT940 sind text-basierte Dateien und benötigen eine Anpassung, um das Debuggen der Extensible Stylesheet Language Transformation (XSLT) zu ermöglichen. Das Programm nimmt diese Anpassung vor, wenn eine Datei importiert wird.

1.  Erstellen Sie eine XML-Datei und kopieren Sie den folgenden Text hinein.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Kopieren Sie den Inhalt der Bankauszugsdatei und fügen Sie ihn in die XML-Datei ein, sodass er **PASTESTATEMENTFILEHERE** ersetzt.

### <a name="debug-the-xslt"></a>Debuggen Sie die XSLT

Weitere Informationen finden Sie unter <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Starten Sie Microsoft Visual Studio.
2.  Erstellen Sie eine Konsolenanwendung.
3.  Öffnen Sie die entsprechende XSLT.
4.  Klicken Sie auf die XLST und dessen Eigenschaftenseite.
5.  Legen Sie die Eingabe auf den Speicherort der Bankauszugsdatei fest.
6.  Definieren Sie einen Speicherort und Dateinamen für die Ausgabe.
7.  Legen Sie die erforderlichen Breakpoints fest.
8.  Klicken Sie im Menü auf **XML** &gt; **Debuggen der XSLT starten.**

### <a name="format-the-xslt-output"></a>Formatieren der XSLT-Ausgabe

Wenn die Umwandlung ausgeführt wird, erstellt sie eine Ausgabedatei, die in Visual Studio angezeigt werden kann. Verwenden Sie STRG+A, STRG+K und STRG+D, um die Ausgabedatei schnell zu formatieren.

### <a name="adjust-the-transformation"></a>Passen Sie die Umwandlung an

Passen Sie die Umwandlung an, um das entsprechende Feld oder Element in der Bankauszugsdatei zu erhalten. Ordnen Sie dann diesem Feld oder Element das entsprechende Finance-Element zu.

### <a name="debitcredit-indicator"></a>Soll-/Habenindikator

Manchmal können Soll- als Habenbeträge importiert werden, und Haben- als Sollbeträge. Zur Behebung dieses Problems, müssen Sie zuerst die entsprechende XSLT ändern. Wenn Bankauszüge von mehreren Banken stammen, müssen Sie sicherstellen, dass alle den selben Soll/Kreditansatz verwenden, oder Sie erstellen separate Umwandlungen.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator Vorlage
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit Vorlage
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator Vorlage

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Beispiele für Bankauszugsformate und technische Layouts
Die folgende Tabelle zeigt Beispiele der technischen Layoutdefinitionen für erweiterte Importdateien zur Bankabstimmung und drei entsprechenden Beispieldateien für Bankauszüge auf. Sie können die Beispielsdateien und die technischen Layouts hier herunterladen: [Importdateibeispiele](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Technische Layoutdefinition                             | Beispieldatei für Bankauszüge          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

