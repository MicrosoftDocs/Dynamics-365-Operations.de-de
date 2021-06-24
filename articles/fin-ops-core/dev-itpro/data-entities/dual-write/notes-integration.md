---
title: Integration von Notizen
description: In diesem Thema wird die Integration von Notizdaten in dualem Schreiben erläutert
author: RamaKrishnamoorthy
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186785"
---
# <a name="note-integration"></a><span data-ttu-id="ee686-103">Integration von Notizen</span><span class="sxs-lookup"><span data-stu-id="ee686-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ee686-104">Im Verlauf von Geschäftsprozessen sammeln Benutzer von Microsoft Dynamics 365 häufig Informationen über ihre Kunden.</span><span class="sxs-lookup"><span data-stu-id="ee686-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="ee686-105">Diese Informationen werden als Aktivitäten und Notizen aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ee686-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="ee686-106">In diesem Thema wird die Integration von Notizdaten in dualem Schreiben erläutert</span><span class="sxs-lookup"><span data-stu-id="ee686-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="ee686-107">Informationen über Kunden können folgendermaßen klassifiziert werden:</span><span class="sxs-lookup"><span data-stu-id="ee686-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="ee686-108">**Umsetzbare Informationen, die ein Dynamics 365-Benutzer im Auftrag eines Kunden bearbeitet** – Contoso (ein Dynamics 365-Benutzer) führt beispielsweise eine Spielshow durch.</span><span class="sxs-lookup"><span data-stu-id="ee686-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="ee686-109">Ein Kunde von Contoso (ein Debitor) möchte an der Spielshow teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="ee686-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="ee686-110">Der Kunde bittet einen Contoso-Mitarbeiter, einen Platz in der Spielshow für ihn zu buchen.</span><span class="sxs-lookup"><span data-stu-id="ee686-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="ee686-111">Die Buchung erfolgt im Veranstaltungskalender von Contoso.</span><span class="sxs-lookup"><span data-stu-id="ee686-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="ee686-112">**Umsetzbare Informationen für einen Dynamics 365-Benutzer** – Ein Kunde, der eine Surface-Einheit kauft, gibt beispielsweise spezielle Anweisungen ein, die darauf hinweisen, dass das Gerät vor der Lieferung in Geschenkverpackung verpackt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ee686-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="ee686-113">Diese Anweisungen sind umsetzbare Informationen, die von dem Contoso-Mitarbeiter bearbeitet werden sollten, der für die Verpackung verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="ee686-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="ee686-114">**Nicht umsetzbare Informationen** – Ein Kunde besucht beispielsweise das Contoso-Geschäft und zeigt während seines Gesprächs mit einem Shopmitarbeiter Interesse an *Halo*-Games und Gamingzubehör.</span><span class="sxs-lookup"><span data-stu-id="ee686-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="ee686-115">Der Shopmitarbeiter notiert diese Informationen.</span><span class="sxs-lookup"><span data-stu-id="ee686-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="ee686-116">Die Produktempfehlungsmodul nutzt sie dann, um dem Kunden Empfehlungen zu geben.</span><span class="sxs-lookup"><span data-stu-id="ee686-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="ee686-117">Im Allgemeinen werden umsetzbare Informationen als *Aktivitäten* in Finance and Operations- und Kundenbindungs-Apps erfasst.</span><span class="sxs-lookup"><span data-stu-id="ee686-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="ee686-118">Nicht umsetzbare Informationen werden in Finance and Operations-Apps als *Notizen* und in Kundenbindungs-Apps als *Anmerkungen* erfasst.</span><span class="sxs-lookup"><span data-stu-id="ee686-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="ee686-119">Obwohl Notizen für nicht umsetzbare Informationen gedacht sind, können Sie sie trotzdem zum Speichern und Verarbeiten von umsetzbaren Informationen in den Apps verwenden, wenn Sie es möchten.</span><span class="sxs-lookup"><span data-stu-id="ee686-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="ee686-120">Microsoft veröffentlicht derzeit Funktionen für die Integration von Notizen.</span><span class="sxs-lookup"><span data-stu-id="ee686-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="ee686-121">(Die Funktionalität zur Integration von Aktivitäten wird später veröffentlicht.) Die Notizintegration ist für Debitoren, Kreditoren, Aufträge und Bestellungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee686-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="ee686-122">Eine Notiz in einer Kundenbindungs-App erstellen</span><span class="sxs-lookup"><span data-stu-id="ee686-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="ee686-123">Befolgen Sie diese Schritte zum Erstellen einer Notiz in einer Kundenbindungs-App und anschließendem Synchronisieren mit einer Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="ee686-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ee686-124">Öffnen Sie in der Kundenbindungs-App den Kontodatensatz eines Debitoren.</span><span class="sxs-lookup"><span data-stu-id="ee686-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="ee686-125">Wählen Sie im Bereich **Zeitskala** das Pluszeichen (**+**) und anschließend **Notiz** aus, um eine Notiz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee686-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Erstellen einer Notiz in der Kundenbindungs-App](media/notes-ce-1.png)

3. <span data-ttu-id="ee686-127">Geben Sie einen Titel und eine Beschreibung ein, und wählen Sie anschließend **Notiz hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Eingeben eines Titels und einer Beschreibung](media/notes-ce-2.png)

    <span data-ttu-id="ee686-129">Die neue Notiz wird der Debitorenzeitskala hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ee686-129">The new note is added to the customer timeline.</span></span>

    ![Neuer Hinweis auf der Debitorenzeitskala](media/notes-ce-3.png)

4. <span data-ttu-id="ee686-131">Melden Sie sich bei der Finance and Operations-App, und öffnen Sie denselben Debitorendatensatz.</span><span class="sxs-lookup"><span data-stu-id="ee686-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="ee686-132">Beachten Sie, dass die **Anhänge**-Schaltfläche (Büroklammersymbol) in der oberen rechten Ecke anzeigt, dass der Datensatz einen Anhang hat.</span><span class="sxs-lookup"><span data-stu-id="ee686-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Benachrichtigung über einen Anhang](media/notes-ce-4.png)

5. <span data-ttu-id="ee686-134">Wählen Sie die **Anhänge**-Schaltfläche zum Öffnen der **Anhänge**-Seite aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="ee686-135">Sie sollten nun die erstellte Notiz in der Kundenbindungs-App finden.</span><span class="sxs-lookup"><span data-stu-id="ee686-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Notiz in der Kundenbindungs-App](media/notes-ce-5.png)

<span data-ttu-id="ee686-137">Alle Aktualisierungen der Notiz werden zwischen der Finance and Operations-App und der Kundenbindungs-App hin und her synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ee686-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="ee686-138">Eine Notiz in einer Finance and Operations-App erstellen</span><span class="sxs-lookup"><span data-stu-id="ee686-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="ee686-139">Sie können eine Notiz ebenfalls in einer Finance and Operations-App erstellen, die dann mit einer Kundenbindungs-App synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee686-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="ee686-140">Befolgen Sie diese Schritte zum Erstellen einer Notiz in einer Finance and Operations-App und anschließendem Synchronisieren mit einer Kundenbindungs-App.</span><span class="sxs-lookup"><span data-stu-id="ee686-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="ee686-141">Wählen Sie in der Finance and Operations-App auf der Seite **Anhänge** die Option **Neu** \> **Notiz** aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Erstellen einer Notiz in der Finance and Operations-App](media/notes-fo-1.png)

2. <span data-ttu-id="ee686-143">Geben Sie einen Titel und eine kurze Anleitung ein. Wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Eingeben eines Titels und einer Anleitung](media/notes-fo-2.png)

3. <span data-ttu-id="ee686-145">Aktualisieren Sie in der Kundenbindungs-App den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="ee686-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="ee686-146">Sie sollten die neue Notiz auf der Zeitskala finden.</span><span class="sxs-lookup"><span data-stu-id="ee686-146">You should find the new note on the timeline.</span></span>

    ![Neue Notiz auf der Zeitskala in der Kundenbindungs-App](media/notes-fo-3.png)

<span data-ttu-id="ee686-148">Sie können eine Notiz entweder als intern oder als extern klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="ee686-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="ee686-149">Öffnen Sie die Notiz in der Finance and Operations-App auf der Seite **Anhänge**, und wählen Sie anschließend im Feld **Einschränkung** die Option **Intern** oder **Extern** aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Einschränkungsfeld](media/notes-fo-4.png)

<span data-ttu-id="ee686-151">Sie können auch eine URL erstellen</span><span class="sxs-lookup"><span data-stu-id="ee686-151">You can also create a URL.</span></span>

1. <span data-ttu-id="ee686-152">Wählen Sie in der Finance and Operations-App auf der Seite **Anhänge** die Option **Neu** \> **URL** aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="ee686-153">Geben Sie einen Titel und die URL ein.</span><span class="sxs-lookup"><span data-stu-id="ee686-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="ee686-154">Wählen Sie im Feld **Einschränkung** die Option **Intern** oder **Extern** aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Erstellen einer URL in der Finance and Operations-App](media/notes-fo-5.png)

4. <span data-ttu-id="ee686-156">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ee686-156">Select **Save**.</span></span>

    <span data-ttu-id="ee686-157">Da Kundenbindungs-Apps keinen URL-Typ enthalten, wird die URL als Notiz über duales Schreiben integriert.</span><span class="sxs-lookup"><span data-stu-id="ee686-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![Als Notiz erscheinende URL in der Kundenbindungs-App](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="ee686-159">Dateianhänge werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee686-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="ee686-160">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="ee686-160">Templates</span></span>

<span data-ttu-id="ee686-161">Die Notizintegration enthält eine Sammlung von Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten – wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ee686-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="ee686-162">Finance and Operations-App</span><span class="sxs-lookup"><span data-stu-id="ee686-162">Finance and Operations app</span></span> | <span data-ttu-id="ee686-163">Customer Engagement-App</span><span class="sxs-lookup"><span data-stu-id="ee686-163">Customer engagement app</span></span> | <span data-ttu-id="ee686-164">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee686-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="ee686-165">Debitorenanhänge</span><span class="sxs-lookup"><span data-stu-id="ee686-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="ee686-166">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="ee686-166">Annotations</span></span> | <span data-ttu-id="ee686-167">Unternehmen, die Klartext und URLs zum Erfassen debitorspezifischer Informationen verwenden (sowohl für Organisationen als auch für Personen).</span><span class="sxs-lookup"><span data-stu-id="ee686-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="ee686-168">Kreditorendokumentanhänge</span><span class="sxs-lookup"><span data-stu-id="ee686-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="ee686-169">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="ee686-169">Annotations</span></span> | <span data-ttu-id="ee686-170">Unternehmen, die Klartext und URLs zum Erfassen kreditorspezifischer Informationen verwenden (sowohl für Organisationen als auch für Personen).</span><span class="sxs-lookup"><span data-stu-id="ee686-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="ee686-171">Auftragskopfdokument-Anhänge</span><span class="sxs-lookup"><span data-stu-id="ee686-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="ee686-172">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="ee686-172">Annotations</span></span> | <span data-ttu-id="ee686-173">Unternehmen, die Klartext und URLs zum Erfassen auftragsspezifischer Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee686-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="ee686-174">Anhänge des Bestellkopfdokuments</span><span class="sxs-lookup"><span data-stu-id="ee686-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="ee686-175">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="ee686-175">Annotations</span></span> | <span data-ttu-id="ee686-176">Unternehmen, die Klartext und URLs zum Erfassen bestellungsspezifischer Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee686-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

## <a name="limitations"></a><span data-ttu-id="ee686-177">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ee686-177">Limitations</span></span>

<span data-ttu-id="ee686-178">Nachdem Sie die Notes-Lösung installiert haben, können Sie sie nicht mehr deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ee686-178">Once you install the notes solution, you cannot uninstall it.</span></span> 

<span data-ttu-id="ee686-179">Weitere Informationen finden Sie unter [Referenz für die Zuordnung von dualem Schreiben](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee686-179">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
