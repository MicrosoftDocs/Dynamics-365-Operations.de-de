---
title: TDS-Parameter festlegen
description: In diesem Thema wird erklärt, wie Sie Parameter festlegen, um die in bestimmten Buchungen die Funktionalität für die Quellenbesteuerung (TDS) zu aktivieren. Dies ist ein notwendiger Schritt, um die Quellenbesteuerungsfunktion (TDS-Funktion) zu verwenden.
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
ms.openlocfilehash: e0c0c830391b790f3bc066e319a855b44f7e243f4e086144bbafaa6bb2fa1df3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781706"
---
# <a name="set-the-tds-parameters"></a>TDS-Parameter festlegen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie Parameter festlegen, um die in bestimmten Buchungen die Funktionalität für die Quellenbesteuerung (TDS) zu aktivieren. Dies ist ein notwendiger Schritt, um die Quellenbesteuerungsfunktion (TDS-Funktion) zu verwenden.

1. Wechseln Sie zu **Hauptbuch \> Sachkonto-Einstellungen \> Hauptbuchparameter**.
2. Stellen Sie auf der Registerkarte **Direkte Steuern** im Abschnitt **Quellenbesteuerung** die Option **TDS aktivieren** auf **Ja**, um die TDS-Funktionalität und die dafür verwendeten Seiten und Felder zu aktivieren.
3. Stellen Sie die Option **Rechnung** auf **Ja**, um die Felder zu aktivieren, mit denen TDS auf Rechnungsebene berechnet und abgezogen werden.
4. Stellen Sie die Option **Zahlung** auf **Ja**, um die Felder zu aktivieren, mit denen TDS auf Zahlungsebene berechnet und abgezogen werden.

    [![Registerkarte „Direkte Steuern“.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Suchen Sie in der Registerkarte **Nummerkreise** die Zeile, bei der das Feld **Referenz** auf **Quellensteuerzahlung** gesetzt ist. Wählen Sie dann im Feld **Nummernkreiscode** der Zeile den Nummernkreiscode aus. Der Nummernkreiscode wird verwendet, um Belegnummern für den periodischen TDS-Ausgleichsprozess zu generieren.

    > [!NOTE]
    > Um den periodischen TDS-Ausgleichsprozess auszuführen, gehen Sie zu **Steuern \> Erklärung \> Quellensteuer \> Quellensteuerzahlung**.

    [![Registerkarte „Nummernkreise“.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Schließen Sie die Seite.
