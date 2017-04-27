---
title: Attribute erstellen und verwalten
description: "Dieser Artikel beschreibt Attribute in Microsoft Dynamics 365 for Operations. Mit Attributen können Sie ein Produkt und die Merkmale mit benutzerdefinierten Feldern beschreiben."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Attribute erstellen und verwalten

Dieser Artikel beschreibt Attribute in Microsoft Dynamics 365 for Operations. Mit Attributen können Sie ein Produkt und die Merkmale mit benutzerdefinierten Feldern beschreiben.

Mit Attributen können Sie ein Produkt und die Merkmale mit benutzerdefinierten Feldern beschreiben. So können Sie die Speichergröße Produkts sowie die Festplattenkapazität angeben und ob das Produkt "Energy Star"-konform ist. Attribute können unterschiedlichen Einzelhandelsentitäten zugeordnet werden, wie Produktkategorien und Einzelhandelskanäle, und Standardwerte können für sie festgelegt werden. Produkte erben deren Attribute und Standardwerte für diese Attribute, wenn sie Produktkategorien oder Einzelhandelskanälen zugeordnet sind. Die Standardwerte können auf der Einzelproduktebene, Einzelhandelskanalebene oder in einem Einzelhandelskatalog überschrieben werden.

#### <a name="examples"></a>Beispiele

Kategorie

Attribut

Zulässige Werte

Standardwert

TV & Video

Marke

Jeder gültige **Marke**-Wert

Keine

TV

Bildschirmgröße

**20"**–**80"**

Keine

Vertikale Auflösung

**480i**, **720p**, **1080i** oder **1080p**

**1080p**

Bildschirm-Aktualisierungsrate

**60 Hz**, **120 Hz** oder **240 Hz**

**60 Hz**

HDMI-Eingaben

**0**–**10**

**3**

DVI-Eingaben

**0**–**10**

**1**

Zusammengesetzte Eingaben

**0**–**10**

**2**

Komponenten-Eingaben

**0**–**10**

**1**

LCD

3D-fähig

**Ja** oder **Nein**

**Ja**

3D-aktiviert

**Ja** oder **Nein**

**Nein**

Plasma

Betriebstemperatur von

**32**–**110** Grad

**32**

Betriebstemperatur bis

**32**–**110** Grad

**100**

Projektion

Projektionstubus-Garantie

**6**, **12** oder **18** Monate

**12**

\# des Projektionstubus

**1**–**5**

**3**

## <a name="attribute-type"></a>Attributtyp
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) Attribute basieren auf Attributarten Attributtypen identifizieren die Art von Daten, die für ein bestimmtes Attribut eingegeben werden können. Derzeit unterstützt Microsoft Dynamics 365 für Operations die folgenden Attributtypen:

-   **Währung** – Dieser Attributtyp unterstützt Währungswerte. Er kann begrenzt (das heißt, kann er einen Wertebereich unterstützen) oder offengelassen werden.
-   **DateTime** – Dieser Attributtyp unterstützt Datums- und Uhrzeitwerte. Er kann begrenzt (das heißt, kann er einen Wertebereich unterstützen) oder offengelassen werden.
-   **Dezimal** – Dieser Attributtyp unterstützt numerische Werte, die Dezimalstellen enthalten. Er unterstützt auch Maßeinheiten. Er kann begrenzt (das heißt, kann er einen Wertebereich unterstützen) oder offengelassen werden.
-   **Ganzzahl** – Dieser Attributtyp unterstützt numerische Werte. Er unterstützt auch Maßeinheiten. Er kann begrenzt (das heißt, kann er einen Wertebereich unterstützen) oder offengelassen werden.
-   **Text** – Dieser Attributtyp unterstützt Textwerte. Er unterstützt auch einen vordefinierten Satz möglicher Werte (Aufzählung).
-   **Boolesch** – Dieser Attributtyp unterstützt Binärwerte (**true**/**false**).
-   **Referenz**.

## <a name="attribute"></a>Attribut
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png)Zusätzlich zum Namen, Anzeigenamen, Beschreibung und Hilfetext kann einer oder mehrererr der folgenden Informationstypen für ein Attribut aufgezeichnet werden:

-   Standardwert
-   Attributmetadaten, wie Metadaten, die angeben, ob das Attribut gesucht, weiterentwickelt oder sortiert werden kann

## <a name="attribute-group"></a>Attributgruppe
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Nachdem Attribute definiert wurden, können sie in Attributgruppen gruppiert werden. Attributgruppen stellen Gruppierungen einzelner Attribute bereit und können Einzelhandelskategorien oder Einzelhandelskanälen zugewiesen werden.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Zuweisen von Attributgruppen zu Einzelhandelskategorien
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Eine oder mehrere Attributgruppen kann zu Kategorieknoten in der Einzelhandel-Produktkategoriehierarchie zugeordnet werden. Wenn Produkte kategorisiert wurden, erben sie die Attribute, die in den Attributgruppen enthalten sind.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Zuweisen von Attributgruppen zu Einzelhandelsgeschäften
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Eine oder mehrere Attributgruppen kann zu einem oder mehreren Einzelhandelsgeschäften in der Einzelhandelsgeschäftshierarchie zugeordnet werden. Wenn Produkte für bestimmte Einzelhandelsgeschäfte erweitert wurden, erben sie die Attribute, die in den Attributgruppen enthalten sind.

## <a name="overriding-attribute-values"></a>Überschreiben von Attributwerten
### <a name="at-the-product-level"></a>Auf der Produktebene

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Die Standardwerte von Attributen können auf der Produktebene (das heißt, für einzelne Produkte) überschrieben werden.

### <a name="in-a-retail-catalog"></a>In einem Einzelhandelskatalog

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Die Standardwerte von Attributen können für einzelne Produkte in bestimmten Katalogen überschrieben werden, die für bestimmte Einzelhandelskanäle ausgerichtet werden.

### <a name="at-the-retail-channel-level"></a>Auf der Einzelhandelskanalebene

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Die Standardwerte von Attributen können für einzelne Produkte in bestimmten Katalogen überschrieben werden, die für bestimmte Einzelhandelskanäle ausgerichtet werden.


