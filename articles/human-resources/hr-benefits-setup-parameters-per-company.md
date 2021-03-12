---
title: Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren
description: Konfigurieren Sie Parameter für die Vorteilsverwaltung je Unternehmen in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "4984599"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="85ec8-103">Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="85ec8-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="85ec8-104">Für jede Organisation, die Vorteile bereitstellt, müssen Sie Einstellungen für E-Mails zur Vorteilsbestätigung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="85ec8-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="85ec8-105">Einstellungen für Bestätigungs-E-Mail konfigurieren</span><span class="sxs-lookup"><span data-stu-id="85ec8-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="85ec8-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="85ec8-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="85ec8-107">Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="85ec8-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="85ec8-108">Feld</span><span class="sxs-lookup"><span data-stu-id="85ec8-108">Field</span></span> | <span data-ttu-id="85ec8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85ec8-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="85ec8-110">**Bestätigungs-E-Mail senden**</span><span class="sxs-lookup"><span data-stu-id="85ec8-110">**Send confirmation email**</span></span> | <span data-ttu-id="85ec8-111">Wenn diese Funktion aktiviert ist, wird eine Bestätigungs-E-Mail an die Mitarbeiter gesendet, wenn sie sich aus der Umgebung zur Vorteilsregistrierung im Mitarbeiter-Self-Service abmelden.</span><span class="sxs-lookup"><span data-stu-id="85ec8-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="85ec8-112">**E-Mail-Vorlage für Bestätigung**</span><span class="sxs-lookup"><span data-stu-id="85ec8-112">**Confirmation email template**</span></span> | <span data-ttu-id="85ec8-113">Wählen Sie die E-Mail-Vorlage der Organisation aus, die beim Senden der Anmeldebestätigung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85ec8-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="85ec8-114">Wenn Sie keine Vorlage auswählen, wird die folgende allgemeine E-Mail gesendet:</span><span class="sxs-lookup"><span data-stu-id="85ec8-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="85ec8-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="85ec8-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="85ec8-116">herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="85ec8-116">Congratulations!</span></span> <span data-ttu-id="85ec8-117">Sie haben sich erfolgreich für Vorteile angemeldet.</span><span class="sxs-lookup"><span data-stu-id="85ec8-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="85ec8-118">Vielen Dank,</span><span class="sxs-lookup"><span data-stu-id="85ec8-118">Thank you,</span></span><br><span data-ttu-id="85ec8-119">Vorteil <Name des Unternehmens/der Organisation>.</span><span class="sxs-lookup"><span data-stu-id="85ec8-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="85ec8-120">**Standard-E-Mail-Adresse des Absenders**</span><span class="sxs-lookup"><span data-stu-id="85ec8-120">**Default email sender address**</span></span> | <span data-ttu-id="85ec8-121">Die E-Mail-Adresse, die beim Senden der Bestätigungs-E-Mail verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85ec8-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="85ec8-122">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="85ec8-122">Select **Save**.</span></span>