---
title: ER Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format (November 2016)
description: In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea5b17873dea4508230f39ffb41a50e2f427584f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142131"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format (November 2016)

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält. Diese Konfiguration wird zur Verarbeitung von Kreditorenzahlungen verwendet.

In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können im GBSI-Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen. Sie müssen auch über eine Excel-Datei verfügen, die importiert wird, wenn die Vorlage erstellt wird. Auf diese Datei kann aus der [Vorlage des Zahlungsberichgte](https://go.microsoft.com/fwlink/?linkid=862266) zugegriffen werden.


## <a name="upload-the-payments-data-model-configuration"></a>Laden Sie die Zahlungsdatenmodell-Konfiguration hoch
1. Gehen Sie im Navigationsbereich zu **Module > Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung**.
2. Markieren Sie in der Liste den Konfigurationsanbieter für die Musterfirma Litware, Inc. Wenn Sie diesen Konfigurationsanbieter nicht sehen können, müssen Sie zunächst die Schritte unter [Konfigurationsanbieter anlegen ausführen und ihn als aktiv](er-configuration-provider-mark-it-active-2016-11.md) markieren.
3. Wählen Sie **Als aktiv festlegen**.
4. Wählen Sie **Repositorys** aus. Wählen Sie ein Repository für den Typ „Betriebliche Ressource” aus, falls verfügbar. Wenn es verfügbar ist, überspringen Sie die folgenden Schritte zur Erstellung eines neuen Repository.  
5. Wählen Sie **Hinzufügen**, um das Dropdown-Dialogfeld zu öffnen.
6. Wählen Sie im Feld **Konfigurationsrepository-Typ** `Operations resourcesdd`.
7. Wählen Sie **Repository erstellen**.
8. Wählen Sie **OK**.
9. Wählen Sie **Öffnen**.
10. Wählen Sie in der Struktur die Option **Zahlungsmodell** aus.
11. **Import** auswählen Importieren Sie dieses Datenmodell. Es wird als Datenquelle in einer neuen Formatkonfiguration verwendet. Überspringen Sie diesen Schritt, wenn diese Konfiguration bereits importiert wurde.  
12. Wählen Sie **Ja** aus.
13. Schließen Sie die Seiten, bis Sie zur Seite „Elektronische Berichterstellung“ zurückgekehrt sind.

## <a name="create-a-new-format-configuration"></a>Dient zum Erstellen einer neuen Format-Konfiguration.
1. Wählen Sie **Berichterstellungskonfigurationen** aus.
2. Wählen Sie in der Struktur die Option **Zahlungsmodell** aus.
3. Wählen Sie **Konfiguration erstellen** aus, um das Dropdown-Dialogfeld zu öffnen.
4. Geben Sie im Feld **Neu** `Format based on data model PaymentModel` ein. Erstellen Sie ein Format, das auf dem PaymentModel-Datenmodell basiert.
5. Geben Sie im Feld **Name** `Sample worksheet report` ein. Beispiel-Arbeitsblattbericht  
6. Geben Sie im Feld **Beschreibung** `Sample worksheet report for vendors' payments` ein. Beispiel-Arbeitsblattbericht für Zahlungen von Händler.  
7. Geben Sie im Feld **Datenmodelldefinition** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie die Definition **CustomerCreditTransferInitiation** aus.  
8. Wählen Sie **Konfiguration erstellen**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Entwerfen Sie ein neues Dokument im OPENXML-Arbeitsblattformat
1. Wählen Sie in der Struktur die Option **Zahlungsmodell\Beispiel-Arbeitsblattbericht** aus.
2. Wählen Sie **Designer** aus.
3. Wählen Sie im Aktivitätsbereich **Importieren** aus.
4. Wählen Sie **Aus Excel importieren** aus.
5. Wählen Sie **Anhänge** aus. Fügen Sie das vorhandene Excel-Dokument als Vorlage an.  
6. Wählen Sie **Neu** aus.
7. Wählen Sie **Datei** aus. Zeigen Sie auf die vorhandene Excel-Datei.  
8. Schließen Sie die Seite.
9. Geben Sie im Feld **Vorlage** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie die angefügte Excel-Datei aus, um als Vorlage verwendet zu werden.  
10. Wählen Sie **OK**. Beachten Sie, dass ER-Formatkomponenten im Entwurfsformat auf Grundlage der Struktur des verweisenden MS Excel-Dokuments (genannte Bereiche) erstellt wurden.  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Erstellen Sie eine neue Datenquelle, um Summen nach Währungscodes zu berechnen
1. Wählen Sie die Registerkarte **Zuordnung** aus.
2. Wählen Sie **Stamm hinzufügen** aus, um das Dropdown-Dialogfeld zu öffnen.
3. Wählen Sie in der Struktur **Funktionen\Gruppieren nach** aus.
4. Geben Sie im Feld **Name** `PaymentByCurrency` ein.
5. Wählen Sie **Gruppe bearbeiten von** aus.
6. Erweitern Sie in der Struktur **Modell**, und wählen Sie dann **Modell\Zahlungen** aus.
7. Wählen Sie **Feld hinzufügen zu** aus.
8. Wählen Sie **Was gruppieren** aus.
9. Erweitern Sie in der Struktur **Modell\Zahlungen**, und wählen Sie dann **Modell\Zahlungen\Währungen** aus.
10. Wählen Sie **Feld hinzufügen zu** aus.
11. Wählen Sie **Gruppierte Felder** aus.
12. In der Struktur wählen Sie **Modell\Zahlungen\Angewiesener Betrag (InstructedAmount)** aus.
13. Wählen Sie **Feld hinzufügen zu** aus, und wählen Sie dann **Aggregationsfelder** aus.
14. Wählen Sie im Feld **Methode** eine Option aus. Wählen Sie die **SUMMEN_Aggregation**-Funktion aus.  
15. Geben Sie im Feld **Name** `TotalInstructuredAmount` ein.
16. Wählen Sie **Speichern**.
17. Schließen Sie die Seite.
18. Wählen Sie **OK**.

## <a name="map-format-components-to-data-sources"></a>Weisen Sie Datenquellen Formatkomponenten zu
1. Wählen Sie in der Struktur **Modell\Zahlungen\Einleitende Partei(InitiatingParty)\Name** und **Excel\ReportHeader\CompanyName** aus.
2. Wählen Sie **Bindung** aus.
3. In der Struktur wählen Sie **Modell\Zahlungen\Kreditor\Kennung\Quell-ID(SourceID)** und **Excel\PaymLines\VendAccountName** aus.
4. Wählen Sie **Bindung** aus.
5. In der Struktur wählen Sie **Modell\Zahlungen\Kreditor\Name** und **Excel\PaymLines\VendName** aus.
6. Wählen Sie **Bindung** aus.
7. In der Struktur wählen Sie **Modell\Zahlungen\Kreditoragent(CreditorAgent)\Name** und **Excel\PaymLines\Bank** aus.
8. Wählen Sie **Bindung** aus.
9. In der Struktur wählen Sie **Modell\Zahlungen\Kreditoragent(CreditorAgent)\Bankleitzahl(RoutingNumber)** und **Excel\PaymLines\RoutingNumber** aus.
10. Wählen Sie **Bindung** aus.
11. In der Struktur wählen Sie **Modell\Zahlungen\Kreditorenkonto(CreditorAccount)\Kennung\Nummer** und **Excel\PaymLines\AccountNumber** aus.
12. Wählen Sie **Bindung** aus.
13. In der Struktur wählen Sie **Modell\Zahlungen\Angewiesener Betrag(InstructedAmount)** und **Excel\PaymLines\Soll** aus.
14. Wählen Sie **Bindung** aus.
15. In der Struktur wählen Sie **Modell\Zahlungen\Währung** und **Excel\PaymLines\Währung** aus.
16. Wählen Sie **Bindung** aus.
17. In der Struktur wählen Sie **PaymentByCurrency\grouped\Currency** und **Excel\SummaryLines\SummaryCurrency** aus.
18. Wählen Sie **Bindung** aus.
19. In der Struktur wählen Sie **PaymentByCurrency\aggregated\TotalInstructuredAmount** und **Excel\SummaryLines\SummaryAmount** aus.
20. Wählen Sie **Bindung** aus.
21. Wählen Sie in der Struktur **PaymentByCurrency** und **Excel\SummaryLines** aus.
22. Wählen Sie **Bindung** aus.
23. In der Struktur wählen Sie **Modell\Zahlungen** und **Excel\PaymLines** aus.
24. Wählen Sie **Bindung** aus.
25. Wählen Sie **Speichern** aus, und schließen Sie dann die Seite.

## <a name="use-the-created-configuration-for-payments-processing"></a>Nutzen Sie die erstellte Konfiguration für die Zahlungsverarbeitung
1. Wählen Sie **Status ändern** aus.
2. Wählen Sie **Abgeschlossen** aus.
3. Wählen Sie **OK**.
4. Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Zahlungseinstellungen > Zahlungsmethoden**.
5. Verwenden Sie den Schnellfilter, um im Feld **Zahlungsmethode** nach dem Wert **Elektronisch** zu filtern.
6. Wählen Sie **Bearbeiten** aus.
7. Erweitern Sie den Abschnitt **Dateiformate**.
8. Wählen Sie **Ja** im Feld **Generische elektronische Berichterstellung** aus.
9. Wählen Sie im Feld **Formatkonfiguration exportieren** einen Wert aus oder geben Sie ihn ein. Wählen Sie die Variante **Beispiel-Arbeitsblattbericht** aus.  
10. Wählen Sie **Speichern**.
11. Schließen Sie die Seite.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Verwenden Sie die erstellte Konfiguration für das Testen der Zahlungserfassungsverarbeitung
1. Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Zahlungen > Zahlungserfassung**.
2. Wählen Sie **Neu** aus, um eine neue Zahlungserfassung zu erstellen.
3. Geben Sie im Feld **Name** **VendPay** ein.
4. Wählen Sie **Positionen** aus.
5. Geben Sie im Feld **Konto** die Werte `GB_SI_000001` ein.
6. Legen Sie **Soll** auf `1000` fest.
7. Wählen Sie **Neu** aus.
8. Geben Sie im Feld **Konto** die Werte `GB_SI_000005` ein.
9. Legen Sie **Soll** auf `2000` fest.
10. Geben Sie im Feld **Währung** die Zeichenfolge `EUR` ein.
11. Geben Sie im Feld **Gegenkonto** den Wert `GBSI OPER` an.
12. Geben Sie im Feld **Zahlungsmethode** `Electronic` ein.
13. Wählen Sie **Speichern**.
14. Wählen Sie **Zahlungen generieren** aus.
15. Geben Sie im Feld **Zahlungsmethode** `Electronic` ein.
16. Geben Sie im Feld **Dateiname** `Payments` ein.
17. Geben Sie im Feld **Bankkonto** `GBSI OPER` ein.
18. Wählen Sie **OK** und dann erneut **OK** aus. Überprüfen Sie das erstellte Arbeitsblatt, einschließlich Details von Zahlungspositionen sowie der Summen für jeden Währungscode, der in dieser Zahlungsnachricht verwendet wird.  

