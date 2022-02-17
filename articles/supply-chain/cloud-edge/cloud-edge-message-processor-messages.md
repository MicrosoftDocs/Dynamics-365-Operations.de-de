---
title: Nachrichtenverarbeitungsmeldungen
description: Dieses Thema enthält Informationen über die Funktion Nachrichtenprozessor-Nachrichten für Scale-Unit Workloads.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 68db4c6561f2cc3fcfd64b49da59a4cc164685f2
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069428"
---
# <a name="message-processor-messages"></a>Nachrichtenverarbeitungsmeldungen

[!include [banner](../includes/banner.md)]

Nachrichten des Nachrichtenprozessors werden beim Ausführen von Cloud- und Edge-Scale-Units für [Fertigungs-Workloads](cloud-edge-workload-manufacturing.md) und [Workloads der Lagerortverwaltung](cloud-edge-workload-warehousing.md) verwendet.

Die Umgebungen, in denen Hub und Scale-Unit bereitgestellt werden, tauschen eine große Menge an Daten aus, um synchron zu bleiben. Einige der ausgetauschten Daten werden zusätzliche Logik im *Nachrichtenprozessor* auslösen. Sie können die Nachrichten einsehen, die vom Nachrichtenprozessor verarbeitet wurden, indem Sie zu **Systemverwaltung > Nachrichtenprozessor > Nachrichten des Nachrichtenprozessors** gehen.

## <a name="message-grid-columns-and-filters"></a>Spalten des Nachrichten-Rasters und Filter

Sie können die Felder oben auf der Seite **Nachrichtenprozessor-Meldungen** verwenden, um bestimmte Nachrichten zu finden, die Sie suchen. Die meisten dieser Filter entsprechen den Spaltenüberschriften im Nachrichten-Raster. Die folgenden Filter und Spaltenüberschriften sind verfügbar:

- **Nachrichtentyp** – Gibt den Typ der Nachricht an.
- **Nachrichtenwarteschlange** – Gibt den Namen der Warteschlange an, in der die Nachricht verarbeitet werden soll. Die folgenden Warteschlangen sind vorhanden:
  - *Skalierungseinheit zu Hub*
  - *Hub-zu-Lagerort-Ausführungsskalierungseinheit*
  - *Hub-zu-Fertigung-Ausführungsskalierungseinheit*
- **Nachrichtenstatus** – Gibt den Status der Nachricht an. Die folgenden Zustände sind vorhanden:
  - *Warteschlange* – Die Nachricht ist bereit, vom Nachrichtenprozessor verarbeitet zu werden.
  - *Verarbeitet* – Die Nachricht wurde erfolgreich vom Nachrichtenprozessor verarbeitet.
  - *Abgebrochen* – Die Nachricht wurde verarbeitet, aber die Verarbeitung ist fehlgeschlagen.
- **Nachrichteninhalt** – Dieser Filter führt eine Volltextsuche im Inhalt der Nachricht durch. (Der Inhalt von Nachrichten wird im Raster nicht angezeigt.) Der Filter behandelt die meisten Sonderzeichen (z. B. „-“) als Leerzeichen und behandelt alle Leerzeichen als boolesche ODER-Operatoren. Wenn Sie z. B. nach einem bestimmten `journalid`-Wert gleich „USMF-123456“ suchen, findet das System alle Nachrichten, die „USMF“ oder „123456“ enthalten, was wahrscheinlich eine lange Liste sein wird. Daher wäre es besser, nur „123456“ einzugeben, weil das spezifischere Ergebnisse liefert.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Beispiel Nachrichtentyp: Finanzaktualisierung der Bestandsanpassung anfordern

Zum Beispiel wird der **Nachrichtentyp** *Anforderung Bestandsanpassung Finanzaktualisierung* verwendet, um ein Zähljournal auf dem Hub zu erstellen und zu buchen, wenn eine Arbeitskraft die Lager-App verwendet, um [eine Bestandsanpassung](cloud-edge-warehouse-inventory-adjustment.md) in einem Scale-Unit-Lagerortverwaltung Workload zu registrieren. Da dieser spezielle Prozess von einer Scale-Unit ausgeht, wird im Feld **Meldungswarteschlange** der Wert *Scale-Unit an Hub* angezeigt.

Für diesen Nachrichtentyp zeichnet ein Scale-Unit Workload den Datensatz als Teil eines Vorgangs zur Anpassung des Lagerort-App-Bestands auf. Die Daten der Nachricht werden dann im Rahmen des gleichen Prozesses, der für die [Commerce Data Exchange-Architektur](../../commerce/commerce-architecture.md) verwendet wird, an den Hub übertragen. Die Nachricht wird aktualisiert, um den **Nachrichtenstatus** als *Warteschlange* anzuzeigen. Der Nachrichtenprozessor versucht dann, die Nachricht zu verarbeiten und aktualisiert den **Status der Nachricht** auf *Bearbeitet* bei Erfolg oder *Abgebrochen* bei Misserfolg.

## <a name="view-the-message-log-message-content-and-details"></a>Anzeigen des Nachrichtenprotokolls, des Inhalts von Nachrichten und der Details

Sie können detaillierte Informationen zu einer Nachricht finden, indem Sie sie im Raster auswählen und dann die Register **Protokoll** oder **Nachrichteninhalt** unter dem Nachrichtenraster öffnen, wo jedes verarbeitete Ereignis angezeigt wird.

Der **Nachrichteninhalt** hängt vom **Nachrichtentyp** ab und wird daher eine unterschiedliche Textlänge haben. Ein typischer Inhaltstext einer Nachricht beginnt mit einem **{** und endet mit einem **}** und hat dazwischen Feldnamen wie `journalId` gefolgt von einem **:** und einem Wert wie *USMF-123456*.

Die Symbolleiste auf der Registerkarte **Protokoll** enthält die folgenden Schaltflächen:

- **Protokoll** – Zeigt die Verarbeitungsergebnisse an. Dies ist besonders hilfreich, um die Gründe für einen Verarbeitungsfehler bei Nachrichten mit einem **Verarbeitungsergebnis** von *Fehlgeschlagen* zu verstehen.
- **Bündel** – Mehrere Vorgänge zur Verarbeitung von Nachrichten können als Teil desselben Batch-Prozesses ausgeführt werden. Wählen Sie diese Schaltfläche, um diese detaillierten Daten anzuzeigen. Sie können z. B. sehen, ob Abhängigkeiten bestehen, die es erforderlich machen, dass das System bestimmte Nachrichten in einer bestimmten Sequenz verarbeitet.

## <a name="message-processor-batch-job"></a>Nachrichten-Prozessor Batchauftrag

Wenn Sie eine verteilte Hybridtopologie mit Skalierungseinheiten ausführen, wird der Batchauftrag *Nachrichtenprozessor* automatisch aufgerufen, wenn eine neue Nachricht zur Verarbeitung erstellt wird, so dass Sie diesen Auftrag nicht manuell planen müssen.

Falls nötig, können Sie auf den Batch-Auftrag zugreifen, indem Sie zu **Systemadministration > Nachrichtenprozessor > Nachrichtenprozessor** gehen.

## <a name="manually-process-or-cancel-a-message"></a>Manuelles Verarbeiten oder Stornieren einer Nachricht

Bei Bedarf können Sie eine Nachricht manuell verarbeiten oder abbrechen, abhängig von ihrem aktuellen Status. Markieren Sie dazu die Nachricht im Raster und wählen Sie dann **Verarbeiten** oder **Abbrechen** im Aktivitätsbereich

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Festlegen von Ereignissen, um Warnungen für fehlgeschlagene Verarbeitungen zu liefern

Zusätzlich zur Filterung auf den **Nachrichtenstatus**-Wert *Abgebrochen*, um nach fehlgeschlagenen Nachrichten zu fragen, können Sie [Geschäftsereignisse](../../fin-ops-core/dev-itpro/business-events/home-page.md) auf dem Hub festlegen, die Sie über fehlgeschlagene Verarbeitungsergebnisse informieren. Aktivieren Sie dazu das Ereignis mit dem Namen *Nachrichtenprozessor Nachricht verarbeitet* auf der Seite **Veranstaltungskatalog** (**Systemadministration > Einrichten > Veranstaltungen > Veranstaltungskatalog**).

Als Teil des Aktivierungsprozesses werden Sie angeleitet, anzugeben, ob das Ereignis spezifisch für eine oder alle juristischen Entitäten ist und einen **Endpunktnamen** anzugeben, der zuerst definiert werden muss.

>[!NOTE]
> Wenn **Wenn ein Ereignis eintritt** auf *Microsoft Power Automate* festgelegt ist (und nicht z. B. auf *HTTPS*), wird der **Endpunktname** automatisch im Supply Chain Management erstellt, basierend auf der *Microsoft Power Automate* Einrichtung.

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate-Beispiel

In diesem Beispiel verwenden Sie **Wenn ein Ereignis eintritt** mit *Microsoft Power Automate* sendet E-Mails mit InfoLog-Meldungen und Hyperlinks zum Öffnen der Seite **Meldungen des Nachrichtenprozessors** für eine bestimmte fehlgeschlagene Nachricht auf dem Hub-Einsatz. Bei Bedarf können Sie zusätzliche Logik hinzufügen, um die Benachrichtigungen parallel über verschiedene Kanäle zu senden und die Empfänger anhand der Ereignisdaten zu steuern.

1. Erstellen Sie in [Power Automate](https://preview.flow.microsoft.com) einen neuen automatisierten Cloud-Flow für den Flow-Auslöser **Wenn ein Geschäftsereignis eintritt – Fin & Ops App (Dynamics 365)**, gefolgt von den Schritten **JSON auslesen** und **E-Mail senden**, wie in der folgenden Abbildung dargestellt.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate Automatisierter Cloud-Flow.":::

1. Im Schritt **Wenn ein Ereignis eintritt** können Sie den Hub **Instanz** nachschlagen oder eingeben, gefolgt von der **Kategorie** und dann dem **Geschäftsereignis** *Nachrichtenprozessor Nachricht verarbeitet*, wie in der folgenden Abbildung gezeigt.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate-Schritt „Wenn ein Ereignis eintritt“.":::

1. Geben Sie für den Schritt **Parse JSON** ein **Schema** ein, das die erweiterten Felder definiert. Sie können die Option *Schema herunterladen* auf der Seite **Terminkatalog** im Supply Chain Management verwenden oder mit dem Einfügen des Beispiel-Schematextes beginnen. Dieser Beispieltext wird nach der folgenden Illustration bereitgestellt.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate-Schritt „JSON parsen“.":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. Im Schritt **E-Mail senden** können Sie die einzelnen Felder auswählen oder mit dem Einfügen des Beispiels für den E-Mail-Text in das Feld **Körper** beginnen. Dieses Beispiel wird nach der folgenden Abbildung dargestellt.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate-Schritt „Eine E-Mail senden“.":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Wenn Sie das Ereignis speichern, wird es automatisch aktiviert und ist als Teil vom Supply Chain Management einsatzbereit.
