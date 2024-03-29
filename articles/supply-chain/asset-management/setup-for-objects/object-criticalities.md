---
title: Typen kritischer Werte für Anlagen
description: In diesem Artikel wird erläutert, was Typen kritischer Werte für Anlagen in Anlagenverwaltung sind.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfde9a9bc681c0d758491fc5c361b5b046e20d9d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899497"
---
# <a name="asset-criticality-types"></a>Typen kritischer Werte für Anlagen

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel wird erläutert, was Typen kritischer Werte für Anlagen in Anlagenverwaltung sind. Kritische Anlagenzustände beziehen sich auf Anlagen und werden an Arbeitsaufträge übertragen. Sie können in einem Arbeitsauftrag nicht geändert werden. Kritische Anlagenzustände werden verwendet, um den kritischen Zustand von Arbeitsaufträgen während der Planung zu berechnen. Sie werden also dazu verwendet, um das Ausmaß zu berechnen, in dem ein Wartungseinzelvorgang für eine Anlage sich auf die Produktionsplan und die Produktivität in Ihrem Unternehmen auswirkt. Weitere Informationen zu den Einstellungen, die sich auf die Berechnung von Bewertungsnoten für Arbeitsauftragsplanung beziehen, finden Sie unter [Anlagenverwaltungsparameter](../setup-for-objects/enterprise-asset-management-parameters.md).

Um kritische Anlagenzustände einzurichten, erstellen Sie zunächst die Typen der kritischen Anlagenzustände, die für die Anlageneinrichtung verwendet werden sollen. Anschließend richten Sie die kritischen Anlagenzustände ein.

## <a name="set-up-criticality-types"></a>Typen kritischer Anlagenzustände

1. Wählen Sie **Anlageverwaltung** \> **Einstellungen** \> **Anlagen** \> **Typen kritischer Werte** aus.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Geben Sie im Feld **Risiko** eine Zahl ein, die der Kritikalität angibt.
4. Geben Sie im Feld **Name** einen Namen für den Kritikalitätstyp ein.
5. Geben Sie im Feld **Faktor** einen Faktor ein. Dieser Faktor wird bei der Berechnung der Arbeitsauftragsplanung verwendet, um den Kritikalitätsdatensatz zu bestimmen, der verwendet werden soll. (Es wird immer der Datensatz mit dem höchsten Faktor verwendet). Diese Einstellung ist relevant, wenn, wie in der folgenden Abbildung dargestellt, Kritikalitätspositionen erstellt werden, die den gleichen Kritikalitätswert haben.

    ![Seite „Typen kritischer Werte“.](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Kritische Anlagenzustände einrichten

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Kritische Anlagenzustände**.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Nehmen Sie abhängig von der erforderlichen Detailebene für die Anlagenkritikalität die zutreffende Auswahl in den Feldern **Funktionaler Standort**, **Anlagentyp**, **Hersteller**, **Modell**, **Anlage**, **Einzelvorgangstypkategorie**, **Einzelvorgangstyp**, **Einzelvorgangstypvariante** und **Einzelvorgangsanforderung** vor.

    > [!NOTE]
    > Wenn eine Anlagenkritikalität ausgewählt ist, durchläuft Asset Management alle Anlagenkritikalitätsdatensätze, um nach einer möglichen Übereinstimmung zu suchen. Die spezifischste Kombination wird immer zuerst geprüft. Asset Management überprüft also zuerst das Feld **Einzelvorgangsanforderung**. Wenn keine Übereinstimmung gefunden wird, wird das Feld **Einzelvorgangstypvariante** überprüft. Wenn keine Übereinstimmung gefunden wird, wird das Feld **Einzelvorgangstyp** überprüft, usw. Wie Sie im Layout der Seite sehen können, bedeutet dieses Verhalten, dass Asset Management zum Auffinden der spezifischsten Kombinationen jeden Datensatz von rechts nach links auf Übereinstimmung prüft. Wenn keine Übereinstimmung gefunden wird, wird der Standarddatensatz verwendet, der keine Auswahl hat.

4. Wählen Sie im Feld **Risiko** einen der Kritikalitätswerte aus, die Sie im vorherigen Verfahren erstellt haben.

### <a name="notes-about-criticality-setup"></a>Hinweise zur Kritikalitätseinstellung

- Wenn Sie eine Anlagenkritikalität in dieser Einstellung ändern, nachdem Sie diese bereits für einen Arbeitsauftrag verwendet haben, wird die Kritikalität für den Arbeitsauftrag nicht entsprechend aktualisiert.
- Die Kritikalität eines Arbeitsauftrags wird jedes Mal neu berechnet, wenn eine Arbeitsauftragsposition zum Arbeitsauftrag hinzugefügt oder daraus gelöscht wird.
- Wenn ein Arbeitsauftrag mehrere Arbeitsauftragseinzelvorgänge enthält, wird die höchste Kritikalität, gemäß dem Feld **Faktor** auf der Seite **Typen kritischer Werte**, immer für den Arbeitsauftrag verwendet.
- Im Allgemeinen kann sich die Anlagenkritikalität mit der Zeit ändern. Kritikalität kann durch den Einkauf von neuer Ausrüstung, Wiederaufbereitungen usw. beeinflusst werden. Sie sollten die kritischen Anlagenzustände regelmäßig erneut bewerten (beispielsweise einmal pro Jahr), um sicherzustellen, dass die Kritikalitätsdefinitionen mit den Einstellungen der aktuellen Produktion übereinstimmen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]