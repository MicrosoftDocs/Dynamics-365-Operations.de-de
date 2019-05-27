---
title: Datensatzvorlagen
description: Dieser Artikel führt das Konzept der Datensatzvorlagen ein und erklärt, wie Sie verwendet werden können, um Datensätze zu erstellen, die Informationen freigeben.
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 426fd8fafec061b649cbb31109ffe8fabc24917d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545670"
---
# <a name="record-templates"></a><span data-ttu-id="6d113-103">Datensatzvorlagen</span><span class="sxs-lookup"><span data-stu-id="6d113-103">Record templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d113-104">Dieser Artikel führt das Konzept der Datensatzvorlagen ein und erklärt, wie Sie verwendet werden können, um Datensätze zu erstellen, die Informationen freigeben.</span><span class="sxs-lookup"><span data-stu-id="6d113-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="6d113-105">Mithilfe von Datensatzvorlagen können Sie Datensätze schneller in Microsoft Dynamics 365 for Finance and Operationserstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d113-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6d113-106">Datensatzvorlagen können nicht für alle Datensatztypen in Microsoft Dynamics 365 for Finance and Operations erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d113-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="6d113-107">Beispiel: Stellen Sie sich vor, Sie geben Mietinformationen für eine Autovermietung mit Sitz in San Francisco ein.</span><span class="sxs-lookup"><span data-stu-id="6d113-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="6d113-108">Da die meisten Kunden vermutlich aus dem Bereich San Francisco kommen, wäre es schön, wenn die Werte für **Bundesland**, **Land** und **Ort** auf dem Mietvertragsformular automatisch gefüllt würden.</span><span class="sxs-lookup"><span data-stu-id="6d113-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="6d113-109">Sie können Vorlagen nur auf Finance and Operations-Bereiche anwenden, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="6d113-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="6d113-110">Wenn Sie einen neuen Datensatz erstellen, können Sie und andere Benutzer jedoch alle Vorlagentitel sehen, wenn Sie Vorlagen erstellen, die für alle Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6d113-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="6d113-111">Berücksichtigen Sie dies beim Benennen von Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="6d113-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="6d113-112">Vermeiden Sie z. B. Namen, in denen Begriffe wie "Provision" vorkommen, wenn die Information, dass einige Mitarbeiter des Unternehmens auf Provisionen beruhende Gehälter haben, vertraulich ist.</span><span class="sxs-lookup"><span data-stu-id="6d113-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="6d113-113">Wenn es für ein bestimmtes Formular eine oder mehrere Vorlagen gibt, auf die Sie zugreifen können, und Sie versuchen, einen neuen Datensatz im Formular zu erstellen, wird die Seite **Vorlage für … wählen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d113-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="6d113-114">Durch Auswählen einer Vorlage aus der Liste wird der neue Datensatz mit den in der ausgewählten Vorlage festgelegten Standardinformationen versehen.</span><span class="sxs-lookup"><span data-stu-id="6d113-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="6d113-115">Wenn Sie beim Erstellen neuer Datensätze keine Vorlagen verwenden möchten, aktivieren Sie das Kontrollkästchen **Nicht erneut fragen** im Formular **Vorlage für …** wählen.</span><span class="sxs-lookup"><span data-stu-id="6d113-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="6d113-116">Soll das Auswahldialogfeld für Vorlagen wieder angezeigt werden, klicken Sie mit der rechten Maustaste auf **Datensatzinfo**, und klicken Sie anschließend auf **Vorlagenabschnitt anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="6d113-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
