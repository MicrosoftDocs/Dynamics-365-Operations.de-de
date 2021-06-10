---
title: Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren
description: Konfigurieren Sie Parameter für die Vorteilsverwaltung je Unternehmen in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057621"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="b2ec0-103">Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b2ec0-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b2ec0-104">Für jede Organisation, die Vorteile bereitstellt, müssen Sie Einstellungen für E-Mails zur Vorteilsbestätigung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="b2ec0-105">Einstellungen für Bestätigungs-E-Mail konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b2ec0-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="b2ec0-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="b2ec0-107">Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="b2ec0-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="b2ec0-108">Feld</span><span class="sxs-lookup"><span data-stu-id="b2ec0-108">Field</span></span> | <span data-ttu-id="b2ec0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2ec0-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b2ec0-110">**Bestätigungs-E-Mail senden**</span><span class="sxs-lookup"><span data-stu-id="b2ec0-110">**Send confirmation email**</span></span> | <span data-ttu-id="b2ec0-111">Wenn diese Funktion aktiviert ist, wird eine Bestätigungs-E-Mail an die Mitarbeiter gesendet, wenn sie sich aus der Umgebung zur Vorteilsregistrierung im Mitarbeiter-Self-Service abmelden.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="b2ec0-112">**E-Mail-Vorlage für Bestätigung**</span><span class="sxs-lookup"><span data-stu-id="b2ec0-112">**Confirmation email template**</span></span> | <span data-ttu-id="b2ec0-113">Wählen Sie die E-Mail-Vorlage der Organisation aus, die beim Senden der Anmeldebestätigung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="b2ec0-114">Wenn Sie keine Vorlage auswählen, wird die folgende allgemeine E-Mail gesendet:</span><span class="sxs-lookup"><span data-stu-id="b2ec0-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="b2ec0-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="b2ec0-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="b2ec0-116">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="b2ec0-116">Congratulations!</span></span> <span data-ttu-id="b2ec0-117">Sie haben sich erfolgreich für Vorteile angemeldet.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="b2ec0-118">Vielen Dank,</span><span class="sxs-lookup"><span data-stu-id="b2ec0-118">Thank you,</span></span><br><span data-ttu-id="b2ec0-119">Vorteil <Name des Unternehmens/der Organisation>.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="b2ec0-120">**Standard-E-Mail-Adresse des Absenders**</span><span class="sxs-lookup"><span data-stu-id="b2ec0-120">**Default email sender address**</span></span> | <span data-ttu-id="b2ec0-121">Die E-Mail-Adresse, die beim Senden der Bestätigungs-E-Mail verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="b2ec0-122">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b2ec0-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]