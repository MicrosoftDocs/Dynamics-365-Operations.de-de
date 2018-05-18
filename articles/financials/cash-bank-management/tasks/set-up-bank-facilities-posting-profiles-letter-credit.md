--- 
title: "Bankfazilitäten und Buchungsprofile für Akkreditiv einrichten"
description: "Gänge dieser Prozedur mithilfe einer Bankfazilität und Buchungsprofilen erforderlich, Kreditbrief zu verarbeiten."
author: kweekley
manager: AnnBe
ms.date: 10/27/2017
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
ms.sourcegitcommit: 18ad27eb673745d09569f6a49c8bc66132550f35
ms.openlocfilehash: 9ad19534091bdbd8924f90174b720d818b9ed778
ms.contentlocale: de-de
ms.lasthandoff: 10/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Bankfazilitäten und Buchungsprofile für Akkreditiv einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gänge dieser Prozedur mithilfe einer Bankfazilität und Buchungsprofilen erforderlich, Kreditbrief zu verarbeiten. 

Für diese Aufgabe wird das Demo-Unternehmen "USMF" verwendet.






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


