---
title: TDS-Parameter festlegen
description: In diesem Artikel wird erklärt, wie Sie Parameter festlegen, um die in bestimmten Buchungen die Funktionalität für die Quellenbesteuerung (TDS) zu aktivieren. Dies ist ein notwendiger Schritt, um die Quellenbesteuerungsfunktion (TDS-Funktion) zu verwenden.
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
ms.openlocfilehash: 3390cad6979858fbff73769d0d25132ba18a2157
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865612"
---
# <a name="set-the-tds-parameters"></a>TDS-Parameter festlegen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erklärt, wie Sie Parameter festlegen, um die in bestimmten Buchungen die Funktionalität für die Quellenbesteuerung (TDS) zu aktivieren. Dies ist ein notwendiger Schritt, um die Quellenbesteuerungsfunktion (TDS-Funktion) zu verwenden.

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
