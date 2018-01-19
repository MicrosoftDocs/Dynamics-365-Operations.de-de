---
title: Elektronische Dokumente generieren und Anwendungsdaten mithilfe des elektronischen Berichterstellungstools aktualisieren
description: "Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Finance and Operations- Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren. Sie können auch ER-Formate entwerfen, die eingehende elektronische Dokumente analysieren und den Inhalt in diesen Dokumenten zum Aktualisieren der Anwendungsdaten verwenden."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 34654c458ce74bf2ee6c2d2bac655d6c399ca393
ms.contentlocale: de-de
ms.lasthandoff: 01/19/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="3b1a1-104">Elektronische Dokumente generieren und Anwendungsdaten mithilfe des elektronischen Berichterstellungstools aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3b1a1-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

<span data-ttu-id="3b1a1-105">Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Finance and Operations- Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="3b1a1-106">Sie können auch ER-Formate entwerfen, die eingehende elektronische Dokumente analysieren und den Inhalt in diesen Dokumenten zum Aktualisieren der Anwendungsdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="3b1a1-107">Mithilfe dieser Funktion kann ein einzelnes ER-Format verwendet werden, um ausgehende elektronische Dokumente zu generieren und die Anwendungsdaten dann zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="3b1a1-108">Diese Funktion kann in den folgenden Szenarien verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="3b1a1-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="3b1a1-109">Um eine wiederholte Verwendung von Anwendungsdaten in Folgeprozessen zu verhindern, können Sie die Daten einer Anwendung markieren, nachdem sie verwendet wurde, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="3b1a1-110">So können z. B. Zahlungsbuchungen direkt nachdem Sie in einer erstellten Zahlungsnachricht einbezogen wurden, als bereits verarbeitet markieren.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="3b1a1-111">Zur Speicherung der Verarbeitungdetails von elektronischen Dokumenten, die mithilfe der ER-Logik generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="3b1a1-112">Beispielsweise eine eindeutige Zahlungsnachrichtenkennung, die mithilfe des ER-Ausdrucks generiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="3b1a1-113">Der Ausdruck basiert auf den Informationen, die im ER-Dialogfeld eingegeben werden, wenn das ER-Format ausgeführt wird, um Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="3b1a1-114">Weitere Informationen über diese Funktion erhalten Sie bei Wiedergabe des ER-Satzes der "Dokumente mit Anwendungsdaten-Update generieren"-Aufgabenleitfäden (Gehört zum 7.5.4.3 Acquire/Develop IT service/solution components (10677) Geschäftsprozess), die Sie durch die Details der Intrastat-Berichterstattung und Archivierung führen.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="3b1a1-115">Die folgenden Dateien sind erforderlich, um bestimmte Schritte in diesen Aufgabenleitfäden abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="3b1a1-116">Laden Sie diese Dateien herunter und speichern Sie sie auf Ihrem lokalen Rechner.</span><span class="sxs-lookup"><span data-stu-id="3b1a1-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="3b1a1-117">ER-Datenmodellkonfiguration: Intrastat (Model)</span><span class="sxs-lookup"><span data-stu-id="3b1a1-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="3b1a1-118">Er-Modellzuordnungskonfiguration: Intrastat (Zuordnung)</span><span class="sxs-lookup"><span data-stu-id="3b1a1-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="3b1a1-119">ER-Formatkonfiguration: Intrastat (format)</span><span class="sxs-lookup"><span data-stu-id="3b1a1-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

