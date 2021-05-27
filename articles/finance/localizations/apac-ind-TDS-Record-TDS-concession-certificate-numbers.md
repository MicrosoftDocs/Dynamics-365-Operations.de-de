---
title: Nummern von TDS-Konzessionszertifikaten erfassen
description: In diesem Thema wird erklärt, wie die für Kreditoren ausgestellte Nummern von Konzessionszertifikaten für die Quellenbesteuerung (TDS) erfasst werden.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023256"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="8f1ba-103">Nummern von TDS-Konzessionszertifikaten erfassen</span><span class="sxs-lookup"><span data-stu-id="8f1ba-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f1ba-104">In diesem Thema wird erklärt, wie die für Kreditoren ausgestellte Nummern von Konzessionszertifikaten für die Quellenbesteuerung (TDS) erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="8f1ba-105">Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuerkonzessionen**.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="8f1ba-106">Wählen Sie im Feld **Steuertyp** **TDS** aus, um Konzessionszertifikate für den Steuertyp „TDS“ zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="8f1ba-107">Wählen Sie auf der Registerkarte **Übersicht** **ALT + N** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="8f1ba-108">[![Kopfzeile der neuen Position](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="8f1ba-109">Wählen Sie im Feld **Quellensteuercode** den TDS-Steuercode aus, für den die Kreditorenkonzessionszertifikate ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="8f1ba-110">Im Feld **Quellensteuercodename** wird der Name des TDS-Steuercodes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="8f1ba-111">Legen Sie in den Feldern **Startdatum** und **Enddatum** den Gültigkeitszeitraum für das Konzessionszertifikat fest, das der TDS-Steuercode verwendet, um die TDS für den Kreditor auf Konzessionsbasis zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="8f1ba-112">Geben Sie im Feld **Hinweis** etwaige Hinweise ein.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="8f1ba-113">Geben Sie im Feld **Abschnitt** den rechtlichen Abschnittscode ein, unter dem das TDS-Konzessionszertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="8f1ba-114">Wenn der Abschnittscode 197 lautet, wird der Wert „A“ sowohl in der Spalte „Grund für Nichtabzug/niedrigeren Abzug“ im Formular 26Q als auch in der Spalte „Grund für (gegebenenfalls) Nichtabzug/niedrigeren Abzug/Hochrechnung“ im Formular 27Q angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="8f1ba-115">Wenn der Abschnittscode 197A lautet, wird an beiden Stellen der Wert „B“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="8f1ba-116">Wählen Sie das Inforegister **Zertifikat** aus, um TDS-Konzessionszertifikatnummern für Kreditoren zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="8f1ba-117">Wählen Sie im Feld **Kreditorenkonto** das Kreditorenkonto aus, für das das TDS-Konzessionszertifikat ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="8f1ba-118">Legen Sie in den Feldern **Startdatum** und **Enddatum** die Gültigkeitsdauer des TDS-Konzessionszertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="8f1ba-119">Die Berechnung der TDS auf Konzessionsbasis basiert auf dem Zeitraum, in dem das Zertifikat für den Kreditoren erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="8f1ba-120">Geben Sie im Feld **Zertifikatnummer** die TDS-Konzessionszertifikatsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="8f1ba-121">[![Inforegister „Zertifikat“](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="8f1ba-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-122">Close the page.</span></span>
