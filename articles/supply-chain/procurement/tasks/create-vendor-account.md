---
title: Erstellen eines Kreditorenkontos
description: Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter.
author: RichardLuan
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7f5723fc2aa50fc66c825eb09a01e45833b817e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022130"
---
# <a name="create-a-vendor-account"></a>Erstellen eines Kreditorenkontos

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter. Das Verfahren wird nicht angezeigt, wie alle Felder für den Einkauf und die Finanzzwecke aufgefüllt werden. Weitere Informationen über diese Felder zu ermitteln, lesen Sie in den Feldbeschreibungen. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Kreditorenkonten sind normalerweise von einem Beschaffungsspezialisten oder von Debitoren mitarbeitern erstellt.


## <a name="create-a-vendor-account"></a>Ein Kreditorenkonto erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Kreditoren > Alle Kreditoren**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Lieferantenkonto** einen Wert ein.
    - Der Wert wird automatisch ausgefüllt. In diesem Fall können Sie diesen Schritt übergehen.  
    - Sie können Kreditor erstellen für eine Person oder eine Organisation. Dies wirkt sich darauf aus, welche Felder verfügbar sind. In diesem Beispiel erstellen wir ein Lieferantenkonto für eine Organisation.   
4. Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus. Wenn Ihr Lieferant bereits eine erfasste Partei im System ist, können Sie das Dropdown-Menü verwenden und sie im Feld auswählen. Das neue Kreditorenkonto erbt die Adresse und die Kontaktinformationen, die bereits erfasst ist.
5. Geben Sie im Feld **Gruppe** einen Wert ein, oder wählen Sie einen Wert aus. Die Lieferantengruppe wird verwendet, um Lieferanten zu gruppieren, die mindestens einen der folgenden Parameter gemeinsam haben: Zahlungsbedingungen, Abrechnungszeitraum, Lagerbuchungssachkonten – einschließlich der Mehrwertsteuergruppe, Standardsachkonten, Produktfiltercodes oder Beschaffungsplanungskonfiguration.
6. Geben Sie im Feld **Anzahl der Mitarbeiter** eine Zahl ein.
7. Geben Sie im Feld **Organisationsnummer** einen Wert ein.

## <a name="add-an-address"></a>Adresse hinzufügen
1. Erweitern Sie den Abschnitt **Adressen**.
2. Klicken Sie auf **Hinzufügen**.
3. Geben Sie im Feld **Zweck** einen Wert ein, oder wählen Sie einen Wert aus. Sie können eine Position oder mehrere Zwecke auswählen. Diese werden verwendet, um die korrekte Adresse für einen bestimmten Zweck auszuwählen. Wenn beispielsweise der Zweck „Rechnung“ lautet, wird diese Adresse verwendet, wenn Sie Rechnungen senden.
4. Geben Sie in das Feld **Name oder Beschreibung** einen Wert ein.
5. Wählen Sie im Feld **Land/Region** einen Wert aus, oder geben Sie einen Wert ein. Geben Sie die Informationen zur Adresse ein. Das Land/die Region, das Sie bestimmen die Felder ausgewählt haben, die Sie mit dargestellt werden, entsprechend dem Adressformat für Land/Region. 
6. Klicken Sie auf **OK**.

## <a name="add-contact-information"></a>Kontaktinformationen hinzufügen
1. Erweitern Sie den Abschnitt **Kontaktinformationen**.
2. Klicken Sie auf **Hinzufügen**.
3. Geben Sie im Feld **Beschreibung** einen Wert ein.
4. Wählen Sie im Feld **Typ** eine Option aus.
5. Geben Sie im Feld **Kontaktnummer/-adresse** einen Wert ein. Sie können das Kontrollkästchen "Primär" auswählen, wenn dies der primäre Kontakt ist.  
6. Klicken Sie auf **Speichern**.
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]