---
title: Berechnen Sie TDS-Rechnungen mithilfe des Bestellformulars und des Auftragsformulars
description: Dieser Artikel erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für verschiedene Rechnungsarten.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 72883741ee7eed6b0296736c80dd648c882ae53e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853284"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Berechnen Sie TDS-Rechnungen mithilfe des Bestellformulars und des Auftragsformulars

[!include [banner](../includes/banner.md)]

Dieser Artikel erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für verschiedene Rechnungsarten mithilfe der Seiten **Bestellung**, **Einkaufserfassung**, **Rahmenauftrag** und **Auftrag**.

1. Erstellen Sie auf der aufgeführten Seite eine Bestellung, ein Einkaufserfassung, einen Rahmenauftrag oder einen Auftrag. Geben Sie die erforderlichen Details ein.

2. Wählen Sie die Registerkarte **Setup** aus, um sich die Art des Steuerschuldners des Kreditors oder Debitors anzeigen zu lassen. Diese Informationen sind im Feld **Art des Steuerschuldners** unter der Feldgruppe **Quellensteuergruppe** aufgeführt.

3. Ändern oder lassen Sie sich im Feld **TDS-Gruppe** die Standard-TDS-Gruppe anzeigen, die für den Kreditor oder Debitor festgelegt ist.

   > [!NOTE]
   > Das Feld **TCS-Gruppe** ist nicht verfügbar, wenn Sie eine TDS-Gruppe im Feld **TDS-Gruppe** auswählen. TDS wird nur berechnet, wenn **Quellensteuer berechnen** für den Kreditor oder Debitor auf der Seite **Alle Kreditoren** oder **Alle Debitoren** aktiviert ist.  

4. Erstellen Sie Artikelpositionen in der Registerkarte **Positionen** und geben Sie die erforderlichen Details ein.

5. Wählen Sie (auf Positionsebene) die Registerkarte **Setup** um die auf Kopfzeilenebene definierte TDS-Gruppe anzusehen oder zu ändern. Die TDS-Gruppe wird im Feld **TDS-Gruppe** angezeigt, das Sie unter der Feldgruppe **Quellensteuergruppe** finden.

6. Wählen Sie die Registerkarte **Steuerliche Angaben** und dann alternative Adressen aus, die für den in diesem Feld angezeigten Unternehmensnamen eingerichtet sind. Der Unternehmensname wird im Feld **Name** angezeigt, das Sie unter der Feldgruppe **Unternehmensdaten** finden. 

   Die TAN des ausgewählten Unternehmensnamens wird im Feld **Steuerkontonummer** (**TAN**) unter der Feldgruppe **Quellensteuer**. 

7. Wählen Sie **Quellensteuer** aus, um die Seite **Temporäre Quellensteuerbuchungen** zu öffnen. Sehen Sie sich die folgenden Felder im oberen Bereich der Seite **Temporäre Quellensteuerbuchungen** an.

   - **Quellensteuergesamtbetrag**: Die Gesamt-TDS, die für die Buchung für die TDS-Gruppe berechnet wurde.

   - **Wert**: Der Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde. Der Gesamtprozentsatz basiert auf der Formel, die für die TDS-Steuercodes festgelegt ist, die der Steuergruppe zugeordnet sind.

   - **Angepasster Quellensteuergesamtbetrag**: Der angepasste TDS-Gesamtbetrag für alle Steuercodes in der TDS-Gruppe.

   - **TDS**: Ist dieses Feld ausgewählt, ist der Buchung eine TDS-Gruppe zugeordnet.

Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Anpassung** auf der Seite **Temporäte Quellensteuerbuchungen** zeigen den berechneten TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.

8. Wählen Sie **Schwellenwert**, um die Seite **Schwellenwert** zu öffnen. Sehen Sie sich auf dieser Seite den Schwellenwert an, der für die TDS-Steuerkomponente definiert ist, die einem bestimmten TDS-Steuercode zugeordnet ist.

9. Wählen Sie **Formeldesigner** aus, um die Seite **Formeldesigner** zu öffnen. Sehen Sie sich auf dieser Seite die Formel an, die für einen bestimmten TDS-Steuercode festgelegt ist. 

10. Buchen Sie die Rechnung. Der auf Einkaufsrechnungen berechnete TDS-Betrag wird auf das Kreditorenkonto gebucht, und der auf Verkaufsrechnungen berechnete TDS-Betrag wird auf das Debitorenkonto gebucht, das für den jeweiligen Steuercode in der TDS-Gruppe festgelegt ist. Die Kreditorenkonten für TDS-Steuercodes sind auf der Seite **Quellensteuercodes** festgelegt.

11. Wählen Sie die Schaltfläche **Anfrage** **> Rechnung > Gebuchte Quellensteuer**, um die Seite **Quellensteuerbuchungen** zu öffnen. Im Feld **Wert** finden Sie den Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.

Die Felder auf den Registerkarten **Übersicht**, **Allgemein** und **Betrag** auf der Seite **Quellensteuerbuchungen** enthalten die Informationen zur für die Buchung berechneten TDS. Sehen Sie sich die Angaben zur TDS-Berechnung für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.
