---
title: Anlagen an funktionalen Standorten installieren
description: In diesem Thema wird erklärt, wie in Asset Management funktionale Standorte erstellt werden.
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
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
ms.openlocfilehash: b236013d19967295514bfc0ce3e94eb6765d620a
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783308"
---
# <a name="install-assets-on-functional-locations"></a>Anlagen an funktionalen Standorten installieren

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Nachdem Sie Strukturen funktionaler Standorte erstellt haben, besteht der nächste Schritt darin, Anlagen an den relevanten funktionalen Standorten zu installieren. In diesem Thema wird erklärt, wie in Asset Management Anlagen für diese funktionale Standorte installiert werden. Informationen zum Erstellen von Anlagen finden Sie unter [Anlagen](../objects/introduction-to-objects.md).

Wenn Sie eine Anlagenstruktur erstellt haben, muss die gesamte Anlagenstruktur an einem funktionalen Standort installiert werden. Daher können an einem funktionalen Standort nur übergeordnete Anlagen (Anlagen der obersten Ebene, die keine übergeordnete Anlage haben) ausgewählt werden. Alle zugehörigen untergeordneten Anlagen werden ebenfalls am funktionalen Standort installiert. Wenn Sie Anlagen an einem funktionalen Standort installieren, werden die Finanzdimensionen des funktionalen Standorts möglicherweise automatisch darauf übertragen, je nach den Einstellungen des funktionalen Standorttyps, der für den funktionalen Standort ausgewählt ist. Weitere Informationen zum Einrichten von funktionalen Standorttypen finden Sie unter [Funktionale Standorttypen](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Sie können im Anlagentypen für den funktionalen Standorttyp einrichten, der für einen funktionalen Standort verwendet wird. In diesem Fall, wenn Sie Anlagen am funktionalen Standort installieren, werden nur übergeordnete Anlagen, die denselben Anlagentyp haben, in der Liste der Anlagen angezeigt, die am funktionalen Standort installiert werden können.

Nachdem Sie Anlagen an einem funktionalen Standort installiert haben, können Sie bei Bedarf eine übergeordnete Anlage oder eine Anlagenstruktur ersetzen. Wie beim Installieren einer Anlage wählen Sie auch hier eine übergeordnete Anlage zum Ersetzen aus. Alle zugehörigen untergeordneten Anlagen werden ebenfalls ersetzt. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Installieren einer Anlagenstruktur an einen funktionalen Standort

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Funktionale Standorte** \> **Alle funktionalen Standorte** oder **Aktive funktionale Standorte** aus.
2. Wählen Sie den funktionalen Standort aus, an dem Sie eine Anlage installieren möchten.
3. Wählen Sie **Anlage installieren** aus.

    Der Abschnitt **Attribute** zeigt eine Liste der Anlagenattributanforderungen an, die für den funktionalen Standorttyp eingerichtet sind, der für den funktionalen Standort ausgewählt wurde. Die Attribute dienen nur zu Informationszwecken. Das System überprüft die Attribute nicht hinsichtlich der Anlagenattribute, die für die Anlage festgelegt sind, die Sie installieren. Sie müssen die Prüfung nach der Auswahl einer Anlage im Feld **Anlage** durchführen.

4. Wählen Sie im Feld **Anlage** die übergeordnete Anlage für die Installation aus. Alle zugehörigen untergeordneten Anlagen werden automatisch in die Installation einbezogen.

    Der Abschnitt **Anlagenattribute** auf der rechten Seite der Anlagenliste zeigt die Anlagenattribute an, die der ausgewählten Anlage zugeordnet sind.

5. Wählen Sie im Feld **Gültig** das Datum und die Uhrzeit aus, ab wann die Anlageninstallation gültig ist. Nach diesem Datum und dieser Uhrzeit werden Kosten für diese Anlage und zugehörige untergeordnete Anlagen auf diesen funktionalen Standort bezogenen.

    > [!NOTE]
    > Die Anlagenattribute, die für die Anlage eingerichtet werden, werden zum Bereich **Attribute** hinzugefügt. Die Attributanforderung **Gewicht** wurde beispielsweise als Anforderung sowohl für das Attribut als auch den funktionalen Standort hinzugefügt. Wenn die Anlage Attributanforderungen desselben Typs hat wie der funktionale Standort, werden die Werte der Attributanforderungen der Anlage in die Felder **Wert** eingegeben. Daher können Sie Anlagenwerte im Hinblick auf die Attributanforderungen prüfen, die für den funktionalen Standort festgelegt sind. Die auf Attributanforderungen, die für den funktionalen Standort eingerichtet sind, werden mit einem Häkchen markiert.

6. Wählen Sie **OK**.

    > [!NOTE]
    > Um die Installation einer Anlage dadurch zu ändern, dass Sie sie an einem neuen funktionalen Standort installieren, gehen Sie wie in Schritt 1 bis 6 in diesem Verfahren beschrieben vor. Wenn Sie eine Anlage an einem neuen funktionalen Speicherort installieren, wird die Anlage automatisch vom vorherigen funktionalen Standort deinstalliert. Alle aktiven Wartungsanfragen oder Arbeitsaufträge, die für die Anlage erstellt wurden, bevor Sie sie an einem neuen funktionalen Standort eingerichtet haben, werden **nicht** automatisch an den neuen funktionalen Standort übertragen. Wenn diese Wartungsanfragen und Arbeitsaufträge weiterhin für die Anlage erforderlich sind, müssen Sie sie manuell neu erstellen, nachdem die Anlage am neuen Standort installiert wurde.

7. Um eine Liste aller Anlagen einschließlich der untergeordneten Anlagen anzuzeigen, die am funktionalen Standort installiert sind, wählen Sie den funktionalen Standort auf der Seite **Alle funktionalen Standorte** aus, und wählen Sie anschließend **Anlagen**.
8. Um eine Liste aktiver Wartungsanfragen, aktiver Arbeitsaufträge oder Fehlererfassungen anzuzeigen, die sich auf Anlagen beziehen, die an einem funktionalen Standort installiert sind, wählen Sie den funktionalen Standort auf der Seite **Alle funktionalen Standorte** aus, und wählen Sie anschließend **Anfragen**, **Arbeitsaufträge** oder **Fehler**.

> [!NOTE]
> Wenn Daten geändert werden, die sich auf Anlagen beziehen, werden sie automatisch an dem funktionalen Standort aktualisiert, an dem die Anlage installiert ist. Diese automatische Aktualisierung betrifft Änderungen an den Wartungsanfragen, Arbeitsaufträgen und Anlagenfehlererfassungen, Erfassungen von Wartungsausfallzeiten und Anlagenmessungserfassungen.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Automatisches Erstellen einer Anlage an einem funktionalen Standort

Sie können Phasen für funktionale Standorte und funktionale Standorttypen einrichten, um die automatische Erstellung *einer* Anlage an einem funktionalen Standort zu behandeln. Die Anlage erhält dieselbe Kennung und denselben Namen wie der funktionale Standort. Diese Funktionen können hilfreich sein, wenn Sie die Wartung einer großen, statische Anlage behandeln, wie z. B. einem Gebäude.

Bevor Sie eine Anlage an einem funktionalen Standort automatisch erstellen können, müssen die folgenden Einstellungsdaten verfügbar sein:

- Erstellen Sie einen funktionalen Standorttypen, um die automatische Erstellung einer Anlage zu behandeln. Wählen Sie im Feld **Anlagentyp** einen Anlagentyp aus. Weitere Informationen finden Sie unter [Funktionale Standorttypen](../setup-for-functional-locations/functional-location-types.md).
- Erstellen Sie einen Lebenszyklusstatus für einen funktionalen Standort, um die automatische Erstellung einer Anlage zu behandeln. Legen Sie die Option **Anlage erstellen** auf **Ja** fest. Weitere Informationen finden Sie unter [Lebenszyklusstatus funktionaler Standorte](../setup-for-functional-locations/functional-location-stages.md).

Nachdem die Einstellungsdaten verfügbar sind, sind Sie bereit, eine Anlage zu erstellen.

1. Stellen Sie auf der Seite **Alle funktionalen Standorte** sicher, dass der funktionale Standort, an dem die Anlage automatisch erstellt werden soll, den funktionalen Standorttypen verwendet, den Sie für diesen Zweck erstellt haben.
2. Wählen Sie den funktionalen Standort aus der Liste aus.
3. Wählen Sie **Status des funktionalen Standorts aktualisieren** aus und anschließend den Lebenszyklusstatus, der für diesen Zweck erstellt wurde. Eine Anlage wird nun automatisch am funktionalen Standort installiert. Die Anlage hat denselben Namen wie der funktionale Standort.
