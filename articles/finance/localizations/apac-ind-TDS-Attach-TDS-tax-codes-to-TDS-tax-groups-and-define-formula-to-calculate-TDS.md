---
title: TDS-Steuercodes zu TDS-Steuergruppen hinzufügen und die Formel zur TDS-Berechnung festlegen
description: In diesem Thema wird erklärt, wie Sie Steuergruppen für die Quellenbesteuerung (TDS) einrichten und TDS-Steuercodes mit TDS-Steuergruppen verknüpfen. Um die TDS für eine TDS-Steuergruppe zu berechnen, müssen Sie die Formel für die damit verbundenen TDS-Steuercodes festlegen.
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
ms.openlocfilehash: f681018c27afbef8d34c88a518941d45aa9d72df
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358481"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>TDS-Steuercodes zu TDS-Steuergruppen hinzufügen und die Formel zur TDS-Berechnung festlegen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie Steuergruppen für die Quellenbesteuerung (TDS) einrichten und TDS-Steuercodes mit TDS-Steuergruppen verknüpfen. Um die TDS für eine TDS-Steuergruppe zu berechnen, müssen Sie die Formel für die damit verbundenen TDS-Steuercodes festlegen.

Gehen Sie wie folgt vor, um eine TDS-Steuergruppe einzurichten, TDS-Steuercodes anzuhängen und die Formel für die TDS-Berechnung festzulegen.

1. Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuergruppen**.

    [![Seite „Quellensteuergruppen“.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Wählen Sie im Aktionsbereich die Option **Neu** aus, um eine Quellensteuergruppe für TDS zu erstellen und die erforderlichen Details einzugeben.
3. Wählen Sie im Feld **Steuertyp** die Option **TDS** aus.
4. Wählen Sie im Inforegister **Setup** **Hinzufügen** aus, um eine Position zu erstellen.
5. Wählen Sie im Feld **Quellensteuercode** den TDS-Steuercode für die TDS-Steuergruppe aus. Das Feld **Quellensteuername** zeigt den Namen des TDS-Steuercodes und das Feld **Wert** zeigt den Wert.
6. Um den Schwellenwert und den Ausnahmeschwellenwert zu ignorieren, die für die TDS-Steuerkomponente festgelegt sind, die in TDS-Buchungen mit dem TDS-Steuercode verbunden sind, wählen Sie die Option **Schwellenwert übersehen**.
7. Um zu verhindern, dass die Steuergruppe in Buchungen berechnet wird, aktivieren Sie **Befreit**.
8. Wählen Sie im Aktionsbereich **Designer** aus, um den Formeldesigner zu öffnen, damit Sie die Formel zur Berechnung der TDS für die TDS-Steuergruppe festlegen können. Auf der Seite **Designer** werden unter der Registerkarte **Steuern** die TDS-Steuercodes angezeigt, die für die TDS-Steuergruppe ausgewählt wurden.

    [![Designerseite.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Wählen Sie auf der Registerkarte **Berechnung** **ALT + N** aus, um eine Position zu erstellen. Im Feld **Kennung** wird die automatisch generierte Prioritätskennung für die TDS-Berechnung.
10. Wählen Sie im Feld **Steuercode** den TDS-Steuercode aus, für den Sie eine Formel festlegen möchten. In diesem Feld können alle TDS-Steuercodes ausgewählt werden, die für die TDS-Steuergruppe ausgewählt wurden.
11. Wählen Sie im Feld **Steuerbemessungsgrundlage** die Grundlage für die Berechnung der TDS aus:

    - **Bruttobetrag**: Berechnen Sie die TDS auf Grundlage des Bruttobuchungsbetrags (d. h. des Rechnungsbetrags) unter Verwendung des für das Steuercodes definierten Berechnungsausdrucks.
    - **Ohne Bruttobetrag**: Berechnen Sie TDS auf Basis des Berechnungsausdrucks, der für den Steuercode festgelegt ist.

    > [!NOTE]
    > Das Feld **Bemessungsgrundlage** kann nicht auf **Ohne Bruttobetrag** gesetzt werden, wenn der Steuercode die Prioritätskennung **1** hat.

12. Die TDS-Berechnung basiert auf der Formel, die im Feld **Berechnungsausdruck** für jeden Steuercode festgelegt ist, der der TDS-Steuergruppe zugeordnet ist. Wählen Sie das Pluszeichen (**+**), Minuszeichen (**-**), Multiplikationszeichen (**\**_) oder Divisonszeichen (_*/**), um den Berechnungsausdruck für den ausgewählten TDS-Steuercode in das Feld **Berechnungsausdruck** einzugeben.

    > [!NOTE]
    > Für den TDS-Steuercode mit der Prioritätskennung **1** kann kein Berechnungsausdruck definiert werden.

13. Um den Berechnungsausdruck für den Steuercode im Feld **Berechnungsausdruck** festzulegen, fügen Sie im Feld TDS-Steuercodes hinzu, die in der Registerkarte **Steuern** verfügbar sind. Um TDS-Steuercodes in das Feld **Berechnungsausdruck** einzufügen können Sie eine der folgenden Methoden verwenden:

    - Ziehen Sie den gewünschten Steuercode aus der Registerkarte **Steuern** in das Feld **Berechnungsausdruck**.
    - Tippen Sie auf den erforderlichen Steuercode in der Registerkarte **Steuern** (oder machen Sie einen Doppelklick darauf).
    - Wählen Sie den erforderlichen Steuercode in der Registerkarte **Steuern** aus und halten Sie ihn fest (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Steuercode hinzufügen**.

    > [!NOTE]
    > Fügen Sie vor jedem TDS-Steuercode einen Berechnungsausdruck ein. Die dem Berechnungsausdruck hinzugefügten TDS-Steuercodes werden in Klammern angezeigt (\[...\]).

14. Um den Berechnungsausdruck zu löschen, der für einen Steuercode im Feld **Berechnungsausdruck** festgelegt ist, drücken Sie die **C**-Taste.
15. Um einen Datensatz aus der Registerkarte **Berechnung** zu löschen, wählen Sie **Löschen**.
16. Schließen Sie die Seite.
