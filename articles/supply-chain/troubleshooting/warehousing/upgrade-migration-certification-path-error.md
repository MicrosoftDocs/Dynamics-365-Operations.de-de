---
title: Zertifizierungspfadfehler beim Upgrade oder Migrieren zu WMS
description: Wenn die App beim Upgrade oder Migrieren zu WMS den Fehler Vertrauensanker für Zertifizierungspfad nicht gefunden anzeigt, finden Sie auf dieser Seite Informationen zur Behebung des Problems.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476418"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Der Vertrauensanker für den Zertifizierungspfad wurde beim Aktualisieren und Migrieren nach WMS nicht gefunden

## <a name="symptoms"></a>Symptome

Bei der Aktualisierung oder Migration zum erweiterten Warehouse Management (WMS), zeigt die Warehouse Management-App möglicherweise folgende Fehlermeldung an:

> java.security.cert.certPathValidatorException: Vertrauensanker für Zertifizierungspfad wurde nicht gefunden.

## <a name="cause"></a>Ursache

Dies tritt auf, weil selbstsignierten Zertifikaten nicht vertraut wird in Android 8+ in lokalen Umgebungen.

## <a name="resolution"></a>Lösung

Verwenden Sie eine externe (öffentliche) Zertifizierungsstelle (CA). Ein Fix für dieses Problem ist in Version 1.9.0.0 der Warehouse Management App verfügbar. Weitere Informationen zu diesem Problem und wie Sie es beheben können, finden Sie unter [Vertrauensanker für Zertifizierungspfad beim Einrichten der App-Verbindung nicht gefunden](certification-path-app-connection-error.md).
