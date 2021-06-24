---
title: Regulatory Configuration Service
description: Dieses Thema bietet einen Überblick über die Funktionen des Regulatory Configuration Service (RCS) und erläutert den Zugriff auf den Dienst.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216561"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="88e81-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="88e81-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88e81-104">Der Regulatory Configuration Service (RCS) ist ein eigenständiger Designer- und Lebenszyklusverwaltungsdienst für No-Code-/Low-Code-Globalisierungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="88e81-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="88e81-105">Mit RCS können Beteiligte der Globalisierung wichtige Globalisierungsbereiche wie Steuern, elektronische Rechnungsstellung, behördliche Berichterstattung, Bank- und Geschäftsdokumente erweitern und anpassen, ohne Entwickler einbeziehen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="88e81-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="88e81-106">Dieser No-Code/Low-Code-Globalisierungsansatz macht die Globalisierung einfacher, schneller und kostengünstiger zu erstellen oder zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="88e81-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="88e81-107">RCS bietet folgende Funktionen:</span><span class="sxs-lookup"><span data-stu-id="88e81-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="88e81-108">Unterstützung aller Funktionen, die durch die elektronische Berichterstellung (EB) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="88e81-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="88e81-109">Voraussetzung für die Konfiguration neuer Globalisierungs-Microservices.</span><span class="sxs-lookup"><span data-stu-id="88e81-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="88e81-110">Unterstützung der elektronischen Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="88e81-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="88e81-111">Weitere Informationen finden Sie unter [Elektronische Rechnungsstellung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="88e81-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="88e81-112">Unterstützung der Steuerberechnung.</span><span class="sxs-lookup"><span data-stu-id="88e81-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="88e81-113">Weitere Informationen finden Sie unter [Steuerdienst](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="88e81-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="88e81-114">Unterstützung für neue Funktionen für Globalisierungsfunktionen, die das Lebenszyklusmanagement von Mehrkomponentenfunktionen vereinfachen und zusätzliche Funktionen zum Konfigurieren von Aktionen und zum Einrichten von Funktionsparametern bieten.</span><span class="sxs-lookup"><span data-stu-id="88e81-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="88e81-115">Weitere Informationen finden Sie unter [Regulatory Configuration Service – vereinfachtes Management von Globalisierungsfunktionen für Globalisierungsdienste](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="88e81-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="88e81-116">Unterstützung für die zentrale Veröffentlichung, Speicherung und Freigabe von benutzerdefinierten Konfigurationen im globalen Repository, um die Konfigurationsverwaltung zu vereinfachen, ohne dass die Verwendung von Microsoft Dynamics Lifecycle Services (LCS) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="88e81-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="88e81-117">Zugriff auf RCS</span><span class="sxs-lookup"><span data-stu-id="88e81-117">Access RCS</span></span>

<span data-ttu-id="88e81-118">Sie können sich über die [Seite „Regulatory Configuration Service“](https://marketing.configure.global.dynamics.com/) für RCS anmelden oder sich bei RCS anmelden.</span><span class="sxs-lookup"><span data-stu-id="88e81-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS-Registrierung/-Anmeldung](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="88e81-120">Überprüfen und akzeptieren Sie auf der Seite **Regulatory Configuration Service** die ergänzenden Nutzungsbedingungen für den Dienst und wählen Sie dann eine der folgenden Schaltflächen aus:</span><span class="sxs-lookup"><span data-stu-id="88e81-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="88e81-121">**Registrieren**, wenn Sie den Dienst zum ersten Mal nutzen und eine geschäftliche E-Mail-Adresse verwenden, um Ihrem Unternehmen eine Dienstumgebung bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="88e81-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="88e81-122">**Anmelden**, wenn Sie sich zuvor schon für den Dienst angemeldet haben und auf Ihre Organisationsumgebung zugreifen möchten</span><span class="sxs-lookup"><span data-stu-id="88e81-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="88e81-123">Regionale Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="88e81-123">Regional availability</span></span>

<span data-ttu-id="88e81-124">RCS ist allgemein in folgenden Regionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="88e81-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="88e81-125">Vereinigte Staaten</span><span class="sxs-lookup"><span data-stu-id="88e81-125">United States</span></span>
- <span data-ttu-id="88e81-126">Indien</span><span class="sxs-lookup"><span data-stu-id="88e81-126">India</span></span>
- <span data-ttu-id="88e81-127">Frankreich</span><span class="sxs-lookup"><span data-stu-id="88e81-127">France</span></span>
- <span data-ttu-id="88e81-128">Europa</span><span class="sxs-lookup"><span data-stu-id="88e81-128">Europe</span></span>

<span data-ttu-id="88e81-129">Eine vollständige Liste der Regionen finden Sie unter [Dynamics 365 und Power Platform: Verfügbarkeit, Datenstandort, Sprache und Lokalisierung](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="88e81-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="88e81-130">RCS-Standardunternehmen</span><span class="sxs-lookup"><span data-stu-id="88e81-130">RCS default company</span></span>

<span data-ttu-id="88e81-131">Die in RCS verwendete Designzeitfunktionalität wird von allen Unternehmen gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="88e81-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="88e81-132">Es gibt keine unternehmensspezifische Funktion.</span><span class="sxs-lookup"><span data-stu-id="88e81-132">There is no company-specific functionality.</span></span> <span data-ttu-id="88e81-133">Daher empfehlen wir Ihnen, ein Unternehmen **DAT** in Ihrer RCS-Umgebung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="88e81-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="88e81-134">In einigen Szenarien möchten Sie jedoch möglicherweise, dass ER-Formate Parameter verwenden, die sich auf eine bestimmte juristische Person beziehen.</span><span class="sxs-lookup"><span data-stu-id="88e81-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="88e81-135">Nur in diesen Szenarien sollten Sie den standardmäßigen Firmenumschalter verwenden.</span><span class="sxs-lookup"><span data-stu-id="88e81-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="88e81-136">Ein Beispiel finden Sie unter [ER-Format zur Verwendung von Parametern konfigurieren, die pro juristischer Person angegeben werden](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="88e81-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="88e81-137">Zugehörige RCS-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="88e81-137">Related RCS documentation</span></span>

<span data-ttu-id="88e81-138">Weitere Informationen zu den zugehörigen Komponenten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="88e81-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="88e81-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="88e81-139">**RCS:**</span></span>

    - [<span data-ttu-id="88e81-140">EB-Konfigurationen in RCS erstellen und in das globale Repository hochladen</span><span class="sxs-lookup"><span data-stu-id="88e81-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="88e81-141">**Globales Repository:**</span><span class="sxs-lookup"><span data-stu-id="88e81-141">**Global repository:**</span></span>

    - [<span data-ttu-id="88e81-142">Eine EB-Konfiguration erstellen und in das globale Repository hochladen</span><span class="sxs-lookup"><span data-stu-id="88e81-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="88e81-143">Konfiguration im globalen Repository freigeben</span><span class="sxs-lookup"><span data-stu-id="88e81-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="88e81-144">Verbesserte Filterung im globalen Repository</span><span class="sxs-lookup"><span data-stu-id="88e81-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="88e81-145">EB-Konfigurationen aus dem globalen Repository herunterladen</span><span class="sxs-lookup"><span data-stu-id="88e81-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="88e81-146">Konfigurationen im globalen Repository einstellen</span><span class="sxs-lookup"><span data-stu-id="88e81-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="88e81-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)-Speichereinstellung</span><span class="sxs-lookup"><span data-stu-id="88e81-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="88e81-148">**Globalisierungsfunktion:**</span><span class="sxs-lookup"><span data-stu-id="88e81-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="88e81-149">Regulatory Configuration Service (RCS) – Globalisierungsfunktion</span><span class="sxs-lookup"><span data-stu-id="88e81-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="88e81-150">Problembehandlung bei der RCS-Registrierung</span><span class="sxs-lookup"><span data-stu-id="88e81-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="88e81-151">Wenn Sie sich über die Serviceseite bei RCS anmelden, tritt möglicherweise ein Problem auf, das mit Azure Active Directory (Azure AD) zusammenhängt.</span><span class="sxs-lookup"><span data-stu-id="88e81-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="88e81-152">Die Fehlermeldung, die Sie erhalten, weist darauf hin, dass die Registrierung für RCS derzeit deaktiviert ist und aktiviert werden muss, bevor Sie den Registrierungsprozess abschließen können.</span><span class="sxs-lookup"><span data-stu-id="88e81-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![Fehlermeldung bei RCS-Registrierung](media/01_RCSSignUpError.jpg)

<span data-ttu-id="88e81-154">Das Problem tritt auf, weil Sie daran gehindert werden, sich für Ad-hoc-Abonnements anzumelden, und die Eigenschaft `AllowAdHocSubscriptions` in Ihrem Mandanten aktiviert sein muss.</span><span class="sxs-lookup"><span data-stu-id="88e81-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="88e81-155">Wenn Ihre IT-Abteilung die Azure-Mandanten Ihrer Organisation verwaltet, wenden Sie sich an diese Abteilung, um das Problem zu melden.</span><span class="sxs-lookup"><span data-stu-id="88e81-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="88e81-156">Wenn Sie für die Verwaltung Ihrer Azure-Mandanten verantwortlich sind, können Sie die Probleme beheben, indem Sie die Schritte in [Wozu dient die Self-Service-Registrierung in Azure Active Directory?](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="88e81-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
