---
title: Bei der Erfassung der Fertigmeldung wird ein Fehler gebucht
description: Wenn Sie den die Erfassung der Fertigmeldung buchen, erhalten Sie eine Fehlermeldung, dass die bestellte Menge nicht reduziert werden kann.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026530"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="fd599-103">Bei der Erfassung der Fertigmeldung wird ein Fehler gebucht</span><span class="sxs-lookup"><span data-stu-id="fd599-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="fd599-104">KB-Nummer: 4612891</span><span class="sxs-lookup"><span data-stu-id="fd599-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="fd599-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="fd599-105">Symptoms</span></span>

<span data-ttu-id="fd599-106">Wenn Sie die Erfassung **Fertigmeldung** buchen, tritt ein Fehler auf und Sie erhalten die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="fd599-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="fd599-107">Die bestellte Menge kann nicht reduziert werden, da nicht genügend offene Lagerposten mit dem Status 'Bestellt' vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fd599-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="fd599-108">Die Artikel sind als „Eingekauft“, „Eingegangen“ und „Registriert“ angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd599-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="fd599-109">Dieser Fehler tritt nur auf, wenn das Feld **Fehlermenge** auf die erste Position der Erfassung **Fertigmeldung** und das Feld **Gutmenge** auf die letzte Position gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="fd599-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="fd599-110">Wenn das Feld **Fehlermenge** auf die letzte Position gesetzt ist, tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fd599-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="fd599-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="fd599-111">Resolution</span></span>

<span data-ttu-id="fd599-112">Um diesen Fehler zu vermeiden, öffnen Sie die Seite **Produktionssteuerungsparameter** und dann die Registerkarte **Allgemein**, stellen Sie die Option **Verbleibende Menge um Fehlermenge erhöhen** auf *Ja*.</span><span class="sxs-lookup"><span data-stu-id="fd599-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
