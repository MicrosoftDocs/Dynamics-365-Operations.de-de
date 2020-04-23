---
title: Maßeinheitsumrechnungen für Produktvarianten
description: In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204492"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Maßeinheitsumrechnungen für Produktvarianten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können. Zudem enthält es ein Beispiel für die Einstellung.

Diese Funktion ermöglicht den Austausch, damit Unternehmen verschiedene Einheitenumrechnung zwischen den Varianten desselben Produkts definieren. Das folgende Beispiel wird in diesem Thema verwendet. Ein Unternehmen verkauft die T-Shirts in kleinen, mittig großen und extra-großen Größen. Das T-Shirt wird als Produkt definiert, und die verschiedenen Größen werden als Varianten des Produkts definiert. Die T-Shirts werden in Kisten verpackt und es haben fünf T-Shirts darin Platz, mit Ausnahme der extra-großen Größe, bei denen es nur Platz für vier T-Shirts gibt. Das Unternehmen möchte die verschiedenen Varianten der T-Shirts in der Einheit **Stücke** nachverfolgen aber verkauft die T-Shirts in der Einheit **Schachteln**. Die Umrechnung zwischen der Lagereinheit und der Verkaufseinheit ist eine Schachtel = 5, außer für die extra-großen, bei denen 1 Schachtel = 4 Stück ist.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Einrichten eines Produkts für Einheitenumrechnung pro Variante

ProtukVarianten können nur für Produkte von **Produkt-Untertyp** **Produktmaster** erstellt werden. Weitere Informationen finden Sie unter [Erstellen eines Produktmasters](tasks/create-product-master.md).

Die Funktion ist nicht für Produkte aktiviert, die für Artikelgewichtsprozesse eingerichtet werden. 

Wenn der Produktmaster mit freigegebenen Produkten erstellt wird, können pro Einheitenumrechnungen Varianten eingerichtet werden. Sie können für die Menüoption das Öffnen der Einheitenumrechnungsseite im Kontext eines Produkts oder die Produktvariante auf den folgenden Seiten finden.

-   Seite **Produktdetails**
-   Seite **Details für freigegebene Produkte**
-   Seite **Varianten für freigegebenes Produkt**

Wenn Sie die Detailebene **Einheitenumrechnung** Seite im Kontext eines Untertyps "Produktmaster" oder Produktvariante öffnen, können Sie auswählen, wenn Sie die Einheitenumrechnung für das Produkt oder eine ausgewählte Produktvariante einrichten möchten. Sie gehen follgendermaßen vor, indem Sie entweder **Produktvariante** oder **Produkt** im Feld **Erstellen Sie für Umwandlungen** auswählen.

### <a name="product-variant"></a>Produktvariante

Wenn Sie **Produktvariante,** wählen, können Sie auswählen, für welche Artikelvariante Sie die Einheitenumrechnung im Feld **Produktvariante** eingerichtet werden soll.

### <a name="product"></a>Produkt

Wenn Sie **Produkt** auswählen, kann eine Einheitenumrechnung für den Produktmaster eingerichtet werden. Diese Einheitenumrechnung gilt für alle Produktvarianten ohne definierte Einheitenumrechnung.

### <a name="example"></a>Beispiel

Ein Produktmaster, **T-Shirt**, besitzt vier kleine, mittlere, große, und X-große Varianten "Freigegebene Produkte". Die T-Shirts werden in Kisten verpackt und es haben fünf T-Shirts darin Platz, mit Ausnahme der extra-großen Größe, bei denen es nur Platz für vier T-Shirts gibt.

Hiermit öffnen Sie die Seite **Einheitenumrechnung** von der Freigabenproduktdetailseite für **T-Shirt.**

Auf der Seite **Einheitenumrechnung** richten Sie die Einheitenumrechnung für die X-große Freigabenproduktvariante ein.

| **Feld**             | **Einstellung**             |
|-----------------------|-------------------------|
| Konvertierung erstellen für | Produktvariante         |
| Produktvariante       | T-Shirt: : X-groß : : |
| Von Einheit             | Schachteln                   |
| Faktor                | 4                       |
| In Einheit               | Stücke                  |

Die freigegebenen Produktvarianten klein, mittel und groß haben dieselbe Einheitenumrechnung zwischen dem Feld Einheit und Stück, was bedeutet, dass Sie die Einheitenumrechnung für die Produktvarianten im Produktmaster definieren können.

| **Feld**             | **Einstellung** |
|-----------------------|-------------|
| Konvertierung erstellen für | Produkt     |
| Produkt               | T-Shirt     |
| Von Einheit             | Schachteln       |
| Faktor                | 5           |
| In Einheit               | Stücke      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Excel verwenden, um die Einheitenumrechnungen zu aktualisieren

Wenn ein Produkt Produktvarianten mit viele unterschiedliche Einheitenumrechnungen hat, wird empfohlen, die Seite **Einheitenumrechnung** in ein Excel-Arbeitsblatt zu exportieren, die Umrechnung zu aktualisieren und diese dann anschließend wieder in Supply Chain Mangement zu veröffentlichen.

Die Option in Excel zu exportieren und die Bearbeitung wieder zurück zu Supply Chain Mangement zu exportieren, wird aktiviert im Menü **Öffnen in Microsoft Office** im Aktivitätsbereich auf der Seite **Einheitenumrechnung**.
