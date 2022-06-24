---
title: Dataverse-Integration konfigurieren
description: In diesem Artikel wird die Integration zwischen Microsoft Dataverse und Dynamics 365 Human Resources beschrieben.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fdc8d15138904336ce7e7b85fe286c815f0743f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869922"
---
# <a name="configure-dataverse-integration"></a>Dataverse-Integration konfigurieren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können die Integration zwischen Microsoft Dataverse und Dynamics 365 Human Resources aktivieren und deaktivieren. Sie können auch die Synchronisierungsdetails anzeigen, Nachverfolgungsdaten löschen und eine Tabelle erneut synchronisieren, um Datenprobleme zwischen den beiden Umgebungen zu beheben.

> [!NOTE]
> Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](/powerapps/maker/data-platform/data-platform-intro)

Wenn Sie die Integration deaktivieren, können Benutzer Änderungen in Human Resources oder Dataverse vornehmen, diese Änderungen werden jedoch nicht zwischen den beiden Umgebungen synchronisiert.

Standardmäßig ist die Integration zwischen Human Resources und Dataverse deaktiviert.

Möglicherweise möchten Sie die Integration in den folgenden Situationen deaktivieren:

- Sie geben Daten über das Data Management Framework ein und müssen die Daten mehrmals importieren, um sie in einen korrekten Zustand zu versetzen.

- Es gibt Probleme mit Daten in Human Resources oder Dataverse. Wenn Sie die Integration deaktivieren, können Sie einen Datensatz in einer Umgebung löschen, ohne ihn in der anderen zu löschen. Wenn Sie die Integration wieder aktivieren, wird der Datensatz in der Umgebung, in der er nicht gelöscht wurde, wieder mit der Umgebung synchronisiert, in der er gelöscht worden ist. Die Synchronisierung beginnt erneut, wenn die **Dataverse-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**.

> [!WARNING]
> Stellen Sie beim Deaktivieren der Datenintegration sicher, dass Sie nicht denselben Datensatz in beiden Umgebungen bearbeiten. Wenn Sie die Integration wieder aktivieren, wird der zuletzt bearbeitete Datensatz synchronisiert. Wenn Sie in beiden Umgebungen nicht dieselben Änderungen am Datensatz vorgenommen haben, kann dies zu Datenverlusten führen.

## <a name="access-the-dataverse-integration-page"></a>Zugreifen auf die Dataverse-Integrationsseite

1. In der Human Resources-Instanz, in der Sie Einstellungen für die Integration mit Dataverse anzeigen oder konfigurieren möchten, wählen Sie die Kachel **Systemverwaltung** aus.

    [![Systemverwaltung-Kachel.](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Wählen Sie die Registerkarte **Links**.

    [![Registerkarte „Links“.](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Wählen Sie unter **Integrationen** **Dataverse-Konfiguration** aus.

    [![Dataverse-Konfigurationslink.](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Aktivieren oder Deaktivieren der Integration zwischen Human Resources und Dataverse

- Um die Integration zu aktivieren, setzen Sie die Option **Dataverse-Integration aktivieren** auf der Seite **Microsoft Dataverse-Integration** auf **Ja**.

    > [!NOTE]
    > Wenn Sie die Integration aktivieren, werden die Daten das nächsten Mal synchronisiert, wenn die **Dataverse-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**. Alle Daten sollten nach Abschluss des Batchauftrags verfügbar sein.

- Um die Integration zu deaktivieren, setzen Sie die Option auf **Nein**.

[![Aktivieren/Deaktivieren der Dataverse-Integration.](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Wir empfehlen dringend, die Dataverse Integration während Datenmigrationsaufgaben auszuschalten. Das Hochladen großer Datenmengen kann die Leistung erheblich beeinträchtigen. Das Hochladen von 2.000 Mitarbeitern kann beispielsweise mehrere Stunden dauern, wenn die Integration aktiviert ist, aber weniger als eine Stunde, wenn sie deaktiviert ist. Die in diesem Beispiel angegebenen Zahlen dienen nur zu Demonstrationszwecken. Die genaue Zeit, die zum Importieren von Datensätzen benötigt wird, kann aufgrund vieler Faktoren stark variieren.

## <a name="view-data-integration-details"></a>Datenintegrationsdetails anzeigen

Auf dem Inforegister **Verwaltung** der Seite **Microsoft Dataverse-Integration** können Sie sehen, wie Zeilen zwischen Human Resources und Dataverse verknüpft sind.

- Um die Zeilen für eine Tabelle anzuzeigen, wählen Sie die Tabelle im Feld **Dataverse-Tabelle**. Das Raster zeigt alle Zeilen an, die mit der ausgewählten Tabelle verknüpft sind.

> [!NOTE]
> Nicht alle Dataverse-Tabellen sind derzeit aufgelistet. Im Raster werden nur Tabellen angezeigt, die die Verwendung benutzerdefinierter Felder unterstützen. Durch fortlaufende Releases von Human Resources werden neue Tabellen verfügbar.

Das Raster enthält die folgenden Felder:

- **Dataverse-Tabelle** – Der Name der Tabelle in Dataverse.
- **Dataverse-Tabellenreferenz** – Der Bezeichner, den Dataverse verwendet, um einen Datensatz zu identifizieren. Dieser Wert entspricht einem **RecId**-Wert von Human Resources. Den Bezeichner finden Sie beim Öffnen der Dataverse-Tabelle in Microsoft Excel.
- **Name der Human Resources-Entität** – Die Human Resources-Entität, die zuletzt Daten mit dem Dataverse synchronisiert hat. Die Entität kann entweder das Dataverse-Präfix oder ein anderes Präfix haben.
- **Human Resources-Referenz** – Der **RecId**-Wert, der mit dem Datensatz in Human Resources verknüpft wird.
- **Aus Dataverse gelöscht** – Ein Wert, der angibt, ob die Zeile aus Dataverse gelöscht wurde.

> [!NOTE]
> Datensätze in der Human Resources entsprechen den Zeilen in Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Entfernen der Zuordnung eines Human Resources-Datensatzes aus einer Dataverse-Zeile

Wenn bei der Datensynchronisierung zwischen Human Resources und Dataverse Probleme auftreten, können Sie diese möglicherweise beheben, indem Sie die Nachverfolgung löschen und die Nachverfolgungstabelle erneut synchronisieren. Wenn Sie die Zuordnung entfernen und dann eine Zeile in Dataverse ändern oder löschen, werden die Änderungen nicht mit Human Resources synchronisiert. Wenn Sie Änderungen in Human Resources vornehmen, wird ein neuer Nachverfolgungsdatensatz erstellt und die Zeile in Dataverse aktualisiert.

- Zum Entfernen der Zuordnung eines Human Resources-Datensatzes und einer Dataverse-Zeile wählen Sie die Tabelle im **Dataverse-Tabelle**-Feld aus und klicken dann auf die Option **Nachverfolgungsinformationen löschen**.

[![Nachverfolgungsinformationen löschen.](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Informationen zum Ausführen einer vollständigen Synchronisierung für die Tabelle nach dem Löschen der Nachverfolgung finden Sie in der nächsten beschriebenen Prozedur.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Synchronisieren einer Tabelle zwischen Human Resources und Dataverse

Verwenden Sie dieses Verfahren, wenn:

- Änderungen von Dataverse dauern zu lange, um in der Personalabteilung zu erscheinen.

- Sie müssen die Tracking-Tabelle aktualisieren, nachdem Sie das Tracking gelöscht haben.

So führen Sie eine vollständige Synchronisierung für eine Tabelle zwischen Human Resources und Dataverse ::

1. Wählen Sie im **Dataverse-Tabelle**-Feld die Tabelle aus.

2. Wählen **Jetzt synchronisieren**.

[![Ausführen einer vollständigen Synchronisierung.](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Siehe auch

[Dataverse-Tabellen](hr-developer-entities.md)<br>
[Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Virtuelle Human Resources-Tabellen – Häufig gestellte Fragen](hr-admin-virtual-entity-faq.md)<br>
[Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologie-Updates](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
