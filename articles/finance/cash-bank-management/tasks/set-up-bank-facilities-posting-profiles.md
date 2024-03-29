---
title: Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten
description: Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0987ae1e9cfbb1e2d2a957a5fd1ad82257292c0a
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804100"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten

[!include [banner](../../includes/banner.md)]

Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten.



Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet. 




## <a name="general-ledger-parameter"></a>Hauptbuchparameter
1. Wechseln Sie zu **Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung**.
2. Erweitern Sie den Abschnitt **Bankdokument**.
3. Wählen Sie diese Option aus, um den **Garantiebrief zu aktivieren**.
4. Klicken Sie im Feld **Transaktionserfassung** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf die Registerkarte **Nummernkreis**.
    * Definieren Sie Nummernkreiscode für Garantiebriefnummer und Garantiebriefbuchungsreferenzen  
8. Klicken Sie auf **Speichern**.
9. Schließen Sie die Seite.

## <a name="create-bank-facility"></a>Bankfazilität erstellen
1. Gehen Sie zu **Kasse und Bankverwaltung > Einstellungen > Bankinstitut**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Fazilitätsgruppe** den Namen der Bankfazilitätsgruppe für die Garantiebriefbuchung ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Klicken Sie auf **Speichern**.
6. Klicken Sie auf die **Fazilitätstyp** Registerkarte.
7. Klicken Sie auf **Neu**.
8. Geben Sie im Feld **Fazilitätsgruppe** den Namen des Bankfazilitätstyps, der sich auf die Bankfazilitätsvereinbarung bezieht.
9. Geben Sie im Feld **Beschreibung** einen Wert ein.
10. Klicken Sie im Feld **Fazilitätsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
13. Wählen Sie im Feld **Fazilitätsart** eine Option aus.
14. Klicken Sie auf **Speichern**.
15. Schließen Sie die Seite.

## <a name="bank-posting-profile"></a>Bankbuchungsprofil
1. Gehen Sie zu **Kasse und Bankverwaltung > Einstellungen > Bankdokumentenbuchungsprofil**.
2. Klicken Sie auf **Neu**.
3. Klicken Sie im Feld **Konto-/Gruppennummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Wählen Sie im Feld **Buchungskonto** das Hauptkonto für den Ausgleich aus.
7. Wählen Sie im Feld **Gebührenkonto** das Konto für Ausgabenbuchungen aus.
8. Wählen Sie im Feld **Einschusskonto** das Konto für die Einschusstransaktion aus.
9. Wählen Sie im Feld **Liquidationskonto** das Liquidationskonto für die Garantiebriefbuchung aus. 
10. Klicken Sie auf **Speichern**.
11. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
