---
title: Bankfazilitäten und Buchungsprofile für Akkreditiv einrichten
description: Gänge dieser Prozedur mithilfe einer Bankfazilität und Buchungsprofilen erforderlich, Kreditbrief zu verarbeiten.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 15a7a4798c4c743c9171fd2258a5573f456c92e5
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726349"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Bankfazilitäten und Buchungsprofile für Akkreditiv einrichten

[!include [banner](../../includes/banner.md)]

Gänge dieser Prozedur mithilfe einer Bankfazilität und Buchungsprofilen erforderlich, Kreditbrief zu verarbeiten. 

Für diese Aufgaben wird das Demo-Unternehmen USMF verwendet.






## <a name="general-ledger-parameter"></a>Hauptbuchparameter
1. Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.
2. Erweitern Sie den Abschnitt 'Bankdokument'.
3. Wählen Sie diese Option aus, um den Importkreditbrief zu aktivieren.
4. Wählen Sie diese Option aus, um den Exportkreditbrief zu aktivieren.
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.

## <a name="create-bank-facility"></a>Bankfazilität erstellen
1. Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankinstitut".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld Fazilitätsgruppe den Namen der Bankfazilitätsgruppe ein.
4. Geben Sie im Feld Beschreibung die Beschreibung der Bankfazilitätsgruppe ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie auf die Fazilitätstypregisterkarte.
7. Klicken Sie auf "Neu".
8. Geben Sie im Feld Fazilitätsgruppe einen eindeutigen Code ein.
9. Geben Sie im Feld "Beschreibung" einen Wert ein.
10. Klicken Sie im Feld Fazilitätsgruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
13. Wählen Sie im Feld Fazilitätstyp die Art der Bankfazilität aus
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.

## <a name="bank-posting-profile"></a>Bankbuchungsprofil
1. Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankdokumentenbuchungsprofil.
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Konto-/Gruppennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Kategorie für den Ausgleich auswählen.
    * Dieses Konto wird bei der Berechnung der Cashflow-Planung verwendet.  
7. Wählen Sie im Feld Gebührenkonto das Konto für Ausgabenbuchungen aus.
8. Wählen Sie im Feld Einschusskonto das Konto für Einschussbuchungen aus.
    * Dieses Konto wird bei der Buchung der Eröffnungsmarge belastet und bei der Buchung der Zahlung entlastet.  
9. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
