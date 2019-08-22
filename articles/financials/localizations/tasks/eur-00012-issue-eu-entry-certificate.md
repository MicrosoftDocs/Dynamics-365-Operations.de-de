---
title: EUR-00012 Ausstellen einer EU-Gelangensbestätigung
description: Diese Prozedur läuft Sie durch das Aktivieren einer EU-Eintragsbescheinigung nach und konfiguriert ein Debitorenkonto, um Eintragsbescheinigungen zu verwenden und eine Bescheinigung auszustellen.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 735331fd399ba9501031084e236b88c0e11bb179
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848846"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a>EUR-00012 Ausstellen einer EU-Gelangensbestätigung

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur läuft Sie durch das Aktivieren einer EU-Eintragsbescheinigung nach und konfiguriert ein Debitorenkonto, um Eintragsbescheinigungen zu verwenden und eine Bescheinigung auszustellen. Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.


## <a name="enable-entry-certificate-management"></a>Verwaltung der Gelangensbestätigung aktivieren
1. Wechseln Sie zu "Kreditoren" > "Einstellung" > "Kreditorenparameter".
2. Klicken Sie auf die Registerkarte ''.
3. Erweitern Sie den Eintragsbescheinigungsabschnitt.
4. Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren
5. Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren
6. Klicken Sie auf die Registerkarte "Nummernkreis".
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Geben Sie im Feld "Ursprüngliche Rechnungsnummer" einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="set-up-a-customer"></a>Einrichten einer Debitorenvorauszahlung
1. Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Konto" mit dem Wert "DE-015".
3. Die Details des Debitorenkontos öffnen.
4. Klicken Sie auf Bearbeiten.
5. Erweitern Sie den Rechnungs- und Lieferungsabschnitt.
6. Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren
7. Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren
8. Klicken Sie auf "Speichern".

## <a name="create-an-eu-entry-certificate-automatically"></a>Erhalt einer EU-Gelangensbestätigung
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
6. Klicken Sie auf "Speichern".
7. Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".
8. Klicken Sie auf "Lieferschein buchen".
9. Erweitern Sie den Abschnitt "Parameter".
10. Wählen Sie im Feld "Menge" die Option "Alle" aus.
11. Aktivieren Sie dieses Kontrollkästchen, um Gelangensbestätigungen auszustellen
    * Eine Eintragsbescheinigung kann während der Lieferscheinbuchung oder während der Auftragsrechnungsstellung ausgegeben werden. Verlassen Sie das Abgangseintrags-Bescheinigungskontrollkästchen deaktiviert, um ihn später auszugeben.  
12. Klicken Sie auf "OK".
13. Klicken Sie auf "OK".
14. Klicken Sie im Aktivitätsbereich auf "Rechnung".
15. Klicken Sie auf "Rechnung".
    * Überprüfen Sie, ob die Eintragsbescheinigung Buchungszeitpunkt und Abgangseintrags-Bescheinigungskontrollkästchen im Überblicksabschnitt markiert sind.  Sie können das Druckseintrags-Bescheinigungskontrollkästchen auch auswählen, um das Drucken der Bescheinigung zu ermöglichen.  
16. Klicken Sie auf "OK".
17. Klicken Sie auf "OK".
18. Klicken Sie im Aktivitätsbereich auf "Rechnung".
19. Klicken Sie auf "Rechnung".
20. Klicken Sie im Aktivitätsbereich auf "Rechnung".
21. Ausgestellte Gelangensbestätigungen anzeigen
22. Klicken Sie auf Drucken.
23. Schließen Sie die Seite.
24. Klicken Sie auf "Status ändern".
25. Wählen Sie im Feld Status eine Option aus.
26. Klicken Sie auf "OK".
27. Schließen Sie die Seite.

## <a name="create-an-eu-entry-certificate-manually"></a>Erhalt einer EU-Gelangensbestätigung
1. Klicken Sie im Aktivitätsbereich auf "Rechnung".
2. Gelangensbestätigung erstellen
3. Klicken Sie auf "OK".
4. Klicken Sie im Aktivitätsbereich auf "Rechnung".
5. Ausgestellte Gelangensbestätigungen anzeigen

