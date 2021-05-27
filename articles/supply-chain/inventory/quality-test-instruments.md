---
title: Qualitätsmanagement Testinstrumente
description: Dieses Thema beschreibt, wie Sie Testinstrumente erstellen, die für Tests bei Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021731"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="55134-103">Qualitätsmanagement Testinstrumente</span><span class="sxs-lookup"><span data-stu-id="55134-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55134-104">Dieses Thema beschreibt, wie Sie Testinstrumente erstellen, die für Tests bei Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="55134-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="55134-105">Sie verwenden die Seite **Testgeräte**, um Details zu den Geräten zu definieren und anzuzeigen, die zur Durchführung von Tests bei Qualitätsprüfungsaufträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55134-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="55134-106">Testinstrumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="55134-106">Test instruments are optional.</span></span> <span data-ttu-id="55134-107">Sie können jedoch den Arbeitskräften in der Qualitätssicherung helfen, zu wissen, welches Gerät oder Tool sie für einen bestimmten Test verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="55134-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="55134-108">Beispiel für ein Testinstrument</span><span class="sxs-lookup"><span data-stu-id="55134-108">Test instrument example</span></span>

<span data-ttu-id="55134-109">Sie führen verschiedene Tests an elektrischen Komponenten durch.</span><span class="sxs-lookup"><span data-stu-id="55134-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="55134-110">Einige Tests beziehen sich auf die Spannungsausgabe der Komponenten, ein Test auf ihre Temperatur und ein Test auf ihr Gewicht.</span><span class="sxs-lookup"><span data-stu-id="55134-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="55134-111">Zur Durchführung der einzelnen Tests werden unterschiedliche Tools, Geräte oder Ausrüstungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="55134-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="55134-112">Zum Beispiel wird ein Spannungsmesser zur Messung der Spannung, ein Thermometer zur Messung der Temperatur und eine Waage zur Messung des Gewichts verwendet.</span><span class="sxs-lookup"><span data-stu-id="55134-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="55134-113">Sie können jedes dieser Geräte als Prüfgerät konfigurieren und die Maßeinheit angeben, in der die Prüfergebnisse erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55134-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="55134-114">Zum Beispiel werden die Ergebnisse des Spannungsmessers in Volt, die Ergebnisse des Thermometers in Grad Fahrenheit oder Grad Celsius und die Ergebnisse der Waage in Pfund oder Kilogramm aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="55134-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="55134-115">Erstellen Sie ein Testinstrument</span><span class="sxs-lookup"><span data-stu-id="55134-115">Create a test instrument</span></span>

1. <span data-ttu-id="55134-116">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Testinstrumente**.</span><span class="sxs-lookup"><span data-stu-id="55134-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="55134-117">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="55134-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="55134-118">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="55134-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="55134-119">**Testgerät** – Geben Sie eine eindeutige ID oder einen Namen für das Testgerät ein.</span><span class="sxs-lookup"><span data-stu-id="55134-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="55134-120">**Beschreibung** – Geben Sie eine detaillierte Beschreibung des Testgeräts ein.</span><span class="sxs-lookup"><span data-stu-id="55134-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="55134-121">**Einheit** – Wählen Sie die Einheit, in der das Gerät die Kennzahlen der Ergebnisse misst.</span><span class="sxs-lookup"><span data-stu-id="55134-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="55134-122">Das Feld **Präzision** wird automatisch festgelegt, basierend auf der von Ihnen gewählten Einheit.</span><span class="sxs-lookup"><span data-stu-id="55134-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="55134-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="55134-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55134-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="55134-124">Additional resources</span></span>

- [<span data-ttu-id="55134-125">Qualitätsmanagement-Test</span><span class="sxs-lookup"><span data-stu-id="55134-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="55134-126">Qualitätsmanagement Testgruppen</span><span class="sxs-lookup"><span data-stu-id="55134-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
