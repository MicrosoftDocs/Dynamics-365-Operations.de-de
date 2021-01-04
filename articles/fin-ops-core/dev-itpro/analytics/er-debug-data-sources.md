---
title: Debuggen Sie Datenquellen eines ausgeführten EB-Formats, um den Datenfluss und die Transformation zu analysieren
description: In diesem Thema wird erläutert, wie Sie die Datenquellen eines ausgeführten EB-Formats debuggen können, um den konfigurierten Datenfluss und die konfigurierte Transformation besser zu verstehen.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680781"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="acb8a-103">Debuggen Sie Datenquellen eines ausgeführten EB-Formats, um den Datenfluss und die Transformation zu analysieren</span><span class="sxs-lookup"><span data-stu-id="acb8a-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="acb8a-104">Wenn Sie eine elektronische Berichterstellungs-(EB)-Lösung [konfigurieren](tasks/er-format-configuration-2016-11.md), um ausgehende Dokumente zu generieren, definieren Sie Methoden, die verwendet werden, um Daten aus der Anwendung abzurufen und sie in die Ausgabe einzugeben, die generiert wird.</span><span class="sxs-lookup"><span data-stu-id="acb8a-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="acb8a-105">Um die Lebenszyklusunterstützung der EB-Lösung effizienter zu gestalten, sollte Ihre Lösung aus einem EB-[Datenmodell](general-electronic-reporting.md#DataModelComponent) und deren [Zuordnung](general-electronic-reporting.md#ModelMappingComponent)-Komponenten bestehen und auch einem EB-[Format](general-electronic-reporting.md#FormatComponentOutbound) und dessen Zuordnungskomponenten bestehen, sodass die Modellzuordnung anwendungsspezifisch ist, wohingegen andere Komponenten anwendungsunabhängig bleiben.</span><span class="sxs-lookup"><span data-stu-id="acb8a-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="acb8a-106">Daher [beeinflussen](general-electronic-reporting.md#FormatComponentOutbound) möglicherweise mehrere EB-Komponenten den Prozess der Dateneingabe in die generierte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="acb8a-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="acb8a-107">Manchmal sehen die Daten der generierten Ausgabe anders aus als die gleichen Daten in der Anwendungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="acb8a-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="acb8a-108">In diesen Fällen möchten Sie bestimmen, welche EB-Komponente für die Datentransformation verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="acb8a-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="acb8a-109">Die EB-Datenquellendebugger-Funktion reduziert den Zeit- und Kostenaufwand für diese Untersuchung erheblich.</span><span class="sxs-lookup"><span data-stu-id="acb8a-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="acb8a-110">Sie können die Ausführung eines EB-Formats unterbrechen und die Datenquellendebugger-Schnittstelle öffnen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="acb8a-111">Dort können Sie die verfügbaren Datenquellen durchsuchen und eine einzelne Datenquelle für die Ausführung auswählen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="acb8a-112">Diese manuelle Ausführung simuliert die Ausführung der Datenquelle während der realen Ausführung eines EB-Formats.</span><span class="sxs-lookup"><span data-stu-id="acb8a-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="acb8a-113">Das Ergebnis wird auf einer Seite dargestellt, auf der Sie die empfangenen Daten analysieren können.</span><span class="sxs-lookup"><span data-stu-id="acb8a-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="acb8a-114">Um die Datenquellendebug-Funktion zu aktivieren, legen Sie in den EB-Benutzerparametern die Option **Datendebuggen bei Formatausführung aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="acb8a-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="acb8a-115">Sie können dann mit dem Debuggen von Datenquellen beginnen, während Sie ein EB-Format ausführen, um ausgehende Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="acb8a-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="acb8a-116">Sie können auch die Option **Debuggen starten** verwenden, um das Datenquellendebuggen für ein EB-Format zu initiieren, das im [EB-Vorgangs-Designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="acb8a-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="acb8a-117">Dieses Thema enthält Richtlinien zum Initiieren des Datenquellendebuggens für ausgeführte EB-Formate.</span><span class="sxs-lookup"><span data-stu-id="acb8a-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="acb8a-118">Es wird erläutert, wie die Informationen Ihnen helfen können, den Datenfluss und die Datentransformationen zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="acb8a-119">In den Beispielen in diesem Thema wird der Geschäftsprozess für die Verarbeitung von Lieferantenzahlungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="acb8a-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="acb8a-120">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="acb8a-120">Limitations</span></span>

<span data-ttu-id="acb8a-121">Der Datenquellen-Debugger kann verwendet werden, um auf die Daten von Datenquellen zuzugreifen, die in EB-Formaten verwendet werden, die zum Generieren ausgehender Dokumente ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="acb8a-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="acb8a-122">Er kann nicht zum Debuggen von Datenquellen in EB-Formaten verwendet werden, mit denen eingehende Dokumente analysiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="acb8a-123">Auf die folgenden Einstellungen von EB-Formaten kann derzeit für das Debuggen von Datenquellen nicht zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="acb8a-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="acb8a-124">Format-Transformationen</span><span class="sxs-lookup"><span data-stu-id="acb8a-124">Format transformations</span></span>
- <span data-ttu-id="acb8a-125">Validierungsregeln für Format und Zuordnung</span><span class="sxs-lookup"><span data-stu-id="acb8a-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="acb8a-126">Ausdrücke aktivieren</span><span class="sxs-lookup"><span data-stu-id="acb8a-126">Enabling expressions</span></span>
- <span data-ttu-id="acb8a-127">Details zur speicherinternen Datenerfassung</span><span class="sxs-lookup"><span data-stu-id="acb8a-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="acb8a-128">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="acb8a-128">Prerequisites</span></span>

- <span data-ttu-id="acb8a-129">Um die Beispiele in diesem Thema abzuschließen, müssen Sie den Zugriff auf eine der folgenden [Rollen](../sysadmin/tasks/assign-users-security-roles.md) haben:</span><span class="sxs-lookup"><span data-stu-id="acb8a-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="acb8a-130">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="acb8a-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="acb8a-131">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="acb8a-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="acb8a-132">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="acb8a-132">System administrator</span></span>

- <span data-ttu-id="acb8a-133">Das Unternehmen muss auf **DEMF** festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="acb8a-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="acb8a-134">Folgen Sie den Schritten in [Anhang 1](#appendix1) dieses Themas, um die Komponenten der Microsoft EB-Lösung herunterzuladen, die zum Verarbeiten von Lieferantenzahlungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="acb8a-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="acb8a-135">Folgen Sie den Schritten in [Anhang 2](#appendix2) dieses Themas, um die Kreditorenkonten für die Verarbeitung von Kreditorenzahlungen mithilfe der von Ihnen heruntergeladenen EB-Lösung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="acb8a-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="acb8a-136">Verarbeiten einer Lieferantenzahlung, um eine Zahlungsdatei abzurufen</span><span class="sxs-lookup"><span data-stu-id="acb8a-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="acb8a-137">Folgen Sie den Schritten in [Anhang 3](#appendix3) dieses Themas, um Kreditorenzahlungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="acb8a-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Verarbeitung der Kreditorenzahlung läuft](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="acb8a-139">Laden Sie die ZIP-Datei auf Ihren lokalen Computer herunter und speichern Sie sie.</span><span class="sxs-lookup"><span data-stu-id="acb8a-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="acb8a-140">Extrahieren Sie die Zahlungsdatei **ISO20022 Credit transfer.xml** aus der ZIP-Datei.</span><span class="sxs-lookup"><span data-stu-id="acb8a-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="acb8a-141">Öffnen Sie die extrahierte Zahlungsdatei mit der XML-Dateianzeige.</span><span class="sxs-lookup"><span data-stu-id="acb8a-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="acb8a-142">In der Zahlungsdatei enthält der IBAN-Code (International Bank Account Number) des Kreditorenbankkontos keine Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="acb8a-143">Daher unterscheidet es sich von dem Wert, der [eingegeben](#enteredIBANcode) wurde auf der Seite **Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN-Code ohne Leerzeichen](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="acb8a-145">Mit dem EB-Datenquellendebugger können Sie erfahren, welche Komponente der EB-Lösung zum Abschneiden von Leerzeichen im IBAN-Code verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="acb8a-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="acb8a-146">Aktivieren Sie das Debuggen von Datenquellen</span><span class="sxs-lookup"><span data-stu-id="acb8a-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="acb8a-147">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="acb8a-148">Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="acb8a-149">Legen Sie die Option **Debuggen von Daten beim Ausführen des Formats** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="acb8a-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="acb8a-150">Dieser Parameter ist benutzerspezifisch und unternehmensspezifisch.</span><span class="sxs-lookup"><span data-stu-id="acb8a-150">This parameter is user-specific and company-specific.</span></span>

    ![Benutzerparameter-Dialogfeld](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="acb8a-152">Verarbeiten einer Kreditorenzahlung zum Debuggen</span><span class="sxs-lookup"><span data-stu-id="acb8a-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="acb8a-153">Folgen Sie den Schritten in [Anhang 3](#appendix3) dieses Themas, um Kreditorenzahlungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="acb8a-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="acb8a-154">Wählen Sie im Meldungsfeld **Ja** aus, um zu bestätigen, dass Sie die Kreditorenzahlungsabwicklung unterbrechen und stattdessen das Debuggen von Datenquellen auf der Seite **Debuggen von Datenquellen** starten möchten.</span><span class="sxs-lookup"><span data-stu-id="acb8a-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Bestätigungsmeldungsfeld](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="acb8a-156">Debuggen von Datenquellen, die bei der Zahlungsabwicklung verwendet werden</span><span class="sxs-lookup"><span data-stu-id="acb8a-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="acb8a-157">Debuggen der Modellzuordnung</span><span class="sxs-lookup"><span data-stu-id="acb8a-157">Debug the model mapping</span></span>

1. <span data-ttu-id="acb8a-158">Auf der Seite **Debuggen von Datenquellen** wählen Sie im Aktionsbereich die Option **Modellzuordnung** aus, um mit dem Debuggen ab dieser EB-Komponente zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="acb8a-159">Wählen Sie im Datenquellenbereich links die Datenquelle **\$notSentTransactions** aus, und wählen Sie dann **Alle Datensätze lesen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="acb8a-160">Sie können **1 Datensatz lesen**, **10 Datensätze lesen**, **100 Datensätze lesen** oder **Alle Datensätze lesen** auswählen, um das Lesen der entsprechenden Anzahl von Datensätzen aus der ausgewählten Datenquelle zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="acb8a-161">Auf diese Weise können Sie den Zugriff auf die Datenquelle aus EB-Format simulieren, das gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="acb8a-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="acb8a-162">Wählen Sie im Datenbereich rechts die Option **Alle erweitern** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="acb8a-163">Sie können sehen, dass die ausgewählte Datenquelle des Typs **Datensatzliste** einen einzelnen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="acb8a-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="acb8a-164">Erweitern Sie die Datenquelle **\$notSentTransactions**, und wählen Sie die geschachtelte Methode **vendBankAccountInTransactionCompany()** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="acb8a-165">Erweitern Sie die Methode **vendBankAccountInTransactionCompany ()**, und wählen Sie das geschachtelte Feld **IBAN** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="acb8a-166">Wählen Sie **Wert abrufen**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-166">Select **Get value**.</span></span>

    <span data-ttu-id="acb8a-167">Sie können **Wert abrufen** auswählen, um das Lesen des Werts eines ausgewählten Felds der ausgewählten Datenquelle zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="acb8a-168">Auf diese Weise können Sie den Zugriff auf dieses Feld aus dem EB-Format simulieren, das gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="acb8a-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="acb8a-169">Wählen Sie **Alle erweitern** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-169">Select **Expand all**.</span></span>

    ![Wert des IBAN-Feldes in der Modellzuordnung](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="acb8a-171">Wie Sie sehen, ist die Modellzuordnung nicht für die abgeschnittenen Leerzeichen verantwortlich, da der IBAN-Code, den sie für das Bankkonto des Kreditors zurückgibt, Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="acb8a-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="acb8a-172">Daher müssen Sie das Datenquellen-Debuggen fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="acb8a-173">Formatzuordnung debuggen</span><span class="sxs-lookup"><span data-stu-id="acb8a-173">Debug the format mapping</span></span>

1. <span data-ttu-id="acb8a-174">Auf der Seite **Debuggen von Datenquellen** wählen Sie im Aktionsbereich die Option **Formatzuordnung** aus, um mit dem Debuggen ab dieser EB-Komponente fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="acb8a-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="acb8a-175">Wählen Sie die Datenquelle **\$PaymentByDebtor** aus, und wählen Sie dann **Alle Datensätze lesen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="acb8a-176">Erweitern Sie **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="acb8a-177">Erweitern Sie **\$PaymentByDebtor.Lines**, und wählen Sie dann **Alle Datensätze auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="acb8a-178">Erweitern Sie **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="acb8a-179">Erweitern Sie **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, und wählen Sie dann **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="acb8a-180">Wählen Sie **Wert abrufen**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-180">Select **Get value**.</span></span>
8. <span data-ttu-id="acb8a-181">Wählen Sie **Alle erweitern** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-181">Select **Expand all**.</span></span>

    ![Wert des IBAN-Feldes in der Formatzuordnung](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="acb8a-183">Wie Sie sehen, sind die Datenquellen der Modellzuordnung nicht für die abgeschnittenen Leerzeichen verantwortlich, da der IBAN-Code, den sie für das Bankkonto des Kreditors zurückgeben, Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="acb8a-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="acb8a-184">Daher müssen Sie das Datenquellen-Debuggen fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="acb8a-185">Das Format debuggen</span><span class="sxs-lookup"><span data-stu-id="acb8a-185">Debug the format</span></span>

1. <span data-ttu-id="acb8a-186">Auf der Seite **Debuggen von Datenquellen** wählen Sie im Aktionsbereich die Option **Format** aus, um mit dem Debuggen ab dieser EB-Komponente fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="acb8a-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="acb8a-187">Erweitern Sie die auszuwählenden Formatelemente **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**, und wählen Sie dann **Alle Datensätze lesen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="acb8a-188">Erweitern Sie die auszuwählenden Formatelemente **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, und wählen Sie dann **Alle Datensätze lesen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="acb8a-189">Erweitern Sie die auszuwählenden Formatelemente **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, und wählen Sie dann **Wert abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="acb8a-190">Wählen Sie **Alle erweitern** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-190">Select **Expand all**.</span></span>

    ![Wert des IBAN-Feldes im Format](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="acb8a-192">Wie Sie sehen, ist die Formatbindung nicht für die abgeschnittenen Leerzeichen verantwortlich, da der IBAN-Code, den sie für das Bankkonto des Kreditors zurückgibt, Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="acb8a-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="acb8a-193">Deshalb ist das Element **BankIBAN** so konfiguriert, dass eine Format-Transformation verwendet wird, bei der Leerzeichen abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="acb8a-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="acb8a-194">Schließen Sie den Datenquellen-Debugger.</span><span class="sxs-lookup"><span data-stu-id="acb8a-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="acb8a-195">Überprüfen Sie die Format-Transformationen</span><span class="sxs-lookup"><span data-stu-id="acb8a-195">Review the format transformations</span></span>

1. <span data-ttu-id="acb8a-196">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="acb8a-197">Auf der Seite **Konfigurationen** wählen Sie **Zahlungsmodell** \> **ISO20022-Kreditübertragung**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="acb8a-198">Wählen Sie **Designer** aus, und erweitern Sie dann die Elemente, um **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN-Element auf der Seite „Format-Designer“](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="acb8a-200">Wie Sie sehen können, ist das Element **BankIBAN** so konfiguriert, dass es die Transformation **nicht alphanumerisch entfernen** verwendet.</span><span class="sxs-lookup"><span data-stu-id="acb8a-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="acb8a-201">Wählen Sie die Registerkarte **Transformationen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-201">Select the **Transformations** tab.</span></span>

    ![Registerkarte „Transformationen“ für das BankIBAN-Element](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="acb8a-203">Wie Sie sehen können, ist die Transformation **nicht alphanumerisch entfernen** so konfiguriert, dass ein Ausdruck verwendet wird, der Leerzeichen aus der bereitgestellten Textzeichenfolge abschneidet.</span><span class="sxs-lookup"><span data-stu-id="acb8a-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="acb8a-204">Debuggen im Vorgangs-Designer starten</span><span class="sxs-lookup"><span data-stu-id="acb8a-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="acb8a-205">Wenn Sie eine Entwurfsversion des EB-Formats konfigurieren, das direkt vom Vorgangs-Designer ausgeführt werden kann, können Sie auf den Datenquellen-Debugger zugreifen, indem Sie **Debuggen starten** im Aktionsbereich auswählen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Schaltfläche „Debuggen starten“ auf der Seite „Format-Designer“](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="acb8a-207">Die Formatzuordnung und Formatkomponenten des EB-Formats, das gerade bearbeitet wird, stehen zum Debuggen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="acb8a-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="acb8a-208">Debuggen im Modellzuordnungs-Designer starten</span><span class="sxs-lookup"><span data-stu-id="acb8a-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="acb8a-209">Wenn Sie eine EB-Modellzuordnung konfigurieren, die direkt von der Seite **Modellzuordnung** ausgeführt werden kann, können Sie auf den Datenquellen-Debugger zugreifen, indem Sie **Debuggen starten** im Aktionsbereich auswählen.</span><span class="sxs-lookup"><span data-stu-id="acb8a-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Schaltfläche „Debuggen starten“ auf der Seite „Modellzuordnungs-Designer“](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="acb8a-211">Die Modellzuordnungskomponente der zu bearbeitenden EB-Zuordnung steht zum Debuggen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="acb8a-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="acb8a-212">Anhang 1: Eine EB-Lösung abrufen</span><span class="sxs-lookup"><span data-stu-id="acb8a-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="acb8a-213">Eine EB-Lösung herunterladen</span><span class="sxs-lookup"><span data-stu-id="acb8a-213">Download an ER solution</span></span>

<span data-ttu-id="acb8a-214">Wenn Sie eine EB-Lösung verwenden möchten, um eine elektronische Zahlungsdatei für eine Kreditorenzahlung zu erstellen, die verarbeitet wird, können Sie [Herunterladen](download-electronic-reporting-configuration-lcs.md) das EB-Zahlungsformat **ISO20022-Kreditübertragung**, das in der Freigegebenen Anlagenbibliothek in Microsoft Dynamics Lifecycle Services (LCS) verfügbar ist oder aus dem globalen Repository.</span><span class="sxs-lookup"><span data-stu-id="acb8a-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![Importieren des EB-Zahlungsformats auf der Seite „Konfigurations-Repository“](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="acb8a-216">Zusätzlich zum ausgewählten EB-Format müssen die folgenden [Konfigurationen](general-electronic-reporting.md#Configuration) automatisch in Ihre Microsoft Dynamics 365 Finance-Instanz als Teil der EB-Lösung **ISO20022-Kreditübertragung** importiert werden.</span><span class="sxs-lookup"><span data-stu-id="acb8a-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="acb8a-217">**Zahlungsmodell** [EB-Datenmodellkonfiguration](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="acb8a-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="acb8a-218">**ISO20022-Kreditübertragung** [EB-Formatkonfiguration](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="acb8a-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="acb8a-219">**Zahlungsmodellzuordnung 1611** [EB-Modellzuordnungskonfiguration](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="acb8a-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="acb8a-220">**Zahlungsmodellzuordnung zu Ziel ISO20022** EB-Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="acb8a-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="acb8a-221">Sie finden diese Konfigurationen auf der Seite **Konfigurationen** des EB-Frameworks (**Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**).</span><span class="sxs-lookup"><span data-stu-id="acb8a-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Auf der Seite „Konfigurationen“ importierte Konfigurationen](./media/er-data-debugger-configurations.png)

<span data-ttu-id="acb8a-223">Wenn irgendeine der zuvor aufgelisteten Konfigurationen in der Konfigurationsstruktur fehlt, müssen Sie sie manuell aus der freigegebenen Anlagebibliothek von LCS in derselben Weise herunterladen, wie Sie das EB-Zahlungsformat **ISO20022-Kreditübertragung** heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="acb8a-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="acb8a-224">Die heruntergeladene EB-Lösung analysieren</span><span class="sxs-lookup"><span data-stu-id="acb8a-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="acb8a-225">Die Modellzuordnung überprüfen</span><span class="sxs-lookup"><span data-stu-id="acb8a-225">Review the model mapping</span></span>

1. <span data-ttu-id="acb8a-226">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="acb8a-227">Wählen Sie **Zahlungsmodell** \> **Zahlungsmodellzuordnung 1611** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="acb8a-228">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-228">Select **Designer**.</span></span>
4. <span data-ttu-id="acb8a-229">Wählen Sie den Zuordnungsdatensatz **Zahlungsmodellzuordnung ISO20022 CT** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="acb8a-230">Wählen Sie **Designer** aus, und überprüfen Sie anschließend die geöffnete Modellzuordnung.</span><span class="sxs-lookup"><span data-stu-id="acb8a-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="acb8a-231">Beachten Sie, dass das Feld **Zahlungen** des Datenmodells an die Datenquelle **\$notSentTransactions** gebunden ist, die die Liste von Kreditorenzahlungspositionen zurück gibt, die verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="acb8a-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Feld „Zahlungen“ auf der Seite „Modellzuordnungs Designer“](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="acb8a-233">Die Formatzuordnung überprüfen</span><span class="sxs-lookup"><span data-stu-id="acb8a-233">Review the format mapping</span></span>

1. <span data-ttu-id="acb8a-234">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="acb8a-235">Wählen Sie **Zahlungsmodell** \> **ISO20022-Kreditübertragung** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="acb8a-236">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-236">Select **Designer**.</span></span>
4. <span data-ttu-id="acb8a-237">In der Registerkarte **Zuordnung** überprüfen Sie die Formatzuordnung, die geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="acb8a-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="acb8a-238">Beachten Sie, dass das Element **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** der Datei **ISO20022CTReports** \> **XMLHeader** an die Datenquelle **\$PaymentByDebtor** gebunden ist, die so konfiguriert ist, dass sie Datensätze des Felds **Zahlungen** des Datenmodells gruppiert.</span><span class="sxs-lookup"><span data-stu-id="acb8a-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf-Element auf der Seite „Format-Designer“](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="acb8a-240">Das Format überprüfen</span><span class="sxs-lookup"><span data-stu-id="acb8a-240">Review the format</span></span>

1. <span data-ttu-id="acb8a-241">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="acb8a-242">Wählen Sie **Zahlungsmodell** \> **ISO20022-Kreditübertragung** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="acb8a-243">Wählen Sie **Designer** aus, und überprüfen Sie anschließend das geöffnete Format.</span><span class="sxs-lookup"><span data-stu-id="acb8a-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="acb8a-244">Beachten Sie, dass das Formatelement unter **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** so konfiguriert ist, dass der IBAN-Code des Kreditorenkontos in der Zahlungsdatei eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="acb8a-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN-Element auf der Seite „Format-Designer“](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="acb8a-246">Anhang 2: Kreditorenkonten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="acb8a-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="acb8a-247">Eine Kreditoreneigenschaft ändern</span><span class="sxs-lookup"><span data-stu-id="acb8a-247">Modify a vendor property</span></span>

1. <span data-ttu-id="acb8a-248">Wechseln Sie zu **Kreditorenkonten** \> **Kreditoren** \> **Alle Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="acb8a-249">Wählen Sie Kreditor **DE-01002** aus, und wählen Sie dann im Aktionsbereich, auf der Registerkarte **Kreditor** in der Gruppe **Einrichten** die Option **Bankkonten** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="acb8a-250">Im Inforegister **Identifizierung** im Feld **IBAN**, <a name="enteredIBANcode"></a>geben Sie **GB33 BUKB 2020 1555 5555 55** ein.</span><span class="sxs-lookup"><span data-stu-id="acb8a-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="acb8a-251">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-251">Select **Save**.</span></span>

![IBAN-Feld, festgelegt auf der Seite „Kreditorenbankkonten“](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="acb8a-253">Einrichten einer Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="acb8a-253">Set up a method of payment</span></span>

1. <span data-ttu-id="acb8a-254">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungseinstellungen** \> **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="acb8a-255">Wählen Sie die Zahlungsmethode **SEPA CT** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="acb8a-256">Legen Sie im Inforegister **Dateiformate** im Abschnitt **Dateiformate** die Option **Generisches elektronisches Exportformat** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="acb8a-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="acb8a-257">Wählen Sie im Feld **Formatkonfiguration exportieren** das EB-Format **ISO20022-Kreditübertragung** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="acb8a-258">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-258">Select **Save**.</span></span>

![Dateiformateinstellungen auf der Seite „Zahlungsmethoden“](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="acb8a-260">Kreditorenzahlung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="acb8a-260">Add a vendor payment</span></span>

1. <span data-ttu-id="acb8a-261">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="acb8a-262">Fügen Sie eine neue Zahlungserfassung hinzu.</span><span class="sxs-lookup"><span data-stu-id="acb8a-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="acb8a-263">Wählen Sie **Positionen** aus, und fügen Sie eine neue Zahlungsposition hinzu.</span><span class="sxs-lookup"><span data-stu-id="acb8a-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="acb8a-264">Wählen Sie im Feld **Konto** den Kreditor **DE-01002** hinzu.</span><span class="sxs-lookup"><span data-stu-id="acb8a-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="acb8a-265">Geben Sie im Feld **Soll** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="acb8a-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="acb8a-266">Wählen Sie im Feld **Zahlungsmethode** die Option **SEPA CT** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="acb8a-267">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-267">Select **Save**.</span></span>

![Kreditorenzahlung auf der Seite Kreditorenzahlungen hinzugefügt](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="acb8a-269">Anhang 3: Eine Kreditorenzahlung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="acb8a-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="acb8a-270">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="acb8a-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="acb8a-271">Auf der Seite **Kreditorenzahlungserfassung** wählen Sie die Zahlungserfassung aus, die Sie zuvor erstellt haben, und wählen Sie dann **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="acb8a-272">Wählen Sie die Zahlungsposition aus, und wählen Sie dann **Zahlungsstatus** \> **Kein** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="acb8a-273">Wählen Sie **Zahlungen generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="acb8a-274">Wählen Sie im Feld **Zahlungsmethode** die Option **SEPA CT** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="acb8a-275">Wählen Sie im Feld **Bankkonto** die Option **DEMF OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="acb8a-276">Wählen Sie im Dialogfeld **Zahlungen generieren** die Option **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="acb8a-277">Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="acb8a-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
