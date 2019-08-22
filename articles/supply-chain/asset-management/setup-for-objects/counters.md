---
title: Anlagenmessungen
description: In diesem Thema wird erläutert, wie Sie in Anlagemesstypen in der Anlagenverwaltung erstellen.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783301"
---
# <a name="asset-measures"></a>Anlagenmessungen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie in Anlagemesstypen in der Anlagenverwaltung erstellen. Anlagenmesstypen werden verwendet, um Messungserfassungen für Anlagen vorzunehmen, z. B. hinsichtlich der Anzahl der Produktionsstunden oder der an der Anlage produzierten Menge. Anlagentypen sind mit Anlagenmesstypen verknüpft. Dies bedeutet, dass eine Anlagenmessung für eine Anlage nur verwendet werden kann, wenn die Anlagenmessung für den Anlagentyp eingerichtet ist, der in der Anlage verwendet wird.

Bevor Sie Messungserfassungen für Anlagen vornehmen können, müssen Sie zunächst im Feld **Zähler** die Anlagenmesstypen erstellen, die Sie verwenden möchten. Danach können Sie Messungserfassungen für Anlagen unter **Anlagenmessungen** erstellen. 

Anlagenmessungen können auf Wartungsplänen verwendet werden. Eine Wartungsplanposition kann vom Typ „Zähler“ sein, beispielsweise in Bezug auf die Anzahl der Produktionsstunden oder die produzierte Menge. 

Eine Anlagenmessungserfassung kann auf der Grundlage der Produktionsstunden oder produzierten Menge manuell oder automatisch aktualisiert werden. Eine Anlagenmessung kann so eingerichtet werden, dass eine von drei Aktualisierungsmethoden verwendet wird (ausgewählt im Feld **Aktualisieren** unter **Zähler**).
  
- Manuell: Sie müssen Anlagenmesswerte manuell erfassen.  
- Produktionsstunden: Der Zähler wird automatisch basierend auf der Anzahl der Produktionsstunden aktualisiert.  
- Produktionsmenge: Der Zähler wird automatisch basierend auf der produzierten Menge aktualisiert.  

>[!NOTE]
>Wenn die produzierte Menge verwendet wird, sind *alle* erfassten Elemente in der Messungserfassung enthalten, sowohl die Gutmenge als auch die Fehlermenge. Es ist immer möglich, bei Bedarf eine manuelle Anlagenmessungserfassung vorzunehmen.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Zählertypen für Anlagenzählererfassungen erstellen

1. Wählen Sie **Anlagenverwaltung** > **Einstellungen** > **Anlagentypen** > **Zähler** aus.
2. Wählen Sie **Neu** aus, um einen neuen Anlagenmesstyp zu erstellen.
3. Geben Sie eine Kennung im Feld **Zähler** und einen Zählernamen im Feld **Name** ein.
4. Wählen Sie auf dem Inforegister **Allgemein** eine Maßeinheit im Feld **Einheit** aus.
5. Wählen Sie im Feld **Aktualisieren** die für die Anlagenmessung zu verwendende Aktualisierungsmethode aus.
6. Wählen Sie auf der Umschaltschaltfläche **Zählerwerte erben** die Option „Ja“ aus, wenn untergeordnete Anlagen in einer Anlagenstruktur automatisch die auf der Ebene der übergeordneten Anlage vorgenommenen Anlagenmessungserfassungen erben sollen.
7. Wählen Sie im Feld **Gesamtsumme** die Summierungsmethode aus, die für eine Anlagenmessung mit diesem Anlagenmesstyp verwendet werden soll. „Summe“ ist die Standardeinstellung. Diese wird verwendet, um kontinuierlich registrierte Werte zum Gesamtwert hinzuzufügen. „Mittelwert“ kann verwendet werden, wenn eine Anlagenmessung eingerichtet wird, um einen Schwellenwert zu überwachen, zum Beispiel bezüglich Temperatur, Erschütterungen oder Abnutzung einer Anlage. 
8. Geben Sie im Feld **Abweichung über** die obere Ebene in Prozent ein, um zu überprüfen, ob sich die manuellen Anlagenmessungserfassungen innerhalb eines erwarteten Bereichs befinden. Die Überprüfung basiert auf einer linearen Erhöhung bei vorhandenen Anlagenmessungserfassungen.
9. Geben Sie im Feld **Abweichung unter** die untere Ebene in Prozent ein, um zu überprüfen, ob sich die manuellen Messungserfassungen innerhalb eines erwarteten Bereichs befinden. Die Überprüfung basiert auf einer linearen Verringerung bei vorhandenen Anlagenmessungserfassungen.
10. Wählen Sie im Feld **Typ** die Art der Meldung aus (Information, Warnung, Fehler), die bei manuellen Anlagenmessungserfassungen angezeigt werden soll, wenn Abweichungen außerhalb des definierten Bereichs auftreten.
11. Fügen Sie auf dem Inforegister **Anlagentypen** die Anlagentypen hinzu, die die Anlagenmessung verwenden können sollen.
12. Fügen Sie auf dem Inforegister **Verwandte Anlagenmessungen** die Anlagenmessungen hinzu, die automatisch aktualisiert werden sollen, wenn diese Anlagenmessung aktualisiert wird.


>[!NOTE]
>Eine zugehörige Anlagenmessung wird nur dann automatisch aktualisiert, wenn die zugehörige Anlagenmessung in den Anlagenmessungseinstellungen über den Anlagentyp verfügt, dem sie zugeordnet ist. Beispiel: Sie richten eine Anlagenmessung für „Produktionsstunden“ ein und fügen den Anlagentyp „Lkw-Motor“ hinzu. Wenn diese Anlagenmessung aktualisiert wird, wird der zugehörige Zähler „Öl“ ebenfalls mit denselben Anlagenmesswerten aktualisiert. Die Einstellung in **Zähler** schließt die Einstellung für „Stunden“ ein. Für die Anlagenmessung „Öl“ sollte außerdem der Anlagentyp „Lkw-Motor“ zum Inforegister **Anlagentypen** hinzugefügt werden, um den Bezug zur Anlagenmessung sicherzustellen. Unten auf den Screenshots sehen Sie ein Beispiel für die Einrichtung der Anlagenmessungen für Stunden und Öl.

Wenn Anlagentypen zu einem Anlagenmessungstyp unter **Zähler** hinzugefügt werden, wird diese Anlagenmessung automatisch zu den Anlagentypen im Inforegister **Zähler** unter [Anlagentypen](../setup-for-objects/object-types.md) hinzugefügt.

![Abbildung 1](media/071-setup-for-objects.png)


