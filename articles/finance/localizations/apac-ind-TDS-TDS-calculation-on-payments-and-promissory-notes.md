---
title: TDS-Berechnung zu Zahlungen und Solawechseln
description: Dieses Thema enthält Referenzinformationen zu den verschiedenen Zahlungsbuchungen, für die die Quellenbesteuerung (TDS) berechnet wird.
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
ms.openlocfilehash: 7f38a8c4b0416abb10bfdaf95c3379e964e9a41e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726461"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>TDS-Berechnung zu Zahlungen und Solawechseln

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Referenzinformationen zu den verschiedenen Zahlungsbuchungen, für die die Quellenbesteuerung (TDS) berechnet wird.

| Seriennummer | Transaktionstyp | Transaktionsbetrag | Seitenname und -pfad | Kontenart und Gegenkontenart |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Anzahlung/Zahlung gegen Rechnung (TDS-Zahlung) | Soll oder Haben | <ul><li>Allgemeine Erfassung (**Hauptbuch \> Journaleinträge \> Allgemeine Erfassungen**)</li><li>Rechnungserfassung (**Kreditorenkonten \> Rechnungen \> Rechnungserfassung**)</li><li>Zahlungserfassung (**Kreditorenkonten \> Zahlungen \> Kreditorenzahlungserfassung**)</li></ul> | Kreditor (S), Bank (H) |
| 2             | Anzahlung/Zahlung gegen Rechnung (Kauf durch Debitor – TDS-Zahlung) | Soll oder Haben | <ul><li>Allgemeine Erfassung (**Hauptbuch \> Journaleinträge \> Allgemeine Erfassungen**)</li><li>Rechnungserfassung (**Kreditorenkonten \> Rechnungen \> Rechnungserfassung**)</li><li>Zahlungserfassung (**Kreditorenkonten \> Zahlungen \> Kreditorenzahlungserfassung**)</li></ul> | Debitor (S), Bank (H) |
| 3             | Solawechsel | Belastung | Erfassung zum Ziehen von Solawechseln (**Kreditorenkonten \> Zahlungen \> Solawechsel \> Erfassung zum Ziehen von Solawechseln**) | Kreditor (S), Sachkonto (H) |
| 4             | Sonstige Einnahmen (TDS-Eingang) | Soll oder Haben | Allgemeine Erfassung (**Hauptbuch \> Journaleinträge \> Allgemeine Erfassungen**) | Bank (S), Sachkonto (H) |
| 5             | Sonstige Aufwendungen (TDS-Zahlung) | Soll oder Haben | Allgemeine Erfassung (**Hauptbuch \> Journaleinträge \> Allgemeine Erfassungen**) | Bank (S), Sachkonto (H) |

Gehen Sie wie folgt vor, um die TDS für Zahlungen und Solawechsel zu berechnen.

1. Erstellen Sie auf den Erfassungsseiten Erfassungspositionen an. Wählen Sie den Typ des Kontos und des Gegenkontos aus.
2. Wählen Sie **Funktionen \> Ausgleich**, um die Seite **Bearbeiten offener Posten** zu öffnen. Wählen Sie dann eine bestimmte Rechnung aus, die ausgeglichen werden muss. Wenn TDS bereits auf Rechnungsebene berechnet wurde, zeigt das Feld **Grundlage** den Grundbetrag an, für den die TDS berechnet wurde. Das Feld **TDS-Betrag** zeigt den TDS-Betrag an, der für die Buchung berechnet wurde. Das Feld **Betrag** zeigt den Nettozahlungsbetrag an (also den Zahlungsbetrag nach Abzug der TDS).

    > [!NOTE]
    > Für eine Zahlung, die gegen eine Rechnung geleistet wurde, gelten folgende Bedingungen:
    >
    > - Wenn der Zahlungsbetrag und der Rechnungsbetrag gleich sind, wird keine TDS berechnet, wenn sie bereits auf Rechnungsebene berechnet wurde.
    > - Wenn der Rechnungsbetrag nach Abzug des TDS-Betrags höher ist als der Zahlungsbetrag, wird keine TDS berechnet.
    > - Wenn der Rechnungsbetrag nach Abzug des TDS-Betrags niedriger ist als der Zahlungsbetrag, wird die TDS auf Grundlage des Betrags berechnet, der den Rechnungsbetrag übersteigt.

3. Überprüfen und ändern Sie auf der Seite **Alle Journale** unter der Registerkarte **Übersicht** im Feld **TDS-Gruppen** die Standard-TDS-Gruppe, die für den Kreditor bzw. Debitor festgelegt ist. TDS, die in Erfassungspositionen berechnet wird, basiert auf der Formel, die für die TDS-Steuercodes in der TDS-Gruppe festgelegt ist.

    > [!NOTE]
    > TDS wird nur berechnet, wenn die Option **Quellensteuer berechnen** für den Kreditor auf der Seite **Kreditor** auf **Ja** gesetzt ist.

4. Auf der Registerkarte **Steuerliche Angaben** können Sie im Abschnitt **Unternehmensdaten** im Feld **Name** einen Unternehmensnamen für alternative Adressen auswählen, die für das Unternehmen eingerichtet wurden.

    Im Abschnitt **Quellensteuer** zeigt das Feld **Art des Steuerschuldners** die Steuerschuldnerkategorie des Kreditors oder Debitors an. Das Feld **Steuerkontonummer (TAN)** zeigt die Steuerkontonummer (TAN) des ausgewählten Unternehmens an.

5. Wählen Sie die **Schaltfläche Quellensteuer \> Quellensteuer**, um die Seite **Temporäre Quellensteuerbuchungen** zu öffnen. Der obere Teil dieser Seite enthält die folgenden Felder:

    - **Quellensteuergesamtbetrag**: Die Gesamt-TDS, die für die Buchung für die TDS-Gruppe berechnet wurde.
    - **Wert**: Der Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde. Der Gesamtprozentsatz basiert auf der Formel, die für die TDS-Steuercodes festgelegt und der TDS-Gruppe zugeordnet ist.
    - **Angepasster Quellensteuergesamtbetrag**: Der angepasste TDS-Gesamtbetrag für alle Steuercodes in der TDS-Gruppe.
    - **TDS**: Ein ausgewähltes Kontrollkästchen zeigt an, dass der Buchung eine TDS-Gruppe zugewiesen wurde.

    Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Anpassung** zeigen den berechnete TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.

6. Wählen Sie **Schwellenwert** aus, um die Seite **Schwellenwert** zu öffnen, wo Sie den Schwellenwert überprüfen, der für die TDS-Steuerkomponente definiert ist, die einem bestimmten TDS-Steuercode zugeordnet ist.
7. Wählen Sie **Formeldesigner** aus, um die Seite **Formeldesigner** zu öffnen, auf der Sie die Formel überprüfen können, die für einen bestimmten TDS-Steuercode festgelegt ist.
8. Schließen Sie den **Formeldesigner** und die Seiten **Temporäre Quellensteuerbuchungen**, um zu der Seite **Alle Journale** zurückzukehren.
9. Prüfen und buchen Sie die Erfassung. Der berechnete TDS-Betrag wird auf das zu Kreditorenkonto gebucht, das für den jeweiligen TDS-Steuercode in der TDS-Gruppe festgelegt ist. Die Debitorenkonto für TDS-Steuercodes sind auf der Seite **Quellensteuercodes** festgelegt.
10. Wählen Sie die **Gebuchte Quellensteuer**, um die Seite **Quellensteuerbuchungen** zu öffnen. Das Feld **Wert** zeigt den Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.

    Die Felder der Registerkarten **Übersicht**, **Allgemein** und **Betrag** zeigen die TDS-Beträge an, die für die der Buchung zugeordnete TDS-Gruppe berechnet wurden.

11. Überprüfen Sie die Angaben zur TDS-Berechnung für jeden TDS-Steuercode, der der TDS-Gruppe zugeordnet ist.

## <a name="generate-payments"></a>Zahlungen generieren

Gehen Sie wie folgt vor, um Zahlungen zu generieren.

1. Führen Sie einen dieser Schritte aus:

    - Gehen Sie zu **Kreditorenkonten \> Zahlungen \> Kreditorenzahlungserfassung**.
    - Gehen Sie zu **Debitorenkonten \> Zahlungen \> Kundenzahlungserfassung**.
    - Gehen Sie zu **Kreditorenkonten \> Zahlungen \> Solawechsel \> Erfassung zum Ziehen von Solawechseln**.
    - Gehen Sie zu **Debitorenkonten \> Zahlungen \> Wechsel \> Erfassung zum Ziehen von Wechseln**.
    - Gehen Sie zu **Debitorenkonten \> Zahlungen \> Wechsel \> Erfassung zum erneuten Ziehen von Wechseln**.

2. Wählen Sie **Positionen** aus.
3. Wählen Sie **Funktionen \> Zahlungen generieren** aus.
