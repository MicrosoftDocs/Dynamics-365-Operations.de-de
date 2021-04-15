---
title: Einzelhandelsprodukte einrichten
description: In diesem Artikel wird beschrieben, wie Produkte in Dynamics 365 Commerce eingerichtet werden.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5c8ae2f385e2e3a4d08412d9da4ab68d50496211
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795500"
---
# <a name="set-up-retail-products"></a>Einzelhandelsprodukte einrichten

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Produkte in Dynamics 365 Commerce eingerichtet werden.

Bevor Sie Produkte für den Verkauf in Ihren Commerce-Kanälen anbieten können, müssen Sie die Produkte erstellen und konfigurieren. Commerce erstellt organisationsweit Produkte im Produktmaster. Sie können die Produkte erstellen, die Produkteigenschaften und -attribute definieren sowie die Produkte den Commerce-Kategoriehierarchien zuweisen. Um die Produkte für Ihre Kanäle verfügbar zu machen und sie einem aktiven Sortiment hinzuzufügen, müssen Sie die Produkte für die juristischen Personen freigeben, in denen sie verfügbar sind. Führen Sie zum Einrichten der Produkte, die Sie über Kanäle verkaufen, die folgenden Aufgaben aus.

1. **Definieren Sie eine Produkthierarchie.** Wenn Sie die Kategoriehierarchiefunktionen in Commerce verwenden, können Sie Kategoriehierarchien definieren, um die Produkte, die Sie an Ihre Kanäle vertreiben, zu gruppieren und kategorisieren. Benutzerdefinierte und Systemattribute können auf der Kategorieebene definiert werden. Daraufhin erben alle Produkte, die der Kategorie zugewiesen sind, diese Attribute. Mehrere Kategoriehierarchien können definiert werden, und jedes Produkt kann mehreren Hierarchien zugewiesen werden. In einer einzelnen Hierarchie kann ein Produkt jedoch nur einer Kategorie zugewiesen werden.
2. **Fügen Sie Produkte und Produktvarianten zum Produktmaster hinzu.** Produkte, die dem Produktmaster hinzugefügt werden, stellen eine globale Liste von Produkten dar. Sie können Produkte manuell und einzeln hinzufügen, oder Sie können Produktdaten von Ihren Kreditoren importieren.
3. **Geben Sie die Produkte für juristische Personen frei.** Nur Produkte, die für juristische Personen freigegeben wurden, können in Ihren Kanälen verfügbar gemacht werden. Wenn Sie ein Produkt erstmals definieren, definieren Sie das Produkt auf organisationsweiter Ebene. Sie können mindestens eine juristische Person auswählen, um das Produkt freigeben. Das Produkt wird dann in mehreren Kanälen in Ihrer Organisation verfügbar. Sie können diese Funktion verwenden, um ein Produkt einmal zu erstellen, Produktattribute und -eigenschaften an einer Stelle hinzuzufügen und zu aktualisieren, und das Produkt dann Organisationsweit an die Kanäle zu vertreiben, in denen es verfügbar ist.
4. **Fügen Sie Produkte Sortimenten hinzu.** Ein Sortiment stellt eine Sammlung von Produkten dar, die Sie in Ihren Kanälen anbieten. Sie können ein oder mehrere Sortimente definieren, und jedes Produkt kann einem oder mehreren Sortimenten zugewiesen werden. Um Produkte den Kanälen zuzuweisen, weisen Sie die Sortimente diesen Kanälen zu. Wenn Sie ein Sortiment erstellen, können Sie Produkte hinzufügen, die noch nicht für eine juristische Person freigegeben wurden. Sie müssen die Produkte jedoch für eine juristische Person freigeben, bevor diese Produkte in den Kanälen verfügbar gemacht werden können.
5. **Hinzufügen von Produkten Navigationshierarchien hinzu.** Bevor Produkte online oder in Verkaufsstellen durchsucht werden können, müssen sie in einer Commerce-Navigationshierarchie kategorisiert werden.
6. **Produkte zum Katalog hinzufügen** Obwohl dieser Schritt für Verkaufsstellen optional ist, erfordern Onlineshops, dass Produkte in mindestens einem Katalog enthalten sind.


[!INCLUDE[footer-include](../includes/footer-banner.md)]