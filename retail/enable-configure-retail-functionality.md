---
title: Initialisieren Sie Startwertdaten in einer neuen Kleinumgebung
description: "In diesem Artikel wird beschrieben die Daten, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge erstellt wird."
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
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Initialisieren Sie Startwertdaten in einer neuen Kleinumgebung

In diesem Artikel wird beschrieben die Daten, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge erstellt wird.

Nachdem die Einzelhandelslösung über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde, müssen Sie die Einzelhandelskonfiguration initialisieren, um die grundlegenden Konfigurationsdaten zu erstellen. **Wichtig:** Bevor Sie die Einzelhandelskonfiguration initialisieren, überprüfen Sie, ob Sie eine Sprache und eine Postadresse für jede juristische Person angegeben haben, für die Sie Einzelhandelsgeschäfte einrichten werden. Dieser Schritt muss für jede juristische Person abgeschlossen werden, die Sie für Einzelhandel verwenden. Um die Einzelhandelskonfiguration zu initialisieren, führen Sie die folgenden Schritte aus:

1.  Starten Sie den Dynamics 365 für Arbeitsgangskunden.
2.  ** Sie Einzelhandel und Handel ** &gt; ** Headquarter Einstellungen ** &gt; ** Parameter ** &gt; ** Einzelhandelsparameter **.
3.  Klicken Sie auf **Initialisieren**.

Durch die Initialisierung werden die folgenden Standardkonfigurationsdaten erstellt:

-   Einzelhandel-Steuerprogramm-Aufträge und -Unteraufträge
-   Retail Channel-Schema
-   Einzelhandel-Vertriebszeitpläne
-   Standard-Bildschirmlayouts mit Schaltflächenrastern, Bildern und Themen
-   Zeitzoneninformation
-   Verkaufsstellen(POS)-Vorgänge
-   POS-Berechtigungen
-   Kanalberichte
-   Attributmetadaten
-   Entitätsprüfungsvorlagen
-   Batchauftrag, um den Commerce Data Exchange-Sitzungsverlauf zu bereinigen

Darüber hinaus wird das Protokollieren, die der Zahlungskartenindustrie (PCI) zugeordnet ist, für das Dynamics 365 für Arbeitsgangsdatenbank aktiviert. **Hinweis:** Es gibt eine Option, um das Einzelhandel-Steuerprogramm separat zu konfigurieren. Mit dieser Option können Sie die Einzelhandel-Steuerprogramm-Konfiguration auf die Standardeinstellungen zurücksetzen. Nachdem die Initialisierung abgeschlossen wurde, müssen Sie zusätzliche Einzelhandelsdaten konfigurieren. Nachfolgend finden Sie einige Beispiele:

-   Einzelhandelsparameter
-   Einzelhandel-Steuerprogramm-Parameter
-   Retail Channels
-   Register und Geräte
-   Sortimente



