---
title: Die Nummern wiederherstellbarer TDS-Zertifikate erfassen
description: In diesem Thema wird erklärt, wie Sie auf der Seite „Wiederherstellbare Zertifikate“ die Zertifikatsnummern und -daten für die Quellenbesteuerung (TDS-Zertifikate) erfassen, die für einen bestimmten Kreditor, Debitor oder ein bestimmtes Sachkonto eingehen.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: bc92a1321e6b2fe44bf7967c2aa1ad21dc353a03
ms.sourcegitcommit: dca3279a8b7cd5d0bcd4e4a3aa9938b337aa8849
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "7402447"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Die Nummern wiederherstellbarer TDS-Zertifikate erfassen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie auf der Seite **Wiederherstellbare Zertifikate** die Zertifikatsnummern und -daten für die Quellenbesteuerung (TDS-Zertifikate) erfassen, die für einen bestimmten Kreditor, Debitor oder ein bestimmtes Sachkonto eingehen. Verwenden Sie, um TDS-Zertifikatsnummern und -daten zu aktualisieren, die für TDS-Buchungen auf dieser Seite erfasst wurden, die Seite **Zertifikat aktualisieren** (**Hauptbuch \> Periodisch \> Quellensteuer \> Zertifikat aktualisieren**). Schließen Sie die TDS-Zertifikatnummern, nachdem Sie sie aktualisiert haben.

Gehen Sie wie folgt vor, um die TDS-Zertifikatsnummern und -daten zu erfassen.

1. Gehen Sie zu **Steuer \> Indirekte Steuer \> Quellensteuer \> Wiederherstellbare Zertifikate**.

    [![Seite „Wiederherstellbare Zertifikate“.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Wählen Sie auf der Seite **Wiederherstellbare Zertifikate** im Feld **Steuertyp** **TDS** aus.
3. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
4. Geben Sie im Feld **Zertifikatnummer** die TDS-Zertifikatnummer ein.
5. Wählen Sie im Feld **Kontotyp** den Kontotyp aus, für den das TDS-Zertifikat eingegangen ist: **Kreditor**, **Debitor** oder **Sachkonto**.
6. Wählen Sie im Feld **Konto** die Kontonummer des Kreditors, Debitors oder Sachkontos aus, je nachdem, welchen Kontotyp Sie ausgewählt haben. Das Feld **Name** Namen des Kreditor-, Debitor- oder Sachkontos an.
7. Geben Sie im Feld **Zertifikatbetrag** den Betrag des TDS-Zertifikats ein.
8. Geben Sie im Feld **Datum** die das Zertifikatsdatum für die Zertifikatnummer ein.
9. Wählen Sie **Anfragen**, um die Seite **Zertifikatsbuchung** zu öffnen, auf der Sie die TDS-Buchungen anzeigen können, für die die TDS-Zertifikatsnummer und das -datum aktualisiert wurden. Diese Informationen können auf der Seite **Zertifikat aktualisieren** aktualisiert werden (**Steuer \> Erklärungen \> Quellensteuer \> Zertifikat aktualisieren**).

    Die Seite **Zertifikat aktualisieren** zeigt die folgenden Informationen für jede offene TDS-Buchung an:

    - **Datum**: Das Buchungsdatum der TDS-Buchung.
    - **Beleg**: Die Belegnummer der TDS-Buchung.
    - **Quelle**: Das Modul, in dem die TDS-Buchung erstellt wurde.
    - **Konto**: Die Kreditor-, Debitor- oder Sachkontonummer, für die die TDS-Buchung erstellt wurde.
    - **Name**: Der Name des Kreditors, Debitors oder Sachkontos, für die die TDS-Buchung erstellt wurde.
    - **Betrag**: Der Rechnungsbetrag, auf dessen Grundlage die TDS berechnet wurde.
    - **Steuerbetrag**: Der TDS-Steuerbetrag, der für die Buchung berechnet wurde.
    - **Zertifikatsdatum**: Das Datum des TDS-Zertifikats, das für die TDS-Buchung aktualisiert wurde.
    - **Zertifikatsnummer**: Die Nummer des TDS-Zertifikats, die für die TDS-Buchung aktualisiert wurde.

10. Wählen Sie auf der Seite **Wiederherstellbare Zertifikate** das Kontrollkästchen **Geschlossen** aus, um die TDS-Zertifikatsnummer zu schließen, nachdem Sie die Aktualisierung für TDS-Buchungen auf der Seite **Zertifikat aktualisieren** beendet haben.

    Um das Kontrollkästchen **Geschlossen** für alle Datensätze auf der Seite auszuwählen, wählen Sie **Alles markieren** aus.

    > [!NOTE]
    > Die TDS-Zertifikatsnummern, für die das Kontrollkästchen **Geschlossen** aktiviert ist, stehen auf der Seite **Zertifikat aktualisieren** nicht zur Verfügung.
