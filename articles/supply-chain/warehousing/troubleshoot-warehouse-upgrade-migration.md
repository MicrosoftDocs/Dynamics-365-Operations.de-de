---
title: Fehlerbehebung bei Upgrade und Migration zur erweiterten Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die beim Upgrade und bei der Migration zur erweiterten Lagerverwaltung auftreten können.
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
ms.openlocfilehash: c07c5894f340fde2834e95d53fa390ec5789feeca9b3902e56c333da0d143f5b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747792"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Fehlerbehebung bei Upgrade und Migration zur erweiterten Lagerortverwaltung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die beim Upgrade und bei der Migration zur erweiterten Lagerverwaltung auftreten können.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Ich erhalte die folgende Fehlermeldung: „java.security.cert.certPathValidatorException: Vertrauensanker für Zertifizierungspfad wurde nicht gefunden.“

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten diese Fehlermeldung in der Warehouse Management Mobile App, da selbstsignierten Zertifikaten auf Android 8+ in lokalen Umgebungen nicht vertraut wird.

### <a name="issue-resolution"></a>Problemlösung

Verwenden Sie eine externe (öffentliche) Zertifizierungsstelle (CA). Ein Fix für dieses Problem ist in Version 1.9.0.0 der Lagerort App verfügbar. Weitere Informationen zu diesem Problem und wie Sie es beheben können, finden Sie unter [Fehlerbehebung bei Verbindungsproblemen der Warehouse Management Mobile App](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Was ist der genehmigte Prozess für den Wechsel von Basis-Lagerort zu erweitertem Lagerort?

### <a name="issue-description"></a>Problembeschreibung

Sie arbeiten derzeit mit der Lagerort-/Bestandsverwaltung und nutzen die Basislagerfunktionalität und möchten zur erweiterten Lagerortverwaltung wechseln, um die Vorteile von mobilen Geräten, Wellen und Arbeit zu nutzen. Allerdings stoßen Sie auf Probleme, wenn Sie versuchen, diesen Wechsel vorzunehmen. Sie können z. B. Ihre Produkte nicht so ändern, dass sie Lagerdimensionen (Standort, Lagerort und Lagerplatz) verwenden, weil die Produkte mit Transaktionen belegt sind. Daher müssen Sie den genehmigten Prozess für den Umzug von der einfachen Lagerhaltung zur erweiterten Lagerhaltung lernen.

### <a name="issue-resolution"></a>Problemlösung

Weitere Informationen über den Prozess für den Wechsel von Basic Warehousing zu Advanced Warehousing finden Sie in den folgenden Blog-Beiträgen und in der Dokumentation:

- [Prozess der Lagerortverwaltung für bestehende Elemente und Lagerorte aktivieren](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Migration von Microsoft Dynamics AX WMS auf neue R3-Lager- und Transportfunktionalität](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 Element-Migration](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Upgrade der Lagerortverwaltung von Microsoft Dynamics AX 2012 auf Supply Chain Management](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]