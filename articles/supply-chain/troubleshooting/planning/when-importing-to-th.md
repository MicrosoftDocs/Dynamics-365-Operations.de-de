---
title: Sie werden aufgefordert, die Einstellungen für die Artikelabdeckung zu speichern, obwohl Sie keine Änderungen vorgenommen haben
description: Sie werden aufgefordert, die Einstellungen für die Artikelabdeckung zu speichern, obwohl Sie keine Änderungen vorgenommen haben.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049468"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="523f0-103">Sie werden aufgefordert, die Einstellungen für die Artikelabdeckung zu speichern, obwohl Sie keine Änderungen vorgenommen haben</span><span class="sxs-lookup"><span data-stu-id="523f0-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="523f0-104">KB-Nummer: 4615588</span><span class="sxs-lookup"><span data-stu-id="523f0-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="523f0-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="523f0-105">Symptoms</span></span>

<span data-ttu-id="523f0-106">In einigen Szenarien erhalten Sie möglicherweise die folgende Meldung, wenn Sie die Seite **Artikelabdeckung** öffnen, nachdem Sie Elemente über die Entität *Artikelabdeckung V2* importiert haben.</span><span class="sxs-lookup"><span data-stu-id="523f0-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="523f0-107">Möchten Sie die Änderungen vor dem Schließen speichern?</span><span class="sxs-lookup"><span data-stu-id="523f0-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="523f0-108">Sie erhalten diese Nachricht, obwohl Sie keine Änderungen vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="523f0-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="523f0-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="523f0-109">Resolution</span></span>

<span data-ttu-id="523f0-110">Die Seite **Artikelabdeckung** enthält eine komplexe Standardlogik, die dazu führen kann, dass die Nachricht angezeigt wird, nachdem kürzlich direkte Änderungen in der Datenbank vorgenommen wurden, z. B. durch Entitätsimport.</span><span class="sxs-lookup"><span data-stu-id="523f0-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="523f0-111">Zum Beispiel ist das Feld `AREGENERALSETTINGSOVERRIDDEN` Entitätsfeld auf *Nein* gesetzt, aber Sie importieren eine Datei, die neue oder geänderte Werte für Felder wie `PRODUCTCOVERAGEGROUPID` und/oder `VENDORACCOUNTNUMBER` bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="523f0-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="523f0-112">In diesem Fall, weil das `AREGENERALSETTINGSOVERRIDDEN` Feld auf *Nein* gesetzt ist, werden die Werte automatisch aus den Feldern gelöscht, wenn Sie die Seite **Artikelabdeckung** zum ersten Mal nach dem Import öffnen.</span><span class="sxs-lookup"><span data-stu-id="523f0-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="523f0-113">Wenn Sie die Änderungen speichern, während das Meldungsfeld Sie dazu auffordert, werden sie in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="523f0-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="523f0-114">Andernfalls erhalten Sie beim nächsten Öffnen der Seite dieselbe Nachricht.</span><span class="sxs-lookup"><span data-stu-id="523f0-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="523f0-115">Um dieses Verhalten zu verhindern, aber auch Werte für Felder wie `PRODUCTCOVERAGEGROUPID` durch Entitätsimport einzuschließen, setzen Sie `AREGENERALSETTINGSOVERRIDDEN` auf *Ja*,  wenn Sie importieren.</span><span class="sxs-lookup"><span data-stu-id="523f0-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
