---
title: Vorhersagen für Debitorenzahlungen aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222584"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="41e05-103">Vorhersagen für Debitorenzahlungen aktivieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="41e05-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="41e05-104">In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="41e05-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="41e05-105">Sie aktivieren die Funktion im Arbeitsbereich **Funktionsverwaltung** und geben die Konfigurationseinstellungen auf der Seite **Parameter für Finance Insights** ein.</span><span class="sxs-lookup"><span data-stu-id="41e05-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="41e05-106">Dieses Thema enthält auch Informationen, mit denen Sie die Funktion effektiv nutzen können.</span><span class="sxs-lookup"><span data-stu-id="41e05-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="41e05-107">Bevor Sie die folgenden Schritte ausführen, müssen Sie die erforderlichen Schritte im Thema [Konfigurieren für Finance Insights](configure-for-fin-insites.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="41e05-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="41e05-108">Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="41e05-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="41e05-109">Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="41e05-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="41e05-110">(Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)</span><span class="sxs-lookup"><span data-stu-id="41e05-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="41e05-111">Überspringen Sie diesen Schritt, wenn Sie Version 10.0.20 oder höher verwenden oder wenn Sie eine Service Fabric-Bereitstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="41e05-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="41e05-112">Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="41e05-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="41e05-113">Wenn die Funktion nicht im **Funktionsverwaltung**-Arbeitsbereich angezeigt wird, oder wenn Sie Probleme beim Aktivieren haben, wenden Sie sich an <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="41e05-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="41e05-114">Aktivieren Sie die Debitorenzahlungseinblicke-Funktion:</span><span class="sxs-lookup"><span data-stu-id="41e05-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="41e05-115">Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="41e05-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="41e05-116">Suchen Sie die Funktion namens **Debitorenzahlungseinblicke (Vorschau)**.</span><span class="sxs-lookup"><span data-stu-id="41e05-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="41e05-117">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="41e05-117">Select **Enable now**.</span></span>

    <span data-ttu-id="41e05-118">Die Debitorenzahlungsvorschau-Funktion ist jetzt aktiviert und kann konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="41e05-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="41e05-119">Konfigurieren Sie die Debitorenzahlungseinblicke-Funktion:</span><span class="sxs-lookup"><span data-stu-id="41e05-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="41e05-120">Gehen Sie zu **Kredit und Inkasso \> Einrichtung \> Finance Insights \> Parameter für Finance Insights**.</span><span class="sxs-lookup"><span data-stu-id="41e05-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="41e05-121">[![Seite der Parameter für Finance Insights, bevor die Funktion konfiguriert wird](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="41e05-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="41e05-122">Wählen Sie auf der **Parameter für Finance Insights**-Seite auf der **Debitorenzahlungseinblicke**-Registerkarte den Link **Die im Vorhersagemodell verwendeten Datenfelder anzeigen** an, um die **Datenfelder für das Vorhersagemodell**-Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="41e05-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="41e05-123">Dort können Sie die Standardliste der Felder anzeigen, die zum Erstellen des Vorhersagemodells für künstliche Intelligenz (KI) für Debitorenzahlungsvorhersagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41e05-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="41e05-124">Um die Standardliste der Felder zum Erstellen des Vorhersagemodells zu verwenden, schließen Sie die **Datenfelder für das Vorhersagemodell**-Seite und legen Sie dann auf der **Parameter für Finance Insights**-Seite die **Funktion aktivieren** Option auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="41e05-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="41e05-125">Geben Sie den „sehr späten“ Transaktionszeitraum an, um zu definieren, was der **Sehr spät**-Vorhersage-Bucket für Ihr Unternehmen bedeutet.</span><span class="sxs-lookup"><span data-stu-id="41e05-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="41e05-126">Für jede offene Rechnung sagt das System die Zahlungswahrscheinlichkeit in drei Buckets voraus: **Pünktlich**, **Verspätet** und **Sehr spät**.</span><span class="sxs-lookup"><span data-stu-id="41e05-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="41e05-127">**Pünktlich** – Dieser Bucket enthält Zahlungen, deren Zahlung voraussichtlich am oder vor dem Fälligkeitsdatum der Transaktion erfolgt.</span><span class="sxs-lookup"><span data-stu-id="41e05-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="41e05-128">**Verspätet** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Fälligkeitsdatum der Transaktion, jedoch vor dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="41e05-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="41e05-129">**Sehr spät** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="41e05-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="41e05-130">Wenn Sie den Transaktionszeitraum „sehr spät“ ändern und **Schwellenwert für „Verspätet“ ändern** auswählen, nachdem das KI-Vorhersagemodell für Debitorenzahlungen erstellt wurde, wird das vorhandene Vorhersagemodell gelöscht und ein neues Modell erstellt.</span><span class="sxs-lookup"><span data-stu-id="41e05-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="41e05-131">Das neue Vorhersagemodell verschiebt Transaktionen basierend auf den zur Definition eingegebenen Einstellungen in den „sehr späten“ Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="41e05-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="41e05-132">Nachdem Sie den Transaktionszeitraum „sehr spät“ definiert haben, wählen Sie **Vorhersagemodell erstellen** aus, um das Vorhersagemodell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41e05-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="41e05-133">Der **Vorhersagemodell**-Abschnitt auf der **Parameter für Finance Insights**-Seite zeigt den Status des Vorhersagemodells.</span><span class="sxs-lookup"><span data-stu-id="41e05-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="41e05-134">Sie können jederzeit während der Erstellung des Vorhersagemodells **Modellerstellung zurücksetzen** auswählen, um den Prozess neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="41e05-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="41e05-135">Die Funktion wurde konfiguriert und kann jetzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41e05-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="41e05-136">Nachdem die Funktion aktiviert und konfiguriert und das Vorhersagemodell erstellt wurde und funktioniert, zeigt der **Vorhersagemodell**-Abschnitt der **Parameter für Finance Insights**-Seite die Genauigkeit des Modells, wie in der folgenden Abbildung gezeigt an.</span><span class="sxs-lookup"><span data-stu-id="41e05-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="41e05-137">[![Genauigkeit des Vorhersagemodells auf der Seite Parameter für Financial Insights](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="41e05-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="41e05-138">Freigabedetails</span><span class="sxs-lookup"><span data-stu-id="41e05-138">Release details</span></span>

<span data-ttu-id="41e05-139">Die öffentliche Finance Insights-Vorschau ist für Testbereitstellungen in den Vereinigten Staaten von Amerika, Europa und Großbritannien verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41e05-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="41e05-140">Microsoft fügt schrittweise Unterstützung für weitere Regionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="41e05-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="41e05-141">Öffentliche Vorschaufunktionen können und sollten nur in Sandbox-Umgebungen der Stufe 2 aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="41e05-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="41e05-142">Einrichtungs- und KI-Mopelle, die in einer Sandbox-Umgebung erstellt werden, können nicht in eine Produktionsumgebung migriert werden.</span><span class="sxs-lookup"><span data-stu-id="41e05-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="41e05-143">Weitere Informationen finden Sie unter [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365 Vorschauen](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="41e05-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
