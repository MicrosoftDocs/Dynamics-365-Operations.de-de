---
title: Übersicht über die Aufnahmevorlagen
description: Dieser Artikel führt das Konzept der Datensatzvorlagen ein und erklärt, wie Sie verwendet werden können, um Datensätze zu erstellen, die Informationen freigeben.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0b55046e6c523398b4a30e674dc9f77bb6fedf3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693207"
---
# <a name="record-templates-overview"></a><span data-ttu-id="f0447-103">Übersicht über die Aufnahmevorlagen</span><span class="sxs-lookup"><span data-stu-id="f0447-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0447-104">Dieser Artikel führt das Konzept der Datensatzvorlagen ein und erklärt, wie Sie verwendet werden können, um Datensätze zu erstellen, die Informationen freigeben.</span><span class="sxs-lookup"><span data-stu-id="f0447-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="f0447-105">Datensatzvorlagen können helfen, Datensätze schneller zu erstellen. Sie können jedoch nur für einige Datensatztypen Datensatzvorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0447-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="f0447-106">Beispiel: Stellen Sie sich vor, Sie geben Mietinformationen für eine Autovermietung mit Sitz in San Francisco ein.</span><span class="sxs-lookup"><span data-stu-id="f0447-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="f0447-107">Da die meisten Kunden vermutlich aus dem Bereich San Francisco kommen, wäre es schön, wenn die Werte für **Bundesland**, **Land** und **Ort** auf dem Mietvertragsformular automatisch gefüllt würden.</span><span class="sxs-lookup"><span data-stu-id="f0447-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="f0447-108">Sie können Vorlagen nur auf Bereiche anwenden, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="f0447-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="f0447-109">Wenn Sie einen neuen Datensatz erstellen, können Sie und andere Benutzer jedoch alle Vorlagentitel sehen, wenn Sie Vorlagen erstellen, die für alle Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f0447-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="f0447-110">Berücksichtigen Sie dies beim Benennen von Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="f0447-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="f0447-111">Vermeiden Sie z. B. Namen, in denen Begriffe wie "Provision" vorkommen, wenn die Information, dass einige Mitarbeiter des Unternehmens auf Provisionen beruhende Gehälter haben, vertraulich ist.</span><span class="sxs-lookup"><span data-stu-id="f0447-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="f0447-112">Wenn es für ein bestimmtes Formular eine oder mehrere Vorlagen gibt, auf die Sie zugreifen können, und Sie versuchen, einen neuen Datensatz im Formular zu erstellen, wird die Seite **Vorlage für … wählen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0447-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="f0447-113">Durch Auswählen einer Vorlage aus der Liste wird der neue Datensatz mit den in der ausgewählten Vorlage festgelegten Standardinformationen versehen.</span><span class="sxs-lookup"><span data-stu-id="f0447-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="f0447-114">Wenn Sie beim Erstellen neuer Datensätze keine Vorlagen verwenden möchten, aktivieren Sie das Kontrollkästchen **Nicht erneut fragen** im Formular **Vorlage für …** wählen.</span><span class="sxs-lookup"><span data-stu-id="f0447-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="f0447-115">Soll das Auswahldialogfeld für Vorlagen wieder angezeigt werden, klicken Sie mit der rechten Maustaste auf **Datensatzinfo**, und klicken Sie anschließend auf **Vorlagenabschnitt anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="f0447-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
