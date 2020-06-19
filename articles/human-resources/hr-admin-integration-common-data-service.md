---
title: Common Data Service-Integration konfigurieren
description: Sie können die Integration zwischen Common Data Service und Dynamics 365 Human Resources aktivieren und deaktivieren. Sie können auch die Synchronisierungsdetails anzeigen, Nachverfolgungsdaten löschen und eine Entität erneut synchronisieren, um Datenprobleme zwischen den beiden Umgebungen zu beheben.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aad8217d48917d6855046a6810fe994f5564d94
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431313"
---
# <a name="configure-common-data-service-integration"></a>Common Data Service-Integration konfigurieren

Sie können die Integration zwischen Common Data Service und Dynamics 365 Human Resources aktivieren und deaktivieren. Sie können auch die Synchronisierungsdetails anzeigen, Nachverfolgungsdaten löschen und eine Entität erneut synchronisieren, um Datenprobleme zwischen den beiden Umgebungen zu beheben.

Wenn Sie die Integration deaktivieren, können Benutzer Änderungen in Human Resources oder Common Data Service vornehmen, diese Änderungen werden jedoch nicht zwischen den beiden Umgebungen synchronisiert.

Standardmäßig ist die Integration zwischen Human Resources und Common Data Service deaktiviert.

Möglicherweise möchten Sie die Integration in den folgenden Situationen deaktivieren:

- Sie geben Daten über das Data Management Framework ein und müssen die Daten mehrmals importieren, um sie in einen korrekten Zustand zu versetzen.

- Es gibt Probleme mit Daten in Human Resources oder Common Data Service. Wenn Sie die Integration deaktivieren, können Sie einen Datensatz in einer Umgebung löschen, ohne ihn in der anderen zu löschen. Wenn Sie die Integration wieder aktivieren, wird der Datensatz in der Umgebung, in der er nicht gelöscht wurde, wieder mit der Umgebung synchronisiert, in der er gelöscht worden ist. Die Synchronisierung beginnt erneut, wenn die **Common Data Service-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**.

> [!WARNING]
> Stellen Sie beim Deaktivieren der Datenintegration sicher, dass Sie nicht denselben Datensatz in beiden Umgebungen bearbeiten. Wenn Sie die Integration wieder aktivieren, wird der zuletzt bearbeitete Datensatz synchronisiert. Wenn Sie in beiden Umgebungen nicht dieselben Änderungen am Datensatz vorgenommen haben, kann dies zu Datenverlusten führen.

## <a name="access-the-common-data-service-integration-page"></a>Zugreifen auf die Common Data Service-Integrationsseite

1. In der Human Resources-Instanz, in der Sie Einstellungen für die Integration mit Common Data Service anzeigen oder konfigurieren möchten, wählen Sie die Kachel **Systemverwaltung** aus.

    [![Systemverwaltung-Kachel](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Wählen Sie die Registerkarte **Links**.

    [![Registerkarte „Links“](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Wählen Sie unter **Integrationen** **Common Data Service-Konfiguration** aus.

    [![Common Data Service-Konfigurationslink](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Aktivieren oder Deaktivieren der Integration zwischen Human Resources und Common Data Service

- Um die Integration zu aktivieren, setzen Sie die Option für **Aktivieren der Integration in Common Data Service** auf **Ja**.

    > [!NOTE]
    > Wenn Sie die Integration aktivieren, werden die Daten das nächsten Mal synchronisiert, wenn die **Common Data Service-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**. Alle Daten sollten nach Abschluss des Batchauftrags verfügbar sein.

- Um die Integration zu deaktivieren, setzen Sie die Option auf **Nein**.

[![Aktivieren/Deaktivieren der Common Data Service-Integration](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Datenintegrationsdetails anzeigen

Auf dem Inforegister **Verwaltung** der Seite **Common Data Service-Integration** können Sie sehen, wie Datensätze zwischen Human Resources und Common Data Service verknüpft sind.

- Um die Datensätze für eine Entität anzuzeigen, wählen Sie die Entität im Feld **CDS-Entitätsname** aus. Das Raster zeigt alle Datensätze an, die mit der ausgewählten Entität verknüpft sind.

[![Anzeigen der Datensätze für eine Entität](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Nicht alle Common Data Service-Unternehmen sind derzeit aufgelistet. Im Raster werden nur Entitäten angezeigt, die die Verwendung benutzerdefinierter Felder unterstützen. Durch fortlaufende Releases von Human Resources werden neue Entitäten verfügbar.

Das Raster enthält die folgenden Felder:

- **CDS-Entitätsname** – Der Name der Entität in Common Data Service.
- **CDS-Entitätsreferenz** – Die Kennung, die Common Data Service verwendet, um einen Datensatz zu identifizieren. Dieser Wert entspricht einem **RecId**-Wert von Human Resources. Die Kennung finden Sie beim Öffnen der Common Data Service-Einheit in Microsoft Excel.
- **Name der Human Resources-Entität** – Die Entität, die zuletzt Daten mit dem Common Data Service synchronisiert hat. Die Entität kann entweder das Common Data Service-Präfix oder ein anderes Präfix haben.
- **Human Resources-Referenz** – Der **RecId**-Wert, der mit dem Datensatz in Human Resources verknüpft wird.
- **Wurde aus CDS gelöscht** – Ein Wert, der angibt, ob der Datensatz aus Common Data Service gelöscht wurde.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Entfernen der Zuordnung eines Datensatzes in Human Resources aus Common Data Service

Wenn bei der Datensynchronisierung zwischen Human Resources und Common Data Service Probleme auftreten, können Sie diese möglicherweise beheben, indem Sie die Nachverfolgung löschen und die Nachverfolgungstabelle erneut synchronisieren. Wenn Sie die Zuordnung entfernen und dann einen Datensatz in Common Data Service ändern oder löschen, werden die Änderungen nicht mit Human Resources synchronisiert. Wenn Sie Änderungen in Human Resources vornehmen, wird ein neuer Nachverfolgungsdatensatz erstellt und der Datensatz in Common Data Service aktualisiert.

- Zum Entfernen der Zuordnung eines Datensatzes zwischen Human Resources und Common Data Service wählen Sie die Entität im Feld **CDS-Entitätsname** aus und klicken dann auf die Option für **Nachverfolgungsinformationen löschen**.

[![Nachverfolgungsinformationen löschen](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Informationen zum Ausführen einer vollständigen Synchronisierung für die Entität nach dem Löschen der Nachverfolgung finden Sie in der nächsten beschriebenen Prozedur.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Synchronisieren einer Entität zwischen Human Resources und Common Data Service

Verwenden Sie dieses Verfahren, wenn:

- Änderungen von Common Data Service dauern zu lange, um in der Personalabteilung zu erscheinen.

- Sie müssen die Tracking-Tabelle aktualisieren, nachdem Sie das Tracking gelöscht haben.

So führen Sie eine vollständige Synchronisierung für eine Entität zwischen Human Resources und Common Data Service ::

1. Wählen Sie die Entität im Feld **CDS Entitätsname** aus.

2. Wählen **Jetzt synchronisieren**.

[![Ausführen einer vollständigen Synchronisierung](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


