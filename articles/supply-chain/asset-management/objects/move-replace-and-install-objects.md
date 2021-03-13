---
title: Anlagen verschieben, ersetzen und installieren
description: In diesem Thema wird erläutert, wie Sie Anlagen in Asset Management verschieben, ersetzen und installieren.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 022ffc59b1b64913fedaf550f3fdb32141a94031
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020278"
---
# <a name="move-replace-and-install-assets"></a>Anlagen verschieben, ersetzen und installieren

[!include [banner](../../includes/banner.md)]

 

In diesem Thema wird erläutert, wie Sie Anlagen in Asset Management verschieben, ersetzen und installieren. Sie können einzelne Anlagen erstellen, die nicht in Beziehung zu anderen Anlagen stehen, oder Sie können eine Anlagenstruktur erstellen, die eine übergeordnete Anlage (Anlage der obersten Ebene) und zugehörige untergeordnete Anlagen (Sub-Anlagen) enthält. In Asset Management gibt es drei Möglichkeiten zum Verschieben und Ändern des Standorts einer Anlage:

- **Verschieben** – Verschiebt eine Anlage entweder in eine andere Anlagenstruktur oder an einen anderen Standort in derselben Anlagenstruktur.
- **Ersetzen** – Entfernt vorübergehend eine Anlage aus einer Anlagenstruktur, sodass sie repariert oder überholt werden kann, und fügen die überholte Anlage dann wieder in die Anlagenstruktur ein. Alternativ können Sie eine verwendete Anlage dauerhaft durch eine neue Anlage ersetzen.
- **Installieren** – Installieren Sie eine übergeordnete Anlage und alle zugehörigen untergeordneten Anlagen an einem funktionalen Standort.

> [!NOTE]
> Die Anlage, die Sie verschieben, ersetzen oder installieren, kann einem anderen funktionalen Standort zugeordnet sein. In diesem Fall verwendet die Anlage möglicherweise Finanzdimensionen des funktionalen Standorts. Auf der Seite **Funktionale Standorttypen** können Sie die Handhabung von Finanzdimensionen für funktionale Standorte einrichten.

## <a name="move-asset"></a>Anlage verschieben

Verwenden Sie die Funktion **Anlage verschieben**, um eine Anlage entweder in eine andere Anlagenstruktur oder an einen anderen Standort in derselben Anlagenstruktur zu verschieben. Sie können eine Anlage auch aus einer Anlagenstruktur verschieben, sodass sie zu einer eigenständigen Anlage wird, die keine Beziehung zu einer Struktur hat.

> [!NOTE]
> Verwenden Sie diese Funktion nicht, wenn Anlagen repariert oder vorübergehend ersetzt werden. Verwenden Sie stattdessen die Funktionen **Anlage ersetzen**, die weiter unten in diesem Thema beschrieben wird.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen** oder **Aktive Anlagen**.
2. Wählen Sie in der Liste die zu verschiebende Anlage aus. Wenn die Anlage untergeordnete Anlagen enthält, verschieben Sie auch diese Anlagen.
3. Wählen Sie **Anlage verschieben** aus.
4. Um die Anlagen so zu verschieben, dass sie Teil einer Anlagenstruktur wird, wählen Sie die neue übergeordnete Anlage im Feld **Übergeordnete Anlage** aus. Wenn Sie eine untergeordnete Anlage verschieben und sie zu einer eigenständige Anlage machen möchten, die keine Beziehungen zu einer Struktur hat, lassen Sie das Feld **Übergeordnete Anlage** leer.
5. Standardmäßig wird das Feld **Gültig** auf das aktuelle Datum und die Uhrzeit festgelegt. Sie können jedoch ein anderes Datum und eine andere Uhrzeit auswählen, wann das Verschieben der Anlagen gültig sein soll.
6. Wählen Sie **OK**.

## <a name="replace-asset"></a>Anlage ersetzen

Verwenden Sie die Funktion **Anlage ersetzen** im Zusammenhang mit Reparaturen, Renovierungen oder dauerhaftem Ersatz einer verbrauchten Anlage durch eine neue Anlage. Diese Funktion wird verwendet, um untergeordnete Anlagen in einer Anlagenstruktur zu ersetzen. Bei übergeordneten Anlagen (d. h. Anlagen, die gerade keine übergeordnete Anlage haben) erfolgt das Ersetzen an einem funktionalen Standort. Weitere Informationen dazu, wie übergeordnete Anlagen an einem funktionalen Standort ersetzt werden, finden Sie unter [Anlagen an funktionalen Standorten installieren](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Wenn eine Werkstatt einer Produktionsabteilung zugeordnet ist, können Sie funktionale Standorte wie **Reparatur**, **Ausschuss** und **Lager** erstellen, um die Reparatur und die Ersetzung von Anlagen zu behandeln.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen** oder **Aktive Anlagen**.
2. Wählen Sie in der Liste die zu ersetzende untergeordnete Anlage aus. Wenn die Anlage untergeordnete Anlagen enthält, ersetzen Sie auch diese Anlagen.
3. Wählen Sie **Anlage ersetzen** aus.

    Das Feld **Strukturänderung** zeigt das Datum und die Uhrzeit an, wann die ausgewählte Anlage und die zugehörigen untergeordneten Anlagen in die Anlagenstruktur verschoben wurden.

4. Wählen Sie im Abschnitt **Ausgewählte Anlage** im Feld **Funktionaler Standort als Ziel** den funktionalen Standort aus, an den die Anlage verschoben werden soll. Wählen Sie beispielsweise den Standort **Reparatur** oder **Ausschuss** aus.

    Im Abschnitt **Übergeordnete Anlage** zeigt das Feld **Gültig** das letzte Datum und die Uhrzeit an, wann die übergeordnete Anlage und die zugehörigen untergeordneten Anlagen installiert oder an den aktuellen funktionalen Standort verschoben wurden.

5. Wählen Sie im Abschnitt **Neue Anlage** im Feld **Anlage** die Anlage aus, die als vorübergehender oder dauerhafter Ersatz für die ausgewählte Anlage eingefügt werden soll. Diese Anlage befindet sich derzeit möglicherweise an einem anderen funktionalen Standort, z. B. **Lager**.
7. Im Abschnitt **Gültig ab** wird das Feld **Gültig** standardmäßig auf das aktuelle Datum und die aktuelle Uhrzeit festgelegt. Sie können jedoch ein anderes Datum und eine andere Uhrzeit auswählen, wann das Ersetzen der Anlagen gültig sein soll.
8. Wählen Sie **OK**.

## <a name="install-asset"></a>Anlage installieren

Verwenden Sie die Funktion **Anlage installieren**, um eine Anlagenstruktur an einen funktionalen Standort zu installieren.

> [!NOTE]
> Wählen Sie immer eine übergeordnete Anlage aus. Die übergeordnete Anlage und die zugehörigen untergeordneten Anlagen werden an den ausgewählten funktionalen Standort verschoben.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen** oder **Aktive Anlagen**.
2. Wählen Sie in der Liste die übergeordnete Anlage aus, die an einem anderen funktionalen Standort installiert werden soll.
3. Wählen Sie **Anlage installieren** aus.

    Der Abschnitt **Attribute** zeigt die Anlagenattribute, die für die übergeordnete Anlage eingerichtet sind.

4. Wählen Sie im Feld **Funktionaler Standort** den neuen Standort aus.
5. Standardmäßig wird das Feld **Gültig** auf das aktuelle Datum und die Uhrzeit festgelegt. Sie können jedoch ein anderes Datum und eine andere Uhrzeit auswählen, wann die Installation in der Anlagenstruktur gültig sein soll.
6. Wählen Sie **OK**.
