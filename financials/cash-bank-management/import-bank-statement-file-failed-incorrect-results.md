---
title: Bankauszugsdatei-Importproblembehandlung
description: "Es ist die Bankauszugdatei von der Bankabgleichung das Layout von Bedeutung, welches Microsoft Dynamics 365 für Arbeitsgänge unterstützt. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: 9717cf2f36033efe8465906324966242977c6eb2
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-file-import-troubleshooting"></a>Bankauszugsdatei-Importproblembehandlung

Es ist die Bankauszugdatei von der Bankabgleichung das Layout von Bedeutung, welches Microsoft Dynamics 365 für Arbeitsgänge unterstützt. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.

<a name="what-is-the-error"></a>Wie lautet der Fehler?
------------------

Nachdem Sie versuchen, eine Bankauszugsdatei zu importieren, wechseln Sie zur Einzelvorgangshistorie der Datenverwaltung und den darin enthaltenen Ausführungsdetails, um den Fehler zu suchen. Der Fehler kann auf einen Kontoauszug, ein Saldo oder eine Auszugszeile verweisen. Es ist allerdings unwahrscheinlich, genügend Informationen zu erhalten, um das Feld oder das Element zu identifizieren, das das Problem verursacht.

## <a name="what-are-the-differences"></a>Wie lauten die Unterschiede:
Vergleichen der Bankdateilayoutdefinition auf Microsoft Dynamics 365 für Arbeitsgangsimportdefinition, und achten Sie eventuelle Differenzen in den Feldern und den Schlüsseln. Vergleichen Sie die Bankauszugdatei zum jeweiligen B Dynamics 365 für Arbeitsgangsdatei. In den Dateien ISO20022 sollten sämtliche Abweichungen einfach sein anzuzeigen.

## <a name="transformations"></a>Umwandlungen
In der Regel muss die Änderung bei einer von drei Umwandlungen vorgenommen werden. Jede Umwandlung ist für einen bestimmten Standard geschrieben.

| Ressourcenname                                         | Dateiname                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport \_BAI2CSV\_zu xslt\_BAI2XML\_            | BAI2CSV BAI2XML.xslt            |
| BankStmtImport \_ISO20022XML\_\_Abstimmungs\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport \_MT940TXT\_zu xslt\_MT940XML\_          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Debuggingumwandlungen
### <a name="adjust-the-bai2-and-mt940-files"></a>Anpassen der Dateien BAI2 und MT940

Die Dateien BAI2 und MT940 sind text-basierte Dateien und benötigen eine Anpassung, um das Debuggen der Extensible Stylesheet Language Transformation (XSLT) zu ermöglichen. Das Programm nimmt diese Anpassung vor, wenn eine Datei importiert wird.

1.  Erstellen Sie eine XML-Datei und kopieren Sie den folgenden Text hinein.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopieren Sie den Inhalt der Bankauszugsdatei und fügen Sie ihn in die XML-Datei ein, sodass er **PASTESTATEMENTFILEHERE** ersetzt.

### <a name="debug-the-xslt"></a>Debuggen Sie die XSLT

Weitere Informationen finden Sie unter <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Starten Sie Microsoft Visual Studio.
2.  Erstellen Sie eine Konsolenanwendung.
3.  Öffnen Sie die entsprechende XSLT.
4.  Klicken Sie auf die XLST und dessen Eigenschaftenseite.
5.  Legen Sie die Eingabe auf den Speicherort der Bankauszugsdatei fest.
6.  Definieren Sie einen Speicherort und Dateinamen für die Ausgabe.
7.  Legen Sie die erforderlichen Breakpoints fest.
8.  Auf der Speisekarte ** auf XML ** &gt; ** starten Sie XSLT-Debugging **.

### <a name="format-the-xslt-output"></a>Formatieren der XSLT-Ausgabe

Wenn die Umwandlung ausgeführt wird, erstellt sie eine Ausgabedatei, die in Visual Studio angezeigt werden kann. Verwenden Sie STRG+A, STRG+K und STRG+D, um die Ausgabedatei schnell zu formatieren.

### <a name="adjust-the-transformation"></a>Passen Sie die Umwandlung an

Passen Sie die Umwandlung an, um das entsprechende Feld oder Element in der Bankauszugsdatei zu erhalten. Ordnen Sie dann dieses Feld oder Element im gewünschten Dynamics 365 für Arbeitsgangselement zu.

### <a name="debitcredit-indicator"></a>Soll-/Habenindikator

Manchmal können Soll- als Habenbeträge importiert werden, und Haben- als Sollbeträge. Zur Behebung dieses Problems, müssen Sie zuerst die entsprechende XSLT ändern. Wenn Bankauszüge von mehreren Banken stammen, müssen Sie sicherstellen, dass alle den selben Soll/Kreditansatz verwenden, oder Sie erstellen separate Umwandlungen.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator Vorlage
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit Vorlage
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator Vorlage

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Beispiele für Bankauszugsformate und technische Layouts
Die folgende Tabelle zeigt Beispiele der technischen Layoutdefinitionen für erweiterte Importdateien zur Bankabstimmung und drei entsprechenden Beispieldateien für Bankauszüge auf. Sie können die Beispielsdateien und die technischen Layouts herunterladen hier: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Technische Layoutdefinition                             | Beispieldatei für Bankauszüge          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |




