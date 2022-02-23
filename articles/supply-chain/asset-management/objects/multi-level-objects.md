---
title: Anlagen auf mehreren Ebenen
description: In diesem Thema wird erläutert, wie Anlagen auf mehreren Ebenen erstellt und gelöscht werden.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4da57c3849095909226db53c23b3c25301acdc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021321"
---
# <a name="multi-level-assets"></a>Anlagen auf mehreren Ebenen

[!include [banner](../../includes/banner.md)]

 

In diesem Thema wird erläutert, wie Anlagen auf mehreren Ebenen erstellt und gelöscht werden. Sie können Anlagen und zugehörige untergeordnete Anlagen in einer hierarchischen Baumstruktur erstellen. Auf diese Weise können Sie Beziehungen und Abhängigkeiten zwischen den Anlagen anzeigen. Wartungsaufträge können auf allen Ebenen der Anlagenstruktur in Beziehung gesetzt werden. Statistiken können für eine einzelne Ebene oder als Summe aller Ebenen mit untergeordneten Anlagen erstellt werden.

Auf der Listenseite **Alle Anlagen** (**Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**) listet die Spalte **Anlagen** die Anlagen in hierarchischer Reihenfolge auf. Die Spalte **Übergeordnet** zeigt die zugehörige übergeordnete Anlage an. Darüber hinaus zeigt, wenn Anlagen und untergeordnete Anlagen erstellt wurden, der **Anlagenstruktur** im Bereich **Zugehörige Informationen** die Anlagen in einer Baumstruktur.

Informationen zum Erstellen von Anlagen finden Sie unter [Anlage erstellen](../objects/create-an-object.md). Um eine untergeordnete Anlage zu erstellen, wählen Sie die übergeordnete Anlage im Feld **Übergeordnet** im Inforegister **Allgemein** aus.

## <a name="copy-an-asset-or-asset-structure"></a>Anlage oder Anlagenstruktur kopieren

Wenn Ihr Unternehmen mehrere ähnliche Anlagenstrukturen hat, können Sie die Funktion zum Kopieren in Asset Management verwenden, um sie schnell zu erstellen.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**.
2. Wählen Sie auf der Listenseite **Alle Anlagen** die zu kopierende Anlage aus. Wenn Sie beispielsweise die gesamte Anlagenstruktur einschließlich der untergeordneten Anlagen kopieren möchten, wählen Sie eine übergeordnete Anlage aus.
3. Wählen Sie **Anlage kopieren** aus. Im Abschnitt **Kopieren von** wird das Feld **Anlage** auf die Anlage festgelegt, die Sie auf der Listenseite ausgewählt haben.
4. Geben Sie im Abschnitt **Kopieren nach** im Feld **Anlage** den Namen der neuen Anlage ein.
5. Wenn die Anlage, die Sie erstellen, Teil einer vorhandenen Anlagenstruktur sein soll, wählen Sie im Abschnitt **Übergeordnete Anlage** im Feld **Anlage** die Kennung der einer übergeordneten Anlage aus.
6. Wählen Sie **OK**. Die neue Anlagenstruktur wird auf der Listenseite **Alle Anlagen** angezeigt. Alle Anlagenattribute, Wartungspläne und Wartungsdurchgänge, die der kopierten Anlage zugeordnet sind, werden in die neue Anlage oder Anlagenstruktur übertragen.

Wenn Sie eine Anlagenstruktur kopieren, haben die untergeordneten Anlagen in der neuen Struktur den gleichen Namen wie die kopierten untergeordneten Anlagen. Nach dem Kopieren können Sie den Namen und andere Einstellungen für eine Anlage einfach ändern. Wählen Sie die Anlage auf der Listenseite **Alle Anlagen** aus, und wählen Sie dann die Schaltfläche **Bearbeiten** aus.

> [!NOTE]
> Wenn Sie eine Anlage oder eine Anlagenstruktur kopieren, wird der Lebenszyklusstatus der neuen Anlagen auf den Status zurückgesetzt, den Sie als anfänglichen Lebenszyklusstatus für Anlagen definiert haben. Der funktionale Standort wird auf den standardmäßigen funktionalen Standort zurückgesetzt.

## <a name="delete-an-asset-or-asset-structure"></a>Anlage oder Anlagenstruktur löschen

Wenn eine Anlage über untergeordnete Anlagen verfügt, können Sie die Anlage nur dann löschen, wenn keine Wartungsanfragen, Arbeitsaufträge, Fehlererfassungen oder Bedingungsbewertungen für die Anlagen erfasst wurden.

1. Wählen Sie auf der Listenseite **Alle Anlagen** die zu löschende Anlage aus.
2. Wählen Sei **Löschen**.

> [!NOTE]
> Wenn Sie eine Anlage nicht auf diese Weise löschen können, können Sie auch einen Anlagenlebenszyklusstatus für diesen Zweck einrichten. Sie können beispielsweise einen Lebenszyklusstatus **Verschrottet** oder **Gelöscht** auf der Seite **Anlagenlebenszyklusstatus** einrichten.
