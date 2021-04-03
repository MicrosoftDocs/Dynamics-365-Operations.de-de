---
title: Überprüfen der Konfiguration von dualem Schreiben in Finance and Operations-Apps und Dataverse
description: In diesem Thema wird erläutert, wie Sie feststellen können, ob duales Schreiben in Finance and Operations Apps und in Dataverse konfiguriert ist.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 0a1da32713f3d4d19b4d343c5b67b416a6c4ffbb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566764"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Überprüfen der Konfiguration von dualem Schreiben in Finance and Operations-Apps und Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse. In diesem Thema wird speziell erläutert, wie Sie feststellen können, ob Dual-Write in Finance and Operations Apps und in Dataverse konfiguriert ist.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Überprüfen, ob duales Schreiben in Finance and Operations Apps konfiguriert ist

Um festzustellen, ob die Fehler, die beim Speichern von Zeilen für die Aktualisierung angezeigt werden, auf Dual-Write zurückzuführen sind, überprüfen Sie zunächst, ob Dual-Write konfiguriert ist.

+ Wenn Sie Administratorrechte in der Finance and Operations App haben, gehen Sie zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**. Wenn die Details der verknüpften Umgebungen und die Liste der ausgeführten Tabellenzuordnungen angezeigt werden, ist Dual-Write konfiguriert.

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über Administratorrechte verfügen](media/verify_fin_ops_1.png)

+ Wenn Sie keine Administratorrechte haben, erhalten Sie eine Fehlermeldung: *Daten können nicht in die Entität geschrieben werden \<entity name\>*. Im Beispiel in der folgenden Abbildung können Sie keine Kundenzeile in der Finance and Operations-App erstellen, da Dual-Write konfiguriert ist, die Referenzdaten für die Kundengruppe und die Zahlungsbedingungen in Dataverse jedoch nicht vorhanden sind.

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über keine Administratorrechte verfügen](media/verify_fin_ops_2.png)

Informationen zum Beheben von Problemen beim Erstellen von Daten in Finance and Operations Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Überprüfen, ob duales Schreiben in Dataverse Apps konfiguriert ist

Wenn Sie Daten erstellen, sehen Sie die Spalte **Unternehmen** auf Seiten in Dataverse. Duales Schreiben ist konfiguriert.

![Überprüfen der Dataverse Verbindung](media/verify_cds.png)

Informationen zum Beheben von Problemen beim Erstellen von Daten in Dataverse Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

Informationen zum Anzeigen von Fehlerdetails, wenn beim Erstellen von Daten Fehler auftreten Dataverse, gehen Sie zu [Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Dataverse, um Fehlerdetails anzuzeigen](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]