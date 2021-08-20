---
title: Funktionale Standorttypen
description: In diesem Thema wird beschrieben, wie in Asset Management funktionalen Standorte erstellt werden.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 301dc838ed204ebe488dd167df75fc84131f235f64285c6ae99c62ee1188362c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739154"
---
# <a name="functional-location-types"></a>Funktionale Standorttypen

[!include [banner](../../includes/banner.md)]

 

In diesem Thema wird beschrieben, wie in Asset Management funktionalen Standorte erstellt werden. Funktionale Standorttypen werden verwendet, um die Anforderungen an funktionale Standorte zu verwalten. Dies schließt ein, wie Anlagen an einem funktionalen Standort installiert werden. Sie können Anlagentypen, Wartungspläne, Attribute für funktionale Standorte und Anlagenattributanforderungen einrichten, die für einen funktionalen Standort verwendet werden, der den speziellen funktionalen Standorttyp verwendet. Wenn Sie einen funktionalen Standort erstellen, ist der funktionale Standorttyp erforderlich.

>[!NOTE] 
>Um mit funktionalen Standorten zu arbeiten, müssen Sie einen standardmäßigen funktionalen Standort erstellen, der allein zum Zweck der Erstellung neuer Anlagen verwendet wird. Für diesen standardmäßigen funktionalen Standort müssen Sie einen standardmäßigen funktionalen Standorttypen erstellen, der einfach ist und ermöglicht, mehrere Anlagen am standardmäßigen funktionalen Standort zu installieren. Weitere Informationen zum Einrichten von funktionalen Standorten finden Sie unter [Erstellen von funktionalen Standorten](../functional-locations/create-functional-locations.md).

## <a name="create-a-default-functional-location-type"></a>Erstellen eines standardmäßigen funktionalen Standorttyps

Dieses Verfahren zeigt, wie Sie einen standardmäßigen funktionalen Standorttyp erstellen, der als standardmäßiger Standorttyp verwendet wird.

1. Wählen Sie **Anlagenverwaltung** > **Einstellungen** > **Funktionale Standorte** > **Funktionale Standorttypen** aus.
2. Wählen Sie **Neu** aus, um einen funktionalen Standorttypen zu erstellen.
3. Fügen Sie eine ID für den funktionalen Standorttyp in das Feld **Funktionaler Standorttyp** ein, z. B. „Standard“, und geben Sie einen Namen in das Feld **Name** ein.
4. Wählen Sie ein Lebenszyklusmodell im Feld **Lebenszyklusmodellen für funktionale Standorte** aus.
5. Wählen Sie für die Umschaltfläche **Mehrere Anlagen** „Ja“ aus, um zu ermöglichen, dass mehrere Anlagen an einem funktionalen Standort (dem standardmäßigen funktionalen Standort) mit diesem Typ installiert werden können.

Jetzt wurde der standardmäßige funktionale Standorttyp erstellt, der nur für einen standardmäßigen Standorttyp verwendet wird. Sie sollten diesem standardmäßigen funktionalen Standorttyp keine weiteren Anforderungen oder Einschränkungen hinzufügen.


## <a name="create-functional-location-types"></a>Erstellen von funktionalen Standorttypen

1. Wählen Sie **Anlagenverwaltung** > **Einstellungen** > **Funktionale Standorte** > **Funktionale Standorttypen** aus.
2. Wählen Sie **Neu** aus, um einen funktionalen Standorttypen zu erstellen.
3. Fügen Sie eine ID für den funktionalen Standorttyp in das Feld **Funktionaler Standorttyp** ein, und geben Sie einen Namen in das Feld **Name** ein.
4. Wählen Sie ein Lebenszyklusmodell im Feld **Lebenszyklusmodellen für funktionale Standorte** aus. Weitere Informationen zu den Lebenszyklusstatus von funktionalen Standorten und Lebenszyklusmodellen finden Sie unter [Lebenszyklusstatus funktionaler Standorte](../setup-for-functional-locations/functional-location-stages.md).
5. Wählen Sie für die Umschaltfläche **Mehrere Anlagen** „Ja“ aus, um zu ermöglichen, dass mehrere Anlagen an einem funktionalen Standort mit diesem funktionalen Standorttyp installiert werden können. Wenn Sie „Nein“ auswählen, können Sie nur *eine* Anlage mit diesem funktionalen Standorttypen an einem funktionalen Standort installieren.
6. Wählen Sie für die Umschaltfläche **Anlagendimension aktualisieren** die Option „Ja“, wenn Anlagen, die an einem funktionalen Standort dieses Typs installiert sind, automatisch die Finanzdimensionen verwenden sollen, die mit diesem funktionalen Standort verknüpft sind. Das bedeutet, wenn Sie die Finanzdimensionen im Formular [Technische Standorte anlegen](../functional-locations/create-functional-locations.md) ändern und der Technische Standort einen Technischen Standorttyp mit dieser Umschaltoption auf „Ja“ verwendet, werden die Finanzdimensionen automatisch auf alle auf diesem Technischen Standort installierten Anlagen aktualisiert.
7. Das Feld **Anlagentyp** wird verwendet, wenn Sie automatisch *eine* Anlage für den funktionalen Standort mit der gleichen ID und dem gleichen Namen erstellen möchten, wie Sie für den funktionalen Standort verwenden, den Sie erstellen. Dies ist zum Beispiel dann relevant, wenn Sie einen statischen funktionalen Standort erstellen, wie z. B. ein Gebäude oder eine Rohrleitung. Wählen Sie in diesem Fall den Anlagentyp aus, den Sie für die automatisch erstellte Anlage verwenden möchten. Denken Sie daran, dass Sie die Umschaltfläche **Mehrere Anlagen** auf „Nein“ festlegen müssen, wenn Sie eine Auswahl in diesem Feld vornehmen.
8. Wählen Sie im Inforegister **Anlagentypen** die Anlagentypen aus, die dem funktionalen Standorttyp zugeordnet werden sollen. Wählen Sie **Position hinzufügen**, und wählen Sie die Anlagentypen aus. Wenn Sie hier Anlagentypen hinzufügen, können nur Anlagen mit diesem Anlagentypen an einem funktionalen Standort mit diesem funktionalen Standorttypen installiert werden. Wenn im Inforegister **Anlagentypen** keine Anlagentypen ausgewählt werden, können alle Anlagentypen installiert werden.
9. Wählen Sie im Inforegister **Wartungspläne** die Wartungspläne aus, die automatisch für neue funktionale Standorte mit diesem funktionalen Standorttypen eingerichtet werden sollen. Wählen Sie **Position hinzufügen**, und wählen Sie die Wartungspläne aus. Wenn Sie hier Wartungspläne hinzufügen, können nur diese Pläne an einem funktionalen Standort mit diesem funktionalen Standorttypen verwendet werden.
10. Richten Sie im Inforegister **Anlagenattributanforderungen** die Anlagenattribute ein, die automatisch für neue funktionale Standorte mit diesem funktionalen Standorttypen eingerichtet werden sollen. Wählen Sie **Position hinzufügen**, und wählen Sie das Attribut aus. Diese Attributanforderungen gelten als Richtlinien. Sie werden nicht im Hinblick auf Attribute geprüft, die für eine Anlage festgelegt wurden (**Anlagenverwaltung** > **Allgemeines** > **Anlagen** > **Alle Anlagen** > Anlage auf der Listenseite auswählen > Registerkarte **Allgemein** > Schaltfläche **Attribute**). Die Attributanforderungen werden angezeigt, wenn Sie Anlagen an funktionalen Standorten einrichten.
11. Wählen Sie im Inforegister **Zulässige Typen** die funktionalen Standorttypen aus, die für untergeordnete funktionale Standorttypen gültig sein sollen, die sich auf einen übergeordneten funktionalen Standorttypen beziehen, der den ausgewählten funktionalen Standorttypen verwendet.
12. Wählen Sie im Inforegister **Attribute** die Attribute für funktionale Standorte aus, die automatisch für funktionale Standorte mit diesem funktionalen Standorttypen eingerichtet werden sollen. Wählen Sie **Position hinzufügen**, und wählen Sie das Attribut aus.


>[!NOTE] 
>Im Inforegister **Allgemein** erhalten Sie eine Übersicht über die Anzahl der Anlagentypen, der Wartungspläne, der Anlagenattributanforderungen, der zulässigen Typen, der Attribute und der funktionalen Standorte, die für den funktionalen Standorttypen eingerichtet sind. Das Feld **Funktionale Standorte** gibt die Anzahl der funktionalen Standorte an, die den funktionalen Standorttypen verwenden. Sie können die Schaltfläche **Kopieren** verwenden, um Einstellungen eines funktionalen Standorttyps in den ausgewählten funktionalen Standorttypen zu kopieren.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]