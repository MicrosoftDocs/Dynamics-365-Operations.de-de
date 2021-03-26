---
title: Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft
description: In diesem Thema wird die Auftragserstellung per Einzelzulauf für Geschäftstransaktionen in Microsoft Dynamics 365 Commerce beschrieben.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0fdb1f636183e8365729ab8947a50614a77eaeac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211044"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="50e51-103">Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft</span><span class="sxs-lookup"><span data-stu-id="50e51-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="50e51-104">In den Versionen Dynamics 365 Retail 10.0.4 und früher ist die Buchung der Aufstellungen ein Vorgang, der am Tagesende durchgeführt wird. Alle Transaktionen werden am Ende des Tages in den Büchern gebucht.</span><span class="sxs-lookup"><span data-stu-id="50e51-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="50e51-105">Große Transaktionen müssen dann in einem begrenzten Zeitfenster verarbeitet werden, was manchmal zu Lade- und Sperrproblemen und Fehlern bei der Buchung von Aufstellungen führt.</span><span class="sxs-lookup"><span data-stu-id="50e51-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="50e51-106">Einzelhändler können so außerdem nicht den ganzen Tag über Einnahmen und Zahlungen in ihren Büchern erfassen.</span><span class="sxs-lookup"><span data-stu-id="50e51-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="50e51-107">Mit der in Retail-Version 10.0.5 eingeführten Auftragserstellung per Einzelzulauf werden Transaktionen den ganzen Tag über bearbeitet. Am Ende des Tages werden nur eine Abstimmung der Zahlungsmittel und andere Bargeldverwaltungstransaktionen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="50e51-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="50e51-108">Diese Funktionalität verteilt den Aufwand für die Erstellung von Aufträgen, Rechnungen und Zahlungen auf den gesamten Tag und sorgt so für eine bessere Leistung und die Möglichkeit, Umsätze und Zahlungen in den Büchern nahezu in Echtzeit zu verbuchen.</span><span class="sxs-lookup"><span data-stu-id="50e51-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="50e51-109">So arbeiten Sie mit der Einzelzulaufbuchung</span><span class="sxs-lookup"><span data-stu-id="50e51-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="50e51-110">Um die Buchung auf Basis von Einzelzuläufen für Einzelhandelstransaktionen zu aktivieren, aktivieren Sie die Funktion **Einzelhandelsaufstellungen – Einzelzulauf** mit der Funktionsverwaltung.</span><span class="sxs-lookup"><span data-stu-id="50e51-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="50e51-111">Bevor Sie diese Funktion aktivieren, stellen Sie sicher, dass keine ausstehenden Anweisungen zur Veröffentlichung anstehen.</span><span class="sxs-lookup"><span data-stu-id="50e51-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="50e51-112">Das aktuelle Anweisungsdokument wird in zwei Typen unterteilt: Transaktionsaufstellung und Finanzaufstellung.</span><span class="sxs-lookup"><span data-stu-id="50e51-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="50e51-113">Die Transaktionsaufstellung erfasst alle nicht gebuchten und geprüften Transaktionen und erstellten Aufträge, Verkaufsrechnungen, Zahlungs‑ und Rabatterfassungen sowie die Einnahmen‑ und Ausgabentransaktionen in der von Ihnen konfigurierten Kadenz.</span><span class="sxs-lookup"><span data-stu-id="50e51-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="50e51-114">Sie sollten diesen Prozess so konfigurieren, dass er sehr häufig ausgeführt wird, sodass Dokumente erstellt werden, wenn die Einzelhandelstransaktionen über den P-Job in die Zentralverwaltung hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="50e51-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="50e51-115">Mit der Transaktionsaufstellung, die bereits Aufträge und Verkaufsrechnungen erstellt, ist es nicht wirklich notwendig, den Batchauftrag **Lager buchen** zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="50e51-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="50e51-116">Sie können ihn jedoch weiterhin verwenden, um möglicherweise vorhandene geschäftliche Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="50e51-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="50e51-117">Die Finanzaufstellung ist für die Erstellung am Ende des Tages ausgelegt und unterstützt nur die Abschlussmethode **Schicht**.</span><span class="sxs-lookup"><span data-stu-id="50e51-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="50e51-118">Diese Aufstellung beschränkt sich auf die finanzielle Abstimmung und erstellt nur die Erfassungen zu den Differenzbeträgen zwischen gezähltem Betrag und Transaktionsbetrag für die verschiedenen Zahlungsmittel sowie Erfassungen zu anderen Bargeldverwaltungstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="50e51-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="50e51-119">Um die Transaktionsaufstellung zu berechnen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Transaktionsaufstellungen stapelweise berechnen**.</span><span class="sxs-lookup"><span data-stu-id="50e51-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="50e51-120">Um die Transaktionsaufstellungen stapelweise zu buchen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Transaktionsaufstellungen stapelweise buchen**.</span><span class="sxs-lookup"><span data-stu-id="50e51-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="50e51-121">Um die Finanzaufstellung zu berechnen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Finanzaufstellungen stapelweise berechnen**.</span><span class="sxs-lookup"><span data-stu-id="50e51-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="50e51-122">Um die Finanzaufstellungen stapelweise zu buchen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Finanzaufstellungen stapelweise buchen**.</span><span class="sxs-lookup"><span data-stu-id="50e51-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="50e51-123">Die Menüpunkte **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Aufstellungen stapelweise berechnen** und **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Aufstellungen stapelweise buchen** werden mit dieser neuen Funktion entfernt.</span><span class="sxs-lookup"><span data-stu-id="50e51-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="50e51-124">Alternativ können Transaktions- und Finanzaufstellungen manuell angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="50e51-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="50e51-125">Wechseln Sie zu **Retail und Commerce > Kanäle > Shops**, und klicken Sie auf **Aufstellungen**.</span><span class="sxs-lookup"><span data-stu-id="50e51-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="50e51-126">Klicken Sie auf **Neu**, und wählen Sie dann den Typ der Aufstellung aus, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="50e51-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="50e51-127">Felder auf der Seite **Aufstellungen** und Aktionen unter der Gruppe **Aufstellung** auf der Seite zeigen relevante Daten und Aktionen basierend auf dem ausgewählten Aufstellungstyp an.</span><span class="sxs-lookup"><span data-stu-id="50e51-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]