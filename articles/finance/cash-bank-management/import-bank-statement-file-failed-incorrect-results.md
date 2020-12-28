---
title: Bankauszugsdatei-Importproblembehandlung
description: Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 Finance unterstützt wird. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09b24b88ee5f8104aabd11397d5bd2745e846cb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443455"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Bankauszugsdatei-Importproblembehandlung

[!include [banner](../includes/banner.md)]

Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 Finance unterstützt wird. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.

<a name="what-is-the-error"></a>Wie lautet der Fehler?
------------------

Nachdem Sie versuchen, eine Bankauszugsdatei zu importieren, wechseln Sie zur Einzelvorgangshistorie der Datenverwaltung und den darin enthaltenen Ausführungsdetails, um den Fehler zu suchen. Der Fehler kann auf einen Kontoauszug, ein Saldo oder eine Auszugszeile verweisen. Es ist allerdings unwahrscheinlich, genügend Informationen zu erhalten, um das Feld oder das Element zu identifizieren, das das Problem verursacht.

## <a name="what-are-the-differences"></a>Wie lauten die Unterschiede:
Vergleichen Sie die Bankdateilayoutdefinition mit der Finance-Importdefinition, und achten Sie auf eventuelle Unterschiede in den Feldern und den Elementen. Vergleichen Sie die Bankauszugdatei mit der jeweiligen Finance-Datei. In den Dateien ISO20022 sollten sämtliche Abweichungen einfach sein anzuzeigen.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Zeitzonendifferenzen in importierten Bankauszügen
Die Datums- und Zeitwerte in der Importdatei können von den in Finance and Operations angezeigten Datums- und Zeitwerten abweichen. Um diese Abweichung zu verhindern, können Sie auf der Seite **Datenquellen konfigurieren** eine Zeitzoneneinstellung einstellen. Weitere Informationen zur Eingabe einer Zeitzoneneinstellung finden Sie unter [Einrichten des erweiterten Bankabstimmungsimportprozesses](set-up-advanced-bank-reconciliation-import-process.md).

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
Die folgende Tabelle zeigt Beispiele der technischen Layoutdefinitionen für erweiterte Importdateien zur Bankabstimmung und drei entsprechenden Beispieldateien für Bankauszüge auf. Sie können die Beispielsdateien und die technischen Layouts hier herunterladen: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Technische Layoutdefinition                             | Beispieldatei für Bankauszüge          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





