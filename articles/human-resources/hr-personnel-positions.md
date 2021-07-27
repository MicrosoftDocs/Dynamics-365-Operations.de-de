---
title: Positionen
description: In diesem Thema werden die konzeptionellen Elemente beschrieben, die eine Position enthalten kann. Es enthält auch Beispiele, die zeigen, wie Sie diese Elemente in Ihrer Organisation verwenden können.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b44cfaedc4e1286d033bba49b54a12b7e096bf99
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "6333125"
---
# <a name="positions"></a>Positionen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die konzeptionellen Elemente beschrieben, die eine Position enthalten kann. Es enthält auch Beispiele, die zeigen, wie Sie diese Elemente in Ihrer Organisation verwenden können.

Bevor Sie eine Position anlegen können, muss eine Stelle eingerichtet werden. Einige Positionsdetails, z. B. die Vergütungsregion, die Arbeitskraftzuweisung, die Positionsdauer und die Berichtsbeziehung, hängen vom Gültigkeitsdatum ab.

## <a name="general-information"></a>Allgemeine Angaben

Wenn Sie eine Position erstellen, müssen Sie eine Stelle auswählen. Die folgenden Informationen werden automatisch aus der von Ihnen ausgewählten Stelle befüllt:

- Beschreibung
- Titel
- Vollzeitäquivalent
- Stellenfamilie

Der Positionstitel wird verwendet, um auf den Titel eines Mitarbeiters zu verweisen. (Der Titel, der bei dem Mitarbeiter angegeben ist, wird nicht verwendet.) Daher sollten Positionstitel so weit wie möglich standardisiert werden.

> [!NOTE]
> Eine Arbeitskraft kann einer Position nicht an einem Datum zugewiesen werden, das vor dem Für-eine-Zuweisung-verfügbar-Datum liegt.
>
> Ein Parameter auf der Registerkarte **Positionen** der Seite **Freigegebene Personalverwaltungsparameter** steuert das Verhalten der Arbeitskraftzuweisung. Wählen Sie einen der folgenden Werte aus:
>
> - **Immer** – Sie können Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Positionen erstellt werden, werden das **Verfügbar für die Zuweisung** Datum und die Uhrzeit auf der Registerkarte " **Allgemein** der Seite **Position** automatisch auf das Datum und die Uhrzeit festgelegt.
> - **Nie** – Sie können keine Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Sie diese Option auswählen, müssen Sie die Seite **Position** für jede neue Position öffnen, sobald sie verfügbar wird. Geben Sie dann auf der Registerkarte **Allgemein** ein **Für eine Zuweisung verfügbar**-Datum ein, um die Mitarbeiterzuweisung zu aktivieren. Wenn Sie diese Option auswählen, wird das Datum der Arbeitskraftzuweisung standardmäßig auf **Nie** gesetzt, wenn Sie versuchen, die Arbeitskraft zuzuweisen.

## <a name="position-duration"></a>Positionsdauer

Jede Position gilt für eine bestimmte Zeit, die als Dauer bezeichnet wird. Sommerpositionen könnten zum Beispiel eine Dauer vom 1. Mai 2021 bis zum 31. August 2021 haben. Das Aktivierungsdatum ist das Datum, an dem die Position im System aktiv ist. Das Deaktivierungsdatum ist das Datum, an dem die Position nicht mehr im System aktiv ist.

Beachten Sie, dass weder das Für-eine-Zuweisung-verfügbar-Datum noch das Datum der Arbeitskraftzuordnung vor dem Aktivierungsdatum liegen dürfen. Eine Position gilt erst als aktiv, wenn das Aktivierungsdatum erreicht ist. Darüber hinaus kann eine Arbeitskraftzuweisung nicht über das Deaktivierungsdatum der Position hinausgehen.

## <a name="reports-to-position"></a>Berichte an Position

Positionen sind wichtiges Elemente in der untergeordneten Ebene einer Organisationshierarchie. Auf der Seite **Position** können Sie die Position angeben, der eine Position untergeordnet ist. Wenn Sie eine Arbeitskraft einer Position zuweisen, die an eine andere Position berichtet, erstellen Sie eine Berichtsbeziehung zwischen den Arbeitskräften, die diesen beiden Positionen zugewiesen werden. Zum Beispiel: Position 000220 berichtet an Position 000300. Kim Akers wird der Position 000220 zugewiesen und Sanjay Patel wird der Position 000300 zugewiesen. Daher berichtet Kim Akers an Sanjay Patel.

> [!TIP]
> Die „Berichtet an Position“ wird im gesamten System verwendet, um festzustellen, wer der Vorgesetzte eines Mitarbeiters ist. Wenn im vorherigen Beispiel Sanjay Patel die Vorgesetztenrolle im System zugewiesen ist, sieht er Kim Akers als direkt an ihn berichtende Arbeitskraft im Manager-Self-Service. Die Berichtsbeziehung kann auch verwendet werden, wenn Sie Workflow-Routingregeln und Checklistenaufgaben erstellen.

## <a name="relationships"></a>Beziehungen

Wenn Ihre Organisation eine Matrixhierarchie oder eine andere benutzerdefinierte Hierarchie verwendet, können Sie Stellenhierarchietypen einrichten. Anschließend können Sie für jeden von Ihnen eingerichteten Hierarchietyp Berichtsbeziehungen zu Positionen hinzufügen. Beispielsweise ist Lori Penor ein Generaldirektor bei Adventure Works und wird der Position **Generaldirektor** zugewiesen. Lori verwaltet die Entwicklung eines Produkts, das verwendet wird, um Produkte zu säubern. Sie braucht einen Buchhalter, der ihr bei den Finanzen hilft. Daher hat sie Kim Akers eingestellt, um ihr Buchhalter zu werden. Kim ist direkt Sanjay Patel unterstellt, arbeitet aber auch mit Lori Penor an der Arbeit, die mit den Finanzen zur Entwicklung des Gerätereinigers zugeordnet ist.

Für das vorhergehende Beispiel müssen Sie die folgenden Aufgaben ausführen, um das Arbeitsverhältnis zwischen Kim Akers und Lori Penor einzurichten:

1. Erstellen Sie einen benutzerdefinierten Positionshierarchietyp namens **Gerät**, um eine Hierarchie zu erstellen, die Positionen enthält, die für die Arbeit an dem Gerätereinigerprodukt zuständig sind.
2. Weisen Sie die **Generaldirektor**-Position als die Position zu, der Kims Position in der Hierarchie **Geräte** unterstellt sein soll.
3. Verwenden Sie die Positionshierarchie, um die Berichtstruktur von Positionen anzuzeigen. Wenn Sie mehrere Positionshierarchien haben, können Sie die Hierarchie für jeden Hierarchietyp in der Positionshierarchie anzeigen. Sie können nach einer Position auch mit der Positionskennung oder dem Namen der Arbeitskraft, die der Position zugeordnet ist, suchen. Die Positionshierarchie ist eine Organisationshierarchie.

## <a name="labor-union"></a>Gewerkschaft

Sie können vermerken, ob für die Stelle eine Gewerkschaftsvereinbarung erforderlich ist und welche Gewerkschaft verwendet wird. Sie können die Vereinbarung auch einer juristischen Person zuordnen.

## <a name="financial-dimensions"></a>Finanzdimensionen

Wenn Sie die Finanzdimension für eine Position erstellen, müssen Sie eine juristische Person angeben. Sie können die Standarddimensionen für jede Dimension einzeln auswählen. Alternativ können Sie eine Verteilungsvorlage auswählen, um die Standarddimensionen automatisch auszufüllen. Eine Verteilungsvorlage bietet auch die Möglichkeit, Beträge mehreren Dimensionswerten zuzuordnen.
