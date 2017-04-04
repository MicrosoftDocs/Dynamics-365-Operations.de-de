---
title: Einrichten des erweiterten Bankabstimmungsimportprozesses
description: "Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 for Operations automatisch mit Bankbuchungen abstimmen. Dieser Artikel erläutert die Einrichtung der Importfunktion für Ihre Bankauszüge."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: acf7bacf6e95725024ff0a542a059349593d01a0
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Einrichten des erweiterten Bankabstimmungsimportprozesses

Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 for Operations automatisch mit Bankbuchungen abstimmen. Dieser Artikel erläutert die Einrichtung der Importfunktion für Ihre Bankauszüge. 

Die Einrichtung des Bankabstimmungsimports variiert je nach Format des elektronischen Bankauszugs. Microsoft Dynamics 365 für Arbeitsgänge Bankauszugsformatstandard drei unterstützt: ISO20022, MT940 BAI2 und.

## <a name="sample-files"></a>Beispieldateien
Für alle drei Formate müssen Sie Dateien haben, die den elektronischen Bankauszug vom ursprünglichen Format in ein Format übersetzen, dass Dynamics 365 für Arbeitsgänge verwenden kann. Sie finden die erforderlichen Ressourcendateien unter dem Knoten **Ressourcen** im Anwendungs-Explorer-in Microsoft Visual Studio. Kopieren Sie sie an einen einzelnen Speicherort, damit Sie sie während des Installationsvorgangs leichter hochladen können.

| Ressourcenname                                           | Dateiname                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport \_BAI2CSV\_zu xslt\_BAI2XML\_              | BAI2CSV BAI2XML.xslt              |
| BankStmtImport \_BAI2XML\_\_Abstimmungs\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| \_BankStmtImport BankReconciliation\_zu zusammengesetztem\_xslt\_ | BankReconciliation-to-Composite.xslt |
| BankStmtImport \_ISO20022XML\_\_Abstimmungs\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport \_MT940TXT\_zu xslt\_MT940XML\_            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport \_MT940XML\_\_Abstimmungs\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport \_\_SampleBankCompositeEntity XML          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Beispiele für Bankauszugsformate und technische Layouts
Im Folgenden sind Beispiele der in Layoutdefinitionen der erweiterten Bankabstimmungsimportdatei und drei Bankauszugsbeispielsdateien Spesen-: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Technische Layoutdefinition                             | Beispieldatei für Bankauszüge          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Einrichten des Imports von ISO20022-Bankauszügen
Zuerst definieren Sie die Bankauszugs-Formatverarbeitungsgruppe für ISO20022-Bankauszüge über das Datenentitätsframework.

1.  Wechseln ** Arbeitsbereiche ** &gt; ** Datenverwaltung **.
2.  Click **Import**.
3.  Geben Sie einen Namen ein (z. B. **ISO20022**).
4.  Legen Sie das Feld **Quelldatenformat** auf **XML-Element** fest.
5.  Wählen Sie im Feld **Entitätsname** **Bankauszüge** aus.
6.  Um Importdateien hochzuladen, klicken Sie auf **Hochladen**. Wählen Sie die Datei **SampleBankCompositeEntity.xml** aus den zuvor gespeicherten Dateien aus.
7.  Nachdem die Bankauszugsentität hochgeladen und die Zuordnung abgeschlossen ist, klicken Sie auf die Aktion **Zuordnung Anzeigen** der Entität.
8.  Die Bankauszugsentität ist eine zusammengesetzte Entität, die aus vier separaten Entitäten besteht. Wählen Sie in der Liste **BankStatementDocumentEntity** aus, und klicken Sie anschließend auf die Aktivität **Zuordnung anzeigen**.
9.  Klicken Sie auf der Registerkarte **Umwandlungen** auf **Neu**.
10. Klicken Sie für Nummernkreis 1 auf **Datei hochladen**, und wählen Sie die Datei **ISO20022XML Reconciliation.xslt** aus den zuvor gespeicherten Dateien. ** Hinweis: ** Dynamics 365 für Arbeitsgangsumwandlungsdateien werden für das Standardformat erstellt. Da Banken oft ab diesem Format auseinander ausgeführt werden, müssen Sie ggf. die Umwandlungsdatei aktualisieren, um in den Bankauszugsformat zuzuordnen. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Click **New**.
12. Klicken Sie für Nummernkreis 2 auf **Datei hochladen**, und wählen Sie die Datei **BankReconciliation-to-Composite.xslt** aus den zuvor gespeicherten Dateien.
13. Klicken Sie auf **Umwandlungen anwenden**.

Nach dem Einrichten der Formatverarbeitungsgruppe müssen Sie die Bankauszugsformatregeln für ISO20022 Bankauszüge definieren.

1.  Wechseln ** Bargeld- und Bankverwaltung ** &gt; ** Einstellungen ** &gt; ** die erweiterte Bankabstimmung eingerichtet ** &gt; ** Bankauszugsformat **.
2.  Click **New**.
3.  Geben Sie ein Standardformat an (z. B. **ISO20022**).
4.  Geben Sie einen Namens für das Format an.
5.  Legen Sie im Feld **Verarbeitungsgruppe** in der zuvor definierten Gruppe fest (z. B. **ISO20022**).
6.  Aktivieren Sie das Kontrollkästchen **XML-Datei**.

Der letzte Schritt ist Aktivieren der erweiterten Bankabstimmung und das Festlegen des Abstimmungsformates für das Bankkonto.

1.  Wechseln ** Bargeld- und Bankverwaltung ** &gt; ** Bankkonten **.
2.  Wählen Sie das Bankkonto und öffnen Sie es, um die Details anzuzeigen.
3.  Auf der **Abstimmung**-Registerkarte legen Sie die **Erweiterte Bankabstimmung**-Option auf **Ja** fest.
4.  Legen Sie im Feld **Auszugsformat** das Format fest, dass Sie zuvor erstellt haben (z. B. **ISO20022**).

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Einrichten des Imports von MT940-Bankauszügen
Zuerst definieren Sie die Bankauszugs-Formatverarbeitungsgruppe für MT940-Bankauszüge über das Datenentitätsframework.

1.  Wechseln ** Arbeitsbereiche ** &gt; ** Datenverwaltung **.
2.  Click **Import**.
3.  Geben Sie einen Namen ein (z. B. **MT940**).
4.  Legen Sie das Feld **Quelldatenformat** auf **XML-Element** fest.
5.  Wählen Sie im Feld **Entitätsname** **Bankauszüge** aus.
6.  Um Importdateien hochzuladen, klicken Sie auf **Hochladen**. Wählen Sie die Datei **SampleBankCompositeEntity.xml** aus den zuvor gespeicherten Dateien aus.
7.  Nachdem die Bankauszugsentität hochgeladen und die Zuordnung abgeschlossen ist, klicken Sie auf die Aktion **Zuordnung Anzeigen** der Entität.
8.  Die Bankauszugsentität ist eine zusammengesetzte Entität, die aus vier separaten Entitäten besteht. Wählen Sie in der Liste **BankStatementDocumentEntity** aus, und klicken Sie anschließend auf die Aktivität **Zuordnung anzeigen**.
9.  Klicken Sie auf der Registerkarte **Umwandlungen** auf **Neu**.
10. Klicken Sie für Nummernkreis 1 auf **Datei hochladen**, und wählen Sie die Datei **MT940TXT-to-MT940XML.xslt** aus den zuvor gespeicherten Dateien.
11. Klicken Sie auf **Neu**.
12. Klicken Sie für Nummernkreis 2 auf **Datei hochladen**, und wählen Sie die Datei **MT940XML Reconciliation.xslt** aus den zuvor gespeicherten Dateien. ** Hinweis: ** Dynamics 365 für Arbeitsgangsumwandlungsdateien werden für das Standardformat erstellt. Da Banken oft ab diesem Format auseinander ausgeführt werden, müssen Sie ggf. die Umwandlungsdatei aktualisieren, um in den Bankauszugsformat zuzuordnen. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Click **New**.
14. Klicken Sie für Nummernkreis 3 auf **Datei hochladen**, und wählen Sie die Datei **BankReconciliation-to-Composite.xslt** aus den zuvor gespeicherten Dateien.
15. Klicken Sie auf **Umwandlungen anwenden**.

Nach dem Einrichten der Formatverarbeitungsgruppe müssen Sie die Bankauszugsformatregeln für MT940 Bankauszüge definieren.

1.  Wechseln ** Bargeld- und Bankverwaltung ** &gt; ** Einstellungen ** &gt; ** die erweiterte Bankabstimmung eingerichtet ** &gt; ** Bankauszugsformat **.
2.  Click **New**.
3.  Geben Sie ein Standardformat an (z. B. **MT940**).
4.  Geben Sie einen Namens für das Format an.
5.  Legen Sie im Feld **Verarbeitungsgruppe** in der zuvor definierten Gruppe fest (z. B. **MT940**).
6.  Legen Sie das Feld **Dateityp** auf **txt** fest.

Der letzte Schritt ist Aktivieren der erweiterten Bankabstimmung und das Festlegen des Abstimmungsformates für das Bankkonto.

1.  Wechseln ** Bargeld- und Bankverwaltung ** &gt; ** Bankkonten **.
2.  Wählen Sie das Bankkonto und öffnen Sie es, um die Details anzuzeigen.
3.  Auf der **Abstimmung**-Registerkarte legen Sie die **Erweiterte Bankabstimmung**-Option auf **Ja** fest.
4.  Wenn Sie aufgefordert werden, bestätigen Sie Ihre Auswahl, und aktivieren Sie die erweiterte Bankabstimmung. Klicken Sie auf **OK**.
5.  Legen Sie im Feld **Auszugsformat** das Format fest, dass Sie zuvor erstellt haben (z. B. **MT940**).

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Einrichten des Imports von BAI2-Bankauszügen
Zuerst definieren Sie die Bankauszugs-Formatverarbeitungsgruppe für BAI2-Bankauszüge über das Datenentitätsframework.

1.  Wechseln ** Arbeitsbereiche ** &gt; ** Datenverwaltung **.
2.  Click **Import**.
3.  Geben Sie einen Namen ein (z. B. **BAI2**).
4.  Legen Sie das Feld **Quelldatenformat** auf **XML-Element** fest.
5.  Wählen Sie im Feld **Entitätsname** **Bankauszüge** aus.
6.  Um Importdateien hochzuladen, klicken Sie auf **Hochladen**. Wählen Sie die Datei **SampleBankCompositeEntity.xml** aus den zuvor gespeicherten Dateien aus.
7.  Nachdem die Bankauszugsentität hochgeladen und die Zuordnung abgeschlossen ist, klicken Sie auf die Aktion **Zuordnung Anzeigen** der Entität.
8.  Die Bankauszugsentität ist eine zusammengesetzte Entität, die aus vier separaten Entitäten besteht. Wählen Sie in der Liste **BankStatementDocumentEntity** aus, und klicken Sie anschließend auf die Aktivität **Zuordnung anzeigen**.
9.  Klicken Sie auf der Registerkarte **Umwandlungen** auf **Neu**.
10. Klicken Sie für Nummernkreis 1 auf **Datei hochladen**, und wählen Sie die Datei **BAI2CSV-to-BAI2XML.xslt** aus den zuvor gespeicherten Dateien.
11. Klicken Sie auf **Neu**.
12. Klicken Sie für Nummernkreis 2 auf **Datei hochladen**, und wählen Sie die Datei **BAI2XML Reconciliation.xslt** aus den zuvor gespeicherten Dateien. ** Hinweis: ** Dynamics 365 für Arbeitsgangsumwandlungsdateien werden für das Standardformat erstellt. Da Banken oft ab diesem Format auseinander Betrieb und von Ihnen kann die Umwandlungsdatei aktualisieren müssen, um dem Bankauszugsformat zuzuordnen. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Click **New**.
14. Klicken Sie für Nummernkreis 3 auf **Datei hochladen**, und wählen Sie die Datei **BankReconciliation-to-Composite.xslt** aus den zuvor gespeicherten Dateien.
15. Klicken Sie auf **Umwandlungen anwenden**.

Nach dem Einrichten der Formatverarbeitungsgruppe müssen Sie die Bankauszugsformatregeln für BAI2 Bankauszüge definieren.

1.  Wechseln ** Bargeld- und Bankverwaltung ** &gt; ** Einstellungen ** &gt; ** die erweiterte Bankabstimmung eingerichtet ** &gt; ** Bankauszugsformat **.
2.  Click **New**.
3.  Geben Sie ein Standardformat an (z. B. **BAI2**).
4.  Geben Sie einen Namens für das Format an.
5.  Legen Sie im Feld **Verarbeitungsgruppe** in der zuvor definierten Gruppe fest (z. B. **BAI2**).
6.  Legen Sie das Feld **Dateityp** auf **txt** fest.

Der letzte Schritt ist Aktivieren der erweiterten Bankabstimmung und das Festlegen des Abstimmungsformates für das Bankkonto.

1.  Wechseln ** Bargeld- und Bankverwaltung ** &gt; ** Bankkonten **.
2.  Wählen Sie das Bankkonto und öffnen Sie es, um die Details anzuzeigen.
3.  Auf der **Abstimmung**-Registerkarte legen Sie die **Erweiterte Bankabstimmung**-Option auf **Ja** fest.
4.  Wenn Sie aufgefordert werden, bestätigen Sie Ihre Auswahl, und aktivieren Sie die erweiterte Bankabstimmung. Klicken Sie auf **OK**.
5.  Legen Sie im Feld **Auszugsformat** das Format fest, dass Sie zuvor erstellt haben (z. B. **BAI2**).

## <a name="test-the-bank-statement-import"></a>Testen des Bankauszugsimports
Der letzte Schritt ist das Überprüfen des Imports der Bankauszüge.

1.  Wechseln ** Bargeld- und Bankverwaltung ** &gt; ** Bankkonten **.
2.  Wählen Sie das Bankkonto, für das die Funktionalität für die erweiterte Bankabstimmung aktiviert ist.
3.  Klicken Sie auf der **Abstimmen**-Seite auf **Bankauszüge**.
4.  Klicken Sie auf der **Bankauszug**-Seite auf **Auszug importieren**.
5.  Legen Sie das **Bankkonto**-Feld auf das ausgewählte Bankkonto fest. Die **Auszugsformat**-Feld wird automatisch festgelegt (basierend auf der Einstellung für das Bankkonto).
6.  Klicken Sie auf **Durchsuchen**, und wählen Sie die elektronische Bankauszugsdatei.
7.  Klicken Sie auf **Hochladen**.
8.  Klicken Sie auf **OK**.

Wenn der Import erfolgreich ist, erhalten Sie eine Meldung, die besagt, dass das Auszug importiert wurde. Wenn der Import nicht erfolgreich war, finden Sie den Einzelvorgang im **Datenmanagement**-Arbeitsbereich im Abschnitt **Einzelvorgangshistorie**. Klicken Sie auf **Ausführungsdetails** des Einzelvorgangs, um die Seite **Ausführungszusammenfassung** zu öffnen. Klicken Sie auf **Ausführungsprotokoll anzeigen**, um die Importfehler anzuzeigen.


