---
title: TDS auf Rechnungen mithilfe von Erfassungen berechnen
description: Dieses Thema erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für Erfassungen.
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
ms.openlocfilehash: 7f98caf92c49c229a11dd29d54e22106329e2401
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711351"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>TDS auf Rechnungen mithilfe von Erfassungen berechnen

[!include [banner](../includes/banner.md)]

Dieses Thema erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für Erfassungen.

Öffnen sie zunächst die Seite **Allgemeine Erfassungen** (**Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen**).

[![Allgemeine Erfassungen.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Erstellen Sie Erfassungspositionen mit den in der Tabelle aufgeführten Erfassungsformularen. Wählen Sie den Kontotyp und den Gegenkontotyp aus und geben Sie den Betrag für die Buchung ein. 

   > [!NOTE]
   > Geben Sie auf der Seite **Rechnungsgenehmigungserfassung** **Belege finden** und wählen Sie die Rechnungen aus, für die TDS berechnet werden soll. Zeigen Sie die Rechnungen an, die auf der Seite **Rechnungsregister** oder der Seite **Belege finden** erstellt wurden.  

2. Sehen Sie auf der Seite **Allgemein** der Seite **Alle Journale** im Feld **TDS-Gruppe** die Standard-TDS-Gruppe an und aktualisieren Sie sie, die für den Kreditor bzw. Debitor festgelegt ist. Der TDS-Betrag, der in Erfassungspositionen berechnet wird, basiert auf der Formel, die für die TDS-Steuercodes im Feld **TDS-Gruppe** aufgeführt ist. 

   > [!NOTE]
   > Wenn Sie eine TDS-Gruppe im Feld **TDS-Gruppe** auswählen, sind die Felder **Quellensteuergruppe** und **TCS-Gruppe** nicht mehr verfügbar. Das Feld **Quellensteuergruppe** ist nur auf der Seite **Allgemeine Erfassung** verfügbar. TDS wird nur berechnet, wenn **Quellensteuer berechnen** für den Kreditor oder Debitor auf den Seiten **Alle Kreditoren** oder **Alle Debitoren** aktiviert ist.   

3. Wählen Sie die Registerkarte **Steuerliche Angaben** und dann gegebenenfalls die alternative Adressen eines Unternehmens aus, das in diesem Feld als Unternehmen eingerichtet ist. Sie können sich den Unternehmensnamen im Feld **Name** anzeigen lassen, das Sie unter der Feldgruppe **Unternehmensdaten** finden. 

4. Lassen sie sich die Steuerschuldnerkategorie dieses Kreditors oder Debitors im Feld **Art des Steuerschuldners** anzeigen, das Sie in der Feldgruppe **Quellensteuer** finden. Lassen Sie sich im Feld **Steuerkontonummer** (**TAN**) die TAN des ausgewählten, angezeigten Unternehmensnamens, anzeigen.  

5. Wählen Sie **Quellensteuer** im Menü **Quellensteuer** aus, um die Seite **Temporäre Quellensteuerbuchungen** zu öffnen. Im oberen Bereich der Seite **Temporäre Quellensteuerbuchungen** werden die folgenden Felder angezeigt.

   - **Quellensteuergesamtbetrag**: Die Gesamt-TDS, die für die Buchung für die TDS-Gruppe berechnet wurde.

   - **Wert**: Der Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde. Der Gesamtprozentsatz basiert auf der Formel, die für die TDS-Steuercodes festgelegt ist, die der Steuergruppe zugeordnet sind.

   - **Angepasster Quellensteuergesamtbetrag**: Der angepasste TDS-Gesamtbetrag für alle Steuercodes in der TDS-Gruppe.

   - **TDS**: Ist dieses Feld ausgewählt, ist der Buchung eine TDS-Gruppe zugeordnet.

  Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Anpassung** auf der Seite **Temporäte Quellensteuerbuchungen** zeigen den berechneten TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.

6. Wählen Sie **Schwellenwert**, um die Seite **Schwellenwert** zu öffnen. Sehen Sie den Schwellenwert und Ausnahmeschwellenwert an, die für die TDS-Steuerkomponente definiert sind, die einem bestimmten TDS-Steuercode zugeordnet sind.

   Wählen Sie **Formeldesigner** aus, um das Formular **Formeldesigner** zu öffnen. Sehen Sie sich auf dieser Seite die Formel an, die für einen bestimmten TDS-Steuercode festgelegt ist. Schließen Sie den **Formeldesigner** und die Seiten **Temporäre Quellensteuerbuchungen**, um zu der Seite **Alle Journale** zurückzukehren.

8. Geben Sie die weiteren erforderlichen Informationen ein. Prüfen und buchen Sie die Erfassung. Der auf Einkaufrechnungen berechnete TDS-Betrag wird auf das Kreditorenkonto gebucht. Der auf Einkaufsrechnungen berechnete TDS-Betrag wird auf das zu Debitorenkonto gebucht, das für den jeweiligen TDS-Steuercode in der TDS-Gruppe festgelegt ist. Die Kreditorenkonten für TDS-Steuercodes sind auf der Seite **Quellensteuercodes** festgelegt.

9. Wählen Sie die **Gebuchte Quellensteuer**, um die Seite **Quellensteuerbuchungen** zu öffnen. Im Feld **Wert** wird der Gesamtprozentsatz angezeigt, der zur Berechnung der TDS für die Buchung verwendet wurde.

   Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Betrag** auf der Seite „Quellensteuerbuchungen“ zeigen den berechneten TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.
