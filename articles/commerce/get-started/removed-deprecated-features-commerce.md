---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Commerce
description: In diesem Artikel werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.
author: josaw1
ms.date: 08/23/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 59ffcc00d67f6538980dec8965f894eb51f7230d
ms.sourcegitcommit: 649f1db26da8f20602f11180fc565b7c59eaf545
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337595"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine *veraltete* Funktion wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

> [!NOTE]
> Ausführliche Informationen über Objekte in Apps für Finanzen und Betrieb finden Sie in den [Technischen Referenzberichten](/dynamics/s-e/). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die in den einzelnen Versionen der Apps für Finanzen und Betrieb geändert oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-commerce-10029-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.29

### <a name="commerce-parameters-setting---allow-price-adjustments-to-increase-product-price"></a>Commerce-Parametereinstellungen: Lassen Sie Preisregulierungen zu, um den Produktpreis zu erhöhen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Mit dieser Einstellung sollte gesteuert werden, ob die Preisregulierungsfunktion eine Erhöhung des Produktpreises zulässt. Wenn dieser Parameter deaktiviert ist, können Organisationen bei Verwendung der Preisregulierungsfunktion nur einen Stückpreis eines Produkts festlegen, der niedriger ist als der Grundpreis und der Verkaufspreis laut Handelsvereinbarung. Wir lassen diese Einstellung veralten, da die Preisregulierungsfunktion aktualisiert wurde, um Anpassungen in zwei Richtungen (Erhöhung oder Senkung) standardmäßig zu unterstützen. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Preise und Rabatte |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Diese Einstellung ist seit Commerce-Version 10.0.29 standardmäßig aktiviert und wird im Oktober 2023 entfernt. |

### <a name="commerce-parameters-setting---enable-price-report-for-retail-store"></a>Commerce-Parametereinstellung: Preisbericht für Einzelhandelsgeschäft aktivieren

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Mit dieser Einstellung sollte gesteuert werden, ob die Preisberichtsfunktion für die Verwendung im Shopkonfigurationsformular verfügbar ist. Wir verwerfen diese Einstellung, da das Shopkonfigurationsformular aktualisiert wurde, um die Preisberichtsfunktion immer als Standardfunktion bereitzustellen. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Preise und Rabatte |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Diese Einstellung wird im Oktober 2023 entfernt. |

### <a name="commerce-parameters-setting---use-todays-date-to-calculate-prices"></a>Commerce-Parametereinstellung: Das heutige Datum verwenden, um die Preise zu berechnen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Standardpreisgestaltungsmodul für das Supply Chain Management (SCM) unterstützt die Preisberechnung basierend auf dem angeforderten Lieferdatum und dem angeforderten Wareneingangsdatum zusammen mit dem heutigen Datum. Das Preisgestaltungsmodul von Commerce unterstützt nur die Preisberechnung basierend auf dem heutigen Datum. Für Kunden, die sowohl SCM- als auch Commerce-Funktionen verwenden, haben wir diese Einstellung bereitgestellt und empfohlen, dass Kunden sie immer auf **Ja** einstellen, sodass die beiden Preisgestaltungsmodule zusammenarbeiten können. Wir lassen diese Einstellung veralten, da sie das Berechnungsverhalten nicht ändert und redundant ist. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Preise und Rabatte |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Diese Einstellung ist seit Commerce-Version 10.0.29 standardmäßig aktiviert und wird im Oktober 2023 entfernt. |

## <a name="feature-deprecation-effective-july-2022"></a>Außer Betrieb genommene Funktionen ab Juli 2022

### <a name="commerce-analytics-preview"></a>Commerce-Analysen (Vorschau)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Dynamics 365 Commerce-Team hat die Nutzung und Akzeptanz der Analysefunktion (Vorschauversion) von Commerce analysiert und beschlossen, die Funktion nicht mehr allgemein zur Verfügung zu stellen.   |
| **Ersetzt durch eine andere Funktion?**   | Zur Zeit wird die Analysefunktion (Vorschaufunktion) von Commerce nicht durch eine andere Funktion oder Lösung ersetzt. Der Export von Rohtransaktionen und Stammdaten aus Finanz- und Betriebs-Apps zu Azure Data Lake ist weiterhin verfügbar, wie in [Export zu Data Lake in Finanz- und Betriebs-Apps](../../fin-ops-core/dev-itpro/data-entities/finance-data-azure-data-lake.md) erläutert. Partner und Debitor können diesen Datenstrom nutzen, um die gewünschten Analyseberichte für ihre Geschäftsanforderungen zu erstellen.
| **Betroffene Produktbereiche**         | Commerce-Analysen (Vorschau) |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Diese Funktion wird voraussichtlich bis zum 30. August 2022 deaktiviert.  Von diesem Zeitpunkt an werden die aktuellen Power BI-Berichte von Commerce analytics (Vorschau) nicht mehr aktualisiert.     |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.21

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Einstellung „Verarbeitung überlappender Rabatte“ in Commerce-Parametern

Die Einstellung **Verarbeitung überlappender Rabatte** auf der Seite **Commerce-Parameter** ist in der Commerce-Version 10.0.21 eingestellt. In Zukunft wird die Commerce-Preis-Engine einen einzigen Algorithmus verwenden, um die optimale Kombination überlappender Rabatte zu bestimmen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | <p>Die Einstellung **Verarbeitung überlappender Rabatte** in den Commerce-Parametern steuert, wie das Commerce-Preisgestaltungsmodul die optimale Kombination überlappender Rabatte sucht und bestimmt. Derzeit werden sind drei Optionen verfügbar:<p><ul><li> **Optimale Leistung** – Diese Option verwendet einen erweiterten Heuristikalgorithmus und die Methode [Schwellenwertklassifizierung](../optimal-combination-overlapping-discounts.md), um die beste Rabattkombination rechtzeitig zu priorisieren, zu bewerten und zu bestimmen.</li><li>**Ausgeglichene Kalkulation** – In der aktuellen Codebasis funktioniert diese Option genauso wie die Option **Optimale Leistung**. Daher ist es im Wesentlichen eine duplizierte Option.</li><li>**Umfassende Kalkulation** – Diese Option verwendet einen alten Algorithmus, der bei der Preisberechnung alle möglichen Rabattkombinationen durchläuft. Bei Aufträgen mit großen Positionen und Mengen kann diese Option zu Leistungsproblemen führen.</li></ul><p>Um die Konfiguration zu vereinfachen, die Leistung zu verbessern und Vorfälle zu reduzieren, die durch den alten Algorithmus verursacht werden, entfernen wir die Einstellung **Verarbeitung überlappende Rabatte** vollständig und aktualisieren die interne Logik des Preisgestaltungsmoduls von Commerce, sodass er jetzt nur den erweiterten Algorithmus verwendet (d. h. den Algorithmus hinter der Option **Optimale Leistung**).</p> |
| **Ersetzt durch eine andere Funktion?**   | Nein. Wir empfehlen Organisationen, die die Option **Ausgeglichene Kalkulation** oder **Umfassende Kalkulation** verwenden, zur Option **Optimale Leistung** zu wechseln, bevor diese Funktion entfernt wird. |
| **Betroffene Produktbereiche**         | Preise und Rabatte |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Ab Version 10.0.21 wird die Einstellung **Verarbeitung überlappender Rabatte** im Oktober 2022 aus den Commerce-Parametern entfernt. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Retail SDK wird über Lifecycle Services verteilt

Das Retail SDK wird in Lifecycle Services (LCS) ausgeliefert. Diese Art der Verteilung ist in Version 10.0.21 veraltet. Zukünftig werden Retail SDK-Referenzpakete, Bibliotheken und Beispiele in öffentlichen Repositories auf GitHub veröffentlicht.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Retail SDK wird in LCS ausgeliefert. Der LCS-Prozess nimmt einige Stunden in Anspruch und muss für jedes Update wiederholt werden. Zukünftig werden Retail SDK-Referenzpakete, Bibliotheken und Beispiele in öffentlichen Repositories auf GitHub veröffentlicht. Erweiterungsbeispiele und Referenzpakete können einfach konsumiert werden, und die Updates sind in wenigen Minuten abgeschlossen. |
| **Ersetzt durch eine andere Funktion?**   |  [Laden Sie Beispiele und Referenzpakete für das Retail SDK von GitHub herunter NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Betroffene Produktbereiche**         | Retail SDK |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Außer Betrieb genommen: Ab Version 10.0.21 wird das SDK, das über die LCS-VMs ausgeliefert wird, im Oktober 2023 entfernt. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Im Einzelhandel bereitzustellende Pakete und kombinierte Installer für POS-, Hardware-Station- und Cloud Scale-Einheiten

Retail-bereitstellbare Pakete, die mit dem Retail SDK MSBuild erzeugt wurden, sind in 10.0.21 veraltet. Verwenden Sie in Zukunft das Cloud Scale-Unit (CSU)-Paket für Cloud Scale-Unit-Erweiterungen (Commerce Runtime, Channel-Datenbank, Headless Commerce APIs, Payments und Cloud Point of Sale (POS)). Verwenden Sie die reinen Erweiterungs-Installationspakete für POS, Hardware-Station und Cloud Scale-Unit self-hosted.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ein für den Einzelhandel bereitstellbares Paket ist ein kombiniertes Paket, das einen kompletten Satz von Erweiterungspaketen und Installern enthält. Dieses kombinierte Paket macht die Bereitstellung komplex, da die CSU-Erweiterungen in die Cloud Scale-Unit gehen und die Installer in den Geschäften bereitgestellt werden. Die Installer enthalten die Erweiterung und das Basisprodukt, was die Updates schwierig macht. Bei jedem Upgrade sind ein Code Merge und eine Paketgenerierung erforderlich. Um diesen Prozess zu vereinfachen, werden die Erweiterungspakete jetzt in Komponenten aufgeteilt, um das Bereitstellen und Verwalten zu erleichtern. Mit dem neuen Ansatz sind Erweiterungen und Basisprodukt-Installer getrennt und können unabhängig voneinander gewartet und aktualisiert werden, ohne dass ein Code-Merge oder eine Neu-Paketierung erforderlich ist.|
| **Ersetzt durch eine andere Funktion?**   | CSU-Erweiterungen, POS-Erweiterungs-Installer, Hardware-Stations-Erweiterungs-Installer |
| **Betroffene Produktbereiche**         | Dynamics 365 Commerce Erweiterung und Bereitstellung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Außer Betrieb genommen: Ab der Version 10.0.21 wird die Unterstützung für das Bereitstellen von RetailDeployablePackage in LCS im Oktober 2022 entfernt. |

Weitere Informationen finden Sie hier:

+ [Erzeugen eines separaten Pakets für Commerce Cloud Scale-Unit (CSU)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Modern POS-Erweiterungspaketprojekt erstellen](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [Integrieren Sie den POS mit einem neuen Hardware-Gerät](../dev-itpro/hardware-device-extension.md)
+ Code-Beispiele.
    + [Cloud Scale-Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU und Hardware-Station](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln und CloudPos.sln im Retail SDK

Die Entwicklung von POS-Erweiterungen mit ModernPos.sln, CloudPos.sln, POS.Extension.csproj und dem POS-Ordner ist in Version 10.0.21 veraltet. Verwenden Sie in Zukunft das POS-unabhängige Paketierungs-SDK für POS-Erweiterungen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | In früheren Versionen des Retail-SDK ist bei POS-Erweiterungen ein Code-Merge und ein Repackaging erforderlich, um auf die neueste Version des POS zu aktualisieren. Das Code Merge war ein zeitaufwändiger Upgrade-Prozess und Sie mussten das komplette Retail SDK im Repository pflegen. Außerdem mussten Sie das Kernprojekt POS.App kompilieren. Durch die Verwendung des unabhängigen Paketierungsmodells müssen Sie nur Ihre Erweiterung pflegen. Der Prozess der Aktualisierung auf die neueste Version der POS-Erweiterungen ist so einfach wie die Aktualisierung der Version des NuGet-Pakets, das Ihr Projekt konsumiert. Die Erweiterungen können unabhängig voneinander bereitgestellt werden, und die Dienste verwenden die Installationsprogramme für die Erweiterungen. Das Basis-POS kann separat bereitgestellt und gewartet werden, und es ist kein Code-Merge oder Repackaging mit dem Basis-Installer oder Code erforderlich. |
| **Ersetzt durch eine andere Funktion?**   | [POS-unabhängiges Paketierungs-SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Betroffene Produktbereiche**         | Dynamics 365 Commerce POS-Erweiterung und -Einsatz |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Außer Betrieb genommen: Ab Version 10.0.21 wird die Unterstützung für kombinierte POS-Pakete und das Erweiterungsmodell unter Verwendung der ModernPos.Sln, CloudPOs.sln und POS.Extensons.csproj im Retail SDK im Oktober 2023 entfernt. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.17

### <a name="full-dataset-generation-interval-is-deprecated"></a>Das vollständige Intervall für die Datensatzgenerierung ist veraltet

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab dieser Version in wird das **Commerce-Scheduler-Parameter**-Formular in der Dynamics 365-Zentralverwaltung das Feld **Vollständiges Intervall für die Datensatzgenerierung in Tagen** veraltet sein. Ab dieser Version wird das Feld auch visuell entfernt, sodass der Wert nicht bearbeitet werden kann. Dies bleibt als Wert **0** erhalten. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Dynamics 365 Commerce |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Verwenden Sie dieses Feld nicht und ändern Sie den Wert darin nicht.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-Unterstützung für Dynamics 365 ist veraltet

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab Dezember 2020 wird die Unterstützung von Microsoft Internet Explorer 11 für alle Dynamics 365-Produkte eingestellt und Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt.<br><br>Dies wirkt sich auf Kunden aus, die Dynamics 365-Produkte verwenden, die für die Verwendung über eine Internet Explorer 11-Schnittstelle entworfen wurden. Nach August 2021 wird Internet Explorer 11 für solche Dynamics 365-Produkte nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen den Kunden den Übergang zu Microsoft Edge.|
| **Betroffene Produktbereiche**         | Alle Dynamics 365-Produkte |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.11
### <a name="data-action-hooks"></a>Datenaktivitätshooks
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Funktion für Datenaktions-Hooks wird aufgrund von Leistungsproblemen nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Es wird empfohlen, [Datenaktion überschreibt](../e-commerce-extensibility/data-action-overrides.md) zu verwenden, um die Geschäftslogik in der Datenaktionsschicht zu ändern.|
| **Betroffene Produktbereiche**         | E-Commerce-Erweiterbarkeit Datenaktionen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Retail SDK Unterstützung für Visual Studio 2015, msbuild 14.0 und Retail SDK\Referencebibliotheken und Tools
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Retail SDK-Unterstützung für Visual Studio 2015 wurde veraltet und aktualisiert, um VS 2017, msbuild 15.0 und alle Referenzbibliotheken und Commerce-Proxy-Generator-Tools im Ordner RetailSDK\Referenzen zu unterstützen, die in verschoben wurden NuGet-Pakete zur Vereinfachung des Erweiterungsmodells und des SDK-Aktualisierungsprozesses.|
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen Ihnen, den Informationen in [Migrieren von Retail SDK von Visual Studio 2015 bis Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) zu folgen, um Ihr System zu aktualisieren. |
| **Betroffene Produktbereiche**         | Retail SDK-Erweiterungen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server-Erweiterung mit IEdmModelExtender und CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Retail Server -Erweiterung mit IEdmModelExtender und CommerceController wurde eingestellt, um ein vereinfachtes Erweiterungsmodell bereitzustellen. Die neue Implementierung enthält nur die Controller-Klasse ohne zusätzliche Implementierung der IEdmModelExtender-Klasse. Dadurch wird auch die Abhängigkeit von einer bestimmten OData-Version vermieden (wenn die OData-Version aktualisiert wird, können Erweiterungen beschädigt werden.) |
| **Ersetzt durch eine andere Funktion?**   |  Wir empfehlen, dass Sie das IController-Klassenerweiterungsmodell verwenden, indem Sie das NuGet-Paket importieren(Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Betroffene Produktbereiche**         | Retail Server-Erweiterungen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Hardware-Stationserweiterung mit IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Erweiterung der Hardwarestation mit IHardwareStationController wird eingestellt, um ein vereinfachtes Erweiterungsmodell bereitzustellen. Die neue Implementierung wird nur die IController-Klasse ohne zusätzliche Klassenimplementierung haben. Um die Abhängigkeit von den wichtigsten Hardware-Stationsbibliotheken zu vermeiden, muss die vorherige Erweiterung auf mehrere Bibliotheken verweisen.) |
| **Ersetzt durch eine andere Funktion?**   | Sie sollten das IController-Klassenerweiterungsmodell verwenden, indem Sie das NuGet-Paket importieren(Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Betroffene Produktbereiche**         | Hardwar-Stationserweiterungen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>POS-Vorgang 803 – Entnahme und Empfang
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Entnahme- und Empfangsvorgänge werden veraltet, aufgrund der Neugestaltung des neuen Vorgangs. |
| **Ersetzt durch eine andere Funktion?**   | Ja. Er wird durch zwei neue POS-Vorgänge ersetzt: Eingangsvorgang (804) und Ausgangsvorgang (805).|
| **Betroffene Produktbereiche**         | Verkaufsstellen-(POS)-Anwendung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab Version 10.0.10 erhält der Entnahme- und Empfangsvorgang keine neuen Funktionsupdates mehr. Nur kritische Fehlerbehebungen werden für diesen Vorgang in zukünftigen Versionen durchgeführt. Alle Kunden werden aufgefordert, auf die neuen [Eingehenden Vorgänge](../pos-inbound-inventory-operation.md) und [Ausgehenden Vorgänge](../pos-outbound-inventory-operation.md) zu wechseln, die weiterhin Teil unserer langfristigen Produkt-Roadmap sein werden. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities und GetAvailableInventoryNearby-APIs
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Neue optimierte APIs sind erstellt worden, um die GetProductAvailabilities und GetAvailableInventoryNearby-APIs zu ersetzen. |
| **Ersetzt durch eine andere Funktion?**   | Ja: Es wird durch GetEstimatedAvailabilty- und GetEstimatedProductWarehouseAvailability-APIs ersetzt. |
| **Betroffene Produktbereiche**         | E-Commerce-Anwendung SDK |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab Version 10.0.7 werden keine technischen Investitionen mehr für GetProductAvailabilities und GetAvailableInventoryNearby getätigt. Organisationen, die diese APIs in ihren E-Commerce-Bereitstellungen verwenden, sollten zu den neuen GetEstimatedAvailability- und GetEstimatedProductWarehouseAvailability-APIs wechseln und die [Optimierte Funktion zur Berechnung der Produktverfügbarkeit](../calculated-inventory-retail-channels.md) aktivieren.  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen
Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

