---
title: Funktionen verwalten
description: In diesem Thema wird beschrieben, wie ein Administrator die Vorschaufunktionen in Microsoft Dynamics 365 Talent aktivieren kann, und es werden die Funktionen aufgeführt, die derzeit für Vorschau aktiviert sind.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006427"
---
# <a name="manage-features"></a><span data-ttu-id="968a6-103">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="968a6-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="968a6-104">Im Rahmen unseres kontinuierlichen Rollouts von Human Capital Management (HCM) Funktionen für Microsoft Dynamics 365 Human Resources, wollen wir unseren Kunden so schnell wie möglich neue Funktionen zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="968a6-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="968a6-105">Administratoren können Vorschaufunktionen in ihrer Umgebung sehen und nutzen.</span><span class="sxs-lookup"><span data-stu-id="968a6-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="968a6-106">Diese Funktionen sind fast fertig für die allgemeine Verfügbarkeit und wurden ausgiebig getestet.</span><span class="sxs-lookup"><span data-stu-id="968a6-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="968a6-107">Wir sind nur auf der Suche nach einer letzten Runde von Kunden-Feedback und Validierung, bevor wir sie zur allgemeinen Verfügbarkeit veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="968a6-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="968a6-108">In diesem Thema wird beschrieben, wie Sie die Vorschaufunktionen aktivieren können, und es werden die Funktionen aufgeführt, die derzeit für Vorschau aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="968a6-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="968a6-109">Diese Liste wird aktualisiert, wenn die Funktionen zur allgemeinen Verfügbarkeit freigegeben werden und wenn neue Funktionen zur Vorschau freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="968a6-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="968a6-110">Es erfolgt keine Benachrichtigung, wenn neue Funktionen zur Vorschau freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="968a6-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="968a6-111">Die Benutzer werden nur beginnen, die Funktionen zu sehen.</span><span class="sxs-lookup"><span data-stu-id="968a6-111">Users will just start to see the features.</span></span> <span data-ttu-id="968a6-112">Weitere Informationen über neue Funktionen im Talent, finden Sie unter [Neuheiten oder Änderungen in Dynamics 365 Talent](./whats-new.md) und [Dynamics 365 und Power Platform-Versionshinweise](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="968a6-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="968a6-113">Vorschaufunktionen aktivieren oder deaktivieren</span><span class="sxs-lookup"><span data-stu-id="968a6-113">Enable or disable preview features</span></span>

<span data-ttu-id="968a6-114">Um auf Vorschaufunktionen zugreifen zu können, müssen Sie sie in Ihrer Umgebung zunächst aktivieren.</span><span class="sxs-lookup"><span data-stu-id="968a6-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="968a6-115">Aktivieren oder Deaktivieren von Vorschaufunktionen ist umgebungsspezifisch.</span><span class="sxs-lookup"><span data-stu-id="968a6-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="968a6-116">Durch das Aktivieren der Einstellung **Vorschaufunktionen** aktivieren Sie Vorschaufunktionen für alle Benutzer in Ihrer Organisation, die sich in dieser Umgebung befinden.</span><span class="sxs-lookup"><span data-stu-id="968a6-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="968a6-117">Wenn Sie die Einstellung deaktivieren, deaktivieren Sie die Vorschaufunktionen und machen sie für Ihre Benutzer unzugänglich.</span><span class="sxs-lookup"><span data-stu-id="968a6-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="968a6-118">Die Vorschaufunktionen werden in Talent nur eingeschränkt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="968a6-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="968a6-119">Sie verwenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen und sind nicht in der Talent-Service-Level-Vereinbarung (SLA) enthalten.</span><span class="sxs-lookup"><span data-stu-id="968a6-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="968a6-120">Sie sollten keine Vorschaufunktionen verwenden, um personenbezogene Daten (d. h. Informationen, die Sie identifizieren könnten) oder andere Daten zu verarbeiten, die gesetzlichen oder behördlichen Anforderungen unterliegen.</span><span class="sxs-lookup"><span data-stu-id="968a6-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="968a6-121">Attract</span><span class="sxs-lookup"><span data-stu-id="968a6-121">Attract</span></span>

1. <span data-ttu-id="968a6-122">Melden Sie sich bei Microsoft Dynamics 365 Talent: Attract an.</span><span class="sxs-lookup"><span data-stu-id="968a6-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="968a6-123">Wählen Sie im **Setup**-Menü (das Zahnradsymbol) in der oberen rechten Ecke **Admin Center**.</span><span class="sxs-lookup"><span data-stu-id="968a6-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="968a6-124">Wählen Sie auf der Registerkarte **Funktion-Verwaltung** die Option neben **Vorschau-Funktion**, so dass sie blau wird und anzeigt **Ein**.</span><span class="sxs-lookup"><span data-stu-id="968a6-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Vorschaufunktionen aktivieren in Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="968a6-126">Dient zum Auswählen oder stornieren von einzelnen Vorschaufunktionen.</span><span class="sxs-lookup"><span data-stu-id="968a6-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="968a6-127">Wenn Sie nichts tun, werden alle verfügbaren Vorschaufunktionen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="968a6-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="968a6-128">Aktualisieren Sie Ihren Browser, um die neuen Funktionen zu sehen.</span><span class="sxs-lookup"><span data-stu-id="968a6-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="968a6-129">Alle Benutzer, die bereits angemeldet sind, sehen die Funktionen beim nächsten Mal, wenn sie sich anmelden, oder sie können ihren Browser aktualisieren, um die Funktionen sofort zu sehen.</span><span class="sxs-lookup"><span data-stu-id="968a6-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="968a6-130">Einige Vorschaufunktionen erfordern ggf. zusätzliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="968a6-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="968a6-131">Folgen Sie den Links neben der Vorschaufunktion, um die Einstellungen für diese durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="968a6-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="968a6-132">Feedback</span><span class="sxs-lookup"><span data-stu-id="968a6-132">Feedback</span></span>

<span data-ttu-id="968a6-133">Wir möchten von Ihnen über Ihre Erfahrung mit diesen Vorschaufunktionen hören</span><span class="sxs-lookup"><span data-stu-id="968a6-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="968a6-134">Wir empfehlen Ihnen, Ihr Feedback regelmäßig auf den folgenden Seiten zu veröffentlichen, wenn Sie diese oder andere Funktionen nutzen:</span><span class="sxs-lookup"><span data-stu-id="968a6-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="968a6-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) - Diese Seite ist eine großartige Ressource, auf der Benutzer Anwendungsfälle diskutieren, Fragen stellen und Hilfe von der Community erhalten können.</span><span class="sxs-lookup"><span data-stu-id="968a6-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="968a6-136">Teilen Sie uns mit, welche Funktionen Sie im Produkt sehen möchten und welche Änderungen Ihrer Meinung nach an bestehenden Funktionen vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="968a6-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="968a6-137">Verwenden Sie die folgenden Webseiten, um Produktideen vorzuschlagen:</span><span class="sxs-lookup"><span data-stu-id="968a6-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="968a6-138">Attract Ideen</span><span class="sxs-lookup"><span data-stu-id="968a6-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="968a6-139">Onboard Ideen</span><span class="sxs-lookup"><span data-stu-id="968a6-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="968a6-140">Stellen Sie sicher, dass Sie keine persönlichen Daten (Informationen, die Sie identifizieren könnten) in Ihre Feedback- oder Produktbewertungseinreichungen mitsenden.</span><span class="sxs-lookup"><span data-stu-id="968a6-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="968a6-141">Die gesammelten Informationen können weiter analysiert werden und werden nicht zur Beantwortung von Anfragen im Rahmen der geltenden Datenschutzgesetze verwendet.</span><span class="sxs-lookup"><span data-stu-id="968a6-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="968a6-142">Personenbezogene Daten, die im Rahmen dieser Programme separat erfasst werden, unterliegen der [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="968a6-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="968a6-143">Setzen Sie ein Lesezeichen für dieses Thema und schauen Sie regelmäßig vorbei, um über neue Vorschaufunktionen auf dem Laufenden zu bleiben, wenn wir sie veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="968a6-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="968a6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="968a6-144">See also</span></span>

- [<span data-ttu-id="968a6-145">Talent Apps testen oder kaufen</span><span class="sxs-lookup"><span data-stu-id="968a6-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="968a6-146">Was ist neu oder geändert in Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="968a6-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="968a6-147">Freigabepläne</span><span class="sxs-lookup"><span data-stu-id="968a6-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="968a6-148">Sie erhalten Unterstützung für Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="968a6-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
