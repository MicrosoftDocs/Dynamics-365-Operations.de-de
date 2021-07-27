---
title: TDS-Parameter für Kreditoren- und Debitorenkonten einrichten
description: In diesem Thema wird erklärt, wie Sie Parameter in Kreditoren- und Debitorenkonten festlegen, um Abzüge aus der Quellenbesteuerung (TDS) zu unterstützen.
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
ms.openlocfilehash: ccf1557d3c95829421b26d5f84750e3d4236c9e0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358217"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>TDS-Parameter für Kreditoren- und Debitorenkonten einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie Parameter in Kreditoren- und Debitorenkonten festlegen, um Abzüge aus der Quellenbesteuerung (TDS) zu unterstützen.

1. Gehen Sie zu **Steuern \> Setup \> Parameter \> Debitorenparameter**.
2. Wählen Sie in der Registerkarte **Aktualisierungen** **Auftragspositionen aktualisieren**, um das Dialogfeld **Auftragspositionen aktualisieren** zu öffnen.
3. Geben Sie im Abschnitt **TDS-Gruppe** im Feld **TDS-Gruppe aktualisieren** die Methode an, mit der die TDS-Gruppe auf Positionsebene aktualisiert werden soll. Diese Einstellung wird verwendet, wenn die TDS-Gruppe in einer Auftragskopfzeile aktualisiert wird. Die folgenden Optionen stehen zur Verfügung:

    - **Nie**: Die TDS-Gruppe wird in den Auftragspositionen nicht aktualisiert, wenn sie in der Auftragskopfzeile aktualisiert wird.
    - **Immer**: Die TDS-Gruppe wird automatisch in den Auftragspositionen aktualisiert, wenn sie in der Auftragskopfzeile aktualisiert wird.
    - **Eingabeaufforderung**: Benutzer erhalten eine Nachricht, die sie auffordert, die TDS-Gruppe in den Auftragspositionen zu aktualisieren.
4. Wählen Sie **OK** aus.

    [![Dialogfeld „Auftragspositionen aktualisieren“.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Gehen Sie zu **Steuern \> Setup \> Parameter \> Kreditorenparameter**.
6. Stellen Sie auf der Registerkarte **Allgemein** im Inforegister **Aufteilung basierend auf Lieferinformationen** die Option **Produktzugang** auf **Ja** ein, um einen Produktzugang mit unterschiedlichen Lieferadressen und Steuerkontonummern (TAN) zu buchen und aufzuteilen. Wenn diese Option auf **Nein** gesetzt ist, können Sie keinen Lieferschein mit unterschiedlichen Lieferadressen und TAN buchen.
7. Stellen Sie die Option **Rechnung** auf **Ja** um eine Einkaufsrechnung mit unterschiedlichen Lieferadressen und TAN zu buchen und aufzuteilen.

    [![Inforegister „Aufteilung basierend auf Lieferinformationen“.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Schließen Sie die Seite.
