---
title: Anlagenanschaffungen vorschlagen
description: In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817164"
---
# <a name="propose-fixed-asset-acquisitions"></a>Anlagenanschaffungen vorschlagen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird. Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet. Um eine Anlage durch eine Anlagenerfassung zu erwerben, müssen Sie zuerst den Anlagendatensatz erstellen und dann den Anschaffungspreis im Anlagenbuch festlegen.

## <a name="create-an-asset-acquisition-proposal"></a>Vorschlag zum Anlagenerwerb erstellen

Führen Sie die folgenden Schritte aus, um einen Vorschlag zum Anlagenerwerb zu erstellen. 

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
- Überprüfen Sie, ob die Transaktionspositionen erstellt werden.  
- Nur Anlagen mit dem Anschaffungsdatum und dem Anschaffungspreis, die im Buch festgelegt sind, werden in den Anschaffungsvorschlag einbezogen.  
11. Wählen Sie auf der Seite die Registerkarte **Bücher** aus.
12. Wählen Sie **Buchen** aus.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Standardfinanzdimensionen in einen Anschaffungsvorschlag aufnehmen

Die Anschaffungstransaktion kann mithilfe von Excel-Add-Ins erstellt werden, indem Sie zu **Anlagen > Journaleinträge > Anlagenerfassung** gehen. Erstellen Sie eine neue Erfassung und wechseln Sie zum **Positionen**-Abschnitt auf der Seite und wählen Sie das Excel-Symbol und dann eine Anlagenerfassungsposition. Das System erstellt und öffnet eine Excel-Vorlage, die Erfassungspositionen darstellt. Sie können Daten für die Erfassungspositionen hinzufügen, die Sie der Vorlage hinzufügen, und diese Informationen dann wieder im System veröffentlichen. 

Wenn für das ausgewählte Anlagenbuch und die entsprechenden Anlagen, die in die Excel-Vorlage eingegeben wurden, Standarddimensionen eingerichtet wurden, werden die Standardfinanzdimensionen von den Anlagenbuch-Masterdaten aufgerufen, wenn die Erfassung aus Excel heraus im System veröffentlicht wird. Um Finanzdimensionen automatisch in ein Anlagenbuch aufzunehmen, während die Anlagenerfassung über das Excel-Add-In veröffentlicht wird, müssen die Standarddimensionen im Voraus eingerichtet werden.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
