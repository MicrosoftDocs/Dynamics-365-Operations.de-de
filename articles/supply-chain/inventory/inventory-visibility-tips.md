---
title: Tipps zu Inventory Visibility
description: Dieser Artikel enthält einige Tipps, die Sie bei der Einrichtung und Verwendung des Bestandssichtbarkeit-Add-Ins beachten sollten.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306084"
---
# <a name="inventory-visibility-tips"></a>Tipps zur Inventory Visibility

[!include [banner](../includes/banner.md)]

Hier finden Sie einige Tipps, die Sie bei der Einrichtung und Verwendung des Bestandssichtbarkeit-Add-Ins beachten sollten:

- Derzeit unterstützt das Bestandssichtbarkeit-Add-In nur Microsoft Dataverse-Umgebungen, die mit Hilfe der Microsoft Dynamics-Lifecycle Services (LCS) erstellt wurden. Wenn Ihre Dataverse-Umgebung auf andere Weise erstellt wurde (z.B. mit Hilfe des Power Apps-Admin-Centers) und mit Ihrer Dynamics 365 Supply Chain Management-Umgebung verknüpft ist, müssen Sie zunächst das Inventory Visibility Produktteam bitten, das Zuordnungsproblem zu beheben. Sie können das Team unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) kontaktieren. Das Team wird Sie informieren, wenn Ihre Umgebung bereit ist, Inventory Visibility zu installieren.
- Wenn Sie mehr als eine LCS Umgebung haben, erstellen Sie für jede Umgebung eine andere Azure Active Directory (Azure AD) Anwendung. Wenn Sie dieselbe Anwendungs-ID und Mandanten-ID verwenden, um das Bestandsanzeige-Add-In für verschiedene Umgebungen zu installieren, tritt in älteren Umgebungen ein Tokenproblem auf. Nur die zuletzt installierte Instanz des Bestandssichtbarkeit-Add-Ins ist gültig.
- Inventory Visibility wird derzeit nicht für Umgebungen unterstützt, die in der Cloud gehostet werden. Es wird nur für Tier-2+ Umgebungen unterstützt.
- Die Anwendungsprogrammierschnittstelle (API) unterstützt derzeit die Abfrage von bis zu 100 einzelnen Elementen nach dem `ProductID`-Wert. In jeder Abfrage können auch mehrere `SiteID`- und `LocationID`-Werte angegeben werden. Die Höchstgrenze ist mit `NumOf(SiteID) * NumOf(LocationID) <= 100` definiert.
- Die Bulk-API kann maximal 512 Datensätze für jede Anfrage zurückgeben.
- Die Datenquelle `fno` ist für das Supply Chain Management reserviert. Wenn Ihr Inventory Visibility-Add-In mit einer Supply Chain Management Umgebung integriert ist, empfehlen wir Ihnen, keine Konfigurationen zu löschen, die mit `fno` in der [Datenquelle](inventory-visibility-configuration.md#data-source-configuration) verbunden sind.
- Die Bestandsanzeige kann keine Daten für die `fno`-Datenquelle ändern. Der Datenfluss ist unidirektional, d. h. alle Mengenänderungen für die `fno`-Datenquelle müssen aus Ihrer Supply Chain Management-Umgebung stammen. Daher können Sie die API nicht verwenden, um vorhandene Änderungs- oder Reservierungsanfragen für die `fno`-Datenquelle zu senden.
- Wenn Sie Ihrer Supply Chain Management-Umgebung eine oder mehrere neue Kennzahlen hinzufügen, sollten Sie diese auch in der Bestandsanzeige hinzufügen. Alle Mengenänderungen für neue Maßnahmen müssen jedoch aus Ihrer Supply Chain Management-Umgebung stammen.
- Die [Partitionskonfiguration](inventory-visibility-configuration.md#partition-configuration) besteht derzeit aus zwei Basis Dimensionen (`SiteId` und `LocationId`), die angeben, wie die Daten verteilt werden. Vorgänge unter der gleichen Partition können eine höhere Leistung zu geringeren Kalkulationen liefern. Die Lösung enthält diese Partitionskonfiguration standardmäßig. Daher *müssen Sie sie nicht selbst definieren*. Passen Sie die Standardkonfiguration der Partition nicht an. Wenn Sie es löschen oder ändern, werden Sie wahrscheinlich einen unerwarteten Fehler verursachen.
- Basisdimensionen, die in der Partitionskonfiguration definiert sind, sollten nicht in der [Produktindexhierarchie-Konfiguration](inventory-visibility-configuration.md#index-configuration) definiert werden.
- Ihre [Produktindexhierarchie-Konfiguration](inventory-visibility-configuration.md#index-configuration) muss mindestens eine Indexhierarchie haben (die beispielsweise die Basisdimension `Empty` enthält), andernfalls schlagen Abfragen mit dem Fehler „Es wurde keine Indexhierarchie festgelegt“ fehl.
- Die Datenquelle `@iv` ist eine vordefinierte Datenquelle und die in `@iv` mit dem Präfix `@` festgelegten physischen Measures sind vordefinierte Measures. Diese Measures sind eine vordefinierte Konfiguration für die Zuordnungsfunktion, also ändern oder löschen Sie sie nicht, da Sie sonst wahrscheinlich auf unerwartete Fehler stoßen, wenn Sie die Zuordnungsfunktion verwenden.
- Sie können der vordefinierten berechneten Measure `@iv.@available_to_allocate` neue physische Measures hinzufügen, aber Sie dürfen ihren Namen nicht ändern.
- Wenn Sie eine Supply Chain Management-Datenbank wiederherstellen, enthält Ihre wiederhergestellte Datenbank möglicherweise Daten, die nicht mehr mit Daten übereinstimmen, welche die Bestandstransparenz vorher mit Dataverse synchronisiert hat. Dieser Datenkonflikt kann Systemfehler und andere Probleme verursachen. Daher ist es wichtig, dass Sie immer alle verbundenen Bestandstransparenzdaten aus Dataverse bereinigen, bevor Sie eine Supply Chain Management-Datenbank wiederherstellen. Weitere Details finden Sie unter [Bestandstransparenzdaten aus Dataverse bereinigen, bevor Sie die Supply Chain Management-Datenbank wiederherstellen](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
