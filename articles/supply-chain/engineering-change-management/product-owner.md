---
title: Produkteigentümer
description: Dieses Thema enthält Informationen über Produktbesitzer. Ein Produktbesitzer ist eine Gruppe von Benutzern, die für bestimmte Produkte verantwortlich sind. Nur Mitglieder der Gruppe können diese Produkte freigeben. Der Besitzer eines Produkts kann auch im Genehmigungs-Workflow verwendet werden.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4de6399f83eeb0b0e1ea6fb13e86fb6dca456ff1c9b113e024afec97cc5b68af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766726"
---
# <a name="product-owners"></a>Produkteigentümer

[!include [banner](../includes/banner.md)]

Der Produktbesitzer ist eine Gruppe von Benutzern, die für bestimmte Produkte verantwortlich sind. Wenn eine Gruppe von Produktbesitzern einem Produkt zugewiesen ist, können nur die Mitglieder dieser Gruppe das Produkt freigeben. Der Produktbesitzer kann auch im Genehmigungs-Workflow in der Verwaltung für technische Änderungen verwendet werden.

Produktbesitzer sind globale Einstellungen. Sie sind daher für alle juristischen Entitäten verfügbar.

## <a name="create-a-product-owner-group"></a>Erstellen einer Gruppe von Produktbesitzern

Gehen Sie folgendermaßen vor, um eine Gruppe von Produktbesitzern zu erstellen und ihr Mitglieder hinzuzufügen.

1. Gehen Sie zu **Verwaltung für technische Änderungen \> Einrichten \> Produktbesitzer**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie in das Feld **Produktbesitzer** einen Namen für die Gruppe ein.
4. Geben Sie in das Feld **Name** eine Beschreibung für die Gruppe ein.
5. Fügen Sie auf dem Inforegister **Mitglieder** die Arbeitskräfte hinzu, die Mitglieder der Gruppe sein sollen.

## <a name="assign-a-product-owner-to-a-product"></a>Zuweisen eines Besitzers zu einem Produkt

Um einem Produkt einen Besitzer zuzuweisen, gehen Sie folgendermaßen vor.

1. Öffnen Sie die Seite **Produktdetails** für das betreffende Produkt oder den Produktstamm.
1. Legen Sie auf dem Inforegister **Allgemein** das Feld **Produktbesitzer** auf den Namen der entsprechenden Gruppe von Produktbesitzern fest.

Während ein Produktbesitzer einem Produkt zugewiesen ist, können nur die Mitglieder der Produktbesitzer-Gruppe die Einstellung **Produktbesitzer** bearbeiten.

Der Besitzer des Produkts ist auch auf der Seite **Freigegebene Produkte** sichtbar.

## <a name="product-owners-and-product-releases"></a>Produktbesitzer und Produktfreigaben

Nur Benutzer aus der Gruppe der Besitzer eines Produkts können dieses Produkt freigeben. Es gibt jedoch eine Ausnahme, wenn das Produkt ein untergeordnetes Element ist und sein übergeordnetes Element vom Besitzer des übergeordneten Elements freigegeben wird. Mit anderen Worten: Wenn das Produkt Teil der Stückliste eines anderen Produkts ist, prüft das System nicht den Besitzer jedes Elements in der Stückliste. Es prüft nur den Besitzer des übergeordneten Elements.

Beispiel: Produkt X ist der Eigentümergruppe *Designschränke* zugewiesen. Produkt X ist auch Teil der Stückliste von Produkt Y, das der Produktbesitzer-Gruppe *Design Speakers* zugeordnet ist. Wenn ein Benutzer aus der Produktbesitzer-Gruppe *Design Speakers* das Produkt Y und dessen Stückliste freigibt, wird das Produkt X zusammen mit dem Produkt Y freigegeben.

## <a name="product-owners-and-approvals"></a>Produktbesitzer und Freigaben

Da die Besitzer der Produkte wissen, ob bestimmte technische Änderungen für ihre Produkte von Vorteil sind, ist es oft sinnvoll, sie als Teil des Genehmigungsprozesses in die Verwaltung für technische Änderungen einzubeziehen. Sie können diesen Ansatz implementieren, indem Sie die Besitzer der Produkte als Teilnehmer in den Workflows festlegen, die für die Verwaltung für technische Änderungen verwendet werden. Das System weist dann Genehmigungsaufgaben in den Workflows zu, basierend auf den Produkten, die in Änderungsanträgen und Änderungsaufträgen enthalten sind. Weitere Informationen finden Sie unter [Verwalten von Änderungen an Engineering-Produkten](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]