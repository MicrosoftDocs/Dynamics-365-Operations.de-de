---
title: Überblick über die erweiterte Bankabstimmung
description: In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben. Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können.
author: angelad116
ms.date: 10/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 677a032ce77fbe57393c85235a1c64dba3958f2d
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715148"
---
# <a name="advanced-bank-reconciliation-overview"></a>Überblick über die erweiterte Bankabstimmung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben. Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können.

Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren. Der importierte Bankauszug kann aus Banktransaktionen heraus automatisch abgestimmt werden. Hierbei gelten die Schritte des erweiterten Bankabstimmungsflusses.

1.  Richten Sie einen Bankauszugsimport ein.
    -   Importieren Sie Bankauszüge durch das Datenentitätsframework.
    -   Drei typische Bankauszugsformate sind integriert: ISO20022, BAI2 und MT940.
    -   Die Funktionen können in jedes beliebige Format erweitert werden.

2.  Richten Sie einen Nummernkreis ein, der für erweiterte Bankabstimmung verwendet wird, und definieren Sie die Abgleichsregeln für Bankabstimmung.
    -   Eine Abstimmungsübereinstimmungsregel ist eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Microsoft Dynamics 365 Finance-Bankbuchungspositionen während des Abstimmungsvorgangs zu filtern. Abhängig von Ihrer Geschäftspraktik können Sie mehrere Übereinstimmungsregel einrichten, die Ihren Abstimmungsprozess automatisieren und optimieren.

3.  Stimmen Sie Bankauszüge mit Finance-Banktransaktionen ab.
    -   Führen Sie den automatischen Abgleich und die Erstellung von Abstimmungserfassungen aus.
    -   Zeigen Sie Bankauszüge und Finance-Banktransaktionen parallel an.
    -   Buchen Sie Finance-Banktransaktionen automatisch, wenn sie auf einem Bankauszug aber nicht in der Finance-App angezeigt werden.
    -   Generieren eines Abstimmungsauszugs







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
