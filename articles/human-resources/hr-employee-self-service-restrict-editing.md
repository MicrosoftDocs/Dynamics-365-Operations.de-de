---
title: Bearbeiten von persönlichen Informationen einschränken
description: Schränken Sie die Bearbeitung von Kontaktdetails durch Mitarbeiter in Dynamics 365 Human Resources ein.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e0d4dbc5b330045bc9f91abab4d43b09e4382
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794804"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="dcaeb-103">Bearbeiten von persönlichen Informationen einschränken</span><span class="sxs-lookup"><span data-stu-id="dcaeb-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="dcaeb-104">Dieses Thema beschreibt, wie Sie Mitarbeiter an der Bearbeitung von Kontaktdaten in Dynamics 365 Human Resources hindern können.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="dcaeb-105">Möglicherweise möchten Sie verhindern, dass Mitarbeiter bestimmte Kontaktdetails bearbeiten, z. B. ihren Lagerplatz oder ihre E-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="dcaeb-106">Um diese Funktion zu nutzen, müssen Sie zuerst **(Vorschau) Mitarbeiter vom Hinzufügen oder Bearbeiten von Adress- und Kontaktinformationen für ausgewählte Zwecke einschränken** in der Funktionsverwaltung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="dcaeb-107">Weitere Informationen zur Aktivierung der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="dcaeb-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="dcaeb-108">![Vorschaufunktion aktivieren](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="dcaeb-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="dcaeb-109">Wählen Sie die Informationen, die ein Mitarbeiter hinzufügen oder bearbeiten kann</span><span class="sxs-lookup"><span data-stu-id="dcaeb-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="dcaeb-110">Wählen Sie in der Personalverwaltung **Personalverwaltung** aus, wählen Sie **Links** aus und dann **Personalverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Gehen Sie zu Human Resources-Parameter](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="dcaeb-112">Wählen Sie auf der Seite **Parameter für Human Resources** die Registerkarte **Mitarbeiter-Self-Service**.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Wählen Sie Mitarbeiter-Self-Service](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="dcaeb-114">Deaktivieren Sie auf der Registerkarte **Mitarbeiter-Self-Service** alle Informationen im Abschnitt **Adress- und Kontaktinformationen**, die ein Mitarbeiter nicht hinzufügen oder bearbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="dcaeb-115">In diesem Beispiel haben wir das Häkchen bei **Geschäftliche** Kontaktinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Bearbeitung für geschäftliche Kontaktinformationen einschränken](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="dcaeb-117">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-117">Select **Save**.</span></span>

   ![Änderungen speichern](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="dcaeb-119">Erfahrung der Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="dcaeb-119">Employee experience</span></span>

<span data-ttu-id="dcaeb-120">Nachdem Sie Mitarbeitern das Hinzufügen oder Bearbeiten von Kontaktinformationen untersagt haben, können sie die Informationen zwar sehen, aber nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="dcaeb-121">In diesem Beispiel, in dem Mitarbeitern das Bearbeiten von **Geschäfts**-Kontaktdetails untersagt ist, können sie die Informationen dennoch im Mitarbeiter-Self-Service sehen:</span><span class="sxs-lookup"><span data-stu-id="dcaeb-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Geschäftskontaktdetails anzeigen](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="dcaeb-123">Wenn sie jedoch die geschäftlichen Kontaktdetails auswählen, wird der Bereich **Adresse bearbeiten** als schreibgeschützt angezeigt, und sie können keines der Felder ändern.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Geschäftskontakt-Details werden als schreibgeschützt angezeigt](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="dcaeb-125">Wenn sie **Hinzufügen** wählen, um eine neue Adresse hinzuzufügen, können sie außerdem nicht **Geschäftlich** aus dem Dropdown-Feld **Zweck** wählen.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Mitarbeiter kann keine Geschäftsadresse hinzufügen](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="dcaeb-127">Das gleiche Erlebnis haben Mitarbeiter, wenn sie **Kontaktdetails** auf der Seite **Persönliche Daten** wählen und eine neue Adresse hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="dcaeb-128">Die Dropdown-Box **Zweck** zeigt nur die Arten von Informationen an, die sie hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Der Mitarbeiter kann im Dropdown-Feld Zweck nicht Geschäftlich auswählen](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="dcaeb-130">**Kontaktdetails** zeigt jetzt **Zweck** im Raster an.</span><span class="sxs-lookup"><span data-stu-id="dcaeb-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Zweck wird im Raster der Kontaktdetails angezeigt](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="dcaeb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcaeb-132">See also</span></span>

[<span data-ttu-id="dcaeb-133">Mitarbeiter- und Manager-Self-Service-Übersicht</span><span class="sxs-lookup"><span data-stu-id="dcaeb-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="dcaeb-134">Parameter in Human Resources konfigurieren</span><span class="sxs-lookup"><span data-stu-id="dcaeb-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="dcaeb-135">Persönliche Daten bearbeiten</span><span class="sxs-lookup"><span data-stu-id="dcaeb-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)