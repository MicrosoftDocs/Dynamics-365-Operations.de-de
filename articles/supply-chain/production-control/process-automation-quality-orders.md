---
title: Rufen Sie Prozessautomatisierungsabläufe auf, um Qualitätsaufträge zu erstellen
description: Dieses Thema bietet Ressourcen für die Verwendung Power Automate Geschäftsprozesse am Beispiel von Qualitätsaufträgen zu automatisieren.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115186"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="c3a9e-103">Rufen Sie Prozessautomatisierungsabläufe auf, um Qualitätsaufträge zu erstellen</span><span class="sxs-lookup"><span data-stu-id="c3a9e-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="c3a9e-104">Unternehmen haben eine zunehmende Nachfrage nach der Automatisierung von Standardgeschäftsprozessen, nach einer bequemeren Interaktion mit den Mitarbeitern und nach der Verwendung verschiedener Datensignale und -Systeme, um Geschäftsprozesse automatisch zu steuern.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="c3a9e-105">Mit robotergesteuertr Prozessautomatisierung (RPA) und Microsoft Power Automate können Unternehmen eine No-Code-Erfahrung nutzen, um sich wiederholende Prozesse zu automatisieren und so Effizienz und Genauigkeit zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="c3a9e-106">Die herunterladbare Vorlage für Automatisierungslösungen für Supply Chain Management zeigt, wie Power Automate verwendet werden kann, um Geschäftsprozesse am Beispiel von Qualitätsaufträgen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="c3a9e-107">Sie können die Vorlage für die Automatisierungslösung [Hier ](https://aka.ms/D365SCMQualityOrderRPASolution) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="c3a9e-108">Eine Übersicht über diese Funktion und ihre Funktionen finden Sie im folgenden Video: [Verwenden Sie RPA, um Qualitätsaufträge in Dynamics 365 Supply Chain Management zu erstellen](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="c3a9e-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="c3a9e-109">![Automatisierungsoptionen mit RPA](media/rpa-automation-options.png "Automatisierungsoptionen mit RPA")</span><span class="sxs-lookup"><span data-stu-id="c3a9e-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="c3a9e-110">Die Power Automate Lösungsvorlage enthält einen Cloud-Automatisierungsablauf und einen Desktop-Automatisierungsablauf, die die Erstellung von Qualitätsaufträgen im Supply Chain Management automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="c3a9e-111">Die Automatisierung kann als Reaktion auf viele Ereignisse und Signale gestartet werden, einschließlich Benutzereingaben oder Maschinensignalen (einschließlich Internet of Things (IoT)).</span><span class="sxs-lookup"><span data-stu-id="c3a9e-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="c3a9e-112">Das *Q-Order* Power Anwendungs-Beispiel ist in der Lösungsvorlage enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="c3a9e-113">Der Benutzer kann mit einer Kamera einen Artikel-QR-Code scannen, die Menge eingeben und Bilder anhängen.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="c3a9e-114">Lösungsparameter sind enthalten, um die Automatisierung für einen bestimmten Anwendungsfall in einer Produktionsanlage zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c3a9e-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="c3a9e-115">![Qualitätsprüfungsauftrag erstellen](media/rpa-create-quality-roder.png "Qualitätsprüfungsauftrag erstellen")</span><span class="sxs-lookup"><span data-stu-id="c3a9e-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="c3a9e-116">Eine vollständige Schritt-für-Schritt-Anleitung zum Herunterladen, Installieren und Verwenden der Beispiellösung zur Automatisierung der Erstellung von Qualitätsaufträgen finden Sie unter [Automatisieren Sie die Erstellung von Qualitätsaufträgen im Dynamics 365 Supply Chain Management mit robotergesteuerter Prozessautomatisierung mithilfe von Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="c3a9e-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

