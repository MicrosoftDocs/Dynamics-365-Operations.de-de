---
title: Globale Quellensteuer
description: Dieses Thema enthält Informationen zur globalen Quellensteuerfunktionalität und zu deren Einrichtung. Die globale Quellensteuerfunktionalität wurde für Kreditoren- und Debitorenbuchungen erweitert, sodass die Quellensteuer auf Artikelebene berechnet wird.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075737"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="951cc-104">Globale Quellensteuer</span><span class="sxs-lookup"><span data-stu-id="951cc-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="951cc-105">Dieses Thema enthält Informationen zur globalen Quellensteuerfunktionalität und erläutert deren Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="951cc-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="951cc-106">Die neue Funktionalität ist ab der Version 10.0.17 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="951cc-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="951cc-107">Die globale Quellensteuerfunktionalität wurde für Kreditoren- und Debitorenbuchungen erweitert, sodass die Quellensteuer auf Artikelebene berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="951cc-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="951cc-108">Der Saldo des Quellensteuerkontos aus Kaufbuchungen kann durch Ausführen des Einzelvorgang zur Quellensteuerzahlung gegen das Quellensteuerverrechnungskonto ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="951cc-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="951cc-109">Die globale Quellensteuer unterstützt nicht die Funktion **Belastungen verwalten** auf den Seiten „Bestellung“, „Kreditorenrechnung“ und „Auftrag“.</span><span class="sxs-lookup"><span data-stu-id="951cc-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="951cc-110">Globale Quellensteuer aktivieren</span><span class="sxs-lookup"><span data-stu-id="951cc-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="951cc-111">Wählen Sie im Arbeitsbereich **Funktionsverwaltung** die Option **Globale Quellensteuer** und anschließend **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="951cc-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="951cc-112">Rufen Sie **Steuer \> Einrichtung \> Parameter \> Hauptbuchparameter** auf. Setzen Sie anschließend auf der Registerkarte **Quellensteuer** die Option **Globale Quellensteuer aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="951cc-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="951cc-113">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="951cc-113">Select **Save**.</span></span>
4. <span data-ttu-id="951cc-114">Aktualisieren Sie die Seite in Ihrem Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="951cc-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="951cc-115">Die globale Quellensteuerfunktionalität kann nicht für Länder/Regionen aktiviert werden, in denen bereits lokalisierte Quellensteuerlösungen existieren.</span><span class="sxs-lookup"><span data-stu-id="951cc-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="951cc-116">Diese Gebiete umfassen Indien, Brasilien, Thailand, Saudi-Arabien, Irland, Großbritannien und die Vereinigten Staaten, sind aber nicht auf diese beschränkt.</span><span class="sxs-lookup"><span data-stu-id="951cc-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
