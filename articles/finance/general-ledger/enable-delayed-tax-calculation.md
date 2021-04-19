---
title: Aktivieren der verzögerten Steuerberechnung in Erfassungen
description: In diesem Thema wird erläutert, wie Sie die Funktion Verzögerte Steuerberechnung aktivieren, um die Leistung der Steuerberechnung zu verbessern, wenn die Anzahl der Erfassungspositionen groß ist.
author: ericwang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: acf5ead6ed90d4dbb41de08520cde8085a7f3935
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823715"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="473f2-103">Aktivieren der verzögerten Steuerberechnung in Erfassungen</span><span class="sxs-lookup"><span data-stu-id="473f2-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="473f2-104">In diesem Thema wird erläutert, wie Sie die Mehrwertsteuerberechnung in Erfassungen verzögern können.</span><span class="sxs-lookup"><span data-stu-id="473f2-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="473f2-105">Diese Funktion kann die Leistung von Steuerberechnungen verbessern, wenn viele Erfassungspositionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="473f2-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="473f2-106">Standardmäßig werden Mehrwertsteuerbeträge in Erfassungspositionen berechnet, sobald steuerbezogene Felder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="473f2-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="473f2-107">Diese Felder enthalten die Felder für Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen.</span><span class="sxs-lookup"><span data-stu-id="473f2-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="473f2-108">Jede Aktualisierung einer Erfassungsposition führt dazu, dass Steuerbeträge für alle Erfassungspositionen neu berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="473f2-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="473f2-109">Obwohl dieses Verhalten Benutzern hilft, Steuerbetragsberechnungen in Echtzeit anzuzeigen, kann es sich auch auf die Leistung auswirken, wenn die Anzahl der Erfassungspositionen sehr groß ist.</span><span class="sxs-lookup"><span data-stu-id="473f2-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="473f2-110">Mit der Funktion Verzögerte Steuerberechnung können Sie die Steuerberechnung für Erfassungen verzögern und damit Leistungsprobleme beheben.</span><span class="sxs-lookup"><span data-stu-id="473f2-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="473f2-111">Wenn diese Funktion aktiviert ist, werden Steuerbeträge nur dann berechnet, wenn ein Benutzer **Mehrwertsteuer** auswählt oder die Erfassung bucht.</span><span class="sxs-lookup"><span data-stu-id="473f2-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="473f2-112">Sie können die Berechnung der Mehrwertsteuer auf drei Ebenen verzögern:</span><span class="sxs-lookup"><span data-stu-id="473f2-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="473f2-113">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="473f2-113">Legal entity</span></span>
- <span data-ttu-id="473f2-114">Journal</span><span class="sxs-lookup"><span data-stu-id="473f2-114">Journal name</span></span>
- <span data-ttu-id="473f2-115">Erfassungskopf</span><span class="sxs-lookup"><span data-stu-id="473f2-115">Journal header</span></span>

<span data-ttu-id="473f2-116">Das System gibt der Einrichtung für den Erfassungskopf Vorrang.</span><span class="sxs-lookup"><span data-stu-id="473f2-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="473f2-117">Standardmäßig wird diese Einstellung aus dem Journal übernommen.</span><span class="sxs-lookup"><span data-stu-id="473f2-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="473f2-118">Standardmäßig wird die Einstellung für das Journal aus der Einstellung auf der Seite **Hauptbuchparameter** übernommen, wenn das Journal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="473f2-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="473f2-119">In den folgenden Abschnitten wird erklärt, wie eine verzögerte Steuerberechnung für juristische Personen, Journale und Erfassungsköpfe aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="473f2-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="473f2-120">Aktivieren der verzögerten Steuerberechnung auf der Ebene der juristische Person</span><span class="sxs-lookup"><span data-stu-id="473f2-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="473f2-121">Wechseln Sie zu **Hauptbuch \> Sachkonto-Einstellungen \> Hauptbuchparameter**.</span><span class="sxs-lookup"><span data-stu-id="473f2-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="473f2-122">Legen Sie auf der Registerkarte **Mehrwertsteuer** im Inforegister **Allgemein** die Option **Verzögerte Steuerberechnung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="473f2-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Hauptbuchparameter – Bild](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="473f2-124">Aktivieren der verzögerten Steuerberechnung auf der Ebene des Journals</span><span class="sxs-lookup"><span data-stu-id="473f2-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="473f2-125">Wechseln Sie zu **Hauptbuch \> Erfassungseinstellungen \> Journale**.</span><span class="sxs-lookup"><span data-stu-id="473f2-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="473f2-126">Legen Sie im Inforegister **Allgemein** im Abschnitt **Mehrwertsteuer** die Option **Verzögerte Steuerberechnung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="473f2-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Journale – Bild](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="473f2-128">Aktivieren der verzögerten Steuerberechnung auf der Ebene des Erfassungskopfes</span><span class="sxs-lookup"><span data-stu-id="473f2-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="473f2-129">Wechseln Sie zu **Hauptbuch \> Journaleinträge \> Allgemeine Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="473f2-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="473f2-130">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="473f2-130">Select **New**.</span></span>
3. <span data-ttu-id="473f2-131">Wählen Sie ein Journal aus.</span><span class="sxs-lookup"><span data-stu-id="473f2-131">Select a journal name.</span></span>
4. <span data-ttu-id="473f2-132">Legen Sie auf der Registerkarte **Einstellungen** die Option **Verzögerte Steuerberechnung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="473f2-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Allgemeine Erfassung – Seitenbild](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]