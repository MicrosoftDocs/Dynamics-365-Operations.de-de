---
title: Quellensteuer bei Verkaufsbuchungen
description: In diesem Artikel werden die Schritte aufgeführt, mit denen die Berechnung der Quellensteuer für ausgewählte Debitoren vermieden werden kann. Für Debitoren, die in ihren Zahlungen an Sie eine Quellensteuer angeben, können Sie die Standard-Quellensteuergruppe zuweisen.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 75a7fc62c1d493007f3aa88a723465828c557df7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910083"
---
# <a name="withholding-tax-in-sales-transactions"></a>Quellensteuer bei Verkaufsbuchungen

In diesem Artikel werden die Schritte aufgeführt, mit denen die Berechnung der Quellensteuer für ausgewählte Debitoren vermieden werden kann. Für Debitoren, die in ihren Zahlungen an Sie eine Quellensteuer angeben, können Sie die Standard-**Quellensteuergruppe** auf der Seite **Debitoren** zuweisen. 

1. Rufen Sie **Navigationsbereich > Module > Debitorenkonten > Debitoren > Alle Debitoren** auf.

2. Klicken Sie auf das entsprechende Debitorenkonto und dann auf **Bearbeiten**.

3. Setzen Sie auf der Registerkarte **Rechnung und Lieferung** das Feld **Quellensteuer berechnen** auf **Ja**.

   > [!NOTE] 
   > Die Quellensteuer wird nicht berechnet, wenn für diesen Debitoren in den Masterdaten nicht **Quellensteuer berechnen** aktiviert ist.

4. Wählen Sie eine Quellensteuergruppe unter **Quellensteuergruppe** aus.

5. Klicken Sie auf **Speichern**.

Für Artikel/Dienstleistungen, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Artikel-Quellensteuergruppe** in **Freigegebene Produkte** zuweisen.

1. Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.

2. Klicken Sie auf die entsprechende Artikelnummer und dann auf **Bearbeiten**.

3. Klicken Sie auf der Registerkarte **Verkauf** auf **Quellensteuer berechnen**.

   > [!NOTE] 
   > Die Quellensteuer wird nicht berechnet, wenn **Quellensteuer berechnen** für diesen Artikel auf der Registerkarte **Verkauf** der Seite **Freigegebenes Produkt** nicht auf **Ja** gesetzt ist.

4. Wählen Sie eine Artikel-Quellensteuergruppe in der Liste **Artikel-Quellensteuergruppe** aus.

5. Klicken Sie auf **Speichern**.

Quellensteuergruppen und Artikel-Quellensteuergruppen können über die Seite **Auftrag** zugewiesen werden. 

Die Standard-Quellensteuergruppe und die Artikel-Quellensteuergruppe werden als Standardeinträge in Auftragspositionen verwendet, wenn Sie einen neuen Auftrag erstellen.

Die Quellensteuer über die **Debitorzahlungserfassung** berechnet und gebucht. Sie können den entsprechenden Quellensteuercode sowie den tatsächlichen Quellensteuerbetrag auf der Registerkarte **Quellensteuer** der Seite **Buchungen ausgleichen** manuell anpassen.

Der berechnete Quellensteuerbetrag wird von der Debitorenzahlung abgezogen und auf das **Quellensteuer-Gegenkonto** über einen dazugehörigen Beleg gebucht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
