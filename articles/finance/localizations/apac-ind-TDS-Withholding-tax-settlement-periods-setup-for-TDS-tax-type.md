---
title: Quellensteuerausgleichsperioden für den Steuertyp „TDS“
description: In diesem Thema wird erklärt, wie Sie Ausgleichsperioden für die Quellenbesteuerung (TDS) einrichten.
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023255"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a>Quellensteuerausgleichsperioden für den Steuertyp „TDS“

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie Ausgleichsperioden für die Quellenbesteuerung (TDS) einrichten.

1. Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuerausgleichsperioden**.

    [![Seite „Quellensteuerausgleichsperioden“](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)

2. Wählen Sie im Feld **Steuertyp** **TDS** aus, um Quellensteuerausgleichsperioden für den Steuertyp „TDS“ einzurichten.
3. Wählen Sie **Neu**, um eine Position zu erstellen.
4. Geben Sie im Feld **Ausgleichsperiode** einen Namen für die TDS-Ausgleichsperiode ein.
5. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
6. Wählen Sie im Feld **Quellensteuerbehörde** die TDS-Behörde aus, für die Sie die TDS-Ausgleichsperiode festlegen.
7. Im Inforegister **Allgemein** wählen Sie im Feld **Periodenintervall** die Art des Periodenintervalls für die TDS-Ausgleichsperiode aus.
8. Geben Sie im Feld **Anzahl der Einheiten** Anzahl der Einheiten für den Periodenintervalltyp an.
9. Wählen Sie im Inforegister **Perioden** im Feld **Startdatum** das Startdatum für die TDS-Ausgleichsperiode aus. Wählen Sie im Feld **Enddatum** das Enddatum aus.
10. Um für eine vorhandene Periode basierend auf dem Periodenintervall und den Periodeneinheiten eine nachfolgende TDS-Ausgleichsperiode zu erstellen, wählen Sie **Neue Periode**.
11. Um die Details des periodischen TDS-Ausgleichs anzuzeigen, der für eine bestimmte Ausgleichsperiode ausgeführt wird, wählen Sie **Quellensteuerzahlungen**, um die Seite **Quellensteuerzahlung** zu öffnen.

    > [!NOTE]
    > Um den periodischen TDS-Ausgleichsprozess auszuführen, gehen Sie zu **Hauptbuch \> Periodisch \> Quellensteuer \> Quellensteuerzahlung**.

    [![Seite „Quellensteuerzahlung“](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)

12. Schließen Sie die Seite.
