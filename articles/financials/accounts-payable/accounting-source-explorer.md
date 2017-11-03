---
title: Buchhaltungsquellen-Explorer
description: "Dieser Artikel enthält Informationen zum Buchhaltungsquellexplorer, den Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 421b371c70abc82907810244e8224d859da9fab2
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="accounting-source-explorer"></a><span data-ttu-id="5feaa-103">Buchhaltungsquellen-Explorer</span><span class="sxs-lookup"><span data-stu-id="5feaa-103">Accounting source explorer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5feaa-104">Dieser Artikel enthält Informationen zum Buchhaltungsquellexplorer, den Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5feaa-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="5feaa-105">Der Buchhaltungsquellen-Explorer ist eine neue Seite, die Quellinformationen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5feaa-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="5feaa-106">Sie können den Buchhaltungsquellexplorer entweder als eigenständiges Tool verwenden oder die Details nach Hauptbuchbuchhaltungseinträgen analysieren.</span><span class="sxs-lookup"><span data-stu-id="5feaa-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="5feaa-107">So können Sie Buchhaltungsquellexplorer verwenden, um die aktuellesten Detailquellinformationen für einen Saldo in der Probebeilanz oder für eine Belegbuchungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5feaa-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="5feaa-108">Sie können dann die Funktion "Nach Microsoft Excel exportieren" verwenden, um die Informationen in Microsoft Excel weiter aufzuteilen (beispielsweise in einer Pivottabelle oder einem PivotTable-Bericht).</span><span class="sxs-lookup"><span data-stu-id="5feaa-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="5feaa-109">Der Buchhaltungsquellen-Explorer zeigt stets denselben Gesamtbetrag pro Sachkonto wie das Hauptbuch an (beispielsweise in der Zwischenbilanz).</span><span class="sxs-lookup"><span data-stu-id="5feaa-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="5feaa-110">Wie in der Zwischenbilanz können Sie Segmente in unterschiedlichen Spalten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5feaa-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="5feaa-111">Wählen Sie einfach den entsprechenden Finanzdimensionssatz aus.</span><span class="sxs-lookup"><span data-stu-id="5feaa-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="5feaa-112">Sie können Parameter verwenden, um ein Datumsintervall für die Analyse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5feaa-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="5feaa-113">Diese Funktion ähnelt der Funktion in der Zwischenbilanz.</span><span class="sxs-lookup"><span data-stu-id="5feaa-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="5feaa-114">Für alle Dokumente, die das Quelldokumentframework verwenden, zeigt das Gegenkonto Quellexplorer zusätzliche Informationen, basierende auf der Buchhaltungsverteilungen und ggf. der  Projektbuchhaltungsverteilungen.</span><span class="sxs-lookup"><span data-stu-id="5feaa-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="5feaa-115">Diese Informationen enthalten den Geldbetrag Typ, Projekt, Kategorie, Projektvorgang und Abrechnungscode.</span><span class="sxs-lookup"><span data-stu-id="5feaa-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="5feaa-116">Nachfolgend finden Sie einige Analysebeispiele:</span><span class="sxs-lookup"><span data-stu-id="5feaa-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="5feaa-117">Abweichungen zwischen Bestellungen und Kreditorenrechnungen, da jede Abweichung durch einen Geldbetragstyp dargestellt wird (z. B. Abweichung der Belastung)</span><span class="sxs-lookup"><span data-stu-id="5feaa-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="5feaa-118">Differenz zwischen berechenbaren Stunden und nicht-berechenbaren Stunden und Ausgaben pro Projekt, Unternehmenseinheit und Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="5feaa-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="5feaa-119">Für Quelldokumente, die das Konzept der Quelldokument-Referenzidentitäten verwenden, zeigt der Buchhaltungsquellen-Explorer noch weitere Details an, z. B. Debitor, Kreditor, Arbeitskraft, Produkt, Menge, Einheitentext und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="5feaa-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="5feaa-120">Nachfolgend finden Sie einige Analysebeispiele:</span><span class="sxs-lookup"><span data-stu-id="5feaa-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="5feaa-121">Hotelkosten pro Unternehmenseinheit und Hotelmarke für einen Finanzzeitraum auf der Grundlage von Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="5feaa-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="5feaa-122">Rabatte nach Kreditor, Produkt, Abteilung</span><span class="sxs-lookup"><span data-stu-id="5feaa-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="5feaa-123">Für diese Dokumente können Sie vom Buchhaltungsquellen-Explorer aus auch zum ursprünglichen Quelldokument navigieren.</span><span class="sxs-lookup"><span data-stu-id="5feaa-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>




