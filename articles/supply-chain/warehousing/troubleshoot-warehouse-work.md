---
title: Fehlerbehebung im Lagerort
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerortarbeit in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837440"
---
# <a name="troubleshoot-warehouse-work"></a>Fehlerbehebung bei der Lagerortarbeit

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerortarbeit in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Ich kann keine Ladungsträger mit Seriennummern-Elementen verschieben, wenn Blanko-Ausgabe und Blanko-Empfang in der Dimensionsgruppe für die Nachverfolgung erlaubt sind.

### <a name="issue-description"></a>Problembeschreibung

Sie können einen Ladungsträger nicht mit dem Menüelement **Verschieben** verschieben, wenn die Seriennummer die Einstellungen *Leerzeichenausgabe erlaubt* und *Leerzeichenquittung erlaubt* auf der Tracking-Dimensionsgruppe hat und wenn sich mehrere Ladungsträger auf demselben Lagerplatz befinden, von denen einige Seriennummern haben und einige nicht.

### <a name="issue-resolution"></a>Problemlösung

Dieses Problem wird durch Änderungen behoben, die in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) bereitgestellt werden. Diese Änderungen werden das Feld **Seriennummer** optional machen, wenn leere Quittungen und leere Ausgaben erlaubt sind.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Ich erhalte in der Warehouse Management Mobile App folgende Fehlermeldung, wenn ich Bewegungen verarbeite: „Der Besitzer des Bestandes %1 ist in diesem Prozess nicht erlaubt.“

### <a name="issue-description"></a>Problembeschreibung

Die Dimension **Besitzer** für die Nachverfolgung fehlt, wenn die Warehouse Management Mobile App verwendet wird, um Bewegungen durchzuführen. Eine reguläre Bestandsumlagerungserfassung aus dem Supply Chain Management Client scheint wie vorgesehen zu funktionieren und kann nur gebucht werden, wenn die Dimension **Besitzer** ausgefüllt ist.

### <a name="issue-resolution"></a>Problemlösung

Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Derzeit unterstützen die Prozesse der Lagerortverwaltung nur Bestände, die im Besitz der juristischen Entität sind.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]