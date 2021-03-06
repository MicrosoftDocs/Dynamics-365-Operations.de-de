---
title: Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten
description: Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1147650944ba40d1c8054444c09db9c5ee97bde3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834619"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]