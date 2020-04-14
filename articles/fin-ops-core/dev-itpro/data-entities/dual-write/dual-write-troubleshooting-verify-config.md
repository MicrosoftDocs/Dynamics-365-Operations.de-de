---
title: Überprüfen, ob duales Schreiben in Finance and Operations-Apps und Common Data Service konfiguriert ist
description: In diesem Thema wird erläutert, wie Sie feststellen können, ob duales Schreiben in Finance and Operations Apps und in Common Data Service konfiguriert ist.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172644"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Überprüfen, ob duales Schreiben in Finance and Operations-Apps und Common Data Service konfiguriert ist

[!include [banner](../../includes/banner.md)]



Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service. In diesem Thema wird speziell erläutert, wie Sie feststellen können, ob Dual-Write in Finance and Operations Apps und in Common Data Service konfiguriert ist.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Überprüfen, ob duales Schreiben in Finance and Operations Apps konfiguriert ist

Um festzustellen, ob die Fehler, die beim Speichern von Datensätzen für die Aktualisierung angezeigt werden, auf Dual-Write zurückzuführen sind, überprüfen Sie zunächst, ob Dual-Write konfiguriert ist.

+ Wenn Sie Administratorrechte in der Finance and Operations App haben, gehen Sie zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**. Wenn die Details der verknüpften Umgebungen und die Liste der ausgeführten Entitätszuordnungen angezeigt werden, ist Dual-Write konfiguriert.

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über Administratorrechte verfügen](media/verify_fin_ops_1.png)

+ Wenn Sie keine Administratorrechte haben, erhalten Sie eine Fehlermeldung: *Daten können nicht in die Entität geschrieben werden \<Entitätsname\>*. Im Beispiel in der folgenden Abbildung können Sie keinen Kundendatensatz in der Finance and Operations App erstellen, da Dual-Write konfiguriert ist, die Referenzdaten für Kundengruppe und Zahlungsbedingungen jedoch nicht vorhanden sind in Common Data Service.

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über keine Administratorrechte verfügen](media/verify_fin_ops_2.png)

Informationen zum Beheben von Problemen beim Erstellen von Daten in Finance and Operations Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Überprüfen, ob duales Schreiben in Common Data Service Apps konfiguriert ist

Wenn Sie Daten erstellen, sehen Sie das Feld **Unternehmen** auf Seiten in Common Data Service. Dual-Write ist konfiguriert.

![Überprüfen der Common Data Service Verbindung](media/verify_cds.png)

Informationen zum Beheben von Problemen beim Erstellen von Daten in Common Data Service Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

Informationen zum Anzeigen von Fehlerdetails, wenn beim Erstellen von Daten Fehler auftreten Common Data Service, gehen Sie zu [Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Common Data Service, um Fehlerdetails anzuzeigen](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
