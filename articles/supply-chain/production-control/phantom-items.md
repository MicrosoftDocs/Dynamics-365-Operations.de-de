---
title: Phantomartikel
description: In diesem Artikel wird beschrieben, wie der Positionstyp „Phantom“ für die Positionen einer Stückliste (BOM) und die Formel in Dynamics 365 Supply Chain Management verwendet werden kann.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 64139873216decd8ecb2fcaf1f284e726c53c332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893322"
---
# <a name="phantom-items"></a>Phantomartikel

[!include [banner](../includes/banner.md)]

In diesem Artikel wird ausführlich beschrieben, wie der Positionstyp "Phantom" für die Positionen einer Stückliste (BOM) und die Formel verwendet werden kann.

In Abbildung 1 ist (a) die Stückliste für Produkt H und Teile F und G und (b) ist der Arbeitsplan für Produkte H und Teil F.

![Abbildung 1: Entwicklungsstückliste.](media/product-H-part-F.png)
*Abbildung 1: Entwicklungsstückliste*

Abbildung 1 zeigt ein Beispiel einer Stückliste auf zwei Ebenen. Produkt H stellt ein Produkt für eine Maschinenzusammenstellung dar. Die Maschinenmontage besteht aus zwei Teilen, einer elektrische Einheit (F), die zwei Materialien hat (A und B) und eine Gruppe Verpackungsmaterialien (G), die auch zwei Materialien hat (C und D). Ein anderes Material (E) wird bei der allgemeinen Zusammenstellung der Maschine verwendet.

Abbildung 1 zeigt die Entwicklungsstückliste für Produkt H. Diese Struktur bietet einen guten Überblick der Teile und Komponenten der gesamten Maschinenmontage. Aber Produktdesigner ziehen es möglicherweise vor, die Stückliste so zu sehen und diese Struktur wird vielleicht nicht korrekt so dargestellt, wie die Maschine im Fertigungsbereich erstellt wird.

Beispielsweise zeigt die Entwicklungsstückliste in Abbildung 1, dass das elektrische Einzelteil F als separater Teil auf einem separaten Arbeitsauftrag zusammengestellt wird. Allerdings kann es im Fertigungsbereich möglicherweise optimaler beurteilt werden, die elektrische Einheit im Rahmen der Gesamtmaschinenzusammenstellung und nicht als separaten Arbeitsauftrag zu verwenden.

Diese Konstruktionsstückliste gibt auch an, dass Teil G ein separater Teil ist. Allerdings ist in dieser Struktur Teil G nicht ein physisches Teil, sondern eine Zusammenstellung von Verpackungsmaterialien.

Auch wenn eine Konstruktionsstückliste möglicherweise einen hohen Wert für den Entwurf eines Produkts sowie der Verwaltung dieses Designs bereitstellt, ist er möglicherweise nicht die logischste Möglichkeit, den Fertigungssteuerungsprozess des Produkts zu unterstützen. Möglicherweise stellt die Produktions-Stückliste die beste Methode dar, ein Produkt zu erstellen.

Abbildung 2 zeigt, wie die vorhergehende Entwicklungsstückliste in eine Produktionsstückliste übergeleitet wird. In Abbildung 2 ist (a) die Stückliste für Produkt H und (b) ist der Arbeitsplan für Produkt H.

![Abbildung 2: Fertigungsstückliste.](media/product-H-part-B.png)
*Abbildung 2: Fertigungsstückliste*

In dieser Struktur wird angezeigt, dass es keinen Hinweis von Teilen F und G gibt und das Material, das aus diesen Teile besteht, wurde auf die folgenden Stücklistenebene gehoben.

Im Gegensatz zur Konstruktionsstückliste, die zwei Arbeitskarten hatte, hat die Produktionsstückliste nur eine Arbeitskarte. Der Verpackungsarbeitsgang, der mit Teil G verknüpft war, wurde ebenfalls erhöht und ist nun Teil der Arbeitskarte für Produkt H. Die Zusammenstellung der elektrische Einheit ist der erste Arbeitsgang. Dieser Auftrag ergibt Sinn, weil diese Einheit im folgenden Arbeitsgang verwendet wird, der die Maschinenzusammenstellung ist. Der letzte Arbeitsgang ist der Verpackungsarbeitsgang, der zwei Verpackungsmaterialien verbraucht (C und D).

Der Übergang zwischen der Konstruktionsstückliste und der Produktionsstückliste wird durch den Stücklistenpositionstyp Phantom ermöglicht. Während die Bedingung" Phantom" angegeben wird, sind die Komponenten F und G während des Übergangs zwischen den zwei Stücklistentypen verschwunden. In diesem Beispiel wird der Positionstyps "Phantom" für die Stücklistenpositionen für Teile F und G in der Konstruktionsstückliste angewendet. Wenn ein Produktions- oder Chargenauftrag erstellt wird, wird die Konstruktionsstückliste in die Produktionsstückliste oder den Chargenauftrag kopiert. Wird der Auftrag vorkalkuliert, erfolgt der Übergang von der Konstruktionsstückliste zur Produktionsstückliste wie in Abbildung 2 dargestellt. Auf der Arbeitskarte in Abbildung 2 werden die Verpackungsmaterialien C und D als Input für den Arbeitsgang eingegeben.

## <a name="multilevel-phantom-bom-structures"></a>Mehrstufige Phantomstücklistenstrukturen

Der Positionstyps „Phantom“ kann in mehrstufigen Stücklistenstrukturen wie in Abbildung 3 dargestellt verwendet werden. In Abbildung 3 ist (a) die Stückliste für Produkt G und (b) ist der Arbeitsplan für Teile E und F und Produkt G.

![Abbildung 3: Entwicklungsstückliste Teil G.](media/product-G.png)
*Abbildung 3: Entwicklungsstückliste Teil G*

Abbildung 4 zeigt die resultierende Fertigungsstückliste und den Arbeitsplan, wenn die Stücklistenpositionen für Teile E und F konfiguriert werden, sodass der Positionstyp „Phantom“ ist. In Abbildung 4 ist (a) die Stückliste für Produkt G und (b) ist der Arbeitsplan für Produkt G.

![Abbildung 4: Fertigungsstückliste Teil G.](media/product-G-route-sheet-G.png)
*Abbildung 4: Fertigungsstückliste Teil G*

## <a name="phantom-and-route-network"></a>Phantom und Arbeitsplan-Netzwerk

Phantomstücklisten können für eine Stückliste verwendet werden, die auch ein Arbeitsplan-Netzwerk haben. In einem Arbeitsplannetzwerk können eine oder mehrere Arbeitsgänge gleichzeitig ausgeführt werden. Abbildung 5 zeigt ein Beispiel eines Routennetzes an, das in einer mehrere Ebenen umfassenden Stückliste verwendet wird. In Abbildung 5 ist (a) die Stückliste für Produkt G und Teil F und (b) ist der Arbeitsplan für Produkt G und Teil F, die ein Arbeitsplannetzwerk haben.

![Abbildung 5: Konstruktionsstückliste Teil G, Arbeitsplannetzwerk.](media/product-G-part-F.png)
*Abbildung 5: Konstruktionsstückliste Teil G, Arbeitsplannetzwerk*

In Abbildung 6 ist (a) die Stückliste für Produkt G und Teil F und (b) ist der Arbeitsplan für Produkt G und Teil F.

![Abbildung 6: Fertigungsstückliste Teil G, Arbeitsplannetzwerk.](media/product-G-part-F-with-route-sheet.png)
*Abbildung 6: Fertigungsstückliste Teil G, Arbeitsplannetzwerk*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]