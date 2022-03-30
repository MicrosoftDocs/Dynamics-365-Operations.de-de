---
title: Einrichten einer Zahlungsgebühr für TDS-Behördenzahlungen
description: In diesem Thema wird erläutert, wie Sie Zahlungsgebühren einrichten, die für Behördenzahlungen für die Quellenbesteuerung (TDS) erhoben werden.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8917abfea73045d57d55d7338a313f414d479b11
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407585"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Einrichten einer Zahlungsgebühr für TDS-Behördenzahlungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Zahlungsgebühren einrichten, die für Behördenzahlungen für die Quellenbesteuerung (TDS) erhoben werden.

1. Gehen Sie zu **Kreditorenkonten \> Zahlungseinstellungen \> Zahlungsgebühr**.

    [![Seite „Zahlungsgebühr“.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Wählen Sie **Neu** aus, um eine Zahlungsgebühr zu erstellen, und geben Sie die erforderlichen Details ein.
3. Wählen Sie im Feld **Gebührentyp** den Typ der Zahlungsgebühr aus:

    - **Keines**
    - **Zinsen**: Zinsen fallen für verspätete Zahlungen an den TDS-Behördenkreditor an.
    - **Andere**: Andere Gebühren, die für verspätete Zahlungen an den TDS-Behördenkreditor anfallen.

    Wenn Sie **Zinsen** oder **Andere** auswählen wird das Feld **Belastung** automatisch auf **Hauptbuch** gesetzt.

4. Wenn Sie **Zinsen** oder **Andere** im Feld **Feldtyp** auswählt haben, wählen Sie im Feld **Hauptkonto** das Sachkonto aus, auf das die Zinsen oder andere Gebühren gebucht werden sollen.
5. Geben Sie die weiteren erforderlichen Informationen ein.
6. Wählen Sie im Aktionsbereich die Option **Zahlungsgebühreinstellungen** aus, um die Seite **Zahlungsgebühreinstellungen** zu öffnen, auf der Sie Zahlungsgebühren für verschiedene Kombinationen von Banken, Zahlungsmethoden, Zahlungsspezifikationen, Währungen und Datumsintervallen einrichten können.

    [![Seite „Zahlungsgebühreinstellungen“.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Legen Sie auf der Registerkarte **Übersicht** im Feld **Gruppierungen** fest, für welche Banken Sie die Zahlungsgebühr einrichten:

    - **Tabelle**: Die Gebühr gilt für ein bestimmtes Bankkonto.
    - **Gruppe**: Die Gebühr gilt für eine bestimmte Bankgruppe.
    - **Alle**: Die Gebühr ist für alle Bankkonten gültig.

8. Wenn Sie **Tabelle** oder **Gruppe** im Feld **Gruppierungen** ausgewählt haben, wählen Sie im Feld **Bankrelation** das spezifische Bankkonto oder die Bankgruppe aus, für die Sie die Zahlungsgebühr einrichten.
9. Wählen Sie im Feld **Zahlungsmethode** die Zahlungsmethode für die Zahlung der Zahlungsgebühren aus.
10. Wählen Sie im Feld **Zahlungsspezifikation** den Zahlungsspezifikationscode aus, der auf der Seite **Zahlungsspezifikation** generiert wurde, oder geben Sie ihn ein.
    - Die Zahlungsspezifikation wird mit Methoden des elektronischen Geldverkehrs für Zahlungen verwendet.
12. Wählen Sie im Feld **Zahlungswährung** die Währung aus, welche die Gebühr aktiviert. Nur Buchungen, die die ausgewählte Währung verwenden, können die Gebühr aktivieren. Wenn Sie dieses Feld leer lassen, aktivieren alle Währungen die Gebühr.
13. Wählen Sie im Feld **Prozentsatz/Betrag** die Berechnungsmethode aus. Als Optionen stehen **Betrag**, **Prozent** und **Intervall** zur Verfügung.
14. Geben Sie im Feld **Gebührenbetrag** den Gebührenbetrag entweder als Prozentsatz der Zahlung oder als Betrag pro Zahlung an.
15. Wählen Sie im Feld **Gebührenwährung** den Währungscode für die Gebühr aus.
16. Wählen Sie die Registerkarte **Allgemein** aus, um die Details des ausgewählten Bankkontos anzuzeigen oder zu ändern.

    [![Registerkarte „Allgemeines“.](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Geben Sie im Feld **Minimum** den Mindestbuchungsbetrag an, der die Gebühr aktiviert.
17. Geben Sie im Feld **Maximum** den Höchstbuchungsbetrag an, der die Gebühr aktiviert.
18. Legen Sie in den Feldern **Startdatum** und **Enddatum** einen Datumsbereich für die Berechnung der Gebühren fest.
19. Geben Sie im Feld **Mindestgebühr** den Gebührenbetrag entweder als Prozentsatz der Zahlung oder als Betrag pro Zahlung an.
20. Wählen Sie im Feld **Mehrwertsteuergruppe** die Mehrwertsteuergruppe aus, anhand der die Mehrwertsteuer für den Gebührenbetrag berechnet werden soll.
21. Wählen Sie im Feld **Artikel-Mehrwertsteuergruppe** die Artikel-Mehrwertsteuergruppe aus, anhand der die Artikel-Mehrwertsteuer für den Gebührenbetrag berechnet werden soll.
22. Wählen Sie die Registerkarte **Intervall** aus. 

    [![Registerkarte „Intervall“.](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Geben Sie im Feld **Tage** die Anzahl der Tage zwischen dem Buchungsdatum (Skontodatum) der Zahlung und dem Fälligkeitsdatum des Solawechsels ein.
24. Wählen Sie im Feld **Prozentsatz/Betrag** aus, ob es sich bei der Spezifikation um einen Prozentsatz oder einen festen Betrag handelt.
25. Geben Sie im Feld **Gebührenbetrag** den Gebührenbetrag entweder als Prozentsatz der Zahlung oder als Betrag pro Zahlung an.
26. Schließen Sie die Seite **Zahlungsgebühreinstellungen**.
27. Schließen Sie die Seite **Zahlungsgebühr**.
