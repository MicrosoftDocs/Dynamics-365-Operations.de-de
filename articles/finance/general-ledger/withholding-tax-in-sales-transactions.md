---
title: Quellensteuer bei Verkaufsbuchungen
description: In diesem Thema werden die Schritte aufgeführt, mit denen die Berechnung der Quellensteuer für ausgewählte Debitoren vermieden werden kann. Für Debitoren, die in ihren Zahlungen an Sie eine Quellensteuer angeben, können Sie die Standard-Quellensteuergruppe zuweisen.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060741"
---
# <a name="withholding-tax-in-sales-transactions"></a>Quellensteuer bei Verkaufsbuchungen

In diesem Thema werden die Schritte aufgeführt, mit denen die Berechnung der Quellensteuer für ausgewählte Debitoren vermieden werden kann. Für Debitoren, die in ihren Zahlungen an Sie eine Quellensteuer angeben, können Sie die Standard-**Quellensteuergruppe** auf der Seite **Debitoren** zuweisen. 

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