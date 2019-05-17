---
title: Konsistenzprüfung für Einzelhandelstransaktionen
description: In diesem Thema werden die Funktionen der Konsistenzprüfung für Einzelhandelstransaktionen in Microsoft Dynamics 365 for Retail beschrieben.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517072"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="29957-103">Konsistenzprüfung für Einzelhandelstransaktionen</span><span class="sxs-lookup"><span data-stu-id="29957-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="29957-104">In diesem Thema werden die in Version 8.1.3 von Microsoft Dynamics 365 for Finance and Operations eingeführten Funktionen der Konsistenzprüfung für Einzelhandelstransaktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="29957-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="29957-105">Die Konsistenzprüfung ermittelt und isoliert inkonsistente Transaktionen, bevor sie im Aufstellungsbuchungsprozess verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="29957-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="29957-106">Wenn eine Aufstellung in Retail gebucht wird, kann die Buchung aufgrund der inkonsistenten Daten in den Einzelhandelstransaktionstabellen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="29957-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="29957-107">Die Datenfehler können durch unvorhergesehene Probleme in der Verkaufsstellenanwendung oder durch Fehler beim Importieren von Buchungen aus POS-Systemen von Drittanbietern auftreten.</span><span class="sxs-lookup"><span data-stu-id="29957-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="29957-108">Im Folgenden sind Beispiele für diese Inkonsistenzen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="29957-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="29957-109">Der Transaktionsgesamtbetrag in der Kopftabelle entspricht nicht dem Transaktionsgesamtbetrag der Positionen.</span><span class="sxs-lookup"><span data-stu-id="29957-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="29957-110">Die Positionsanzahl in der Kopftabelle entspricht nicht der Anzahl von Positionen in der Transaktionstabelle.</span><span class="sxs-lookup"><span data-stu-id="29957-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="29957-111">Die Steuern in der Kopftabelle stimmen nicht mit dem Steuerbetrag in den Positionen überein.</span><span class="sxs-lookup"><span data-stu-id="29957-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="29957-112">Wenn inkonsistente Transaktionen durch den Aufstellungsbuchungsprozess verarbeitet werden, werden inkonsistente Verkaufsrechnungen und Zahlungserfassungen erstellt, und der gesamte Aufstellungsbuchungsprozess schlägt anschließend fehl.</span><span class="sxs-lookup"><span data-stu-id="29957-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="29957-113">Das Wiederherstellen der Aufstellungen aus einem solchen Zustand umfasst komplexe Datenkorrekturen in mehreren Transaktionstabellen.</span><span class="sxs-lookup"><span data-stu-id="29957-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="29957-114">Die Konsistenzprüfung für Einzelhandelstransaktionen verhindert solche Probleme.</span><span class="sxs-lookup"><span data-stu-id="29957-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="29957-115">Das folgende Diagramm veranschaulicht den Buchungsprozess mit Transaktionskonsistenzprüfung.</span><span class="sxs-lookup"><span data-stu-id="29957-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="29957-116">![Aufstellungsbuchungsprozess mit der Konsistenzprüfung für Einzelhandelstransaktionen](./media/validchecker.png "Aufstellungsbuchungsprozess mit der Konsistenzprüfung für Einzelhandelstransaktionen")</span><span class="sxs-lookup"><span data-stu-id="29957-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="29957-117">Der **Geschäftsbuchungen überprüfen** Stapelverarbeitungsvorgang prüft die Konsistenz der Einzelhandelstransaktionstabellen für die folgenden Szenarien.</span><span class="sxs-lookup"><span data-stu-id="29957-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="29957-118">Debitorenkonto - überprüft, dass das Debitorenkonto in den Einzelhandelstransaktionstabellen in den HQ-Debitorenmasterdaten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29957-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="29957-119">Positionsanzahl – überprüft, dass die Positionsanzahl mit der Anzahl der Positionen in den Verkaufstransaktionstabellen übereinstimmt, wie diese in der Transaktionskopftabelle aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="29957-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="29957-120">Konsistenzprüfung einrichten</span><span class="sxs-lookup"><span data-stu-id="29957-120">Set up the consistency checker</span></span>
<span data-ttu-id="29957-121">Konfigurieren Sie den Stapelverarbeitungsvorgang „Geschäftsbuchungen überprüfen“ unter **Einzelhandel \> IT für den Einzelhandel \> POS-Buchung**, sodass er regelmäßig ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29957-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="29957-122">Der Stapelverarbeitungsauftrag kann basierend auf der Shoporganisationshierarchie in ähnlicher Weise wie die Funktionen zum Berechnen und Buchen im Stapel geplant werden.</span><span class="sxs-lookup"><span data-stu-id="29957-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="29957-123">Es wird empfohlen, diesen Stapelverarbeitungsauftrag so zu konfigurieren, dass mehrmals am Tag ausgeführt wird, und ihn so zu planen, dass er am Ende jeder P-Auftragsausführung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29957-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="29957-124">Ergebnisse des Überprüfungsprozesses</span><span class="sxs-lookup"><span data-stu-id="29957-124">Results of validation process</span></span>
<span data-ttu-id="29957-125">Die Ergebnisse der Überprüfung durch den Stapelverarbeitungsauftrag werden in der entsprechenden Einzelhandelstransaktion markiert.</span><span class="sxs-lookup"><span data-stu-id="29957-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="29957-126">Das Feld **Überprüfungsstatus** im Einzelhandelstransaktionsdatensatz wird entweder auf **Erfolgreich** oder **Fehler** festgelegt und das Datum der letzten Prüfungsausführung wird im Feld **Uhrzeit der letzten Überprüfung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29957-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="29957-127">Um eine ausführlichere Fehlerbeschreibung in Bezug auf einen Validierungsfehler zu erhalten, wählen Sie den entsprechenden Shoptransaktionsdatensatz aus und klicken auf die Schaltfläche **Überprüfungsfehler**.</span><span class="sxs-lookup"><span data-stu-id="29957-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="29957-128">Transaktionen mit Überprüfungsfehlern und noch nicht validierte Transaktionen werden nicht in Aufstellungen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="29957-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="29957-129">Während des Prozesses „Auszug berechnen“ werden Benutzer darüber informiert, wenn Transaktionen vorliegen, die in die Aufstellung aufgenommen hätten werden können, wo dies jedoch nicht der Fall war.</span><span class="sxs-lookup"><span data-stu-id="29957-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="29957-130">Wenn ein Überprüfungsfehler gefunden wird, können Sie ihn nur beheben, indem Sie sich an den Microsoft Support wenden.</span><span class="sxs-lookup"><span data-stu-id="29957-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="29957-131">In einer zukünftigen Version werden Funktionen hinzugefügt, mit denen Benutzer die Fehler, die in der Benutzeroberfläche erfolgten, in den Datensätzen selbst beheben können.</span><span class="sxs-lookup"><span data-stu-id="29957-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="29957-132">Es werden außerdem Protokollierungs- und Überwachungsfunktionen zur Nachverfolgung des Änderungsverlaufs bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="29957-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="29957-133">In zukünftigen Versionen werden zudem zusätzliche Validierungsregeln zur Unterstützung weiterer Szenarien hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="29957-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
