---
title: Finanzerfassungsvorlagen in Office öffnen
description: Dieses Thema beschreibt, wie Sie Probleme beheben, die beim Erstellen benutzerdefinierter Finanzerfassungen mit einer Microsoft Excel-Vorlage auftreten.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089456"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="8c59c-103">Finanzerfassungsvorlagen in Office öffnen</span><span class="sxs-lookup"><span data-stu-id="8c59c-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c59c-104">Dieses Thema beschreibt, wie Sie Probleme beheben, die beim Erstellen benutzerdefinierter Finanzerfassungen mit einer Microsoft Excel-Vorlage auftreten.</span><span class="sxs-lookup"><span data-stu-id="8c59c-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="8c59c-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="8c59c-105">Symptom</span></span>

<span data-ttu-id="8c59c-106">Sie haben eine benutzerdefinierte Excel-Vorlage für Finanzerfassungen erstellt, die jedoch nicht im Menü **Positionen in Excel öffnen** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c59c-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="8c59c-107">Sie wird alternativ im Menü angezeigt, es wird jedoch eine andere Vorlage geöffnet, wenn Sie sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="8c59c-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c59c-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="8c59c-108">Resolution</span></span>

<span data-ttu-id="8c59c-109">Die Standardfunktion „In Excel öffnen“ verwendet die Stammdatenquelle (Tabelle) der aktuellen Seite, um zu bestimmen, welche Office-Vorlagen oder Datenentitäten als Optionen im Menü **In Excel öffnen** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c59c-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="8c59c-110">Dieses Verhalten ist für Finanzerfassungen nicht ideal, da sie dieselben Tabellen (LedgerJournalTable und LedgerJournalTrans) wie die Stammdatenquelle vieler anderer Erfassungstypen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c59c-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="8c59c-111">Für Finanzerfassungen dient die Funktion „Positionen in Excel öffnen“ dazu, Vorlagen anzuzeigen, die für die Erfassung vorgesehen sind, in deren Kontext Sie gerade arbeiten, z. B. die allgemeine Erfassung oder eine Zahlungserfassung.</span><span class="sxs-lookup"><span data-stu-id="8c59c-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="8c59c-112">Eine Vorlage, die mit einer Kreditorzahlungserfassung verwendet werden soll, ist dafür vorgesehen, Ihr primäres Konto als Kreditorenkonto zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="8c59c-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="8c59c-113">Wenn Sie eine Vorlage höher stufen möchten, damit sie in den Menüs **Positionen in Excel öffnen** und **In Excel öffnen** verfügbar ist, muss eine einfache Entwicklerumgebung die Schnittstelle **LedgerIJournalExcelTemplate** implementieren und die Klasse **DocuTemplateRegistrationBase** erweitern.</span><span class="sxs-lookup"><span data-stu-id="8c59c-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="8c59c-114">Viele Beispiele für diesen Ansatz sind im System implementiert.</span><span class="sxs-lookup"><span data-stu-id="8c59c-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="8c59c-115">Ein Beispiel, das als Referenz verwendet werden kann, ist die Schnittstelle **LedgerDailyJournalExcelTemplate**, die für das Fibu Buch.-Blatt (oder die Tageserfassung) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c59c-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="8c59c-116">Wenn die Schnittstelle **LedgerIJournalExcelTemplate** für Ihre Vorlage implementiert ist, filtert das Menü **Positionen in Excel öffnen** Vorlagen nach dem Erfassungstyp Ihrer Erfassung und zeigt nur die Vorlagen an, die für diese Erfassung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8c59c-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="8c59c-117">Die Schnittstelle bietet außerdem eine Validierungsmethode, mit der sichergestellt wird, dass eine Vorlage für eine Erfassung nicht geöffnet werden kann, wenn sie die Anforderungen für den Kontotyp nicht erfüllt.</span><span class="sxs-lookup"><span data-stu-id="8c59c-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="8c59c-118">Sie können beispielsweise angeben, dass der Kontotyp vom Typ **Kreditor** oder **Sachkonto** ist.</span><span class="sxs-lookup"><span data-stu-id="8c59c-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="8c59c-119">Weitere Informationen zu dieser Funktion finden Sie unter [Vorlagen zum Menü „Positionen in Excel öffnen“ hinzufügen](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="8c59c-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
