---
title: Ein Kreditorenbankkonto erstellen
description: Diese Prozedur zeigt Ihnen, wie Sie ein Bankkonto für einen Kreditor erstellen.
author: RichardLuan
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3523dec15363bd42219d40ed8048681c56829ac
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019252"
---
# <a name="create-a-vendor-bank-account"></a>Ein Kreditorenbankkonto erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie ein Bankkonto für einen Kreditor erstellen. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.

1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Kreditoren > Alle Kreditoren**.
2. Wählen Sie den Kreditor aus, für den Sie ein Bankkonto erstellen möchten, und klicken Sie dann auf den Link im Feld **Kreditorkontenkennung**.
3. Klicken Sie im **Aktivitätsbereich** auf **Kreditor**.
4. Klicken Sie auf **Bankkonten**.
5. Klicken Sie im **Aktivitätsbereich** auf **Neu**.
6. Geben Sie im Feld **Bankkonto** einen Wert ein. Diese Kennung wird verwendet, um das Bankkonto im Kreditorendatensatz zu identifizieren.  
7. Geben Sie im Feld **Name** einen Wert ein.
8. Geben Sie im Feld **Bankgruppen** einen Wert ein, oder wählen Sie einen Wert aus.
9. Wählen Sie im Feld **Bankleitzahltyp** eine Option aus. Das ist der Bankleitzahltyp, der für die internationalen Zahlungen verwendet wird.  
10. Geben Sie im Feld **Bankkontonummer** einen Wert ein.
11. Geben Sie im Feld **SWIFT-Code** einen Wert ein.
12. Geben Sie im Feld **IBAN** einen Wert ein.
    - Die IBAN-Nummer muss im korrekten Format sein. Sie könnten zum Beispiel "DE89370400440532013000" verwenden.  
    - Der Status des Bankkontos ist "Aktiv", wenn das "Aktives Datum" erreicht worden ist, und das "Ablaufdatum" noch nicht überschritten wurde. Es ist auch aktiv, wenn die Felder „Aktives Datum“ und „Ablaufdatum“ leer sind. Wenn die Datumsangaben sowohl im Feld "Aktives Datum" als auch im Feld "Ablaufdatum" in der Zukunft liegen, sind elektronische Zahlungen nicht verfügbar. Andere Zahlungstypen sind verfügbar, und das Bankkonto ist aktiv.  
13. Erweitern Sie den Abschnitt **Einrichtung**.
14. Geben Sie im Feld **Textcode** einen Wert ein. Dieses Feld gibt einen Code an, der auf dem Bankauszug des Empfängers angezeigt wird.  
15. Geben Sie im Feld **Nachricht an die Bank** einen Wert ein.
16. Geben Sie im Feld **Wechselkursreferenz** einen Wert ein. Das ist die Referenznummer für einen beliebigen Terminwechselkurs oder festen Wechselkurs.
17. Geben Sie im Feld **Währung** einen Wert ein, oder wählen Sie einen Wert aus. Wenn Testtransaktionen ausgestellt werden, stellt dieser Abschnitt einen Überblick über ihren Status (ausstehend oder genehmigt) bereit.  
18. Erweitern Sie den Abschnitt **Adresse**.
19. Erweitern Sie den Abschnitt **Testtransaktionen**.
20. Erweitern Sie den Abschnitt **Kontaktinformationen**.
21. Geben Sie im Feld **Telefon** einen Wert ein.
22. Schließen Sie die Seite.
23. Klicken Sie auf **Bearbeiten**.
24. Erweitern Sie den Abschnitt **Zahlung**.
25. Wählen Sie im Feld **Bankkonto** das Konto aus, dass Sie gerade erstellt haben.
26. Klicken Sie auf **Speichern**. Die Adresse wird möglicherweise von der Bankgruppe geerbt, wenn eine angegeben ist, oder Sie können sie hier hinzufügen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]