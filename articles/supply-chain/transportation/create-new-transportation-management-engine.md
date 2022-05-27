---
title: Neues Transportverwaltungsmodul erstellen
description: In diesem Thema wird beschrieben, wie Sie eine neue Transportmanagement-Engine in Dynamics 365 Supply Chain Management erstellen.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be52c6afb66e88b36f3b2cdf5af14e17b3d3005f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678121"
---
# <a name="create-a-new-transportation-management-engine"></a>Neues Transportverwaltungsmodul erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine neue Transportmanagement-Engine in Dynamics 365 Supply Chain Management erstellen. 

Transportverwaltungsmodule (TMS) definieren die Logik, die verwendet wird, um Transportsätze in der Transportverwaltung zu generieren und zu verarbeiten. Supply Chain Management bietet verschiedene Engine-Typen, die verschiedene Parameter berechnen, z. B. Tarife, Transitzeiten und die Anzahl der Zonen, die während des Transits durchquert werden. In diesem Artikel wird erläutert, wie Sie die Microsoft Visual Studio Entwicklungsumgebung zusammen mit Supply Chain Management-Entwicklungstools verwenden, um eine neue TMS-Engine zu erstellen und bereitzustellen, und dann, wie die Engine in Operations eingerichtet wird. Weitere Informationen zu den Motoren finden Sie unter [Transportmanagement-Engines](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Neuen TMS-Engine erstellen

In diesem Abschnitt wird erläutert, wie Sie eine Klassenbibliothek mit einer TMS-Engine-Implementierung erstellen und von einem Supply Chain Management-Modell aus darauf verweisen.

1. Um Ihre neuen Engines bereitzustellen, benötigen Sie ein Modell, das die Engines enthält. Klicken Sie im Menü **Dynamics 365** &gt; **Modellverwaltung** auf **Modell erstellen**, um ein neues Modell zu erstellen. Auf der ersten Seite des Assistenten **Modell erstellen** benennen Sie das Modell **TMSEngines**. 

   [![Erstellen eines Modells.](./media/012.png)](./media/012.png)

2. Wählen Sie auf der nächsten Seite **Neues Paket erstellen**. 

   [![Neues Paket erstellen.](./media/021.png)](./media/021.png)

3. Wählen Sie auf der nächsten Seite das Modell **ApplicationSuite** als Referenz. (Das Modell **ApplicationPlatform** ist vorausgewählt.) 

   [![Auswahl des zu referenzierenden Modells.](./media/032.png)](./media/032.png)

4. Klicken Sie auf der nächsten Seite auf **Beenden**, um die Erstellung eines neuen Modells zu bestätigen. 

   [![Abschluss der Modellerstellung.](./media/042.png)](./media/042.png)

5. Erstellen Sie in einer neuen Lösung ein neues Supply Chain Management-Projekt und benennen Sie es **TMSThirdParty**. Setzen Sie in den Projekteigenschaften das Modell des Projekts auf **TMSEngines**.
6. Füge eine neue C\# Klassenbibliothek zu Ihrer Lösung hinzu, und benennen Sie sie **ThirdPartyTMSEngines**.
7. Fügen Sie im Projekt ThirdPartyTMSEngines Verweise auf Supply Chain Management-spezifische Assemblys hinzu:
   -   Anwendungsassemblys, die es ermöglichen, auf X++-Typen zu verweisen. Diese Baugruppen finden Sie an den folgenden Orten. \[Packages root\] ist der Pfad des Speicherorts, an dem alle bereitgestellten Assemblys platziert werden, z. B. C:\\Pakete.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Frameworkassemblys, die den Zugriff auf Daten, LINQ und Hilfsfunktionen ermöglichen. Alle diese Assemblies finden Sie im Behälter \[Pakete root\]\\.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Die TMS-Kernassembly (die Engines enthält) und die TMS-Basisassembly (die Helfer, Konstanten, Datenübertragungsklassendefinitionen usw. enthält). Diese Baugruppen finden Sie an den folgenden Orten.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Benennen Sie die C\#-Klasse um, die automatisch im ThirdPartyTMSEngines-Projekt generiert wird, um **SampleRatingEngine**.
9. Implementieren Sie den Engine. Da wir in diesem Beispiel ein Tarifmodul erstellen, erben wir von der Basisklasse für Tarifmodule. Die Basisklasse implementiert den größten Teil der Tarifmodul-Schnittstelle (**TMSFwkIRateEngine**). Wir müssen nur die Bewertungsmethode implementieren. Um dieses Beispiel einfach zu halten, lassen wir diese Methode eine hartcodierte Rate von 100 registrieren. Sie können Engines erstellen, die jede der Engine-Schnittstellen implementieren, wie z. B. **TMSFwkIAccessorialEngine**. Alle Engine-Schnittstellen sind in X++ definiert.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Erstellen Sie die Lösung.
11. Fügen Sie eine neue Referenz zum TMSThirdParty-Projekt hinzu. Der Verweis sollte auf das Projekt ThirdPartyTMSEngines verweisen. Wenn Sie fertig sind, sollte Ihre Lösung so aussehen. 

    [![Die Lösung, die einen Verweis auf das TMSThirdParty-Projekt enthält.](./media/052.png)](./media/052.png)

12. Erstellen Sie die Lösung. Stellen Sie sicher, dass die neue Bibliothek im **Verweise**-Knoten im Anwendungs-Explorer erscheint. 

    [![Die neue Bibliothek im Referenzknoten des Anwendungs-Explorer.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Bereitstellen der TMS-Engine als Paket

Eine Möglichkeit zur Bereitstellung von TMS-Engines von Drittanbietern besteht in einem Bereitstellungspaket. Dieser Ansatz wird in einer Produktionsumgebung empfohlen. In einer Entwicklungsumgebung können Sie die Assemblys manuell kopieren, wie im nächsten Abschnitt „Einrichten einer TMS-Engine im Supply Chain Management“ beschrieben. Um das Modul als Paket bereitzustellen, führen Sie die folgenden Schritte aus:

1. Klicken Sie im Menü **Dynamics 365** &gt; **Bereitstellen** auf <strong>Bereitstellungspaket erstellen</strong>.
2. Wählen Sie im Dialogfeld **Bereitstellungspaket erstellen** das TMSEngines-Modell aus und geben Sie den Pfad ein, in dem Sie Ihre Paketdateien speichern möchten. 

   [![Auswahl des TMSEngines-Modells .](./media/071.png)](./media/071.png)

3. Sie können das Paket jetzt in der Zielumgebung bereitstellen. Eine Anleitung finden Sie unter [Installieren Sie ein bereitstellbares Paket](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Einrichten eines TMS-Moduls in Supply Chain Management

In diesem Abschnitt wird erläutert, wie Sie Supply Chain Management für die Verwendung einer TMS-Engine einrichten und wie die von uns erstellte neue Engine beim Ratenkauf verwendet wird. Dieses Beispiel in diesem Abschnitt verwendet das Demodatenunternehmen USMF.

1. Erstellen Sie eine neue Engine, wie im Abschnitt „Neue TMS-Engine erstellen“ beschrieben.
2. Erstellen Sie Ihre Lösung.
3. Kopieren Sie die resultierende Assembly in den binären Speicherort des Supply Chain Management-Servers, \[AOSWebRoot\]-Behälter. **Hinweis:** Dieser Schritt ist nur in einer Entwicklungsumgebung relevant. In einer Produktionsumgebung sollten Sie die Bereitstellung über ein Bereitstellungspaket durchführen. Anweisungen hierzu finden Sie im vorherigen Abschnitt „Bereitstellen der TMS-Engine als Paket“.
4. Im Supply Chain Management, auf der Seite **Tarifmodule** erstellen Sie eine neues Bewertungsmodul. Die Engine sollte auf die Engine-Assembly verweisen, die durch das Erstellen der Engine-Klassenbibliothek und der von Ihnen implementierten Engine-Klasse erzeugt wird. 

   [![Erstellen ein neues Bewertungsmodul auf der Seite „Tarifmodule“.](./media/081.png)](./media/081.png)

5. Erstellen Sie einen Versanddienstleister, der die Beispiel-Tarifmodule verwendet. Da unsere Engine keine Daten verwendet, müssen Sie keinen Preismaster zuweisen. 

   [![Neuen Spediteur erstellen .](./media/092.png)](./media/092.png)

6. Klicken Sie auf der Seite **Route-Workbench bewerten** auf **Shop bewerten**. Sie sollten eine Rate von 100,00 von SampleCarrier sehen, wie im folgenden Screenshot gezeigt. In diesem Beispiel bewerten wir den Einkauf für eine Route vom Lager 24 zum Kunden US-004. Da die Rate jedoch fest codiert ist, sehen Sie immer eine Rate von 100,00.

   [![Route-Workbench bewerten.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Hinweise und Tricks

- Wenn Sie Entwicklungstools für das Supply Chain Management verwenden, ist es sinnvoll, Ihrer Lösung ein neues Projekt hinzuzufügen. Wenn Sie dieses Projekt als Ihr Startprojekt festlegen und eine Debugging-Sitzung starten, können Sie sowohl X++ als auch C\# Code in derselben Debugging-Sitzung debuggen.
- Jedes Mal, wenn Sie Ihr ThirdPartyTMSEngines-Projekt ändern und neu kompilieren, müssen Sie die resultierende Assembly manuell an den Binärspeicherort kopieren oder über ein Bereitstellungspaket bereitstellen. Andernfalls können Sie die Ausführung mithilfe einer veralteten Assembly ausführen.
- Nachdem Sie TMS-spezifische Vorgänge in Supply Chain Management ausgeführt haben, sperrt der Internetinformationsdienste-Workerprozess (IIS) möglicherweise die ThirdPartyTMSEngines-Assembly, sodass die Assembly nicht aktualisiert werden kann. Starten Sie in diesem Fall den w3svc-Prozess neu.

### <a name="whitepaper"></a>Whitepaper

Laden Sie für weitere Informationen das folgende Whitepaper herunter (geschrieben zur Unterstützung von AX2012, gilt jedoch weiterhin für Dynamics 365 Supply Chain Management)

- [Implementieren und Bereitstellen von Transportmanagement-Engines](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]