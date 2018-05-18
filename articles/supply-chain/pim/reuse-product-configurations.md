---
title: Produktkonfigurationen wiederverwenden
description: "Sie können angeben, dass Sie eine Variante für ein Produkt automatisch recyceln möchten. Wenn der Benutzer eine Konfigurationssitzung beendet hat, prüft das System, ob eine Konfiguration, die mit der Auswahl des Benutzers übereinstimmt, bereits vorhanden ist. Wenn eine übereinstimmende Variante gefunden wird, werden die Konfigurationskennung, die korrekte Stückliste (BOM) und der Arbeitsplan recycelt."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: c447440c33c1f80c6056974086b90d3b43e8499e
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---

# <a name="reuse-product-configurations"></a>Produktkonfigurationen wiederverwenden

[!include [banner](../includes/banner.md)]

Sie können angeben, dass Sie eine Variante für ein Produkt automatisch recyceln möchten. Wenn der Benutzer eine Konfigurationssitzung beendet hat, prüft das System, ob eine Konfiguration, die mit der Auswahl des Benutzers übereinstimmt, bereits vorhanden ist. Wenn eine übereinstimmende Variante gefunden wird, werden die Konfigurationskennung, die korrekte Stückliste (BOM) und der Arbeitsplan recycelt.

<a name="requirements-for-reusing-configurations"></a>Anforderungen für die Wiederverwendung von Konfigurationen
---------------------------------------

Damit Konfigurationen wieder verwendet werden können, müssen Sie die folgenden Informationen für die Komponenten und Attribute auf der Seite **Produktkonfigurationsmodelldetails** angeben:

-   **Komponenten und Unterkomponenten** – Wählen Sie im Inforegister**Allgemein** im Feld **Konfiguration wiederverwenden** **Ja**.
-   **Attribute** – Auf dem Inforegister **Attribute** wählen Sie die Option **In Wiederverwendung einbeziehen** aus. Diese Option wird nur angezeigt, wenn die zugehörige Komponente zur Wiederverwendung aktiviert ist. Wenn Sie keine Attribute zur Wiederverwendung auswählen, wird die Konfiguration immer recycelt, unabhängig von der Auswahl des Benutzers für eine Konfigurationssitzung. Die Attributwerte in der vorhandenen Konfiguration müssen der Auswahl des Benutzers entsprechen. Wenn der Benutzer zum Beispiel die Farbe **Blau** für eine Farbe während der Konfigurationssitzung auswählt, prüft das System, ob eine Variante der Komponente ein Attribut für die Farbe Blau hat.

## <a name="resetting-configuration-reuse"></a>Wiederverwendung der Konfiguration zurücksetzen
Wenn Sie die Konfigurationswiederverwendung zurücksetzen, werden zuvor erstellte Konfigurationen nicht mehr berücksichtigt. Sie wollen möglicherweise die Konfigurationswiederverwendung zurücksetzen, wenn die Stückliste oder der Arbeitsplan geändert aber keine entsprechenden Attribute geändert wurden. Sie können die Konfiguration auf dem Inforegister **Allgemeines** für die Komponente wieder verwenden.




