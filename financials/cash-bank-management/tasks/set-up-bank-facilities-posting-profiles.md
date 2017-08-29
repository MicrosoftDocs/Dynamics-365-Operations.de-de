--- 
title: "Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten"
description: "Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten."
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a4b7f54dfd4f88688691fd9294d71aaae121382b
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten.



Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet. 




## <a name="general-ledger-parameter"></a>Hauptbuchparameter
1. Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.
2. Erweitern Sie den Abschnitt 'Bankdokument'.
3. Wählen Sie diese Option aus, um den Garantiebrief zu aktivieren.
4. Klicken Sie im Feld Transaktionserfassung auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf die Registerkarte "Nummernkreis".
    * Definieren Sie Nummernkreiscode für Garantiebriefnummer und Garantiebriefbuchungsreferenzen  
8. Klicken Sie auf "Speichern".
9. Schließen Sie die Seite.

## <a name="create-bank-facility"></a>Bankfazilität erstellen
1. Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankinstitut".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld Fazilitätsgruppe den Namen der Bankfazilitätsgruppe für die Garantiebriefbuchung ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie auf die Fazilitätstypregisterkarte.
7. Klicken Sie auf "Neu".
8. Geben Sie im Feld Fazilitätsgruppe den Namen des Bankfazilitätstyps, der sich auf die Bankfazilitätsvereinbarung bezieht.
9. Geben Sie im Feld "Beschreibung" einen Wert ein.
10. Klicken Sie im Feld Fazilitätsgruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
13. Wählen Sie im Feld Fazilitätsart eine Option aus.
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.

## <a name="bank-posting-profile"></a>Bankbuchungsprofil
1. Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankdokumentenbuchungsprofil.
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Konto-/Gruppennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Wählen Sie im Feld Buchungskonto das Hauptkonto für den Ausgleich aus.
7. Wählen Sie im Feld Gebührenkonto das Konto für Ausgabenbuchungen aus.
8. Wählen Sie im Feld Einschusskonto das Konto für die Einschusstransaktion aus.
9. Wählen Sie im Feld Liquidationskonto das Liquidationskonto für die Garantiebriefbuchung aus. 
10. Klicken Sie auf Speichern.
11. Schließen Sie die Seite.


