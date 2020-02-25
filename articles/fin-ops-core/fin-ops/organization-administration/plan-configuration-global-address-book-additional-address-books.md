---
title: Planen für das globale Adressbuch und andere Adressbücher
description: Dieses Thema beschreibt die Überlegungen und die Entscheidungen, die Sie während des Planungsprozesses vornehmen müssen, bevor Sie das globale Adressbuch und alle zusätzlichen Adressbücher einrichten und konfigurieren.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aeed503500abf4f4b7ccf166f589d09bba306689
ms.sourcegitcommit: 7a855deed9f95ca2589f38db214890464b2b9061
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/13/2020
ms.locfileid: "2951208"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="89b70-103">Planen für das globale Adressbuch und andere Adressbücher</span><span class="sxs-lookup"><span data-stu-id="89b70-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89b70-104">Dieses Thema beschreibt die Überlegungen und die Entscheidungen, die Sie während des Planungsprozesses vornehmen müssen, bevor Sie das globale Adressbuch und alle zusätzlichen Adressbücher einrichten und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="89b70-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="89b70-105">Einige der Entscheidungen erfordern, dass Sie die Entscheidungen bestätigen, die für andere Bereiche des Produkts getroffen wurden, wie die Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="89b70-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="89b70-106">Globales Adressbuch</span><span class="sxs-lookup"><span data-stu-id="89b70-106">Global address book</span></span>

<span data-ttu-id="89b70-107">Bevor Sie beginnen mit dem globalen Adressbuch zu arbeiten, müssen Sie die dafür notwendigen Standardwerte bestimmen.</span><span class="sxs-lookup"><span data-stu-id="89b70-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="89b70-108">Diese Standardwerte werden dann für weitere Adressbücher verwendet, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="89b70-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="89b70-109">**Entscheidungen**</span><span class="sxs-lookup"><span data-stu-id="89b70-109">**Decisions**</span></span>

- <span data-ttu-id="89b70-110">In welcher Reihenfolge sollen die Namen der Parteidatensätze vom Typ **Person** angezeigt werden?</span><span class="sxs-lookup"><span data-stu-id="89b70-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="89b70-111">So kann beispielsweise eine Reihenfolge Nachname, zweiter Vorname, Vorname sein.</span><span class="sxs-lookup"><span data-stu-id="89b70-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="89b70-112">Müssen Parteidatensätze aus dem Adressbuch gelöscht werden, wenn die Rolle Datensatz gelöscht wird?</span><span class="sxs-lookup"><span data-stu-id="89b70-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="89b70-113">Sollte der Parteidatensatz auch gelöscht werden, wenn beispielsweise ein Debitorendatensatz gelöscht wird?</span><span class="sxs-lookup"><span data-stu-id="89b70-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="89b70-114">Sollten Benutzer benachrichtigt werden, sobald ein doppelter Datensatz im globalen Adressbuch gefunden wird, wenn ein neuer Datensatz erstellt wird?</span><span class="sxs-lookup"><span data-stu-id="89b70-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="89b70-115">Sollte die Data Universal Numbering System (DUNS)-Nummer in den Informationen eines Parteidatensatzes angezeigt werden?</span><span class="sxs-lookup"><span data-stu-id="89b70-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="89b70-116">Wenn die DUNS-Nummer in einem Parteidatensatz enthalten ist, sollte die Eindeutigkeit der Nummer überprüft werden?</span><span class="sxs-lookup"><span data-stu-id="89b70-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="89b70-117">Möchten Sie einen standardmäßigen Parteityp, -person oder -Organisation einrichten, wenn ein Parteidatensatz im globalen Adressbuch erstellt wird?</span><span class="sxs-lookup"><span data-stu-id="89b70-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="89b70-118">Welche Benutzerrollen sollen Zugriff auf private Adress- und Kontaktinformationen der Parteidatensätze haben?</span><span class="sxs-lookup"><span data-stu-id="89b70-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="89b70-119">Zusätzliche Adressbücher</span><span class="sxs-lookup"><span data-stu-id="89b70-119">Additional address books</span></span>

<span data-ttu-id="89b70-120">Nachdem Sie das globale Adressbuch erstellt haben, können Sie, wenn nötig, zusätzliche Adressbücher, wie z. B. ein separates Adressbuch für jedes Unternehmen in der Organisation oder für jede einzelne Sparte, erstellen.</span><span class="sxs-lookup"><span data-stu-id="89b70-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="89b70-121">Fabrikam beispielsweise ist eine internationale Organisation mit mehreren Unternehmen und Sparten.</span><span class="sxs-lookup"><span data-stu-id="89b70-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="89b70-122">Fabrikam plant die Erstellung eines Adressbuchs für jede Sparte.</span><span class="sxs-lookup"><span data-stu-id="89b70-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="89b70-123">Für Sparten mit mehreren Standorten wie der für pneumatische Werkzeuge, erstellt Fabrikam ein Adressbuch für jeden Standort.</span><span class="sxs-lookup"><span data-stu-id="89b70-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="89b70-124">Heiko, der IT-Manager bei Fabrikam, hat die folgende Liste von Adressbüchern erstellt, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="89b70-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="89b70-125">Diese Liste beschreibt auch die Parteidatensätze, die jedes Adressbuch enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="89b70-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="89b70-126">**Verträge Öffentlicher Sektor (PubSC)** – Parteidatensätze für alle Parteien, die an Verträgen im öffentlichen Sektor von Fabrikam beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="89b70-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="89b70-127">**Verträge Privatkundenbereich (PriSC)** – Parteidatensätze für alle Parteien, die an Verträgen im Privatkundenbereich von Fabrikam beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="89b70-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="89b70-128">**Elektronische Werkzeuge (ET)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von elektronischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-Japan eingekauften elektronischen Werkzeugen interagieren.</span><span class="sxs-lookup"><span data-stu-id="89b70-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="89b70-129">**Pneumatische Werkzeuge (PTJPN)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von pneumatischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-Japan eingekauften pneumatischen Werkzeugen interagieren.</span><span class="sxs-lookup"><span data-stu-id="89b70-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="89b70-130">**Pneumatische Werkzeuge (PTUSA)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von pneumatischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-USA eingekauften pneumatischen Werkzeugen interagieren.</span><span class="sxs-lookup"><span data-stu-id="89b70-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="89b70-131">**Entscheidung:**</span><span class="sxs-lookup"><span data-stu-id="89b70-131">**Decision:**</span></span>

- <span data-ttu-id="89b70-132">Wie viele zusätzliche Adressbücher wollen Sie erstellen?</span><span class="sxs-lookup"><span data-stu-id="89b70-132">How many additional address books will you create?</span></span>
