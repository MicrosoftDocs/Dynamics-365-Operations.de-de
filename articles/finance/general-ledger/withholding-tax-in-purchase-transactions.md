---
title: Quellensteuer bei Kaufbuchungen
description: Bei Kreditoren, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Quellensteuergruppe** auf der Seite **Alle Kreditoren** zuweisen.
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
ms.openlocfilehash: 06997e2d6b47d867e014a7d493d91015c78a5e04
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060739"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Quellensteuer bei Kaufbuchungen

Bei Kreditoren, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Quellensteuergruppe** auf der Seite **Alle Kreditoren** zuweisen.

1. Rufen Sie **Navigationsbereich > Module > Kreditorenkonten > Kreditoren > Alle Kreditoren** auf.

2. Klicken Sie auf das entsprechende Kreditorenkonto und dann auf **Bearbeiten**.

3. Setzen Sie auf der Registerkarte **Rechnung und Lieferung** das Feld **Quellensteuer berechnen** auf **Ja**.

   > [!NOTE] 
   > Die Quellensteuer wird nicht berechnet, wenn für diesen Kreditor in den Daten nicht **Quellensteuer berechnen** aktiviert ist.

4. Wählen Sie eine Quellensteuergruppe unter **Quellensteuergruppe** aus.

5. Klicken Sie auf **Speichern**.

Für Artikel/Dienstleistungen, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Artikel-Quellensteuergruppe** in **Freigegebene Produkte** zuweisen.

1. Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.

2. Klicken Sie auf die entsprechende Artikelnummer und dann auf **Bearbeiten**.

3. Klicken Sie auf der Registerkarte **Kauf** auf **Quellensteuer berechnen**.

   > [!NOTE] 
   > Die Quellensteuer wird nicht berechnet, wenn **Quellensteuer berechnen** für diesen Artikel auf der Registerkarte **Kauf** der Seite **Freigegebenes Produkt** nicht auf **Ja** gesetzt ist.

4. Wählen Sie eine Artikel-Quellensteuergruppe in der Liste **Artikel-Quellensteuergruppe** aus.

5. Klicken Sie auf **Speichern**.

Quellensteuergruppen und Artikel-Quellensteuergruppen können auf folgenden Seiten zugewiesen werden: 

- **Bestellung**
- **Kreditorenrechnung**
- **Rechnungserfassung**

Die Standard-Quellensteuergruppe und die Artikel-Quellensteuergruppe werden beim Erstellten von **Bestellungen** und/oder **Ausstehende Kreditorenrechnungen** in die Positionen übernommen. Sie können für die **Kreditorenrechnungserfassung** die Option **Quellensteuer berechnen** aktivieren und auf der Registerkarte **Allgemein** der Erfassung **Artikel-Quellensteuergruppe** auswählen.

Der vorübergehende Quellensteuerbetrag wird im Feld **Angepasste Quellensteuer** der Registerkarte **Summen** auf der Seite **Bestellung** angezeigt.

![Die Quellensteuer ist in der Bestellung enthalten](media/withholding-tax-adjusted.png)

Die Quellensteuer wird in der **Kreditorenzahlungserfassung** berechnet. Sie können die entsprechenden Quellensteuercodes sowie die tatsächlichen Quellensteuerbeträge auf der Registerkarte **Quellensteuer** der Seite **Buchungen ausgleichen** manuell anpassen.

![Die Quellensteuer kann auf der Seite „Buchungen ausgleichen“ manuell angepasst werden](media/withholding-tax-vendor-payment-tab.png)

Der abgeleitete Quellensteuerbetrag wird von der Kreditorenzahlung abgezogen und auf das **Quellensteuerkonto** über einen dazugehörigen Beleg gebucht.

![Das Quellensteuerkonto zeigt einen dazugehörigen Beleg an](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]