---
title: Einrichten von Sortimenten
description: Dieser Artikel beschreibt, was ein Sortiment ist, und erläutert, wie Sie Sortimente in Dynamics 365 Commerce einrichten.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26614d319453041177e8072793f09f52ebfd51fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412664"
---
# <a name="set-up-assortments"></a>Sortimente einrichten

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt, was ein Sortiment ist, und erläutert, wie Sie Sortimente in Dynamics 365 Commerce einrichten.

Ein Sortiment ist eine Sammlung zugehöriger Produkte, die einem Commerce-Kanal, wie einem physischen Laden oder einem Onlineshop, zugewiesen werden. Sie verwenden Sortimente, um die Produkte zu erkennen, die in jedem Shop verfügbar sind. Ein Sortiment kann Produktgruppen enthalten. Daher werden alle Produkte, die einer bestimmten Kategorie zugeordnet sind, ins Sortiment eingeschlossen. Ein Sortiment kann außerdem bestimmte Produkte und bestimmte Varianten von Produkten enthalten. Wenn Sie ein Sortiment einrichten, können Sie Tausende von Produkten für Ihre Kanäle in beliebigen Kombinationen, die Ihre Shops erfordern, gleichzeitig zuordnen. Sie können so viele Sortimente einrichten, wie Sie benötigen. Jedes Produkt kann einem oder mehreren Sortimenten hinzugefügt werden, und jedes Sortiment kann einem oder mehreren Kanälen zugewiesen werden. Sie definieren z. B. ein Sortiment, das einen Basissatz an Produkten enthält. Alle Filialen erhalten dieses Sortiment. Sie können dann ein anderes Sortiment definieren, das nur große Sportausrüstung enthält. Nur die größeren Filialen erhalten dieses Sortiment. Das folgende Diagramm zeigt, wie Produkte Sortimenten zugewiesen werden können und wie diese Sortimente Kanälen zugewiesen werden können.

![Produktsortimentbeziehungen](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie ein Sortiment einrichten und dieses einem Commerce-Kanal zuweisen können, müssen Sie die folgenden Aufgaben abschließen.

| Aufgabe                              | Beschreibung |
|-----------------------------------|-------------|
| Einen Kanal einrichten.          | Kanäle stellen einen physischen Laden, einen Onlineshop oder einen Onlinemarktplatz dar. Sie müssen mindestens einen Kanal festlegen und die Optionen für den Shop konfigurieren. Sortimente werden den Filialen zugewiesen, um die Produkte zu erkennen, die eine bestimmte Filiale führt. |
| Dient zum Erstellen einer Organisationshierarchie. | Nachdem Sie die Commerce-Kanäle für Ihre Organisation eingerichtet haben, müssen Sie eine Organisationshierarchie konfigurieren, die die Organisationsstruktur Ihrer Kanäle darstellt. Eine Organisationshierarchie kann für Sortimente, Auffüllung und Berichterstellung verwendet werden. Indem Sie die Kanäle zu einer Organisationshierarchie hinzufügen, können Sie Sortimente Gruppen von Shops zuordnen. Anstatt das Sortiment zu jedem Shop einzeln zuzuordnen, weisen Sie das Sortiment dem allgemeinen Organisationsknoten zu. Wenn anschließend ein neuer Kanal dem übergeordneten Organisationsknoten hinzugefügt wird, werden diesem Kanal automatisch alle Sortimente zugewiesen, die dem übergeordneten Organisationsknoten zugeordnet waren. Sie können Sortimente nur Kanälen zuweisen, die in einer Organisationshierarchie eingeschlossen sind, die dem **Commerce-Sortiment** zugewiesen ist. |
| Produkte definieren.                  | Bevor Sie Produkte einem Sortiment hinzufügen können, müssen Sie sie in Commerce hinzufügen. Sie können auch Produkte manuell hinzufügen oder von einem Lieferanten importieren. Nachdem Sie die Produkte hinzufügen, müssen Sie diese einer juristischen Person freigeben. Nur Produkte, die für eine juristische Person freigegeben wurden, können in Ihren Kanälen verfügbar gemacht werden. Produkte, die noch nicht für eine juristische Person freigegeben wurden, können einem Sortiment hinzugefügt werden, und das Sortiment kann genehmigt werden. Bis jedoch die Produkte für eine juristische Person freigegeben wurden, können sie nicht den Kanälen verfügbar gemacht werden. |
| Einrichten einer Kategoriehierarchie.      | Wenn Sie Ihre Commerce-Produkte erstellen, können Sie diese gruppieren und kategorisieren, indem Sie die Kategoriehierarchiefunktion verwenden. Sie können eine Kernhierarchie erstellen, um alle Produkte zu gruppieren und zu kategorisieren, die Sie über Ihre Kanäle vertreiben. Sie können auch einzelnen, zusätzliche Kategoriehierarchien erstellen, um die Produkte zu bestimmten Kostenträgern, wie verkaufsfördernden Maßnahmen oder Sortimente, zu gruppieren oder kategorisieren. Wenn Sie Kategoriehierarchien verwenden, können Sie alle die Produkte in einer bestimmten Kategorie einem Sortiment zuweisen. Alle Produkte, die der Kategorie hinzugefügt werden, die im Sortiment enthalten ist, werden automatisch ins Sortiment einbezogen. Beim nächsten Ausführen des Commerce-Sortimentplaners werden diese Produkte dann für die Kanäle verfügbar gemacht, denen das Sortiment zugeordnet ist. |

## <a name="setting-up-an-assortment"></a>Einrichten eines Sortiments

Nachdem Sie die Voraussetzungen abgeschlossen haben, können Sie ein Sortiment erstellen und es Ihren Kanälen zuweisen. Zum Einrichten eines Sortiments müssen folgende Aufgaben ausgeführt werden.

1. Erstellen Sie ein neues Sortiment, oder kopieren Sie ein vorhandenes Sortiment.
2. Wählen Sie die Kanäle oder die übergeordneten Gruppen von Kanälen aus, für die das Sortiment gilt.
3. Fügen Sie Produktkategorien, Einzelprodukte oder Produktvarianten dem Sortiment hinzu. Sie können alle Produkte in einer bestimmten Kategorie einschließen oder Sie können bestimmte Produkte aus einer Kategorie ausschließen, die im Sortiment enthalten ist.
4. Veröffentlichen Sie das Sortiment. Wenn Sie ein Sortiment veröffentlichen, wird der Sortimentplaner automatisch ausgeführt. Dieser Vorgang generiert die Liste der Produkte. Wenn dieser Prozess abgeschlossen ist, werden die Produkte für die Kanäle verfügbar gemacht, denen das Produktsortiment zugeordnet ist. Wenn Änderungen an einem Sortiment vorgenommen werden, das veröffentlicht wurde, oder an den Kanälen, denen das Sortiment zugeordnet ist, muss das Sortiment aktualisiert werden. Um das Sortiment zu aktualisieren wenn Änderungen vorgenommen wurden, können Sie den Sortimentplaner als Batchauftrag ausführen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]