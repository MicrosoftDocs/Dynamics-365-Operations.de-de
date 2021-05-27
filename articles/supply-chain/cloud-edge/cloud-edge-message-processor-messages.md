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
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021054"
---
# <a name="message-processor-messages"></a><span data-ttu-id="0acd3-103">Nachrichtenverarbeitungsmeldungen</span><span class="sxs-lookup"><span data-stu-id="0acd3-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0acd3-104">Nachrichten des Nachrichtenprozessors werden beim Ausführen von Cloud- und Edge-Scale-Units für [Fertigungs-Workloads](cloud-edge-workload-manufacturing.md) und [Workloads der Lagerortverwaltung](cloud-edge-workload-warehousing.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0acd3-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="0acd3-105">Eine große Menge an Daten wird zwischen den Umgebungen des Hubs und der bereitgestellten Scale-Unit ausgetauscht, um sie synchron zu halten, aber nur ein Teil dieses Datenaustauschs wird vom *Nachrichtenprozessor* verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0acd3-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="0acd3-106">Sie können die vom Nachrichtenprozessor verarbeiteten Nachrichten einsehen, indem Sie zu **Systemverwaltung > Nachrichtenprozessor > Nachrichtenprozessor-Meldungen** gehen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="0acd3-107">Spalten des Nachrichten-Rasters und Filter</span><span class="sxs-lookup"><span data-stu-id="0acd3-107">Message grid columns and filters</span></span>

<span data-ttu-id="0acd3-108">Sie können die Felder oben auf der Seite **Nachrichtenprozessor-Meldungen** verwenden, um bestimmte Nachrichten zu finden, die Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="0acd3-109">Die meisten dieser Filter entsprechen den Spaltenüberschriften im Nachrichten-Raster.</span><span class="sxs-lookup"><span data-stu-id="0acd3-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="0acd3-110">Die folgenden Filter und Spaltenüberschriften sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="0acd3-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="0acd3-111">**Nachrichtentyp** – Gibt den Typ der Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="0acd3-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="0acd3-112">**Nachrichtenwarteschlange** – Gibt den Namen der Warteschlange an, in der die Nachricht verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0acd3-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="0acd3-113">Die folgenden Warteschlangen sind vorhanden:</span><span class="sxs-lookup"><span data-stu-id="0acd3-113">The following queues are provided:</span></span>
  - <span data-ttu-id="0acd3-114">*Skalierungseinheit zu Hub*</span><span class="sxs-lookup"><span data-stu-id="0acd3-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="0acd3-115">*Hub-zu-Lagerort-Ausführungsskalierungseinheit*</span><span class="sxs-lookup"><span data-stu-id="0acd3-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="0acd3-116">*Hub-zu-Fertigung-Ausführungsskalierungseinheit*</span><span class="sxs-lookup"><span data-stu-id="0acd3-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="0acd3-117">**Nachrichtenstatus** – Gibt den Status der Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="0acd3-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="0acd3-118">Die folgenden Zustände sind vorhanden:</span><span class="sxs-lookup"><span data-stu-id="0acd3-118">The following states exists:</span></span>
  - <span data-ttu-id="0acd3-119">*Warteschlange* – Die Nachricht ist bereit, vom Nachrichtenprozessor verarbeitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="0acd3-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="0acd3-120">*Verarbeitet* – Die Nachricht wurde erfolgreich vom Nachrichtenprozessor verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0acd3-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="0acd3-121">*Abgebrochen* – Die Nachricht wurde verarbeitet, aber die Verarbeitung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="0acd3-122">**Nachrichteninhalt** – Dieser Filter führt eine Volltextsuche im Inhalt der Nachricht durch.</span><span class="sxs-lookup"><span data-stu-id="0acd3-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="0acd3-123">(Der Inhalt von Nachrichten wird im Raster nicht angezeigt.) Der Filter behandelt die meisten Sonderzeichen (z. B. „-“) als Leerzeichen und behandelt alle Leerzeichen als boolesche ODER-Operatoren.</span><span class="sxs-lookup"><span data-stu-id="0acd3-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="0acd3-124">T=Wenn Sie z.B. nach einem bestimmten `journalid`-Wert gleich „USMF-123456“ suchen, findet das System alle Nachrichten, die „USMF“ oder „123456“ enthalten, was wahrscheinlich eine lange Liste sein wird.</span><span class="sxs-lookup"><span data-stu-id="0acd3-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="0acd3-125">Daher wäre es besser, nur „123456“ einzugeben, weil das spezifischere Ergebnisse liefert.</span><span class="sxs-lookup"><span data-stu-id="0acd3-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="0acd3-126">Beispiel Nachrichtentyp: Finanzaktualisierung der Bestandsanpassung anfordern</span><span class="sxs-lookup"><span data-stu-id="0acd3-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="0acd3-127">Zum Beispiel wird der **Nachrichtentyp** *Anforderung Bestandsanpassung Finanzaktualisierung* verwendet, um ein Zähljournal auf dem Hub zu erstellen und zu buchen, wenn eine Arbeitskraft die Lager-App verwendet, um [eine Bestandsanpassung](cloud-edge-warehouse-inventory-adjustment.md) in einem Scale-Unit-Lagerortverwaltung Workload zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0acd3-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="0acd3-128">Da dieser spezielle Prozess von einer Scale-Unit ausgeht, wird im Feld **Meldungswarteschlange** der Wert *Scale-Unit an Hub* angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0acd3-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="0acd3-129">Für diesen Nachrichtentyp zeichnet ein Scale-Unit Workload den Datensatz als Teil eines Vorgangs zur Anpassung des Lagerort-App-Bestands auf.</span><span class="sxs-lookup"><span data-stu-id="0acd3-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="0acd3-130">Die Daten der Nachricht werden dann im Rahmen des gleichen Prozesses, der für die [Commerce Data Exchange-Architektur](../../commerce/commerce-architecture.md) verwendet wird, an den Hub übertragen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="0acd3-131">Die Nachricht wird aktualisiert, um den **Nachrichtenstatus** als *Warteschlange* anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="0acd3-132">Der Nachrichtenprozessor versucht dann, die Nachricht zu verarbeiten und aktualisiert den **Status der Nachricht** auf *Bearbeitet* bei Erfolg oder *Abgebrochen* bei Misserfolg.</span><span class="sxs-lookup"><span data-stu-id="0acd3-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="0acd3-133">Anzeigen des Nachrichtenprotokolls, des Inhalts von Nachrichten und der Details</span><span class="sxs-lookup"><span data-stu-id="0acd3-133">View the message log, message content, and details</span></span>

<span data-ttu-id="0acd3-134">Sie können detaillierte Informationen zu einer Nachricht finden, indem Sie sie im Raster auswählen und dann die Register **Protokoll** oder **Nachrichteninhalt** unter dem Nachrichtenraster öffnen, wo jedes verarbeitete Ereignis angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0acd3-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="0acd3-135">Der **Nachrichteninhalt** hängt vom **Nachrichtentyp** ab und wird daher eine unterschiedliche Textlänge haben.</span><span class="sxs-lookup"><span data-stu-id="0acd3-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="0acd3-136">Ein typischer Inhaltstext einer Nachricht beginnt mit einem **{** und endet mit einem **}** und hat dazwischen Feldnamen wie `journalId` gefolgt von einem **:** und einem Wert wie *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="0acd3-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="0acd3-137">Die Symbolleiste auf der Registerkarte **Protokoll** enthält die folgenden Schaltflächen:</span><span class="sxs-lookup"><span data-stu-id="0acd3-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="0acd3-138">**Protokoll** – Zeigt die Verarbeitungsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="0acd3-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="0acd3-139">Dies ist besonders hilfreich, um die Gründe für einen Verarbeitungsfehler bei Nachrichten mit einem **Verarbeitungsergebnis** von *Fehlgeschlagen* zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="0acd3-140">**Bündel** – Mehrere Vorgänge zur Verarbeitung von Nachrichten können als Teil desselben Batch-Prozesses ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0acd3-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="0acd3-141">Wählen Sie diese Schaltfläche, um diese detaillierten Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="0acd3-142">Sie können z. B. sehen, ob Abhängigkeiten bestehen, die es erforderlich machen, dass das System bestimmte Nachrichten in einer bestimmten Sequenz verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0acd3-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="0acd3-143">Nachrichten-Prozessor Batchauftrag</span><span class="sxs-lookup"><span data-stu-id="0acd3-143">Message processor batch job</span></span>

<span data-ttu-id="0acd3-144">Wenn Sie eine Cloud- und Edge-Bereitstellung ausführen, wird der Batchauftrag *Nachrichtenprozessor* automatisch aufgerufen, wenn eine neue Nachricht zur Verarbeitung erstellt wird, so dass Sie diesen Auftrag nicht manuell planen müssen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="0acd3-145">Falls nötig, können Sie auf den Batch-Auftrag zugreifen, indem Sie zu **Systemadministration > Nachrichtenprozessor > Nachrichtenprozessor** gehen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="0acd3-146">Manuelles Verarbeiten oder Stornieren einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="0acd3-146">Manually process or cancel a message</span></span>

<span data-ttu-id="0acd3-147">Bei Bedarf können Sie eine Nachricht manuell verarbeiten oder abbrechen, abhängig von ihrem aktuellen Status.</span><span class="sxs-lookup"><span data-stu-id="0acd3-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="0acd3-148">Markieren Sie dazu die Nachricht im Raster und wählen Sie dann **Verarbeiten** oder **Abbrechen** im Aktivitätsbereich</span><span class="sxs-lookup"><span data-stu-id="0acd3-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="0acd3-149">Festlegen von Ereignissen, um Warnungen für fehlgeschlagene Verarbeitungen zu liefern</span><span class="sxs-lookup"><span data-stu-id="0acd3-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="0acd3-150">Zusätzlich zur Filterung auf den **Nachrichtenstatus**-Wert *Abgebrochen*, um nach fehlgeschlagenen Nachrichten zu fragen, können Sie [Geschäftsereignisse](../../fin-ops-core/dev-itpro/business-events/home-page.md) auf dem Hub festlegen, die Sie über fehlgeschlagene Verarbeitungsergebnisse informieren.</span><span class="sxs-lookup"><span data-stu-id="0acd3-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="0acd3-151">Aktivieren Sie dazu das Ereignis mit dem Namen *Nachrichtenprozessor Nachricht verarbeitet* auf der Seite **Veranstaltungskatalog** (**Systemadministration > Einrichten > Veranstaltungen > Veranstaltungskatalog**).</span><span class="sxs-lookup"><span data-stu-id="0acd3-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="0acd3-152">Als Teil des Aktivierungsprozesses werden Sie angeleitet, anzugeben, ob das Ereignis spezifisch für eine oder alle juristischen Entitäten ist und einen **Endpunktnamen** anzugeben, der zuerst definiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0acd3-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="0acd3-153">Wenn **Wenn ein Ereignis eintritt** auf *Microsoft Power Automate* festgelegt ist (und nicht z. B. auf *HTTPS*), wird der **Endpunktname** automatisch im Supply Chain Management erstellt, basierend auf der *Microsoft Power Automate* Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="0acd3-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="0acd3-154">Microsoft Power Automate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="0acd3-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="0acd3-155">In diesem Beispiel verwenden Sie **Wenn ein Ereignis eintritt** mit *Microsoft Power Automate* sendet E-Mails mit InfoLog-Meldungen und Hyperlinks zum Öffnen der Seite **Meldungen des Nachrichtenprozessors** für eine bestimmte fehlgeschlagene Nachricht auf dem Hub-Einsatz.</span><span class="sxs-lookup"><span data-stu-id="0acd3-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="0acd3-156">Bei Bedarf können Sie zusätzliche Logik hinzufügen, um die Benachrichtigungen parallel über verschiedene Kanäle zu senden und die Empfänger anhand der Ereignisdaten zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0acd3-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="0acd3-157">Erstellen Sie in [Power Automate](https://preview.flow.microsoft.com) einen neuen automatisierten Cloud-Flow für den Flow-Auslöser **Wenn ein Geschäftsereignis eintritt – Fin & Ops App (Dynamics 365)**, gefolgt von den Schritten **JSON auslesen** und **E-Mail senden**, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0acd3-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate Automatisierter Cloud-Flow":::

1. <span data-ttu-id="0acd3-159">Im Schritt **Wenn ein Ereignis eintritt** können Sie den Hub **Instanz** nachschlagen oder eingeben, gefolgt von der **Kategorie** und dann dem **Geschäftsereignis** *Nachrichtenprozessor Nachricht verarbeitet*, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0acd3-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Wenn ein Ereignis eintritt Schritt":::

1. <span data-ttu-id="0acd3-161">Geben Sie für den Schritt **Parse JSON** ein **Schema** ein, das die erweiterten Felder definiert.</span><span class="sxs-lookup"><span data-stu-id="0acd3-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="0acd3-162">Sie können die Option *Schema herunterladen* auf der Seite **Terminkatalog** im Supply Chain Management verwenden oder mit dem Einfügen des Beispiel-Schematextes beginnen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="0acd3-163">Dieser Beispieltext wird nach der folgenden Illustration bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0acd3-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Schritt „JSON parsen“":::

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

1. <span data-ttu-id="0acd3-165">Im Schritt **E-Mail senden** können Sie die einzelnen Felder auswählen oder mit dem Einfügen des Beispiels für den E-Mail-Text in das Feld **Körper** beginnen.</span><span class="sxs-lookup"><span data-stu-id="0acd3-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="0acd3-166">Dieses Beispiel wird nach der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0acd3-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate Eine E-Mail senden Schritt":::

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

1. <span data-ttu-id="0acd3-168">Wenn Sie das Ereignis speichern, wird es automatisch aktiviert und ist als Teil vom Supply Chain Management einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="0acd3-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
