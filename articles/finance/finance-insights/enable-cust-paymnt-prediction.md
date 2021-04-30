---
title: Vorhersagen für Debitorenzahlungen aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren.
author: ShivamPandey-msft
ms.date: 05/27/2020
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
ms.openlocfilehash: 0f972b6f3c0c7c4fcf69b3644a5e73d863cd817d
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897355"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="18fd2-103">Vorhersagen für Debitorenzahlungen aktivieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="18fd2-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="18fd2-104">In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="18fd2-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="18fd2-105">Sie aktivieren die Funktion im Arbeitsbereich **Funktionsverwaltung** und geben die Konfigurationseinstellungen auf der Seite **Parameter für Finance Insights** ein.</span><span class="sxs-lookup"><span data-stu-id="18fd2-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="18fd2-106">Dieses Thema enthält auch Informationen, mit denen Sie die Funktion effektiv nutzen können.</span><span class="sxs-lookup"><span data-stu-id="18fd2-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="18fd2-107">Bevor Sie die folgenden Schritte ausführen, müssen Sie die erforderlichen Schritte im Thema [Konfigurieren für Finance Insights](configure-for-fin-insites.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="18fd2-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="18fd2-108">Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="18fd2-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="18fd2-109">Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="18fd2-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="18fd2-110">(Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)</span><span class="sxs-lookup"><span data-stu-id="18fd2-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="18fd2-111">Wenn es sich bei Ihrer Bereitstellung von Microsoft Dynamics 365 Finance um eine Service Fabric-Bereitstellung handelt, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="18fd2-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="18fd2-112">Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="18fd2-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="18fd2-113">Wenn die Funktion nicht im **Funktionsverwaltung**-Arbeitsbereich angezeigt wird, oder wenn Sie Probleme beim Aktivieren haben, wenden Sie sich an <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="18fd2-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="18fd2-114">Aktivieren Sie die Debitorenzahlungseinblicke-Funktion:</span><span class="sxs-lookup"><span data-stu-id="18fd2-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="18fd2-115">Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="18fd2-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="18fd2-116">Suchen Sie die Funktion namens **Debitorenzahlungseinblicke (Vorschau)**.</span><span class="sxs-lookup"><span data-stu-id="18fd2-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="18fd2-117">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="18fd2-117">Select **Enable now**.</span></span>

    <span data-ttu-id="18fd2-118">Die Debitorenzahlungsvorschau-Funktion ist jetzt aktiviert und kann konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="18fd2-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="18fd2-119">Konfigurieren Sie die Debitorenzahlungseinblicke-Funktion:</span><span class="sxs-lookup"><span data-stu-id="18fd2-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="18fd2-120">Gehen Sie zu **Kredit und Inkasso \> Einrichtung \> Finance Insights \> Parameter für Finance Insights**.</span><span class="sxs-lookup"><span data-stu-id="18fd2-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="18fd2-121">[![Seite der Parameter für Finance Insights, bevor die Funktion konfiguriert wird](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="18fd2-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="18fd2-122">Wählen Sie auf der **Parameter für Finance Insights**-Seite auf der **Debitorenzahlungseinblicke**-Registerkarte den Link **Die im Vorhersagemodell verwendeten Datenfelder anzeigen** an, um die **Datenfelder für das Vorhersagemodell**-Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="18fd2-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="18fd2-123">Dort können Sie die Standardliste der Felder anzeigen, die zum Erstellen des Vorhersagemodells für künstliche Intelligenz (KI) für Debitorenzahlungsvorhersagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18fd2-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="18fd2-124">Um die Standardliste der Felder zum Erstellen des Vorhersagemodells zu verwenden, schließen Sie die **Datenfelder für das Vorhersagemodell**-Seite und legen Sie dann auf der **Parameter für Finance Insights**-Seite die **Funktion aktivieren** Option auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="18fd2-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="18fd2-125">Geben Sie den „sehr späten“ Transaktionszeitraum an, um zu definieren, was der **Sehr spät**-Vorhersage-Bucket für Ihr Unternehmen bedeutet.</span><span class="sxs-lookup"><span data-stu-id="18fd2-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="18fd2-126">Für jede offene Rechnung sagt das System die Zahlungswahrscheinlichkeit in drei Buckets voraus: **Pünktlich**, **Verspätet** und **Sehr spät**.</span><span class="sxs-lookup"><span data-stu-id="18fd2-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="18fd2-127">**Pünktlich** – Dieser Bucket enthält Zahlungen, deren Zahlung voraussichtlich am oder vor dem Fälligkeitsdatum der Transaktion erfolgt.</span><span class="sxs-lookup"><span data-stu-id="18fd2-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="18fd2-128">**Verspätet** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Fälligkeitsdatum der Transaktion, jedoch vor dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="18fd2-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="18fd2-129">**Sehr spät** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="18fd2-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="18fd2-130">Wenn Sie den Transaktionszeitraum „sehr spät“ ändern und **Schwellenwert für „Verspätet“ ändern** auswählen, nachdem das KI-Vorhersagemodell für Debitorenzahlungen erstellt wurde, wird das vorhandene Vorhersagemodell gelöscht und ein neues Modell erstellt.</span><span class="sxs-lookup"><span data-stu-id="18fd2-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="18fd2-131">Das neue Vorhersagemodell verschiebt Transaktionen basierend auf den zur Definition eingegebenen Einstellungen in den „sehr späten“ Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="18fd2-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="18fd2-132">Nachdem Sie den Transaktionszeitraum „sehr spät“ definiert haben, wählen Sie **Vorhersagemodell erstellen** aus, um das Vorhersagemodell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="18fd2-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="18fd2-133">Der **Vorhersagemodell**-Abschnitt auf der **Parameter für Finance Insights**-Seite zeigt den Status des Vorhersagemodells.</span><span class="sxs-lookup"><span data-stu-id="18fd2-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="18fd2-134">Sie können jederzeit während der Erstellung des Vorhersagemodells **Modellerstellung zurücksetzen** auswählen, um den Prozess neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="18fd2-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="18fd2-135">Die Funktion wurde konfiguriert und kann jetzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18fd2-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="18fd2-136">Nachdem die Funktion aktiviert und konfiguriert und das Vorhersagemodell erstellt wurde und funktioniert, zeigt der **Vorhersagemodell**-Abschnitt der **Parameter für Finance Insights**-Seite die Genauigkeit des Modells, wie in der folgenden Abbildung gezeigt an.</span><span class="sxs-lookup"><span data-stu-id="18fd2-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="18fd2-137">[![Genauigkeit des Vorhersagemodells auf der Seite Parameter für Financial Insights](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="18fd2-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="18fd2-138">Freigabedetails</span><span class="sxs-lookup"><span data-stu-id="18fd2-138">Release details</span></span>

<span data-ttu-id="18fd2-139">Die öffentliche Finance Insights-Vorschau ist für Testbereitstellungen in den Vereinigten Staaten von Amerika, Europa und Großbritannien verfügbar.</span><span class="sxs-lookup"><span data-stu-id="18fd2-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="18fd2-140">Microsoft fügt schrittweise Unterstützung für weitere Regionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="18fd2-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="18fd2-141">Öffentliche Vorschaufunktionen können und sollten nur in Sandbox-Umgebungen der Stufe 2 aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="18fd2-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="18fd2-142">Einrichtungs- und KI-Mopelle, die in einer Sandbox-Umgebung erstellt werden, können nicht in eine Produktionsumgebung migriert werden.</span><span class="sxs-lookup"><span data-stu-id="18fd2-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="18fd2-143">Weitere Informationen finden Sie unter [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365 Vorschauen](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="18fd2-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="18fd2-144">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="18fd2-144">Privacy notice</span></span>

<span data-ttu-id="18fd2-145">Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.</span><span class="sxs-lookup"><span data-stu-id="18fd2-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]