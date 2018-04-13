---
title: "Überblick über die erweiterte Bankabstimmung"
description: "In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben. Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ff59250b836a73986848109ce48f843fed1d71a9
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="advanced-bank-reconciliation-overview"></a>Überblick über die erweiterte Bankabstimmung

[!INCLUDE [banner](../includes/banner.md)]

In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben. Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können.

Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren. Der importierte Bankauszug kann aus Banktransaktionen heraus automatisch abgestimmt werden. Hierbei gelten die Schritte des erweiterten Bankabstimmungsflusses.

1.  Richten Sie einen Bankauszugsimport ein.
    -   Importieren Sie Bankauszüge durch das Datenentitätsframework.
    -   Drei typische Bankauszugsformate sind integriert: ISO20022, BAI2 und MT940.
    -   Die Funktionen können in jedes beliebige Format erweitert werden.

2.  Richten Sie einen Nummernkreis ein, der für erweiterte Bankabstimmung verwendet wird, und definieren Sie die Abgleichsregeln für Bankabstimmung.
    -   Eine Abstimmmungsregel ist eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Microsoft Dynamics 365 for Finance and Operations  Banktransaktionspositionen während des Abstimmungsvorgangs zu filtern. Abhängig von Ihrer Geschäftspraktik können Sie mehrere Übereinstimmungsregel einrichten, die Ihren Abstimmungsprozess automatisieren und optimieren.

3.  Stimmen Sie Bankauszüge mit Finance and Operations Banktransaktionen ab.
    -   Führen Sie den automatischen Abgleich und die Erstellung von Abstimmungserfassungen aus.
    -   Zeigen Sie Bankauszüge und Finance and Operations-Banktransaktionen parallel an.
    -   Buchen Sie Finance and Operations-Banktransaktionen automatisch, wenn sie auf einem Bankauszug aber nicht in Finance and Operations angezeigt werden.
    -   Generieren eines Abstimmungsauszugs






