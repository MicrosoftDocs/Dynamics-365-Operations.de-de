---
title: Anlagenanschaffungen vorschlagen
description: In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443430"
---
# <a name="propose-fixed-asset-acquisitions"></a>Anlagenanschaffungen vorschlagen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird. Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet. Um eine Anlage durch eine Anlagenerfassung zu erwerben, müssen Sie zuerst den Anlagendatensatz erstellen und dann den Anschaffungspreis im Anlagenbuch festlegen.

1. Gehen Sie im Navigationsbereich zu **Module > Anlage > Journalbuchungen > Anlagenbuchhaltung**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.
4. Wählen Sie im Aktivitätsbereich **Positionen** aus.
5. Wählen Sie **Vorschläge** aus.
6. Wählen Sie **Anschaffungsvorschlag** aus.
7. Wählen Sie **Filter** aus. Wählen Sie **Zurücksetzen** aus, um vorherige Werte zu löschen.
8. Wählen Sie die Zeile **Anlagennummer** aus.
9. Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus. Legen Sie die verbleibenden Kriterien für die Anlagen fest, die Sie mit diesem Vorschlag abrufen möchten.  
10. Wählen Sie zweimal **OK** aus, um den Bereich zu verlassen.
- Überprüfen Sie die erstellten Transaktionspositionen.  
- Nur Anlagen mit dem Anschaffungsdatum und dem Anschaffungspreis, die im Buch festgelegt sind, werden in den Anschaffungsvorschlag einbezogen.  
11. Wählen Sie auf der Seite die Registerkarte **Bücher** aus.
12. Wählen Sie **Buchen** aus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]