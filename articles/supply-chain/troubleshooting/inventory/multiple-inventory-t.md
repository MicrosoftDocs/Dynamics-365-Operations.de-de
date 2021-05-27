---
title: Mehrere Lagerbuchungen für Chargennummern, wenn „Bei physischer Aktualisierung“ deaktiviert ist
description: Nachdem Sie eine Bestellposition für Artikel angepasst haben, für die die Option „Bei physischer Aktualisierung“ der Chargennummerngruppe auf „Nein“ gesetzt ist, werden mehrere Bestandsbuchungen erstellt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026555"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="2c300-103">Mehrere Lagerbuchungen für Chargennummern, wenn „Bei physischer Aktualisierung“ deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="2c300-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="2c300-104">KB-Nummer: 4613390</span><span class="sxs-lookup"><span data-stu-id="2c300-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="2c300-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="2c300-105">Symptoms</span></span>

<span data-ttu-id="2c300-106">Nachdem Sie eine Bestellposition für Artikel angepasst haben, für die die Option **Bei physischer Aktualisierung** der Chargennummerngruppe auf *Nein* gesetzt ist, werden mehrere Bestandsbuchungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c300-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="2c300-107">Wenn Sie einen Artikel erstellen, in dem die Option **Bei physischer Aktualisierung** der Chargennummerngruppe auf *Nein* gesetzt ist, erstellt das System automatisch eine neue Chargennummer, wenn Sie eine Bestellpostenmenge ändern und die Bestellseite speichern.</span><span class="sxs-lookup"><span data-stu-id="2c300-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="2c300-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="2c300-108">Resolution</span></span>

<span data-ttu-id="2c300-109">Die Einstellung **Bei physischer Aktualisierung** für Chargennummerngruppen funktioniert folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="2c300-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="2c300-110">Wenn die Option auf *Ja* gesetzt ist, werden neue Chargennummern erst nach einer physischen Aktualisierung erstellt (z. B. wenn Artikel versendet oder empfangen werden).</span><span class="sxs-lookup"><span data-stu-id="2c300-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="2c300-111">Wenn die Option auf *Nein* gesetzt ist, wird jedes Mal, wenn eine entsprechende Aktualisierung erfolgt, eine neue Chargennummer erstellt (z. B. wenn einer Bestellung eine neue Menge hinzugefügt wird).</span><span class="sxs-lookup"><span data-stu-id="2c300-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
