--- 
title: Kreditorenrechnungsrichtlinien einrichten
description: "Kreditorenrechnungsrichtlinien werden ausgeführt, wenn Sie mit der Seite \"Kreditorenrechnung\" eine Kreditorenrechnung buchen und wenn Sie die Seite \"Richtlinienverstöße\" der Kreditorenrechnung öffnen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f51c117da75a0382a38e75154ecef758f9a5d6c1
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vendor-invoice-policies"></a>Kreditorenrechnungsrichtlinien einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kreditorenrechnungsrichtlinien werden ausgeführt, wenn Sie mit der Seite "Kreditorenrechnung" eine Kreditorenrechnung buchen und wenn Sie die Seite "Richtlinienverstöße" der Kreditorenrechnung öffnen. Sie können auch den Workflow für Kreditorenrechnungen konfigurieren, sodass Kreditorenrechnungsrichtlinien immer ausgeführt werden, wenn eine Rechnung an den Workflow übermittelt wird. 

Kreditorenrechnungsrichtlinien werden nicht auf Rechnungen angewendet, die im Rechnungsbuch oder in einer Rechnungserfassung erstellt wurden. 

Für die Rechnungsabgleichüberprüfung werden keine Kreditorenrechnungsrichtlinien verwendet. Stattdessen wird die Prüfung auf der Seite "Kreditorenkontenparameter" eingerichtet.

Für diese Erfassung wird das Demo-Unternehmen USMF verwendet. Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen. Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Vorbereitung zum Erstellen von Kreditorenrechnungsrichtlinien
1. Wechseln Sie zu Kreditoren > Einstellung > Kreditorenparameter.
2. Klicken Sie auf die Registerkarte "Rechnungsprüfung".
3. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Rechnungskopfstatus automatisch aktualisieren".
4. Klicken Sie auf "OK".
5. Wählen Sie im Feld "Rechnung mit Abweichungen buchen" eine Option aus.
6. Schließen Sie die Seite.
7. Wechseln Sie zu "Kreditoren" > "Richtlinieneinstellung" > "Kreditorenrechnungsrichtlinien".
8. Klicken Sie auf "Parameter".
9. Klicken Sie auf die Schaltfläche "Hinzufügen."
10. Schließen Sie die Seite.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Erstellen von Richtlinienregeltypen für Kreditorenrechnungen
1. Wechseln Sie zu "Kreditoren" > "Richtlinieneinstellung" > "Kreditorenrechnungs-Richtlinienregeltypen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Regelname" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Abfragename" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie auf "Speichern".
9. Schließen Sie die Seite.

## <a name="define-a-vendor-invoice-policy"></a>Definieren einer Kreditorenrechnungsrichtlinie
1. Wechseln Sie zu "Kreditoren" > "Richtlinieneinstellung" > "Kreditorenrechnungsrichtlinien".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Erweitern oder reduzieren Sie den Abschnitt "Richtlinienorganisationen".
6. Wählen Sie in der Struktur "Contoso Unterhaltungsanlagen USA" aus.
7. Klicken Sie auf Hinzufügen.
8. Erweitern oder reduzieren Sie den Abschnitt "Richtlinienregeln".
9. Klicken Sie auf "Richtlinienregel erstellen".
10. Geben Sie im Feld "Richtlinienregel" einen Wert ein.
11. Klicken Sie auf "Filter".
12. Klicken Sie auf Hinzufügen.
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. Klicken Sie im Feld "Tabelle" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
16. Klicken Sie im Feld "Abgeleitete Tabelle" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
18. Klicken Sie im Feld "Feld" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
19. Geben Sie im Feld "Feld" einen Wert ein.
20. Schließen Sie die Seite.
21. Geben Sie im Feld "Kriterien" einen Wert ein.
22. Klicken Sie auf "OK".
23. Klicken Sie auf "OK".
24. Schließen Sie die Seite.
25. Schließen Sie die Seite.


