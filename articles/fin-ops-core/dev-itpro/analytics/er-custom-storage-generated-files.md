---
title: Benutzerdefinierte Speicherorte für generierte Dokumente angeben
description: In diesem Thema wird erläutert, wie Sie die Liste der Speicherorte für Dokumente erweitern, die von Formaten der electronischen Berichterstellung (EB) generiert werden.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680757"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="a77fa-103">Benutzerdefinierte Speicherorte für generierte Dokumente angeben</span><span class="sxs-lookup"><span data-stu-id="a77fa-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a77fa-104">Mit der Anwendungsprogrammierschnittstelle (API) des Framework der elektronischen Berichterstellung (ER) können Sie die Liste der Speicherorte für Dokumente, die von ER-Formaten generiert werden, erweitern.</span><span class="sxs-lookup"><span data-stu-id="a77fa-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="a77fa-105">In diesem Thema wird erläutert, wie Sie einen benutzerdefinierten Speicherort für generierte Dokumente hinzufügen, indem Sie die Aufgabe zum Erstellen von EB-Zielen an das Standardempfängerwerk delegieren und anschließend eine benutzerdefinierte Klasse mit eigener Ziellogik implementieren.</span><span class="sxs-lookup"><span data-stu-id="a77fa-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a77fa-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a77fa-106">Prerequisites</span></span>

<span data-ttu-id="a77fa-107">Stellen Sie eine Topologie bereit, die einen fortlaufenden Build unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a77fa-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="a77fa-108">Weitere Informationen finden Sie unter [Bereitstellen von Topologien, die fortlaufenden Build und Testautomatisierung unterstützen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation) Sie unter.</span><span class="sxs-lookup"><span data-stu-id="a77fa-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="a77fa-109">Sie müssen für eine der folgenden Rollen Zugriff auf diese Topologie haben:</span><span class="sxs-lookup"><span data-stu-id="a77fa-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="a77fa-110">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="a77fa-110">Electronic reporting developer</span></span>
- <span data-ttu-id="a77fa-111">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="a77fa-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="a77fa-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="a77fa-112">System administrator</span></span>

<span data-ttu-id="a77fa-113">Sie müssen zudem Zugriff auf die Entwicklungsumgebung für diese Topologie haben.</span><span class="sxs-lookup"><span data-stu-id="a77fa-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="a77fa-114">Alle Aufgaben in diesem Thema können im **USMF**-Unternehmen erledigt werden.</span><span class="sxs-lookup"><span data-stu-id="a77fa-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="a77fa-115">EB-Format „Rollforward für Anlagen“ importieren</span><span class="sxs-lookup"><span data-stu-id="a77fa-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="a77fa-116">Um die Dokumente zu generieren, für die Sie einen benutzerdefinierten Speicherort hinzufügen möchten, [importieren](er-download-configurations-global-repo.md) Sie das EB-Format **Rollforward für Anlagen** in die aktuelle Topologie.</span><span class="sxs-lookup"><span data-stu-id="a77fa-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Konfigurationsrepository-Seite](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="a77fa-118">Bericht „Rollforward für Anlagen“ ausführen</span><span class="sxs-lookup"><span data-stu-id="a77fa-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="a77fa-119">Wechseln Sie zu **Anlage** \> **Anfragen und Berichte** \> **Transaktionsberichte** \> **Rollforward für Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="a77fa-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="a77fa-120">Geben Sie im Feld **Von Datum** das Datum **1/1/2017** (1. Januar 2017) ein.</span><span class="sxs-lookup"><span data-stu-id="a77fa-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="a77fa-121">Geben Sie im Feld **Bis Datum** das Datum **1/31/2017** (31. Januar 2017) ein.</span><span class="sxs-lookup"><span data-stu-id="a77fa-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="a77fa-122">Wählen Sie im Feld **Währung** die Option **Buchhaltungswährung** aus.</span><span class="sxs-lookup"><span data-stu-id="a77fa-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="a77fa-123">Wählen Sie im Feld **Formatzuordnung** die Option **Rollforward für Anlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="a77fa-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="a77fa-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="a77fa-124">Select **OK**.</span></span>

![Dialogfeld „Laufzeit“ für den Bericht „Rollforward für Anlagen“](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="a77fa-126">Überprüfen Sie in Microsoft Excel das ausgehende Dokument, das generiert wurde und zum Download zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a77fa-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="a77fa-127">Dieses Verhalten ist das [Standardverhalten](electronic-reporting-destinations.md#default-behavior) für ein EB-Format, für das keine [Ziele](electronic-reporting-destinations.md) konfiguriert sind und das im interaktiven Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a77fa-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="a77fa-128">Quellcode überprüfen</span><span class="sxs-lookup"><span data-stu-id="a77fa-128">Review the source code</span></span>

<span data-ttu-id="a77fa-129">Überprüfen Sie den Code der `generateReportByGER()`-Methode der Klasse `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="a77fa-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="a77fa-130">Beachten Sie, dass die `Run()`-Methode verwendet wird, um das EB-Framework aufzurufen und den Bericht **Rollforward für Anlagen** zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a77fa-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="a77fa-131">Quellcode ändern</span><span class="sxs-lookup"><span data-stu-id="a77fa-131">Modify the source code</span></span>

1. <span data-ttu-id="a77fa-132">Fügen Sie in Ihrem Visual Studio-Projekt eine neue Klasse hinzu (in diesem Beispiel `AssetRollForwardDestination`) und schreiben Sie Code, um Ihr benutzerdefiniertes Ziel für die Berichte **Rollforward für Anlagen** zu implementieren, die generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a77fa-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="a77fa-133">Die `new()`-Methode dient zum Abrufen des ursprünglichen EB-Zielobjekts und des von der Anwendungslogik gesteuerten Parameters, der den benutzerdefinierten Speicherort angibt, an dem generierte Berichte gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a77fa-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="a77fa-134">In diesem Beispiel ist der benutzerdefinierte Speicherort der Name eines Ordners des lokalen Dateisystems auf dem Server, auf dem der AOS-Dienst (Application Object Server) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a77fa-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="a77fa-135">Die `saveFile()`-Methode dient zum Speichern eines generierten Dokuments in einem Ordner des lokalen Dateisystems auf dem Server, auf dem der AOS-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a77fa-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="a77fa-136">Fügen Sie in Ihrem Visual Studio-Projekt eine neue Klasse hinzu (in diesem Beispiel `AssetRollForwardDestinationFactory`) und schreiben Sie Code, um ein benutzerdefiniertes Empfängerwerk einzurichten, das die Erstellung eines Ziels an das Standardempfängerwerk delegiert, und um ein Dateiziel mit Ihrem eigenen Ziel zu versehen.</span><span class="sxs-lookup"><span data-stu-id="a77fa-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="a77fa-137">Ändern Sie die vorhandene Klasse `AssetRollForwardService` und schreiben Sie Code, um ein benutzerdefiniertes Empfängerwerk für die Berichtsausführung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="a77fa-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="a77fa-138">Beachten Sie, dass beim Erstellen eines benutzerdefinierten Empfängerwerks der anwendungsgesteuerte Parameter, der einen Zielordner angibt, übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a77fa-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="a77fa-139">Auf diese Weise wird dieser Zielordner zum Speichern generierter Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="a77fa-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="a77fa-140">Stellen Sie sicher, dass der angegebene Ordner (in diesem Beispiel **c:\\0**) im lokalen Dateisystem des Servers vorhanden ist, auf dem der AOS-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a77fa-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="a77fa-141">Ansonsten wird zur Laufzeit eine [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1)-Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a77fa-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="a77fa-142">Ihr Projekt neu erstellen</span><span class="sxs-lookup"><span data-stu-id="a77fa-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="a77fa-143">Bericht „Rollforward für Anlagen“ erneut ausführen</span><span class="sxs-lookup"><span data-stu-id="a77fa-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="a77fa-144">Wechseln Sie zu **Anlage** \> **Anfragen und Berichte** \> **Transaktionsberichte** \> **Rollforward für Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="a77fa-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="a77fa-145">Geben Sie im Feld **Von Datum** den Wert **1/1/2017** ein.</span><span class="sxs-lookup"><span data-stu-id="a77fa-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="a77fa-146">Geben Sie im Feld **An Datum** den Wert **1/31/2017** ein.</span><span class="sxs-lookup"><span data-stu-id="a77fa-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="a77fa-147">Wählen Sie im Feld **Währung** die Option **Buchhaltungswährung** aus.</span><span class="sxs-lookup"><span data-stu-id="a77fa-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="a77fa-148">Wählen Sie im Feld **Formatzuordnung** die Option **Rollforward für Anlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="a77fa-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="a77fa-149">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="a77fa-149">Select **OK**.</span></span>
7. <span data-ttu-id="a77fa-150">Suchen Sie im lokalen Ordner **C:\\0** dies generierte Datei.</span><span class="sxs-lookup"><span data-stu-id="a77fa-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="a77fa-151">Weil das `originDestination`-Objekt im `AssetRollForwardDestination`-Objekt in diesem Beispiel nicht verwendet wird, werden die Konfigurationen für die [Ziele](electronic-reporting-destinations.md) des EB-Formats zur Laufzeit ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a77fa-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a77fa-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a77fa-152">Additional resources</span></span>

- [<span data-ttu-id="a77fa-153">Zielorte für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="a77fa-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="a77fa-154">Startseite für Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="a77fa-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
