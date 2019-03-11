---
title: Startdaten in neuen Retail-Umgebungen initialisieren
description: In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 for Retail erstellt werden.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "327894"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Startwertdaten in Retail-Umgebungen initialisieren

[!include [banner](includes/banner.md)]

In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 for Retail erstellt werden.

Nachdem die Retail-Lösung über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde, müssen Sie die Einzelhandelskonfiguration initialisieren, um die grundlegenden Konfigurationsdaten zu erstellen.

> [!IMPORTANT]
> Bevor Sie die Einzelhandelskonfiguration initialisieren, überprüfen Sie, ob Sie eine Sprache und eine Postadresse für jede juristische Person angegeben haben, für die Sie Einzelhandelsgeschäfte einrichten werden. Dieser Schritt muss für jede juristische Person abgeschlossen werden, die Sie für Einzelhandel verwenden.

Um die Einzelhandelskonfiguration zu initialisieren, führen Sie die folgenden Schritte aus:

1. Starten Sie den Dynamics 365 for Retail-Client.
2. Klicken Sie auf **Einzelhandel** &gt; **Zentralverwaltungseinrichtun** &gt; **Parameter** &gt; **Einzelhandelsparamete**.
3. Klicken Sie auf **Initialisieren**.

Durch die Initialisierung werden die folgenden Standardkonfigurationsdaten erstellt:

- Einzelhandel-Steuerprogramm-Aufträge und -Unteraufträge
- Retail Channel-Schema
- Einzelhandel-Vertriebszeitpläne
- Standard-Bildschirmlayouts mit Schaltflächenrastern, Bildern und Themen
- Zeitzoneninformation
- Verkaufsstellen(POS)-Vorgänge
- POS-Berechtigungen
- Kanalberichte
- Attributmetadaten
- Entitätsprüfungsvorlagen
- Batchauftrag zum Löschen der Commerce Data Exchange-Sitzungshistorie

Darüber hinaus ist das Protokollieren in Zusammenhang mit der Zahlungskartenindustrie (PCI) für die Dynamics 365 for Retail-Datenbank aktiviert.

> [!NOTE]
> Es gibt eine Option, um das Einzelhandel-Steuerprogramm separat zu konfigurieren. Mit dieser Option können Sie die Einzelhandel-Steuerprogramm-Konfiguration auf die Standardeinstellungen zurücksetzen.

Nachdem die Initialisierung abgeschlossen wurde, müssen Sie zusätzliche Einzelhandelsdaten konfigurieren. Nachfolgend finden Sie einige Beispiele:

- Einzelhandelsparameter
- Einzelhandel-Steuerprogramm-Parameter
- Retail Channels
- Register und Geräte
- Sortimente
