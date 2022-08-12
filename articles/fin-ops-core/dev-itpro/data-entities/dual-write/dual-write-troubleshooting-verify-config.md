---
title: Überprüfen Sie die Dual-write Konfiguration in Finanz- und Betriebs-Apps und Dataverse.
description: Dieser Artikel erklärt, wie Sie feststellen können, ob Dual-write in Finanz- und Betriebs-Apps und in Dataverse konfiguriert ist.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d5191f5dd9c3a286abac622aede07d04fb72a8f7
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111391"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Überprüfen Sie die Dual-write Konfiguration in Finanz- und Betriebs-Apps und Dataverse.

[!include [banner](../../includes/banner.md)]





Dieser Artikel enthält Informationen zur Problembehandlung für die Dual-write Integration zwischen Finanz- und Betriebs-Apps und Dataverse. Insbesondere wird erklärt, wie Sie feststellen können, ob Dual-write in Finanz- und Betriebs-Apps und in Dataverse konfiguriert ist.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Überprüfen Sie, ob Dual-write in einer Finanz- und Betriebs-App konfiguriert ist.

Um festzustellen, ob die Fehler, die beim Speichern von Zeilen für die Aktualisierung angezeigt werden, auf Dual-Write zurückzuführen sind, überprüfen Sie zunächst, ob Dual-Write konfiguriert ist.

+ Wenn Sie über Admin-Rechte in der Finanz- und Betriebs-App verfügen, gehen Sie zu **Arbeitsbereiche \> Datenverwaltung** und wählen Sie die Kachel **Dual-write**. Wenn die Details der verknüpften Umgebungen und die Liste der ausgeführten Tabellenzuordnungen angezeigt werden, ist Dual-Write konfiguriert.

    ![Überprüfen der Verbindung der Finanz- und Betriebs-App, wenn Sie über Admin-Rechte verfügen.](media/verify_fin_ops_1.png)

+ Wenn Sie keine Administratorrechte haben, erhalten Sie eine Fehlermeldung: *Daten können nicht in die Entität geschrieben werden \<entity name\>*. In dem Beispiel in der folgenden Abbildung können Sie in der Finanz- und Betriebs-App keine Debitor-Zeile erstellen, weil Dual-write konfiguriert ist, aber die Referenzdaten für die Kundengruppe und die Zahlungsbedingungen nicht in Dataverse vorhanden sind.

    ![Überprüfen Sie die Verbindung der Finanz- und Betriebs-App, wenn Sie keine Admin-Rechte haben.](media/verify_fin_ops_2.png)

Informationen zur Behebung von Problemen beim Erstellen von Daten in Finanz- und Betriebs-Apps finden Sie unter [Problembehandlung von Problemen bei der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Überprüfen, ob duales Schreiben in Dataverse Apps konfiguriert ist

Wenn Sie Daten erstellen, sehen Sie die Spalte **Unternehmen** auf Seiten in Dataverse. Duales Schreiben ist konfiguriert.

![Überprüfen der Dataverse-Verbindung.](media/verify_cds.png)

Informationen zum Beheben von Problemen beim Erstellen von Daten in Dataverse Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

Informationen zum Anzeigen von Fehlerdetails, wenn beim Erstellen von Daten Fehler auftreten Dataverse, gehen Sie zu [Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Dataverse, um Fehlerdetails anzuzeigen](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
