---
title: Sie können keine Vorlage auf ein freigegebenes Produkt anwenden
description: Sie können keine Vorlage auf ein freigegebenes Produkt anwenden.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026534"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="437c8-103">Sie können keine Vorlage anwenden, um ein freigegebenes Produkt zu erstellen</span><span class="sxs-lookup"><span data-stu-id="437c8-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="437c8-104">KB-Nummer: 4612097</span><span class="sxs-lookup"><span data-stu-id="437c8-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="437c8-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="437c8-105">Symptoms</span></span>

<span data-ttu-id="437c8-106">Wenn Sie ein neues freigegebenes Produkt erstellen, indem Sie das Dialogfeld **Neu freigegebenes Produkt** verwenden, können Sie eine Vorlage auswählen.</span><span class="sxs-lookup"><span data-stu-id="437c8-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="437c8-107">Die Vorlage sollte Standardeinstellungen für viele Felder des neuen freigegebenen Produkts enthalten.</span><span class="sxs-lookup"><span data-stu-id="437c8-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="437c8-108">Einige oder alle Felder werden jedoch nicht festgelegt, nachdem Sie die Vorlage ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="437c8-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="437c8-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="437c8-109">Cause</span></span>

<span data-ttu-id="437c8-110">Viele Seiten in Microsoft Dynamics 365 Supply Chain Management lassen Sie eine Vorlage erstellen, mit der die Anfangseinstellungen für die auf diesen Seiten angezeigten Datensätze festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="437c8-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="437c8-111">Sie können eine dieser Vorlagen erstellen, indem Sie **Datensatzinfo** auf der Registerseite **Optionen** des Aktionsbereichs auswählen.</span><span class="sxs-lookup"><span data-stu-id="437c8-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="437c8-112">Freigegebene Produkte sind jedoch viel komplexer als die meisten anderen Arten von Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="437c8-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="437c8-113">Obwohl Sie auswählen **Datensatzinfo** auf der Seite **Freigegebene Produkte** zum Erstellen einer Vorlage auswählen können und obwohl Sie diese Vorlage beim Erstellen eines freigegebenen Produkts auswählen können, liefert die Vorlage nicht die erwarteten Feldwerte für das neue freigegebene Produkt.</span><span class="sxs-lookup"><span data-stu-id="437c8-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="437c8-114">Daher können Sie für freigegebene Produkte keine „Datensatzinfo“-Vorlagen verwenden.</span><span class="sxs-lookup"><span data-stu-id="437c8-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="437c8-115">Stattdessen müssen Sie dedizierte Produktvorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="437c8-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="437c8-116">Lösung</span><span class="sxs-lookup"><span data-stu-id="437c8-116">Resolution</span></span>

<span data-ttu-id="437c8-117">Verwenden Sie zum Erstellen einer Produktvorlage das Menü **Vorlage** auf der Registerkarte **Produkt** des Aktionsbereichs, nicht die Schaltfläche **Datensatzinfo** auf der Registerkarte **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="437c8-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="437c8-118">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="437c8-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="437c8-119">Wählen Sie im Aktionsbereich auf der Registerkarte **Produkt** **Neu** und dann **Vorlage** aus. Wählen Sie dann entweder, wie erforderlich, **Persönliche Vorlage erstellen** oder **Gemeinsame Vorlage erstellen**.</span><span class="sxs-lookup"><span data-stu-id="437c8-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
