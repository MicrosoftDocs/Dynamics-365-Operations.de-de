---
title: Einrichten von Sortimenten
description: "In diesem Artikel wird beschrieben, was ein Sortiment ist, und es wird beschrieben, wie Sie Sortimente in Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge eingerichtet."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 906fc6eb42eb54cb3a3d5621377f250f59de20d7
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-assortments"></a>Einrichten von Sortimenten

In diesem Artikel wird beschrieben, was ein Sortiment ist, und es wird beschrieben, wie Sie Sortimente in Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge eingerichtet.

Ein Sortiment ist eine Sammlung von zugehörigen Produkte, die an einem Einzelhandelskanal, wie einem physischen Filiale oder einen Onlineshop zuweisen. Sie verwenden Sortimente, um die Produkte zu erkennen, die in jedem Shop verfügbar sind. Ein Sortiment kann Produktgruppen enthalten. Daher werden alle Produkte, die einer bestimmten Kategorie zugeordnet sind, ins Sortiment eingeschlossen. Ein Sortiment kann außerdem bestimmte Produkte und bestimmte Varianten von Produkten enthalten. Wenn Sie ein Sortiment einrichten, können Sie Tausende von Produkten für Ihre Einzelhandelskanälen gleichzeitig zuweisen, in beliebigen Kombinationen, die Ihre Shops erfordern. Sie können so viele Sortimente einrichten, wie Sie benötigen. Jedes Produkt kann einem oder mehreren Sortimenten hinzugefügt werden, und jedes Sortiment kann zu einem oder mehreren Einzelhandelskanälen zugewiesen werden. Sie definieren z. B. ein Sortiment, das einen Basissatz an Produkten enthält. Alle Filialen erhalten dieses Sortiment. Sie können dann ein anderes Sortiment definieren, das nur große Sportausrüstung enthält. Nur die größeren Filialen erhalten dieses Sortiment. Das folgende Diagramm zeigt, wie Produkte Sortimenten zugewiesen werden können und wie diese Sortimente Einzelhandelskanälen zugewiesen werden können. ![Produktsortimentbeziehungen](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Erforderliche Komponenten
Bevor Sie ein Sortiment einrichten und dieses einem Einzelhandelskanal zuweisen können, müssen Sie die folgenden Aufgaben ausführen.

| Aufgabe                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einrichten eines Einzelhandelskanals.          | Einzelhandelskanäle stellen einen physischen Laden, einen Onlineshop oder einen Onlinemarktplatz dar. Sie müssen mindestens einen Einzelhandelskanal festlegen und Optionen für die Filiale konfigurieren. Sortimente werden den Filialen zugewiesen, um die Produkte zu erkennen, die eine bestimmte Filiale führt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Dient zum Erstellen einer Organisationshierarchie. | Nachdem Sie die Einzelhandelskanäle für Ihre Organisation eingerichtet haben, müssen Sie eine Einzelhandels-Organisationshierarchie konfigurieren, die die Organisationsstruktur der Einzelhandelskanäle darstellt. Eine Organisationshierarchie kann für Sortimente, Auffüllung und Berichterstellung verwendet werden. Wenn Sie die Einzelhandelskanäle zu einer Organisationshierarchie hinzufügen, können Sie Sortimente den Gruppen von Filialen zuordnen. Anstatt das Sortiment zu jedem Shop einzeln zuzuordnen, weisen Sie das Sortiment dem allgemeinen Organisationsknoten zu. Wenn anschließend ein neuer Einzelhandelskanal dem allgemeinen Organisationsknoten hinzugefügt wird, werden diesem Einzelhandelskanal automatisch alle Sortimente zugewiesen, die dem Organisationsknoten höherer Ebene zugeordnet waren. Sie können Sortimente nur Einzelhandelskanälen zuweisen, die in einer Organisationshierarchie eingeschlossen sind, der der Kostenträger **Einzelhandelssortiment** zugewiesen ist. |
| Produkte definieren.                  | Bevor Sie Produkte einem Sortiment hinzufügen können, müssen Sie sie in Microsoft Dynamics AX hinzufügen. Sie können auch Produkte manuell hinzufügen oder von einem Lieferanten importieren. Nachdem Sie die Produkte hinzufügen, müssen Sie diese einer juristischen Person freigeben. Nur Produkte, die für eine juristische Person freigegeben wurden, können den Einzelhandelskanälen verfügbar gemacht werden. Produkte, die noch nicht für eine juristische Person freigegeben wurden, können einem Sortiment hinzugefügt werden, und das Sortiment kann genehmigt werden. Bis jedoch die Produkte für eine juristische Person freigegeben wurden, können sie nicht den Einzelhandelskanälen verfügbar gemacht werden.                                                                                                                                                                                                                                                                                     |
| Einrichten einer Kategoriehierarchie.      | Wenn Sie Ihre Einzelhandelsprodukte erstellen, können der Gruppierung und kategorisiert, indem Sie die Kategoriehierarchiefunktion in Dynamics 365 für Arbeitsgänge verwenden. Sie können eine Kernhierarchie erstellen, um alle Produkte zu gruppieren und zu kategorisieren, die Sie über die Einzelhandelskanäle vertreiben. Sie können auch einzelnen, zusätzliche Kategoriehierarchien erstellen, um die Produkte zu bestimmten Kostenträgern, wie verkaufsfördernden Maßnahmen oder Sortimente, zu gruppieren oder kategorisieren. Wenn Sie Kategoriehierarchien verwenden, können Sie alle die Produkte in einer bestimmten Kategorie einem Sortiment zuweisen. Alle Produkte, die der Kategorie hinzugefügt werden, die im Sortiment enthalten ist, werden automatisch ins Sortiment einbezogen. Anschließend wird beim nächsten Ausführen des Einzelhandelssortimentplaners diese Produkte für die Einzelhandelskanäle verfügbar gemacht, denen das Sortiment zugeordnet ist.                                            |

## <a name="setting-up-an-assortment"></a>Einrichten eines Sortiments
Nachdem Sie die Voraussetzungen abgeschlossen haben, können Sie ein Sortiment erstellen und es den Einzelhandelskanälen zuweisen. Zum Einrichten eines Sortiments müssen folgende Aufgaben ausgeführt werden.

1.  Erstellen Sie ein neues Sortiment, oder kopieren Sie ein vorhandenes Sortiment.
2.  Wählen Sie die Einzelhandelskanäle oder die allgemeinen Gruppen von Einzelhandelskanälen aus, für die das Sortiment gilt.
3.  Fügen Sie Produktkategorien, Einzelprodukte oder Produktvarianten dem Sortiment hinzu. Sie können alle Produkte in einer bestimmten Kategorie einschließen oder Sie können bestimmte Produkte aus einer Kategorie ausschließen, die im Sortiment enthalten ist.
4.  Veröffentlichen Sie das Sortiment. Wenn Sie ein Sortiment veröffentlichen, wird der Einzelhandelssortimentplaner automatisch ausgeführt. Dieser Vorgang generiert die Liste der Produkte. Wenn dieser Prozess abgeschlossen ist, werden die Produkte für die Einzelhandelskanäle verfügbar gemacht, denen das Produktsortiment zugeordnet ist. Wenn Änderungen an einem Sortiment vorgenommen werden, das veröffentlicht wurde, oder am dem Einzelhandelskanälen, denen das Sortiment zugeordnet ist, muss das Sortiment aktualisiert werden. Um das Sortiment aktualisieren wenn Änderungen vorgenommen wurden, können Sie den Einzelhandelssortimentplaner Chargenauftrag ausführen.



