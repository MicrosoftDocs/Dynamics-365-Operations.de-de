---
title: Maßeinheitsumrechnungen für Produktvarianten
description: In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 36fc98c44625cce03945d76973de67021d53353e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844368"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Maßeinheitsumrechnungen für Produktvarianten

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

In diesem Thema wird erläutert, wie Maßeinheitsumrechnungen in Produktvarianten eingerichtet werden können. Zudem enthält es ein Beispiel für die Einstellung.

Diese Funktion ermöglicht den Austausch, damit Unternehmen verschiedene Einheitenumrechnung zwischen den Varianten desselben Produkts definieren. Das folgende Beispiel wird in diesem Thema verwendet. Ein Unternehmen verkauft die T-Shirts in kleinen, mittig großen und extra-großen Größen. Das T-Shirt wird als Produkt definiert, und die verschiedenen Größen werden als Varianten des Produkts definiert. Die T-Shirts werden in Kisten verpackt und es haben fünf T-Shirts darin Platz, mit Ausnahme der extra-großen Größe, bei denen es nur Platz für vier T-Shirts gibt. Das Unternehmen möchte die verschiedenen Varianten der T-Shirts in der Einheit **Stücke** nachverfolgen aber verkauft die T-Shirts in der Einheit **Schachteln**. Die Umrechnung zwischen der Lagereinheit und der Verkaufseinheit ist eine Schachtel = 5, außer für die extra-großen, bei denen 1 Schachtel = 4 Stück ist.

## <a name="setup"></a>Einstellungen

Sie können die Parameter für die Verwendung der Funktion für die Produkte festlegen, die für **Alle Prozesse** oder nur für das Produkt aktiviert werden, das für **Lagerortprozesse** aktiviert ist, indem Sie die Option **Aktivieren Sie Maßeinheits-Unterhaltungen** auf der Seite **Produktinformationsparameter** nutzen.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Einrichten eines Produkts für Einheitenumrechnung pro Variante

ProtukVarianten können nur für Produkte von **Produkt-Untertyp** **Produktmaster** erstellt werden. Weitere Informationen finden Sie unter [Erstellen eines Produktmasters](tasks/create-product-master.md).

Die Funktion ist nicht für Produkte aktiviert, die für Artikelgewichtsprozesse eingerichtet werden. 

Während der Erstellung eines Produktmasters aktivieren Sie Maßeinheitsumrechnung, indem Sie die **Aktivieren Sie Maßeinheitsumrechnungen** auf der Seite **Produktdetails** nutzen.

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

Wenn ein Produkt Produktvarianten mit viele unterschiedliche Einheitenumrechnungen hat, wird empfohlen, die Seite **Einheitenumrechnung** in ein Excel-Arbeitsblatt zu exportieren, die Umrechnung zu aktualisieren und diese dann anschließend wieder in Finance and Operations zu veröffentlichen.

Die Option in Excel zu exportieren und die Bearbeitung wieder zurück zu Finance and Operations zu exportieren, wird aktiviert im Menü **Öffnen in Microsoft Office** im Aktivitätsbereich auf der Seite **Einheitenumrechnung**.
