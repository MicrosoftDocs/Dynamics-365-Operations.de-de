---
title: Sortimentsverwaltung
description: In diesem Thema werden die grundlegende Begriffe der Sortimentsverwaltung in Dynamics 365 Commerce erläutert und die Implementierungsüberlegungen für Ihr Projekt zur Verfügung gestellt.
author: jblucher
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: 74df8ac27c2028582b8909db0a7260b9b0ed38f5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797280"
---
# <a name="assortment-management"></a>Sortimentsverwaltung

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce stellt *Sortimente* bereit, mit denen Sie die Produktverfügbarkeit in Kanälen verwalten können. Sortimente bestimmen, welche Produkte für bestimmte Shops und für einen bestimmten Zeitraum verfügbar sind.

In Commerce ist ein Sortiment eine Zuordnung eines oder mehrerer Kanäle oder Gruppen von Kanälen, wenn Organisationshierarchien verwendet werden (oder Gruppen von Produkten, wenn Kategoriehierarchien verwendet werden).

Die Gesamtgesamtproduktion eines Kanals wird durch die veröffentlichten Sortimente bestimmt, die dem Kanal zugeordnet werden. Daher können mehrere aktive Sortimente pro Kanal konfigurieren werden.

### <a name="basic-assortment-setup"></a>Grundsortimentseinstellung

Im folgenden Beispiel wird ein eindeutiges Sortiment für jeden Shop konfiguriert. In diesem Fall steht nur Produkt 1 im Shop 1 zur Verfügung und nur Produkt 2 ist in Shop verfügbar.

![Jedem Produkt ist in einem Shop verfügbar](./media/Managing-assortments-figure1.png)

Um Produkt 2 bereitzustellen im Shop 1 können Sie das Produkt für Sortiment 1 hinzufügen.

![Produkt 2 zu Sortiment 1 hinzugefügt](./media/Managing-assortments-figure2.png)

Alternativ können Sie Shop 1 Sortiment. 2 hinzufügen.

![Shop 1 zu Sortiment 2 hinzugefügt](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organisationshierarchien

In den folgenden Situationen, in denen mehrere Kanäle denselben Sortimenten freigeben sind, können Sie die Sortimente konfigurieren, indem Sie die Sortimentsorganisationshierarchie in Commerce verwenden. Wenn Knoten dieser Hierarchie hinzugefügt werden, sind alle Kanäle in diesem Knoten und untergenordneten Knoten enthalten.

![Organisationshierarchie](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Produktkategorien

Ebenso auf der Produktseite können Sie Gruppen von Produkten einbeziehen, indem Sie die Produktkategorie Hierarchien verwenden. Alternativ können Sie auch Sortimente konfigurieren, indem Sie mindestens einen Kategoriehierarchieknoten einbeziehen. In diesem Fall schließt das Sortiment alle Produkte in diesem Kategorieknoten sowie deren zugrunde liegenden Knoten ein.

![Produktkategorien](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Ausgeschlossene Produkte oder Kategorien

Zusätzlich zum Einschließen von Produkten und der Kategorien in Sortimenten können Sie die Ausschließungsoption verwenden, um bestimmte Produkte oder Kategorien zu definieren, die von Sortimenten ausgeschlossen werden sollen. Im folgenden Beispiel möchten Sie alle Produkte in einer bestimmten Kategorie, mit Ausnahme von Produkt 2 einbeziehen. In diesem Fall müssen Sie das Sortimentsproduktnebenprodukt nicht definieren oder zusätzliche Kategorieknoten erstellen. Stattdessen können Sie die Kategorie ein- aber das Produkt ausschließen.

> [!NOTE]
> Wenn ein Produkt in einem oder mehreren Sortimenten nach Definition eingeschlossen und ausgeschlossen ist, gilt das Produkt immer als nicht berücksichtigt.

![Ausgeschlossenes Produkt](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Globale und freigegebene Produkte

Sortimente werden auf globaler Ebene definiert und können Kanäle von mehreren juristischen Personen anzeigen. Die Produkte und Kategorien, die in Sortimenten enthalten sind, werden ebenfalls über juristische Personen freigegeben. Ein Produkt muss jedoch freigegeben werden, bevor es tatsächlich im Kanal verkauft, bestellt oder empfangen wird, berechnet werden oder empfangen werden kann (beispielsweise in der Verkaufsstelle \[POS\]). Daher obwohl zwei Shops in verschiedenen juristischen Personen gemeinsam ein Sortiment nutzen können, das die gleichen Produkte enthält, werden die Produkte nur verfügbar, wenn es an diesen juristischen Personen freigegeben wurden.

### <a name="dynamic-and-static-assortments"></a>Dynamische und statische Sortimente

Sortimente können mit spezifischen Kanälen und Produkten oder indem Organisationseinheiten und Kategorien einbezogen werden freigegeben werden. Sortimente einschließlich Referenzen für diese Gruppen gelten als dynamischer Sortimente. Wenn die Definition oder der Inhalt dieser Gruppen ändern, während das Sortiment aktiv ist, ändert die Definition des Sortiments.

So wird beispielsweise ein Sortiment ursprünglich definierten und veröffentlicht, damit es auf eine Produktgruppe verweist. Wenn zusätzliche Produkte später zur Kategorie hinzugefügt werden, sind diese Produkte automatisch in der Definition des vorhandenen Sortimente einbezogen. Sie müssen das neue Material nicht der manuell der Produktionsstückliste hinzufügen. Und auch wenn eine andere Organisationseinheit zu einem Knoten hinzugefügt wird, wird das Sortiment der Organisationseinheit automatisch auf Basis dieser Definition reguliert.

### <a name="stopped-products"></a>Gestoppte Produkte

Sie können gemeinsam genutzte Produkte für den Verkaufsvorgang "beenden" mithilfe einer Einstellung in den **Standardauftrag** Einstellungen aktivieren. Diese Einstellung ist oft verwendet, wenn ein Produkt am Ende der Nutzungsdauer angezeigt wird und keinem Kanal verkauft werden soll. Sortimente respektieren diese Einstellung und beendete Produkte werden nicht unabhängig von der Sortimentskonfiguration sortiert.

### <a name="blocked-products"></a>Gesperrte Produkte

Zusätzlich zum Beenden des Vertriebs eines Produkts können Sie vorübergehend den Verkauf eines Produkts sperren. Sie können diese Einstellung auf der Registerkarte **Commerce** eines gemeinsamen Produkts konfigurieren. Gesperrte Produkte werden weiterhin sortiert, aber Sie erhalten eine Meldung im POS, das angibt, dass das Produkt nicht verkauft werden kann.

### <a name="date-effectivity"></a>Datumsgültigkeit

Sortiment hängen von Gültigkeitsdaten ab. Daher können Einzelhändler konfigurieren, wenn Produkte nicht pro Kanal verfügbar sind oder sein sollen. Alternativ können Sie auch Sortimente vorzeitig definieren und Veröffentlichen und das Start- und Enddatum angeben. Die Produkte werden automatisch verfügbar oder zum festgelegten Datum nicht verfügbar.

### <a name="process-assortments-batch-job"></a>Führen Sie den Stapelverarbeitungsauftrag aus.

Sortimente, die in Commerce definiert sind, müssen verarbeitet werden, bevor sie in Kraft treten. Dieser Prozess wird aus folgenden Gründen durchgeführt:

- Sortimentsdefinitionen müssen denormalisiert werden, damit sie Kanäle leichter verbrauchen können. Eine Gesamtproduktion für Kanäle kann durch mehrere Sortimente definiert werden, die unterschiedliche Datumsbereiche enthalten. Wird einigen dieser Daten vorzeitig im Feld Server berechnet werden, wird die Leistung im Kanal verbessert.
- Die Produkte und die Kanäle im Sortiment können außerhalb des Sortiments auch ändern. Dynamische Sortimente, die Verweise auf Kategorien oder Organisationseinheiten enthalten oder regelmäßig verarbeitet werden müssen, damit sie Datensätze einbeziehen oder ausschließen, basierend auf aktuellen Zuweisung.

## <a name="implementation-considerations"></a>Implementierungsüberlegungen

Berücksichtigen Sie die folgenden Implementierungsanforderungen, wie Sie Sortimente für Ihre Commerce-Implementierung planen und verwalten:

- **Datenenwiederholung und Datenbankgröße** – Obwohl Sortimente helfen, den Geschäftsanforderungen zu entsprechen, verwalten sie die Produktverfügbarkeit. Sie sind außerdem ein wichtiges Werkzeug für die Verwaltung der Größe des Kanals und Offline-Datenbanken. Gut-verwaltete Sortimente helfen, die Datenmenge zu verringern, die im Kanal sowie offline verarbeitet und repliziert werden müssen. Sie helfen auch, die Anzahl von Datensätzen zu reduzieren, die verwaltet werden müssen. Weniger Datensätzen in diesen Datenbanken erhöhen die Leistung, wenn Sie einer Buchung Artikel, Suchen für Produkte hinzufügen oder Produkte durchsuchen.
- **Datum-effektiv/, ablaufende Sortimente** Eindes der effektivsten Tools zum Verwalten der Anzahl von Produkten im Kanal und der Offline-Datenbanken ist die Datumswirksamkeit von Sortimenten. Wenn Sie (offene) nicht-ablaufende Sortimente für Saisonprodukte oder Produkte, die am Ende der Nutzungsdauer sind, verlassen, werden diese Datenbanken auf unbestimmte Zeit wachsen. Sie können unterschiedliche Arten verwenden, mit deren Hilfe Sie diese Situation zu verwalten. Beispielsweise können Sie separate Sortimente für Produkte und Saisonprodukte unterhalten, die immer verfügbar sind.
- **Vertrieb und externe Sortimente der Rücklieferungen** – Diese Funktion hilft Einzelhändlern, die Sortimente verwalten, indem sie die Anzahl der verfügbaren Produkte in den Produkten einschränken können, die der Kerngesamtproduktion für den Shop angehören. Diese Funktion ermöglicht auch Einzelhändlern, Situationen zu ermöglichen, in der ein Produkt irrtümlich von einem Sortiment ausgelassen wurde, oder in ein Produkt außerhalb des Gültigkeitsdatums für das Sortiment zurückgegeben wurde.

Wenn Produktdaten nicht in der Kanaldatenbank vorhanden sind, können POS Anrufe in Echtzeit zu den Hauptsitzen machen, um die erforderlichen Informationen abzurufen, damit das Produkt verkauft, angezeigt oder zurückgegebenen oder einem Kundenauftrag hinzugefüt werden kann. Produktinformationen, die auf diese Weise abgerufen werden, gelten nur während des Bereichs dieser Buchung. Das Produkt wird nicht der Sortimentsdefinition hinzugefügt. Daher werden folgende Echtzeitanrufe bei Bedarf ausgeführt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]