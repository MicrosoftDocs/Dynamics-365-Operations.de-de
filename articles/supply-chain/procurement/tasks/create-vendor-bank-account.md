--- 
title: Ein Kreditorenbankkonto erstellen
description: "Diese Prozedur zeigt Ihnen, wie Sie ein Bankkonto für einen Kreditor erstellen."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: adb759c59d7275e7323dbb760de56acdef2e3cff
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-bank-account"></a>Ein Kreditorenbankkonto erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie ein Bankkonto für einen Kreditor erstellen. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.

1. Klicken Sie auf "Beschaffung" > "Kreditoren" > "Alle Kreditoren".
2. Wählen Sie den Kreditor aus, für den Sie ein Bankkonto erstellen möchten und klicken Sie dann auf den Link auf der "Kreditorkontenkennung".
3. Klicken Sie im Aktivitätsbereich auf "Händler".
4. Klicken Sie auf Bankkonten.
5. Klicken Sie auf "Neu".
6. Geben Sie im Feld "Bankkonto" einen Wert ein.
    * Diese Kennung wird verwendet, um das Bankkonto im Kreditorendatensatz zu identifizieren.  
7. Geben Sie im Feld "Name" einen Wert ein.
8. Geben Sie im Feld 'Bankgruppen' einen Wert ein, oder wählen Sie einen Wert aus.
9. Wählen Sie im Feld "Bankleitzahltyp" eine Option aus.
    * Das ist der Bankleitzahltyp, der für internationale Zahlungen verwendet wird.  
10. Geben Sie im Feld "Bankkontonummer" einen Wert ein.
11. Geben Sie im Feld "SWIFT-Code" einen Wert ein.
12. Geben Sie im Feld "IBAN" einen Wert ein.
    * Die IBAN-Nummer muss im korrekten Format sein. Sie könnten zum Beispiel "DE89370400440532013000" verwenden.  
    * Der Status des Bankkontos ist "Aktiv", wenn das "Aktives Datum" erreicht worden ist, und das "Ablaufdatum" noch nicht überschritten wurde. Es ist auch aktiv, wenn die Felder "Aktives Datum" und "Ablaufdatum" leer sind. Wenn die Datumsangaben sowohl im Feld "Aktives Datum" als auch im Feld "Ablaufdatum" in der Zukunft liegen, sind elektronische Zahlungen nicht verfügbar. Andere Zahlungstypen sind verfügbar, und das Bankkonto ist aktiv.  
13. Erweitern Sie den Abschnitt 'Einstellungen'.
14. Geben Sie im Feld "Textcode" einen Wert ein.
    * Dieses Feld gibt einen Code an, der auf dem Bankauszug des Empfängers angezeigt wird.  
15. Geben Sie im Feld "Nachricht an die Bank" einen Wert ein.
16. Geben Sie im Feld "Wechselkursreferenz" einen Wert ein.
    * Das ist die Referenznummer für einen beliebigen Terminwechselkurs oder festen Wechselkurs.  
17. Geben Sie im Feld "Währung" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Testtransaktionen ausgestellt werden, stellt dieser Abschnitt einen Überblick über ihren Status (ausstehend oder genehmigt) bereit.  
18. Erweitern Sie den Abschnitt "Adresse".
19. Erweitern Sie den Abschnitt "Testtransaktionen".
20. Erweitern Sie den Abschnitt "Kontaktinformationen".
21. Geben Sie im Feld "Telefon" einen Wert ein.
22. Schließen Sie die Seite.
23. Klicken Sie auf "Bearbeiten".
24. Erweitern Sie den Abschnitt "Zahlung".
25. Wählen Sie im Feld "Bankkonto" das Konto aus, dass Sie soeben erstellt haben.
26. Klicken Sie auf "Speichern".
    * Die Adresse wird möglicherweise von der Bankgruppe geerbt, wenn eine angegeben ist, oder Sie können sie hier hinzufügen.  


