---
title: Maßeinheitsumrechnungen für Produktvarianten
description: In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen für Produktvarianten eingerichtet werden können. Zudem enthält es ein Beispiel für die Einstellung.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ed28928b0f07833d5906a68f780e3bb5bbe0bfe9
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921216"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Maßeinheitsumrechnungen für Produktvarianten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen für verschiedene Produktvarianten eingerichtet werden können.

Sie können Produktvarianten verwenden, um Variationen eines einzelnen Produkts zu erstellen, anstatt mehrere einzelne Produkte zu erstellen, die verwaltet werden müssen. Eine Produktvariante kann beispielsweise ein T-Shirt einer bestimmten Größe und Farbe sein.

Bisher konnten Einheitenumrechnungen nur im Produktmaster eingerichtet werden. Daher hatten alle Produktvarianten die gleichen Regeln für die Einheitenumrechnung. Wenn jedoch die Funktion *Umrechnung von Maßeinheiten für Produktvarianten* aktiviert ist, Ihre T-Shirts in Kartons verkauft werden, und die Anzahl der T-Shirts, die in einem Karton verpackt werden können, von der Größe der T-Shirts abhängt, können Sie jetzt Einheitenumrechnungen zwischen den verschiedenen Shirtgrößen und den Kartons, die für die Verpackung verwendet werden, einrichten.

## <a name="turn-on-the-feature-in-your-system"></a>Funktion in Ihrem System aktivieren

Wenn Sie diese Funktion in Ihrem System noch nicht sehen, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), und aktivieren Sie die Funktion *Umrechnung von Maßeinheiten für Produktvarianten*.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Einrichten eines Produkts für Einheitenumrechnung pro Variante

Protuktvarianten können nur für Produkte des Typs Produktmaster erstellt werden. Weitere Informationen finden Sie unter [Erstellen eines Produktmasters](tasks/create-product-master.md). Die Funktion *Umrechnung von Maßeinheiten für Produktvarianten* ist nicht für Produkte verfügbar, die für Artikelgewichtsprozesse eingerichtet sind.

Führen Sie die folgenden Schritte aus, um einen Produktmaster für die Unterstützung der Einheitenumrechnung pro Variante zu konfigurieren.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produktmaster**.
1. Erstellen oder öffnen Sie einen Produktmaster, um zur Seite **Produktdetails** zu wechseln.
1. Setzen Sie die Option auf **Konvertierung von Maßeinheiten aktivieren** auf *Ja*.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Einheitenumrechnung**.
1. Die Seite **Einheitenumrechnungen** wird geöffnet. Wählen Sie eine der folgenden Registerkarten aus:

    - **Klasseninterne Umrechnungen** – Wählen Sie diese Registerkarte aus, um zwischen Einheiten zu konvertieren, die zur gleichen Einheitenklasse gehören.
    - **Klassenübergreifende Umrechnungen** – Wählen Sie diese Registerkarte aus, um zwischen Einheiten zu konvertieren, die zu verschiedenen Einheitenklassen gehören.

1. Klicken Sie zum Hinzufügen einer neuen Einheitsumrechnung auf **Neu**.
1. Setzen Sie das Feld **Konvertierung erstellen für** auf einen der folgenden Werte:

    - **Produkt** – Wenn Sie diesen Wert auswählen, kann eine Einheitenumrechnung für den Produktmaster eingerichtet werden. Diese Einheitenumrechnung wird als Fallback für alle Produktvarianten verwendet, für die keine Einheitenumrechnung definiert ist.
    - **Produktvariante** – Wenn Sie diesen Wert auswählen, kann eine Einheitenumrechnung für eine spezifische Produktvariante eingerichtet werden. Verwenden Sie das Feld **Produktvariante** zur Auswahl der Variante.

    ![Hinzufügen einer neuen Einheitenumrechnung](media/uom-new-conversion.png "Hinzufügen einer neuen Einheitenumrechnung")

1. Verwenden Sie die anderen verfügbaren Felder, um Ihre Einheitenumrechnung einzurichten.
1. Wählen Sie **OK**, um die neue Einheitenumrechnung zu speichern.

> [!TIP]
> Sie können die Seite **Einheitenumrechnungen** für ein Produkt oder eine Produktvariante von einer der folgenden Seiten öffnen:
> 
> - Produktdetails
> - Details für freigegebene Produkte
> - Freigegebene Produktvarianten

## <a name="example-scenario"></a>Beispielszenario

In diesem Szenarion verkauft ein Unternehmen die T-Shirts in kleinen, mittig großen und extra-großen Größen. Das T-Shirt wird als Produkt definiert, und die verschiedenen Größen werden als Varianten dieses Produkts definiert. Die Shirts sind in Kartons verpackt. Für kleine, mittlere und große Größen können fünf Shirts in jeder Box enthalten sein. Bei der Größe „extra-groß“ ist jedoch nur Platz für vier Shirts in jeder Schachtel.

Das Unternehmen möchte die verschiedenen Varianten in der Einheit *Stücke* nachverfolgen, aber verkauft die T-Shirts in der Einheit *Kartons*. Für kleine, mittlere und große Größen beträgt die Umrechnung zwischen der Inventareinheit und der Verkaufseinheit 1 Karton = 5 Stück. Für die extra große Größe beträgt die Umrechnung 1 Karton = 4 Stück.

1. Öffnen Sie auf der Seite **Freigegebene Produktdetails** für das Produkt **T-Shirt** die Seite **Einheitenumrechnungen**.
1. Auf der Seite **Einheitenumrechnungen** richten Sie die folgende Einheitenumrechnung für die **X-große** Freigabenproduktvariante ein.

    | Feld                 | Einstellung                 |
    |-----------------------|-------------------------|
    | Konvertierung erstellen für | Produktvariante         |
    | Produktvariante       | T-Shirt: : X-groß : : |
    | Von Einheit             | Schachteln                   |
    | Faktor                | 4                       |
    | In Einheit               | Stückzahl                  |

1. Die freigegebenen Produktvarianten **klein**, **mittel** und **groß** haben dieselbe Einheitenumrechnung zwischen dem Feld *Karton* und *Stück*, was bedeutet, dass Sie die Einheitenumrechnung für sie im Produktmaster definieren können.

    | Feld                 | Einstellung |
    |-----------------------|---------|
    | Konvertierung erstellen für | Produkt |
    | Produkt               | T-Shirt |
    | Von Einheit             | Schachteln   |
    | Faktor                | 5       |
    | In Einheit               | Stücke  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Excel verwenden, um die Einheitenumrechnungen zu aktualisieren

Wenn ein Produkt viele Produktvarianten mit unterschiedlichen Einheitenumrechnungen hat, ist es eine gute Idee, die Einheitenumrechnungen in eine Microsoft Excel-Arbeitsmappe zu exportieren, zu aktualisieren und sie dann wieder in Dynamics 365 Supply Chain Management zu veröffentlichen.

Um Einheitenumrechnungen nach Excel zu exportieren, klicken Sie auf der Seite **Einheitenumrechnungen** im Aktionsbereich auf **In Microsoft Office öffnen**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Maßeinheiten verwalten](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]