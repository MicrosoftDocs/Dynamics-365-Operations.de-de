--- 
title: Erstellen eines Kreditorenkontos
description: Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter.
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-account"></a>Erstellen eines Kreditorenkontos

[!include [task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter. Das Verfahren wird nicht angezeigt, wie alle Felder für den Einkauf und die Finanzzwecke aufgefüllt werden. Weitere Informationen über diese Felder zu ermitteln, lesen Sie in den Feldbeschreibungen. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Kreditorenkonten sind normalerweise von einem Beschaffungsspezialisten oder von Debitoren mitarbeitern erstellt.


## <a name="create-a-vendor-account"></a>Erstellen eines Kreditorenkontos
1. Klicken Sie auf "Beschaffung" > "Kreditoren" > "Alle Kreditoren".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Kreditorenkonto" einen Wert ein.
    * Der Wert wird automatisch ausgefüllt. In diesem Fall können Sie diesen Schritt übergehen.  
    * Sie können Kreditor erstellen für eine Person oder eine Organisation. Dies wirkt sich darauf aus, welche Felder verfügbar sind. In diesem Beispiel erstellen wir ein Händlerkonto für eine Organisation.   
4. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Ihr Kreditor bereits eine erfasste Partei im System ist, die verwendet werden ablegen unten und wählen Sie diese in diesem Feld aus und das neue Kreditorenkonto erbt die Adresse und die Kontaktinformationen, die bereits erfasst wird.  
5. Geben Sie im Feld "Gruppe" einen Wert ein, oder wählen Sie einen Wert aus.
    * Die Händlergruppe wird verwendet, um Händler zu gruppieren, die mindestens einen der folgenden Parameter gemeinsam haben: Zahlungsbedingungen, Abrechnungszeitraum, Lagerbuchungssachkonten – einschließlich der Mehrwertsteuergruppe, Standardsachkonten, Produktfiltercodes oder Beschaffungsplanungskonfiguration.  
6. Geben Sie im Feld "Anzahl der Mitarbeiter" eine Zahl ein.
7. Geben Sie im Feld "Organisationsnummer" einen Wert ein.

## <a name="add-an-address"></a>Adresse hinzufügen
1. Erweitern Sie den Abschnitt Adressen.
2. Klicken Sie auf Hinzufügen.
3. Geben Sie im Feld "Zweck" einen Wert ein, oder wählen Sie einen Wert aus.
    * Sie können eine Position oder mehrere Zwecke auswählen. Diese werden verwendet, um die korrekte Adresse für einen bestimmten Zweck auszuwählen. Wenn beispielsweise der Zweck "Rechnung" lautet, wird diese Adresse verwendet, wenn Sie Rechnungen senden.  
4. Geben Sie im Feld "Name oder Beschreibung" einen Wert ein.
5. Wählen Sie im Feld Name/Region einen Wert aus oder geben Sie ihn ein«».
    * Geben Sie die Informationen zur Adresse ein. Das Land/die Region, das Sie bestimmen die Felder ausgewählt haben, die Sie mit dargestellt werden, entsprechend dem Adressformat für Land/Region.   
6. Klicken Sie auf "OK".

## <a name="add-contact-information"></a>Kontaktinformationen hinzufügen
1. Klicken Sie auf Hinzufügen.
2. Geben Sie im Feld "Beschreibung" einen Wert ein.
3. Wählen Sie im Feld "Typ" eine Option aus.
4. Geben Sie im Feld "Kontaktnummer/-adresse" einen Wert ein.
    * Sie können das Kontrollkästchen "Primär" auswählen, wenn dies der primäre Kontakt ist.  
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.
7. Schließen Sie die Seite.


