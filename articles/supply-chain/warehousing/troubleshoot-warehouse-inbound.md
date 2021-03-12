---
title: Fehlerbehebung bei eingehenden Lagerort-Vorgängen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit eingehenden Lagerort-Operationen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970246"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Fehlerbehebung bei eingehenden Lagerort-Vorgängen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit eingehenden Lagerort-Operationen in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Ich erhalte die folgende Fehlermeldung: „Qualitätsauftrag %1 wurde erzeugt. Clusterprofil konnte nicht gefunden werden, bitte überprüfen Sie Ihre Konfiguration.“

### <a name="issue-description"></a>Problembeschreibung

Diese Fehlermeldung bezieht sich auf einen Eingangsvorgang, bei dem das Qualitätsmanagement (QMS) eingeschaltet ist. Abhängig von den Konfigurationen in Ihrer Umgebung können zusätzliche Details über die Transaktion, die die Fehlermeldung erzeugt, helfen, das Problem zu beheben.

### <a name="issue-resolution"></a>Problemlösung

Überprüfen Sie zunächst die [Clusterkommissionierung](set-up-cluster-picking.md) und stellen Sie sicher, dass Ihre Cluster-Profile richtig festgelegt sind. Sie können kein Menüelement für die Cluster-Kommissionierung auf einem mobilen Gerät verwenden, wenn keine Cluster-Profile festgelegt sind. Abhängig von Ihrer Umgebung müssen Sie möglicherweise auch andere zugehörige Konfigurationen überprüfen.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Der Empfang von gemischten Ladungsträgern funktioniert nicht für alle Dispositionscodes außer Guthaben.

### <a name="issue-description"></a>Problembeschreibung

Wenn das Feld **Aktion** für einen Dispositionscode auf *Kredit* oder *Schrott* festgelegt ist, können Sie nur den Menüpunkt [Mischkennzeichen-Empfang](mixed-license-plate-receiving.md) verwenden, um zurückgegebene Elemente zu verarbeiten.

### <a name="issue-resolution"></a>Problemlösung

Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Derzeit werden für den gemischten Ladungsträger-Empfang nur [Positionscodes](../service-management/set-up-disposition-codes.md) unterstützt, bei denen das Feld **Aktion** auf *Gutschrift* oder *Ausschuss* festgelegt ist.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Wenn ich die Aufgabe „Periodische Wareneingänge aktualisieren“ ausführe, werden unbestätigte Einkaufsbestellungen bestätigt.

### <a name="issue-description"></a>Problembeschreibung

Nachdem Sie die periodische Aufgabe *Produkteingänge aktualisieren* ausgeführt haben, bestätigt das System automatisch unbestätigte Einkaufsbestellungen, die einen Bestandstransaktionsstatus von *Registriert* haben.

### <a name="issue-resolution"></a>Problemlösung

Eine neue Funktion zur Behandlung eingehender Ladungen, *Übernahme von Ladungsmengen*, behebt dieses Problem. Um diese Funktion zu aktivieren, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die folgenden Funktionen ein (in der Reihenfolge, in der sie aufgelistet sind):

1. Zuordnung von Bestellbestandsbuchungen zur Ladung
1. Zu hoher Zugang bei Auslastungsmengen

Weitere Informationen finden Sie unter [Registrierte Produktmengen gegen Einkaufsbestellungen verbuchen](inbound-load-handling.md#post-registered-quantities).
