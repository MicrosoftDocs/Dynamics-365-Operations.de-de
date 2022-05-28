---
title: TDS-Berechnung auf Rechnungen von der Seite „Freitextrechnung“
description: In diesem Thema wird erklärt, wie Sie die Quellenbesteuerung (TDS) auf Rechnungen mithilfe der Seite „Freitextrechnung“ berechnen.
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
ms.openlocfilehash: 5a1960974dff90ef5f0cc8eab018351a9e412858
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725176"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>TDS-Berechnung auf Rechnungen von der Seite „Freitextrechnung“

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie die Quellenbesteuerung (TDS) auf Rechnungen mithilfe der Seite **Freitextrechnung** berechnen.

1. Wechseln Sie zu **Debitoren \> Rechnungen \> Alle Freitextrechnungen**.

    [![Freitextrechnungs-Seite.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Wählen Sie **Neu** aus, um eine Freitextrechnung zu erstellen, und geben Sie die erforderlichen Details ein.
3. Wählen Sie die Registerkarte **Rechnung** aus. Im Abschnitt **Quellensteuergruppe** zeigt das Feld **Art des Steuerschuldners** die Steuerschuldnerkategorie des Debitors an.
4. Überprüfen oder ändern Sie im Feld **TDS-Gruppe** die Standard-TDS-Gruppe, die für den Debitor festgelegt ist.

    > [!NOTE]
    > Wenn Sie das Feld **TDS-Gruppe** auswählen, ist das Feld **TCS-Gruppe** nicht verfügbar. TDS wird nur berechnet, wenn die Option **Quellensteuer berechnen** für den Debitor auf der Seite **Alle Debitoren** auf **Ja** gesetzt ist.

5. Auf der Registerkarte **Steuerliche Angaben** können Sie im Abschnitt **Unternehmensdaten** im Feld **Name** den Unternehmensnamen für eine alternative Adresse auswählen, die für das Unternehmen eingerichtet wurden.

    Im Abschnitt **Quellensteuer** zeigt das Feld **Steuerkontonummer (TAN)** die Steuerkontonummer (TAN) für das ausgewählte Unternehmen an.

6. Erstellen Sie in der Registerkarte **Rechnungspositionen** Rechnungspositionen und geben Sie die erforderlichen Details ein.

    Im Abschnitt **Quellensteuergruppe** wird im Feld **Steuerkontonummer (TAN)** die TAN und das Feld **TDS-Gruppe** die TDS-Gruppe angezeigt.

7. Wählen Sie **Quellensteuer** aus, um die Seite **Temporäre Quellensteuerbuchungen** zu öffnen. Der obere Teil dieser Seite enthält die folgenden Felder:

    - **Quellensteuergesamtbetrag**: Die Gesamt-TDS, die für die Buchung für die TDS-Gruppe berechnet wurde.
    - **Wert**: Der Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde. Der Gesamtprozentsatz basiert auf der Formel, die für die TDS-Steuercodes festgelegt und der TDS-Gruppe zugeordnet ist.
    - **Angepasster Quellensteuergesamtbetrag**: Der angepasste TDS-Gesamtbetrag für alle Steuercodes in der TDS-Gruppe.
    - **TDS**: Ein ausgewähltes Kontrollkästchen zeigt an, dass der Buchung eine TDS-Gruppe zugewiesen wurde.

    Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Anpassung** zeigen den berechnete TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.

8. Wählen Sie **Schwellenwert** aus, um die Seite **Schwellenwert** zu öffnen, wo Sie den Schwellenwert überprüfen, der für die TDS-Steuerkomponente definiert ist, die einem bestimmten TDS-Steuercode zugeordnet ist.
9. Wählen Sie **Formeldesigner** aus, um die Seite **Formeldesigner** zu öffnen, auf der Sie die Formel überprüfen können, die für einen bestimmten TDS-Steuercode festgelegt ist.
10. Buchen Sie die Freitextrechnung. Der für Freitextrechnungen berechnete TDS-Betrag wird auf das zu Debitorenkonto gebucht, das für den jeweiligen TDS-Steuercode in der TDS-Gruppe festgelegt ist. Die Debitorenkonto für TDS-Steuercodes sind auf der Seite **Quellensteuercodes** festgelegt.
11. Wählen Sie die **Gebuchte Quellensteuer**, um die Seite **Quellensteuerbuchungen** zu öffnen. Das Feld **Wert** zeigt den Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.

    Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Betrag** werden die TDS-Beträge angezeigt, die in den Rechnungspositionen berechnet wurden.

12. Überprüfen Sie die Angaben zur TDS-Berechnung für jeden TDS-Steuercode, der der TDS-Gruppe zugeordnet ist.
