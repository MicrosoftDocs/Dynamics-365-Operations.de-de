---
title: Zahlungsrechnungen erstellen
description: In diesem Thema wird erläutert, wie Sie monatliche Mietrechnungen erstellen. Sie können Rechnungen für einzelne Mietverträge erstellen oder sie mithilfe eines Stapelverarbeitungsprozesses für mehrere Mietverträge erstellen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969577"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="eaedc-104">Zahlungsrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="eaedc-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaedc-105">Sie können monatliche Rechnungen für einzelne Mietverträge erstellen oder sie mithilfe eines Stapelverarbeitungsprozesses für mehrere Mietverträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="eaedc-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="eaedc-106">Das folgende Verfahren zeigt, wie Sie einen individuellen Mietzahlungseintrag erstellen, wenn der **An Kreditor bezahlen**-Parameter auf der **Leasingbuch-Einrichtung**-Seite eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="eaedc-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="eaedc-107">Auf der **Mietvertragsübersicht**-Seite, wählen Sie einen Mietvertrag und dann **Bücher \> Zahlungsplan**.</span><span class="sxs-lookup"><span data-stu-id="eaedc-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="eaedc-108">Wählen Sie die Zahlung aus, die ausgeführt werden muss, und wählen Sie dann **Erfassung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="eaedc-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="eaedc-109">Sie erhalten eine Nachricht, die besagt, dass für die ausgewählte Zahlung eine Erfassung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="eaedc-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="eaedc-110">Wählen Sie **Rechnungserfassungen** und dann die Rechnung aus, die bezahlt werden muss.</span><span class="sxs-lookup"><span data-stu-id="eaedc-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="eaedc-111">Auf der Registerkarte **Zeilen** überprüfen Sie den Journaleintrag, bevor Sie ihn im Hauptbuch buchen.</span><span class="sxs-lookup"><span data-stu-id="eaedc-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eaedc-112">Standardmäßig verwenden die erstellten Kreditorenrechnungszeilen das Kreditorenbuchungsprofil aus der **Kreditorenparameter**-Seite.</span><span class="sxs-lookup"><span data-stu-id="eaedc-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="eaedc-113">Wählen Sie die korrekte Erfassung und dann die Rechnung aus, die bezahlt werden muss.</span><span class="sxs-lookup"><span data-stu-id="eaedc-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="eaedc-114">Für dieses Beispiel ist der **An den Kreditor bezahlen**-Parameter im Leasingbuch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eaedc-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="eaedc-115">Daher befindet sich die Rechnung in der Rechnungserfassung.</span><span class="sxs-lookup"><span data-stu-id="eaedc-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="eaedc-116">Der **Übersicht**-Abschnitt zeigt eine Zusammenfassung des Journaleintrags, und der **Zeilen**-Abschnitt zeigt Details der tatsächlichen Erfassungszeilen.</span><span class="sxs-lookup"><span data-stu-id="eaedc-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eaedc-117">Wenn der **An den Kreditor bezahlen**-Parameter deaktiviert ist, werden die Einträge in der Zahlungserfassung auf der **Anlagenleasing**-Seite für das Leasingbuch aufgeführt, und das System erstellt anstelle einer Rechnung einen Eintrag für das Anlagenleasing.</span><span class="sxs-lookup"><span data-stu-id="eaedc-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="eaedc-118">Der Eintrag für die Mietzahlung wird auf den Erfassungsnamen gebucht, der im Feld **Monatliches Mieterfassung** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="eaedc-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="eaedc-119">Nachdem die Transaktion gebucht wurde, können Sie die Transaktionsinformationen und den Buchwert der Leasingverbindlichkeit anzeigen, indem Sie **Verbindlichkeitstransaktionen** im Leasingbuch auswählen.</span><span class="sxs-lookup"><span data-stu-id="eaedc-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="eaedc-120">Im Zahlungsplan wird das Kontrollkästchen **Erfassung gebucht** aktiviert und in der Zeile wird die Rechnungserfassungsnummer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eaedc-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="eaedc-121">Nachdem eine Zahlungserfassung und ein Eintrag für diese Erfassung erstellt wurden, müssen Sie den Eintrag stornieren, bevor er neu erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eaedc-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
