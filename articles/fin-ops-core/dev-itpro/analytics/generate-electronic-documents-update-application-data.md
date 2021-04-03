---
title: Generieren elektronischer Dokumente und Aktualisieren von Anwendungsdaten mithilfe von EB
description: Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdf595548ac1e67b99018495d2f0278dc305254d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568652"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="da3f0-103">Generieren von elektronischen Dokumenten und Aktualisieren von Anwendungsdaten per ER</span><span class="sxs-lookup"><span data-stu-id="da3f0-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da3f0-104">Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="da3f0-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="da3f0-105">Sie können auch ER-Formate entwerfen, die eingehende elektronische Dokumente analysieren und den Inhalt in diesen Dokumenten zum Aktualisieren der Anwendungsdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="da3f0-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="da3f0-106">Mithilfe dieser Funktion kann ein einzelnes ER-Format verwendet werden, um ausgehende elektronische Dokumente zu generieren und die Anwendungsdaten dann zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="da3f0-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="da3f0-107">Diese Funktion kann in den folgenden Szenarien verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="da3f0-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="da3f0-108">Um eine wiederholte Verwendung von Anwendungsdaten in Folgeprozessen zu verhindern, können Sie die Daten einer Anwendung markieren, nachdem sie verwendet wurde, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="da3f0-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="da3f0-109">So können z. B. Zahlungsbuchungen direkt nachdem Sie in einer erstellten Zahlungsnachricht einbezogen wurden, als bereits verarbeitet markieren.</span><span class="sxs-lookup"><span data-stu-id="da3f0-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="da3f0-110">Zur Speicherung der Verarbeitungdetails von elektronischen Dokumenten, die mithilfe der ER-Logik generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="da3f0-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="da3f0-111">Beispielsweise eine eindeutige Zahlungsnachrichtenkennung, die mithilfe des ER-Ausdrucks generiert wird.</span><span class="sxs-lookup"><span data-stu-id="da3f0-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="da3f0-112">Der Ausdruck basiert auf den Informationen, die im ER-Dialogfeld eingegeben werden, wenn das ER-Format ausgeführt wird, um Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="da3f0-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="da3f0-113">Weitere Informationen über diese Funktion erhalten Sie bei Wiedergabe des ER-Satzes der "Dokumente mit Anwendungsdaten-Update generieren"-Aufgabenleitfäden (Gehört zum 7.5.4.3 Acquire/Develop IT service/solution components (10677) Geschäftsprozess), die Sie durch die Details der Intrastat-Berichterstattung und Archivierung führen.</span><span class="sxs-lookup"><span data-stu-id="da3f0-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="da3f0-114">Die folgenden Dateien sind erforderlich, um bestimmte Schritte in diesen Aufgabenleitfäden abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="da3f0-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="da3f0-115">Laden Sie diese Dateien herunter und speichern Sie sie auf Ihrem lokalen Rechner.</span><span class="sxs-lookup"><span data-stu-id="da3f0-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="da3f0-116">ER-Datenmodellkonfiguration: Intrastat (Model)</span><span class="sxs-lookup"><span data-stu-id="da3f0-116">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="da3f0-117">Er-Modellzuordnungskonfiguration: Intrastat (Zuordnung)</span><span class="sxs-lookup"><span data-stu-id="da3f0-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="da3f0-118">ER-Formatkonfiguration: Intrastat (format)</span><span class="sxs-lookup"><span data-stu-id="da3f0-118">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]