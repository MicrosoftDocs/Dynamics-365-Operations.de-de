---
title: Aktivieren Sie die Azure Active Directory-Authentifizierung für die POS-Anmeldung
description: In diesem Thema wird erläutert, wie die Anmeldung für die Microsoft Dynamics 365 Commerce POS (Point of Sale) so konfiguriert wird, dass sie die Azure Active Directory Authentifizierung verwendet.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 6946cb5f8bc8aa451f72d1eebcd324f408ad5f7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412487"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="b9379-103">Aktivieren Sie die Azure Active Directory-Authentifizierung für die POS-Anmeldung</span><span class="sxs-lookup"><span data-stu-id="b9379-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="b9379-104">Viele Kunden, die Microsoft Dynamics 365 Commerce verwenden, nutzen auch andere Cloud-Dienste von Microsoft, und sie könnten Azure Active Directory (Azure AD) verwenden, um die Benutzeranmeldeinformationen für diese Dienste zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b9379-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="b9379-105">In diesen Fällen möchten die Kunden möglicherweise anwendungsübergreifend dasselbe Azure AD-Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9379-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="b9379-106">In diesem Thema wird erläutert, wie die Anmeldemöglichkeit am POS (Point of Sale) für die Verwendung der Azure AD-Authentifizierung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="b9379-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="b9379-107">Konfigurieren der Azure AD-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="b9379-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="b9379-108">Um Azure AD als Authentifizierungsmethode für die POS-Anmeldung für eine Filiale verfügbar zu machen, müssen Sie die Einstellungen des Funktionsprofils der Filiale konfigurieren und diese Einstellungen dann auf POS-Clients anwenden.</span><span class="sxs-lookup"><span data-stu-id="b9379-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="b9379-109">Führen Sie die folgenden Schritte aus, um ein Funktionsprofil zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b9379-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="b9379-110">Gehen Sie zu **Retail und Commerce** \> **Kanaleinrichtung** \> **POS-Einrichtung** \> **POS-Profile** \> **Funktionsprofile**.</span><span class="sxs-lookup"><span data-stu-id="b9379-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="b9379-111">Wählen Sie das zu ändernde Funktionalitätsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="b9379-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="b9379-112">Ändern Sie auf der Registerkarte **Funktionen** im Abschnitt **POS-Personalanmeldung** den Wert des Feldes **Anmeldeauthentifizierungsmethode** von **Personal-ID und Passwort** auf **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="b9379-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="b9379-113">Standardmäßig verwenden alle Funktionsprofile **Personen-ID und Passwort** als POS-Authentifizierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="b9379-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="b9379-114">Daher müssen Sie den Wert des Feldes **Anmelde-Authentifizierungsmethode** ändern, wenn Sie Azure AD verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b9379-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="b9379-115">Jedes Einzelhandelsgeschäft, das mit dem ausgewählten Funktionsprofil verknüpft ist, ist von dieser Änderung betroffen.</span><span class="sxs-lookup"><span data-stu-id="b9379-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="b9379-116">Um die Einstellungen auf POS-Clients anzuwenden, führen Sie folgende Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b9379-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="b9379-117">Gehen Sie zu **Retail and Commerce** \> **Retail and Commerce IT** \> **Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="b9379-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="b9379-118">Führen Sie den Verteilungsplan **1070** (**Kanalkonfiguration**) aus.</span><span class="sxs-lookup"><span data-stu-id="b9379-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="b9379-119">Die Azure AD-Authentifizierung erfordert eine Internetverbindung.</span><span class="sxs-lookup"><span data-stu-id="b9379-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="b9379-120">Sie funktioniert nicht, wenn sich POS im Offline-Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="b9379-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="b9379-121">Derzeit unterstützt die Funktion **Manager überschreiben** Azure AD nicht als Authentifizierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="b9379-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="b9379-122">Eine Operator-ID und ein Kennwort sind auch dann erforderlich, wenn Azure AD als Authentifizierungsmethode für die POS-Anmeldung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="b9379-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="b9379-123">Verknüpfen eines Azure AD-Kontos mit einem Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b9379-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="b9379-124">Bevor sich ein Mitarbeiter einer Filiale mit einem Azure AD-Konto bei der POS-Anwendung anmelden kann, muss das Azure AD-Konto mit diesem Mitarbeiter verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="b9379-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="b9379-125">Um ein Azure AD-Konto mit einem Mitarbeiter zu verknüpfen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b9379-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="b9379-126">Gehen Sie zu **Retail and Commerce** \> **Mitarbeiter** \> **Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="b9379-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="b9379-127">Öffnen Sie die Detailseite für einen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="b9379-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="b9379-128">Wählen Sie im Aktionsbereich auf der Registerkarte **Commerce** in der Gruppe **Externe Identität** die Option **Existierende Identität zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="b9379-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="b9379-129">Wählen Sie im Dialogfeld **Existierende externe Identität verwenden** **Mit E-Mail** suchen, geben Sie eine E-Mail-Adresse Azure AD ein und wählen Sie dann **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="b9379-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="b9379-130">Wählen Sie das Konto Azure AD, das zurückgegeben wird, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9379-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="b9379-131">Die Felder **Alias**, **UPN** und **Externer Sub-Identifikator** auf der Registerkarte **Commerce** auf der Seite mit den Details des Mitarbeiters werden ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b9379-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="b9379-132">Nachdem ein Arbeitskraftdatensatz, z. B. wenn ihm ein neues Azure AD-Konto zugeordnet wurde, aktualisiert, ein Kennwort geändert oder das Adressbuch einer Arbeitskraft aktualisiert wird, sollten Sie Verteilungsplan **1060** (**Personal**) ausführen, um den Kanal mit den neuesten Personalinformationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b9379-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="b9379-133">So kann die POS-Anwendung die richtigen Daten für die Benutzerauthentifizierung und Autorisierungsüberprüfung abrufen.</span><span class="sxs-lookup"><span data-stu-id="b9379-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9379-134">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b9379-134">Additional resources</span></span>

[<span data-ttu-id="b9379-135">Erweiterte Anmeldungsfunktionen für MPOS und Cloud POS einrichten</span><span class="sxs-lookup"><span data-stu-id="b9379-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="b9379-136">Ein Einzelhandelsfunktionsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="b9379-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="b9379-137">Eine Arbeitskraft konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b9379-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
