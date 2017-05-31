---
title: Initialisieren Sie Startwertdaten in einer neuen Kleinumgebung
description: "In diesem Artikel wird beschrieben die Daten, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge erstellt wird."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 534c9ab0f4d95f42d09f35d3197a2258c8d39526
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Initialisieren Sie Startwertdaten in einer neuen Kleinumgebung

[!include[banner](includes/banner.md)]


In diesem Artikel wird beschrieben die Daten, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge erstellt wird.

Nachdem die Einzelhandelslösung über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde, müssen Sie die Einzelhandelskonfiguration initialisieren, um die grundlegenden Konfigurationsdaten zu erstellen. **Wichtig:** Bevor Sie die Einzelhandelskonfiguration initialisieren, überprüfen Sie, ob Sie eine Sprache und eine Postadresse für jede juristische Person angegeben haben, für die Sie Einzelhandelsgeschäfte einrichten werden. Dieser Schritt muss für jede juristische Person abgeschlossen werden, die Sie für Einzelhandel verwenden. Um die Einzelhandelskonfiguration zu initialisieren, führen Sie die folgenden Schritte aus:

1.  Start des Dynamics 365 for Operations Client
2.  Klicken Sie auf **Einzelhandel und Handel** &gt; **Zentralverwaltungseinrichtun** &gt; **Parameter** &gt; **Einzelhandelsparamete**.
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

Darüber hinaus ist das Protokollieren in Zusammenhang mit der Zahlungskartenindustrie (PCI) für die Dynamics 365 Operations Datenbank aktiviert. **Hinweis:** Es gibt eine Option, um das Einzelhandel-Steuerprogramm separat zu konfigurieren. Mit dieser Option können Sie die Einzelhandel-Steuerprogramm-Konfiguration auf die Standardeinstellungen zurücksetzen. Nachdem die Initialisierung abgeschlossen wurde, müssen Sie zusätzliche Einzelhandelsdaten konfigurieren. Nachfolgend finden Sie einige Beispiele:

-   Einzelhandelsparameter
-   Einzelhandel-Steuerprogramm-Parameter
-   Retail Channels
-   Register und Geräte
-   Sortimente





