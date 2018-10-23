--- 
title: "ER Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format (November 2016)"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format (November 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält. Diese Konfiguration wird zur Verarbeitung von Kreditorenzahlungen verwendet.



In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können im GBSI-Unternehmen ausgeführt werden.



Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen. Sie müssen auch über eine Excel-Datei verfügen, die importiert wird, wenn die Vorlage erstellt wird. Auf diese Datei kann aus der [Vorlage des Zahlungsberichgte](https://go.microsoft.com/fwlink/?linkid=862266) zugegriffen werden.


## <a name="upload-the-payments-data-model-configuration"></a>Laden Sie die Zahlungsdatenmodell-Konfiguration hoch
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie den Konfigurationsanbieter für das Beispielunternehmen "Litware, Inc.". Wenn Sie diesen Konfigurationsanbieter nicht finden, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.  
3. Klicken Sie auf "Als aktiv festlegen"
4. Klicken Sie auf Repositorys.
    * Wählen Sie ein Repository für den Typ „Betriebliche Ressource” aus, falls verfügbar. Wenn es verfügbar ist, überspringen Sie die folgenden Schritte zur Erstellung eines neuen Repository.  
5. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
6. Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.
7. Klicken Sie auf "Repository erstellen".
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Öffnen".
10. Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.
11. Klicken Sie auf Import.
    * Importieren Sie dieses Datenmodell. Es wird als Datenquelle in einer neuen Formatkonfiguration verwendet. Überspringen Sie diesen Schritt, wenn diese Konfiguration bereits importiert wurde.  
12. Klicken Sie auf "Ja".
13. Schließen Sie die Seite.
14. Schließen Sie die Seite.

## <a name="create-a-new-format-configuration"></a>Dient zum Erstellen einer neuen Format-Konfiguration.
1. Klicken Sie auf "Berichterstellungskonfigurationen".
2. Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.
3. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
4. Wählen Sie im neuen Feld geben Sie "Format auf Grundlage Datenmodell PaymentModel" ein.
    * Erstellen Sie ein Format, das auf dem PaymentModel-Datenmodell basiert.  
5. Geben Sie im Feld "Name" die Bezeichnung "Beispiel-Arbeitsblattbericht" ein.
    * Beispiel-Arbeitsblattbericht  
6. Geben Sie im Feld "Beschreibung" die Bezeichnung "Beispiel-Arbeitsblattbericht für Kreditorenzahlungen" ein.
    * Beispiel-Arbeitsblattbericht für Zahlungen der Händler.  
7. Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die Definition "CustomerCreditTransferInitiation" aus.  
8. Klicken Sie auf Konfiguration erstellen.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Entwerfen Sie ein neues Dokument im OPENXML-Arbeitsblattformat
1. Wählen Sie in der Struktur die Option "Zahlungsmodell \Beispiel-Arbeitsblattbericht" aus.
2. Klicken Sie auf Designer.
3. Klicken Sie im Aktivitätsbereich auf "Importieren".
4. Klicken Sie auf "Aus Excel importieren".
5. Klicken Sie auf Anhänge.
    * Fügen Sie das vorhandene Excel-Dokument als Vorlage an.  
6. Klicken Sie auf "Neu".
7. Klicken Sie auf "Datei".
    * Zeigen Sie auf die vorhandene Excel-Datei.  
8. Schließen Sie die Seite.
9. Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die angefügte Excel-Datei aus, um als Vorlage verwendet zu werden.  
10. Klicken Sie auf "OK".
    * Beachten Sie, dass ER-Formatkomponenten im Entwurfsformat auf Grundlage der Struktur des verweisenden MS Excel-Dokuments (genannte Bereiche) erstellt wurden.  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Erstellen Sie eine neue Datenquelle, um Summen nach Währungscodes zu berechnen
1. Klicken Sie auf die Registerkarte Zuordnung.
2. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
3. Wählen Sie in der Struktur "Funktionen\Gruppieren nach" aus.
4. Geben Sie im Feld "Name" die Zeichenfolge "PaymentByCurrency" ein.
    * PaymentByCurrency  
5. Klicken Sie auf "Gruppe bearbeiten von".
6. Erweitern Sie in der -Struktur den Knoten 'Modell'.
7. Wählen Sie 'Modell\Zahlungen' in der Struktur aus.
8. Klicken Sie auf "Feld hinzufügen zu".
9. Klicken Sie auf "Was gruppieren".
10. Erweitern Sie 'Modell\Zahlungen' in der Struktur.
11. Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.
12. Klicken Sie auf "Feld hinzufügen zu".
13. Klicken Sie auf "Gruppierte Felder".
14. In der Struktur wählen Sie "Modell\Zahlungen\Angewiesener Betrag (InstructedAmount)" aus.
15. Klicken Sie auf "Feld hinzufügen zu".
16. Klicken Sie auf "Aggregationsfelder".
17. Wählen Sie im Feld "Methode" eine Option aus.
    * Wählen Sie die SUMMEN_Aggregationsfunktion aus.  
18. Geben Sie im Feld "Name" die Zeichenfolge "TotalInstructuredAmount" ein.
    * TotalInstructuredAmount  
19. Klicken Sie auf "Speichern".
20. Schließen Sie die Seite.
21. Klicken Sie auf "OK".

## <a name="map-format-components-to-data-sources"></a>Weisen Sie Datenquellen Formatkomponenten zu
1. Erweitern Sie in der -Struktur den Knoten 'Modell'.
2. Erweitern Sie 'Modell\Zahlungen' in der Struktur.
3. Erweitern Sie in der Struktur "Modell\Zahlungen\Einleitende Partei(InitiatingParty)".
4. Wählen Sie in der Struktur "'Modell\Zahlungen\Einleitende Partei(InitiatingParty)\Name" aus.
5. Erweitern oder reduzieren Sie „Excel\ReportHeader” in der Struktur.
6. Wählen Sie „Excel\ReportHeader\CompanyName” in der Struktur aus.
7. Klicken Sie auf Binden.
8. Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.
9. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Kennung".
10. In der Struktur wählen Sie "Modell\Zahlungen\Kreditor\Kennung\Quell-ID(SourceID)" aus.
11. Erweitern Sie „Excel\PaymLines” in der Struktur.
12. Wählen Sie in der Struktur „Excel\PaymLines\VendAccountName” aus.
13. Klicken Sie auf Binden.
14. Wählen Sie 'Modell\Payments\Creditor\Account\Name' in der Struktur aus.
15. Wählen Sie in der Struktur „Excel\PaymLines\VendName” aus.
16. Klicken Sie auf Binden.
17. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)".
18. In der Struktur wählen Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)\Name" aus.
19. Wählen Sie in der Struktur „Excel\PaymLines\Bank” aus.
20. Klicken Sie auf Binden.
21. Wählen Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)\Bankleitzahl(RoutingNumber)" in der Struktur aus.
22. Wählen Sie in der Struktur „Excel\PaymLines\RoutingNumber” aus.
23. Klicken Sie auf Binden.
24. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)".
25. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)\Identification".
26. In der Struktur wählen Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)\Kennung\Nummer".
27. Wählen Sie in der Struktur „Excel\PaymLines\AccountNumber” aus.
28. Klicken Sie auf Binden.
29. In der Struktur wählen Sie "Modell\Zahlungen\Angewiesener Betrag (InstructedAmount)" aus.
30. Wählen Sie in der Struktur „Excel\PaymLines\Soll” aus.
31. Klicken Sie auf Binden.
32. Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.
33. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)".
34. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)".
35. Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.
36. Wählen Sie in der Struktur „Excel\PaymLines\Währung” aus.
37. Klicken Sie auf Binden.
38. Erweitern Sie "PaymentByCurrency" in der Struktur.
39. Erweitern Sie "PaymentByCurrency\grouped" in der Struktur.
40. Wählen Sie in der Struktur "PaymentByCurrency\grouped\Currency" aus.
41. Erweitern Sie „Excel\SummaryLines” in der Struktur.
42. Wählen Sie in der Struktur „Excel\SummaryLines\SummaryCurrency” aus.
43. Klicken Sie auf Binden.
44. Erweitern Sie "PaymentByCurrency\aggregated" in der Struktur.
45. Wählen Sie in der Struktur "PaymentByCurrency\aggregated\TotalInstructuredAmount" aus.
46. Wählen Sie in der Struktur „Excel\SummaryLines\SummaryAmount” aus.
47. Klicken Sie auf Binden.
48. Wählen Sie in der Struktur "PaymentByCurrency" aus.
49. Wählen Sie in der Struktur „Excel\SummaryLines” aus.
50. Klicken Sie auf Binden.
51. Wählen Sie 'Modell\Zahlungen' in der Struktur aus.
52. Wählen Sie in der Struktur „Excel\PaymLines” aus.
53. Klicken Sie auf Binden.
54. Klicken Sie auf "Speichern".
55. Schließen Sie die Seite.

## <a name="use-the-created-configuration-for-payments-processing"></a>Nutzen Sie die erstellte Konfiguration für die Zahlungsverarbeitung
1. Klicken Sie auf "Status ändern".
2. Klicken Sie auf "Abgeschlossen".
3. Klicken Sie auf "OK".
4. Schließen Sie die Seite.
5. Schließen Sie die Seite.
6. Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
7. Verwenden Sie den Schnellfilter, um im Feld „Zahlungsmethode” nach dem Wert „Elektronisch” zu filtern.
    * Elektronisch  
8. Klicken Sie auf "Bearbeiten".
9. Erweitern Sie den Abschnitt 'Dateiformate'.
10. Wählen Sie "Ja" im Feld "Generische elektronische Berichterstellung" aus.
11. Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.
    * Wählen Sie die Variante "Beispiel-Arbeitsblattbericht" aus.  
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Verwenden Sie die erstellte Konfiguration für das Testen der Zahlungserfassungsverarbeitung
1. Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".
2. Klicken Sie auf "Neu".
    * Erstellen Sie eine Zahlungserfassung.  
3. Geben Sie im Namensfeld "VendPay" ein.
    * VendPay  
4. Klicken Sie auf "Positionen".
5. Geben Sie im Feld "Konto" die Werte "GB_SI_000001" an.
    * GB_SI_000001  
6. Legen Sie "Soll" auf "1000" fest.
7. Klicken Sie auf "Neu".
8. Geben Sie im Feld "Konto" die Werte "GB_SI_000005" an.
    * GB_SI_000005  
9. Legen Sie "Soll" auf "2000" fest.
10. Geben Sie im Feld "Währung" die Zeichenfolge "EUR" ein.
    * EUR  
11. Geben Sie im Feld "Gegenkonto" die Werte "GBSI OPER" an.
    * GBSI OPER  
12. Geben Sie im Feld "Zahlungsmethode" die Option "Elektronisch" ein.
    * Elektronisch  
13. Klicken Sie auf "Speichern".
14. Klicken Sie auf Zahlungen generieren.
15. Geben Sie im Feld "Zahlungsmethode" die Option "Elektronisch" ein.
    * Elektronisch  
16. Geben Sie im Feld „Dateiname” die Bezeichnung „Zahlungen” ein.
    * Geben Sie beispielsweise "Zahlungen" ein.  
17. Geben Sie im Feld "Bankkonto" die Zeichenfolge "GBSI OPER" ein.
    * GBSI OPER  
18. Klicken Sie auf "OK".
19. Klicken Sie auf "OK".
    * Überprüfen Sie das erstellte Arbeitsblatt, einschließlich Details von Zahlungspositionen sowie der Summen für jeden Währungscode, der in dieser Zahlungsnachricht verwendet wird.  


