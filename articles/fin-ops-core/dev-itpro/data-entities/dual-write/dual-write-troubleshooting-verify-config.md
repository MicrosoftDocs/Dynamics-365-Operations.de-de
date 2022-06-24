---
title: Konfiguration für duales Schreiben in Finanz- und Betriebs-Apps und Dataverse überprüfen
description: In diesem Artikel wird erklärt, wie Sie feststellen können, ob duales Schreiben in Finanz- und Betriebs-Apps und in Dataverse konfiguriert ist.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884458"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Konfiguration für duales Schreiben in Finanz- und Betriebs-Apps und Dataverse überprüfen

[!include [banner](../../includes/banner.md)]





Dieser Artikel enthält Informationen zur Problembehandlung für die Integration von dualem Schreiben zwischen Finanz- und Betriebs-Apps und Dataverse. Insbesondere wird erklärt, wie Sie feststellen können, ob duales Schreiben in den Apps Finance und Operations und in Dataverse konfiguriert ist.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Überprüfen Sie, ob duales Schreiben in einer Finance und Operations App konfiguriert ist

Um festzustellen, ob die Fehler, die beim Speichern von Zeilen für die Aktualisierung angezeigt werden, auf Dual-Write zurückzuführen sind, überprüfen Sie zunächst, ob Dual-Write konfiguriert ist.

+ Wenn Sie über Admin-Rechte in der App Finance und Operations verfügen, gehen Sie zu **Arbeitsbereiche \> Datenverwaltung** und wählen Sie die Kachel **duales Schreiben**. Wenn die Details der verknüpften Umgebungen und die Liste der ausgeführten Tabellenzuordnungen angezeigt werden, ist Dual-Write konfiguriert.

    ![Überprüfen der Verbindung zur Finance und Operations App, wenn Sie über Admin-Rechte verfügen.](media/verify_fin_ops_1.png)

+ Wenn Sie keine Administratorrechte haben, erhalten Sie eine Fehlermeldung: *Daten können nicht in die Entität geschrieben werden \<entity name\>*. In dem Beispiel in der folgenden Abbildung können Sie in der App Finance und Operations keine Debitor-Zeile erstellen, da duales Schreiben konfiguriert ist, aber die Referenzdaten für die Kundengruppe und die Zahlungsbedingungen nicht in Dataverse vorhanden sind.

    ![Überprüfen der Verbindung zur App Finance und Operations, wenn Sie keine Admin-Rechte haben.](media/verify_fin_ops_2.png)

Informationen zur Behebung von Problemen beim Erstellen von Daten in Apps für Finanzen und Betrieb finden Sie unter [Problembehandlung von Problemen bei der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Überprüfen, ob duales Schreiben in Dataverse Apps konfiguriert ist

Wenn Sie Daten erstellen, sehen Sie die Spalte **Unternehmen** auf Seiten in Dataverse. Duales Schreiben ist konfiguriert.

![Überprüfen der Dataverse-Verbindung.](media/verify_cds.png)

Informationen zum Beheben von Problemen beim Erstellen von Daten in Dataverse Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).

Informationen zum Anzeigen von Fehlerdetails, wenn beim Erstellen von Daten Fehler auftreten Dataverse, gehen Sie zu [Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Dataverse, um Fehlerdetails anzuzeigen](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]