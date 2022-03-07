---
title: Zertifikatsnummern und -daten für TDS-Buchungen aktualisieren
description: In diesem Thema wird erklärt, wie Sie auf die Nummern und Daten wiederherstellbarer Zertifikat aktualisieren, die für die Quellensteuerung (TDS) für Kreditor-, Debitor- und Sachkonten erstellt wurden.
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023264"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Zertifikatsnummern und -daten für TDS-Buchungen aktualisieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie auf die Nummern und Daten wiederherstellbarer Zertifikat aktualisieren, die für die Quellensteuerung (TDS) für Kreditor-, Debitor- und Sachkonten erstellt wurden. Sie können sich die Zertifikate für TDS-Buchungen auf der Seite **Wiederherstellbare Zertifikate** anzeigen lassen. Sie können die Zertifikate mithilfe der Seite **Zertifikate aktualisieren** aktualisieren.

Gehen Sie wie folgt vor, um die Zertifikatsnummern und -daten für TDS-Buchungen zu aktualisieren.

1. Gehen Sie zu **Steuer \> Erklärungen \> Quellensteuer \> Zertifikat aktualisieren**.

    [![Seite „Zertifikat aktualisieren“](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Wählen Sie auf der Seite **Zertifikat aktualisieren** im Abschnitt **Auswählen** im Feld **Steuertyp** **TDS** aus.
3. Wählen Sie im Feld **Zertifikatsnummer** die TDS-Zertifikatsnummer des Debitors oder Kreditors aus.

    > [!NOTE]
    > Das Feld **Zertifikatsnummer** enthält nur TDS-Zertifikatsnummern, bei denen **Geschlossen** auf der Seite **Wiederherstellbare Zertifikate** nicht aktiviert ist.

    Im Feld **Zertifikatsdatum** ist das Zertifikatsdatum angegeben. Im Feld **Kontotyp** ist der Kontotyp angegeben, für den die TDS-Zertifikatsnummer eingegangen ist. Das Feld **Name** zeigt den Namen des Kontos an.

5. Wählen Sie in den Feldern **Startdatum** und **Enddatum** das Start- und Enddatum des Zeitraums aus, für den TDS-Buchungen angezeigt werden sollen.
6. Wählen Sie **Daten anzeigen** aus, um die TDS-Buchungen anzuzeigen, die im ausgewählten Zeitraum gebucht wurden.

    Das Raster im oberen Bereich der Registerkarte **Übersicht** enthält zu jeder TDS-Buchung, die im ausgewählten Zeitraum für den Kreditor oder Debitor gebucht wurde, die folgende Informationen:

    - **Beleg**: Die Belegnummer der TDS-Buchung.
    - **Datum**: Das Datum der TDS-Buchung.
    - **Betrag**: Der Rechnungsbetrag, auf dessen Grundlage die TDS berechnet wurde.
    - **Steuerbetrag**: Der TDS-Steuerbetrag, der für die Buchung berechnet wurde.

7. Um bestimmte TDS-Buchungen vom oberen in das untere Raster zu verschieben, wählen Sie die Buchungen und dann **Einschließen** aus. Alternativ wählen Sie **Alle einschließen** aus, um alle TDS-Buchungen vom oberen in das untere Raster zu verschieben.

    Um bestimmte oder alle TDS-Buchungen vom unteren in das obere Raster zu verschieben, nutzen Sie die Schaltfläche **Ausschließen** oder **Alle ausschließen**.

8. Wählen Sie **Aktualisieren**, um die Felder **Zertifikatsnummer** und **Zertifikatsdatum** für TDS-Buchungen im unteren Raster zu aktualisieren.
10. Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Wiederherstellbares Zertifikat** und wählen Sie **Anfrage** aus, um die aktualisierten Buchungspositionen mit den neuen Zertifikatsnummern auf der Seite **Zertifikatsbuchungen** anzuzeigen.

    [![Seite „Zertifikatsbuchungen“](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
