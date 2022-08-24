---
title: Neue Produkthierarchie erstellen
description: In diesem Artikel wird beschrieben, wie Sie eine neue Produkthierarchie in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 54a29381bb9231766d76b653904339d4bd60c257
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270126"
---
# <a name="create-a-new-product-hierarchy"></a>Neue Produkthierarchie erstellen


[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine neue Produkthierarchie in Microsoft Dynamics 365 Commerce erstellen.

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce unterstützt mehrere Retail Channels. Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt). Jeder Einzelhandelskanal kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten. Sie müssen alle Elemente einrichten, bevor Sie ein Ladengeschäftskanal erstellen können. 

Es wird eine Commerce-Produkthierarchie verwendet, um die Gesamtprodukthierarchie für Ihre Organisation zu definieren. Sie können eine Commerce-Produkthierarchie für den Verkauf, die Preisgestaltung und die verkaufsfördernden Maßnahmen, die Berichterstellung und die Sortimentsplanung verwenden. Pro Organisation kann nur eine Commerce-Produkthierarchie zugewiesen werden.

## <a name="create-and-configure-a-product-hierarchy"></a>Produkthierarchie erstellen und konfigurieren

Um eine Commerce-Produkthierarchie zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Commerce-Produkthierarchie**.
1. Wenn noch keine Hierarchie existiert, wählen Sie unter **Aktionsbereich** die Option **Neu**, um die Wurzel der Hierarchie zu erstellen.
1. Unter **Allgemeines**:
    1. Geben Sie im Kästchen **Name** einen Namen ein.
    1. Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.
    1. Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.
    1. Setzen Sie **Aktiv** auf **Ja**.

## <a name="add-hierarchy-nodes"></a>Hierarchieknoten hinzufügen

Gehen Sie folgendermaßen vor, um Hierarchieknoten hinzuzufügen.

1. Klicken Sie im Aktivitätsbereich auf **Kategoriehierarchie bearbeiten**.
1. Wählen Sie den übergeordneten Knoten aus, dem Sie einen neuen Knoten hinzufügen möchten, und wählen Sie dann **Neuer Kategorieknoten** aus.
1. Im Abschnitt **Allgemeines** geben Sie **Name**, **Beschreibung**, **Anzeigename** und **Schlüsselwörter** ein.
1. Unter **Allgemeines**:
    1. Geben Sie im Kästchen **Name** einen Namen ein.
    1. Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.
    1. Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.
    1. Geben Sie im Feld **Schlüsselwörter** die relevanten Schlüsselwörter ein.
    1. Geben Sie im Feld **Anzeigereihenfolge** eine Anzeigereihenfolge ein (optional).
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wiederholen Sie die obigen Schritte, um weitere Knoten hinzuzufügen.

Das folgende Bild zeigt die Erstellung eines neuen Produkthierarchieknotens an.

![Produkthierarchie erstellen.](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Andere Einstellungen

Bei Bedarf können jeder Gruppe auch Kategorieattributgruppen zugewiesen werden.  

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hierarchien in Commerce](retail-hierarchies.md)

[Produktkategorien und Produkte verwalten ](category-management-product-creation.md)

[Sortierreihenfolge für Verkaufsentitäten ändern](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
