---
title: Technische Attribute und Suche nach technischen Attributen
description: In diesem Thema wird erklärt, wie Sie Engineering-Attribute verwenden können, um alle Nicht-Standard-Merkmale zu spezifizieren, um sicherzustellen, dass alle Produktstammdaten im System registriert werden können. Es wird auch erklärt, wie Sie die technische Attributsuche verwenden können, um Produkte anhand dieser registrierten Merkmale leicht zu finden.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: a367b95a65c45b1e7ac46e9ac96baa2417bf3e48e3d5bfeca21c82cc8c427c24
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714353"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Technische Attribute und Suche nach technischen Attributen

[!include [banner](../includes/banner.md)]

Um sicherzustellen, dass alle Produktstammdaten im System registriert werden können, sollten Sie alle Nicht-Standard-Merkmale mit technischen Attributen angeben. Sie können dann die technische Attributsuche verwenden, um Produkte auf der Basis dieser registrierten Merkmale leicht zu finden.

## <a name="engineering-attributes"></a>Entwicklungsattribute

Typischerweise haben technische Produkte viele Merkmale und Eigenschaften, die Sie erfassen müssen. Obwohl Sie einige der Eigenschaften mit Hilfe der Standard-Produktfelder registrieren können, können Sie bei Bedarf auch neue Engineering-Eigenschaften erstellen. Sie können Ihre eigenen *Technik-Attribute* definieren und sie zum Bestandteil der Produktdefinition machen.

### <a name="create-engineering-attributes-and-attribute-types"></a>Erstellen von Engineering-Attributen und Attributstypen

Jedes Engineering-Attribut muss zu einem *Attribut-Typ* gehören. Diese Anforderung besteht, weil jedes Engineering-Attribut einen *Datentyp* haben muss, der die Arten von Werten definiert, die es enthalten kann. Ein Engineering-Attribut-Typ kann ein Standard-Typ sein (z. B. Freitext, Ganzzahl oder Dezimal) oder ein benutzerdefinierter Typ (z. B. Text, der eine bestimmte Anzahl von Werten zur Auswahl hat). Sie können jeden Attributtyp mit einer beliebigen Anzahl von Engineering-Attributen wiederverwenden.

#### <a name="set-up-engineering-attribute-types"></a>Festlegen von Engineering-Attribut-Typen

Um einen Engineering-Attribut-Typ anzuzeigen, zu erstellen oder zu bearbeiten, gehen Sie wie folgt vor.

1. Gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Attribute \> Attributtypen**.
1. Wählen Sie einen vorhandenen Attributtyp im Listenbereich aus, oder wählen Sie **Neu** im Aktivitätsbereich, um einen neuen Attributtyp zu erstellen.
1. Stellen Sie die folgenden Felder ein:

    - **Attributtyp-Name** - Geben Sie einen Namen für den Attributtyp ein.
    - **Typ** - Wählen Sie einen Standard-Datentyp (*Währung*, *Datum*, *Dezimal*, *Ganzzahl*, *Text*, *Boolean*, oder *Referenz*).
    - **Feste Liste** - Diese Option ist nur verfügbar, wenn Sie das Feld **Typ** auf *Text* festgelegt haben. Legen Sie sie auf *Ja* fest, um bestimmte Werte für Attribute dieses Typs zu definieren. In diesem Fall wird eine Dropdown-Liste erstellt. Sie verwenden das Inforegister **Wert**, um die Werte festzulegen, die für diesen Attributtyp verfügbar sind. Legen Sie diese Option auf *Nein* fest, damit Benutzer einen beliebigen Wert eingeben können. In diesem Fall wird ein Eingabefeld erstellt.
    - **Wertebereich** - Diese Option ist nur verfügbar, wenn Sie das Feld **Typ** auf *Ganzzahl*, *Dezimal* oder *Währung* festlegen. Legen Sie es auf *Ja* fest, um Mindest- und Höchstwerte festzulegen, die für Attribute dieses Typs akzeptiert werden. Sie verwenden das Inforegister **Bereich**, um die Minimal- und Maximalwerte und (bei Währung) die Währung festzulegen, die für die eingegebenen Grenzen gilt. Legen Sie diese Option auf *Nein* fest, um einen beliebigen Wert zu akzeptieren. 
    - **Maßeinheit** - Dieses Feld ist nur verfügbar, wenn Sie das Feld **Typ** auf *Ganzzahl* oder *Dezimal* festlegen. Wählen Sie die Einheit der Messung, die für diesen Attributtyp gilt. Wenn keine Einheit erforderlich ist, lassen Sie dieses Feld leer.

#### <a name="set-up-engineering-attributes"></a>Festlegen von Engineering-Attributen

Um ein Engineering-Attribut anzuzeigen, zu erstellen oder zu bearbeiten, gehen Sie wie folgt vor.

1. Gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Attribute \> Entwicklungsattribute**.
1. Wählen Sie ein vorhandenes Attribut im Listenbereich oder wählen Sie **Neu** im Aktivitätsbereich, um ein neues Attribut zu erstellen.
1. Stellen Sie die folgenden Felder ein:

    - **Name** - Geben Sie einen Namen für das Attribut ein. Dieser Name erscheint nur auf der Seite **Engineering-Attribute**. Überall sonst im System wird normalerweise der Wert des Feldes **Anzeigename** angezeigt, um das Attribut zu identifizieren.
    - **Attributtyp** - Wählen Sie einen Attributtyp, den Sie im vorherigen Abschnitt definiert haben.
    - **Anzeigename** - Geben Sie einen Namen ein, der das Attribut im System identifiziert (außer auf der Seite **Engineering-Attribute**). 
    - **Beschreibung** - Geben Sie eine Beschreibung für das Attribut ein.
    - **Hilfetext** - Geben Sie einen Hilfetext ein, der anderen Benutzern erklärt, wofür das Attribut gedacht ist.
    - **Standardwert** - Geben Sie einen Standardwert für das Attribut ein. Welche Optionen angezeigt werden, hängt von dem gewählten Attributtyp ab.
    - **Währung** - Wenn der Attributtyp, den Sie ausgewählt haben, eine Währung ist, wählen Sie die Währung, in der das Attribut Werte akzeptiert und anzeigt.

1. Wenn der gewählte Attributtyp eine Ganzzahl oder ein Dezimalwert ist, wird das Inforegister **Bereich** angezeigt. Legen Sie in diesem Inforegister die folgenden Felder nach Bedarf fest:

    - **Toleranzaktion** - Wählen Sie, wie das System reagieren soll, wenn ein Benutzer einen Wert außerhalb des angegebenen Bereichs eingibt. Wenn Sie *Warnung* wählen, wird eine Warnung angezeigt, aber der Benutzer kann den Wert speichern. Wenn Sie *Nicht erlaubt* wählen, wird eine Warnung angezeigt und der Wert kann nicht gespeichert werden, bis der Benutzer ihn korrigiert.
    - **Minimum** - Geben Sie den empfohlenen oder akzeptierten Mindestwert ein.
    - **Maximum** - Geben Sie den maximalen empfohlenen oder akzeptierten Wert ein.

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Engineering-Attribute mit einer Engineering-Produktkategorie verbinden

Einige technische Attribute gelten für alle Produkte, während andere spezifisch für einzelne Produkte oder Produktkategorien sind. Zum Beispiel sind elektrische Attribute für mechanische Produkte nicht erforderlich. Daher können Sie *technische Produktkategorien* festlegen. Eine technische Produktkategorie legt die Sammlung von technischen Attributen fest, die Teil der Definition für Produkte sein müssen, die zu dieser Kategorie gehören. Sie können auch festlegen, welche Engineering-Attribute obligatorisch sind und ob es einen Standardwert gibt.

Weitere Informationen über die Arbeit mit Engineering-Produktkategorien, einschließlich Informationen darüber, wie Sie Attribute mit Kategorien verbinden, finden Sie unter [Engineering-Versionen und Engineering-Produktkategorien](engineering-versions-product-category.md).

### <a name="set-values-for-engineering-attributes"></a>Werte für Engineering-Attribute festlegen

Die Engineering-Attribute, die mit einer Engineering-Produktkategorie verbunden sind, werden angezeigt, wenn Sie ein neues Engineering-Produkt erstellen, das auf dieser Kategorie basiert. Zu diesem Zeitpunkt können Sie Werte für die Attribute festlegen. Später können diese Werte auf der Seite **Engineering-Version** oder im Rahmen der Verwaltung für technische Änderung in einem Entwicklungsänderungsauftrag geändert werden. Weitere Informationen finden Sie unter [Verwalten von Änderungen an Engineering-Produkten](engineering-change-management.md).

### <a name="create-an-engineering-product"></a>Erzeugen eines Engineering-Produkts

Um ein Engineering-Produkt zu erstellen, öffnen Sie die Seite **Freigegebene Produkte**. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Neu** die Option **Engineering-Produkt**.

Sie müssen die Engineering-Kategorie angeben, zu der das Produkt gehört. Die Kategorie legt alle Standardwerte und Merkmale für das Produkt fest. Sie legt auch die Attribute fest, die auf das Produkt anwendbar sind. Nachdem die Kategorie ausgewählt wurde, werden Werte für die Attribute festgelegt. Sie können diese Werte dann ändern.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Suche nach Produkten anhand von technischen Attributwerten

Sie können die Engineering-Attribut-Suche verwenden, um Produkte zu finden, indem Sie nach ihren Engineering-Attribut-Werten suchen. So können Sie auf einfache Weise Engineering-Produkte anhand ihrer Eigenschaften finden. Sie können in den Produkten suchen, die zu einer Engineering-Produktkategorie gehören, oder Sie können über alle Engineering-Produkte suchen.

Die Suche ist auf Produktstammdaten-Seiten und von transaktionalen Elementen im System aus verfügbar, z. B. von Aufträgen aus. Bei einem transaktionalen Element können Sie die Seite **Attributsuche Engineering** verwenden, um nach einem Produkt zu suchen. Sie können dann die Schaltfläche **Als neue Zeile hinzufügen** verwenden, um das Produkt zu den Zeilen des Verkaufsauftrags hinzuzufügen. Produkte aus den Suchergebnissen können auch direkt zum Auftrag hinzugefügt werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]