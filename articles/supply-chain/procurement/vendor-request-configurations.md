---
title: Konfigurationen für Kreditorenanforderungen
description: In diesem Thema werden die Felder beschrieben, deren Auffüllung in einer neuen Kreditorenanforderung erforderlich ist.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a78ec681ff9bfe9f7792da04553e4b543bf4a183
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809301"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="c97bb-103">Konfigurationen für Kreditorenanforderungen</span><span class="sxs-lookup"><span data-stu-id="c97bb-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c97bb-104">Um eine Kreditorenanforderung abzuschließen, muss eine Kontaktperson des Kreditors den Registrierungs-Assistenten des künftigen Kreditors abschließen.</span><span class="sxs-lookup"><span data-stu-id="c97bb-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="c97bb-105">Im Formular **Kreditorenanforderungskonfigurationen** können Sie Profile erstellen, die erforderliche Felder und sichtbare Felder im Registrierungs-Assistenten des künftigen Kreditors angeben.</span><span class="sxs-lookup"><span data-stu-id="c97bb-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="c97bb-106">Der Kreditorenregistrierungs-Assistent beginnt, indem er den künftigen Kreditorbenutzer fragt, in welchem Land/Region der Kreditor geschäftliche tätig ist.</span><span class="sxs-lookup"><span data-stu-id="c97bb-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="c97bb-107">Diese Information bestimmt die anzuwendende Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c97bb-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="c97bb-108">Wenn keine bestimmte Konfiguration für ein Land/eine Region definiert wird, wird eine Standardkonfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="c97bb-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="c97bb-109">Eine Kreditorenanforderungskonfiguration einrichten</span><span class="sxs-lookup"><span data-stu-id="c97bb-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="c97bb-110">Standardmäßig ist eine Kreditorenkonfiguration im Kreditorenanforderungskonfigurationsformular verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c97bb-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="c97bb-111">Es ist nicht möglich, Länder/Regionen für die Standardkonfiguration auszuwählen, somit kann der Abschnitt **Länder/Regionen** nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c97bb-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="c97bb-112">Klicken Sie auf **Beschaffung** > **Einstellungen** > **Kreditoren**, und klicken Sie dann auf **Kreditorenanforderungskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c97bb-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="c97bb-113">Klicken Sie auf die Registerkarte **Felder**, um den Status der aufgeführten Felder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c97bb-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="c97bb-114">Ausgeblendet (Nicht sichtbar)</span><span class="sxs-lookup"><span data-stu-id="c97bb-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="c97bb-115">Angezeigt (Sichtbar, aber nicht obligatorisch)</span><span class="sxs-lookup"><span data-stu-id="c97bb-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="c97bb-116">Erorderlich (Sichbar und obligatorisch)</span><span class="sxs-lookup"><span data-stu-id="c97bb-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="c97bb-117">Klicken Sie auf die Registerkarte **Inhalt**, um anzugeben, ob Text im Assistenten angezeigt wird und ob es eine Bestätigung geben soll, dass der künftige Kreditorenbenutzer diesen bestätigen muss, bevor er zum nächsten Schritt im Assistenten wechselt.</span><span class="sxs-lookup"><span data-stu-id="c97bb-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="c97bb-118">Die Bestätigung wird für alle Bedingungen angefordert, die der Benutzer akzeptieren muss, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c97bb-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="c97bb-119">Sie können auch eine Bestätigungsmeldung eingeben, die angezeigt wird, wenn der Assistent abgeschlossen ist, und Sie können einen oder mehrere Fragebögen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c97bb-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="c97bb-120">Erstellen einer Kreditorenkonfiguration für ein bestimmtes Land/Region</span><span class="sxs-lookup"><span data-stu-id="c97bb-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="c97bb-121">Klicken Sie auf **Beschaffung** > **Einstellungen** > **Kreditoren**, und klicken Sie dann auf **Kreditorenanforderungskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c97bb-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="c97bb-122">Klicken Sie auf **Neu**, um eine neue Konfiguration zu erstellen, und geben Sie einen Namen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c97bb-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="c97bb-123">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c97bb-123">Click **Save**.</span></span>
4.  <span data-ttu-id="c97bb-124">Öffnen Sie die Registerkarte **Land/Regionen**, um das Land/die Region auszuwählen, für das/die die Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c97bb-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="c97bb-125">Schließen Sie die Konfiguration ab, indem Sie die für Richtlinien die Standardkonfiguration befolgen.</span><span class="sxs-lookup"><span data-stu-id="c97bb-125">Complete the configuration by following the guidelines for the default configuration.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]