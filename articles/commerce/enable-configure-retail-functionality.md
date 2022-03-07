---
title: Startdaten in neuen Commerce-Umgebungen initialisieren
description: In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Dynamics 365 Commerce erstellt werden.
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
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a12bd7a178d8d40db8c919410a00fbf021625f50
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238749"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Startdaten in neuen Commerce-Umgebungen initialisieren

[!include [banner](includes/banner.md)]

In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Dynamics 365 Commerce erstellt werden.

Nachdem die Commerce-Lösung über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde, müssen Sie die Commerce-Konfiguration initialisieren, um die grundlegenden Konfigurationsdaten zu erstellen.

> [!IMPORTANT]
> Bevor Sie die Commerce-Konfiguration initialisieren, überprüfen Sie, ob Sie eine Sprache und eine Postadresse für jede juristische Person angegeben haben, für die Sie Geschäfte einrichten werden. Dieser Schritt muss für jede juristische Person abgeschlossen werden, die Sie für Commerce verwenden.

Um die Konfiguration zu initialisieren, führen Sie die folgenden Schritte aus:

1. Starten Sie den Commerce-Client.
2. Klicken Sie auf **Einzelhandel und Handel** &gt; **Zentralverwaltungseinrichtung** &gt; **Parameter** &gt; **Commerce-Parameter**.
3. Klicken Sie auf **Initialisieren**.

Durch die Initialisierung werden die folgenden Standardkonfigurationsdaten erstellt:

- Aufträge und Unteraufträge für Commerce-Steuerprogramm
- Handelskanalschema
- Vertriebszeitpläne für Commerce
- Standard-Bildschirmlayouts mit Schaltflächenrastern, Bildern und Themen
- Zeitzoneninformation
- Verkaufsstellen(POS)-Vorgänge
- POS-Berechtigungen
- Kanalberichte
- Attributmetadaten
- Entitätsprüfungsvorlagen
- Batchauftrag zum Löschen der Commerce Data Exchange-Sitzungshistorie

Darüber hinaus ist das Protokollieren in Zusammenhang mit der Zahlungskartenindustrie (PCI) für die Commerce-Datenbank aktiviert.

> [!NOTE]
> Es gibt eine Option, um das Commerce-Steuerprogramm separat zu konfigurieren. Mit dieser Option können Sie die Commerce-Steuerprogramm-Konfiguration auf die Standardeinstellungen zurücksetzen.

Nachdem die Initialisierung abgeschlossen wurde, müssen Sie zusätzliche Commerce-Daten konfigurieren. Im Folgenden finden Sie einige Beispiele hierfür:

- Handelsparameter
- Handelsplanungsparameter
- Commerce-Kanäle
- Register und Geräte
- Sortimente


[!INCLUDE[footer-include](../includes/footer-banner.md)]