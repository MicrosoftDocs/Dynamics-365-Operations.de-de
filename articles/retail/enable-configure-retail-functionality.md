---
title: Initialisieren Sie Startwertdaten in einer neuen Kleinumgebung
description: "In diesem Artikel werden die Daten beschrieben , die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 for Retail erstellt werden."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7388324fe8a9abc8fc3d723b7c8df2c73d76a2ae
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Initialisieren Sie Startwertdaten in einer neuen Kleinumgebung

[!include[banner](includes/banner.md)]


In diesem Artikel werden die Daten beschrieben , die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 for Retail erstellt werden.

Nachdem die Einzelhandelslösung über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde, müssen Sie die Einzelhandelskonfiguration initialisieren, um die grundlegenden Konfigurationsdaten zu erstellen. **Wichtig:** Bevor Sie die Einzelhandelskonfiguration initialisieren, überprüfen Sie, ob Sie eine Sprache und eine Postadresse für jede juristische Person angegeben haben, für die Sie Einzelhandelsgeschäfte einrichten werden. Dieser Schritt muss für jede juristische Person abgeschlossen werden, die Sie für Einzelhandel verwenden. Um die Einzelhandelskonfiguration zu initialisieren, führen Sie die folgenden Schritte aus:

1.  Start des Dynamics 365 for Retail-Client
2.  Klicken Sie auf **Einzelhandel** &gt; **Zentralverwaltungseinrichtun** &gt; **Parameter** &gt; **Einzelhandelsparamete**.
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

Darüber hinaus ist das Protokollieren in Zusammenhang mit der Zahlungskartenindustrie (PCI) für die Dynamics 365 Retail- Datenbank aktiviert. **Hinweis:** Es gibt eine Option, um das Einzelhandel-Steuerprogramm separat zu konfigurieren. Mit dieser Option können Sie die Einzelhandel-Steuerprogramm-Konfiguration auf die Standardeinstellungen zurücksetzen. Nachdem die Initialisierung abgeschlossen wurde, müssen Sie zusätzliche Einzelhandelsdaten konfigurieren. Nachfolgend finden Sie einige Beispiele:

-   Einzelhandelsparameter
-   Einzelhandel-Steuerprogramm-Parameter
-   Retail Channels
-   Register und Geräte
-   Sortimente





