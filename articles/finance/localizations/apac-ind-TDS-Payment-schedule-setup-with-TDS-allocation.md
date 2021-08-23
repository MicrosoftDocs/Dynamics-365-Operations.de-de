---
title: Zahlungsplänen mit TDS-Zuteilung einrichten
description: In diesem Thema wird erklärt, wie Zahlungspläne mit Zuteilung für die Quellenbesteuerung (TDS) einrichten.
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
ms.openlocfilehash: 55bfdfb97c418ec9fd856a151da46c1bcf94aa2cb4df85185b47f722d8526ef2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769721"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Zahlungsplänen mit TDS-Zuteilung einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Zahlungspläne mit Zuteilung für die Quellenbesteuerung (TDS) einrichten.

1. Gehen Sie zu **Kreditorenkonten \> Zahlungseinstellungen \> Zahlungspläne**.

    [![Seite „Zahlungspläne“.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Wählen Sie im Aktionsbereich die Option **Neu** aus, um einen Zahlungsplan zu erstellen und die erforderlichen Details einzugeben.
3. Wählen Sie im Feld **Zuteilung** die Methode aus, mit der die Zahlung dem Zahlungsplan zugeteilt werden soll:

    - Summe
    - Fester Betrag
    - Feste Menge
    - Angegeben

    Das Feld **Quellensteuerzuteilung** zeigt die TDS-Zuteilungsmethode für den Zahlungsplan. Wenn Sie **Gesamt** im Feld **Zuteilung** auswählen, wird die **Quellensteuerzuteilung** automatisch auf **Gesamt** gesetzt. Wenn Sie **Fester Betrag**, **Feste Menge** oder **Angegeben** im Feld **Zuteilung** auswählen, wird die **Quellensteuerzuteilung** automatisch auf **Anteilig** gesetzt.

    > [!NOTE]
    > Wenn das Feld **Quellensteuerzuteilung** auf **Gesamt** gesetzt ist, werden die Zahlungsraten auf Grundlage des Bruttobetrags berechnet, der den TDS-Betrag enthält. Wenn das Feld **Quellensteuerzuteilung** auf **Anteilig** gesetzt ist, werden die Zahlungsraten auf Grundlage des Nettorechnungsbetrags nach Abzug des TDS-Betrag berechnet.

4. Geben Sie im Formular die restlichen erforderlichen Informationen ein und schließen Sie die Seite.
