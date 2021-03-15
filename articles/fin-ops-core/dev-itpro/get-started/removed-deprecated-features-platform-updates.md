---
title: Entfernte oder veraltete Plattformfunktionen
description: Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.
author: sericks007
manager: AnnBe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d57182aa34c4897ef3703d0f8ed08d032c261170
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154086"
---
# <a name="removed-or-deprecated-platform-features"></a>Entfernte oder veraltete Plattformfunktionen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://docs.microsoft.com/dynamics/s-e/). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="feature-removed-effective-january-28-2021"></a>Die Funktion wurde mit Wirkung zum 28. Januar 2021 entfernt.

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Stapelverarbeitungsauftrag zur Verarbeitung von SQL-Indexdefragmentierung

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um den Aufwand für den Betrieb, die Überwachung und die Pflege der Indexverwaltung durch Kunden zu verringern, wurde diese Funktion entfernt. |
| **Ersetzt durch eine andere Funktion?**   | In Zukunft wird die Indexpflege von Microsoft-Diensten durchgeführt. Dies geschieht kontinuierlich, ohne die Arbeitslast der Benutzer zu beeinträchtigen. |
| **Betroffene Produktbereiche**         | Finance and Operations Apps|
| **Bereitstellungsoption**              | Cloud-Bereitstellung: Wirkt sich auf von Microsoft verwaltete Produktionsumgebungen und Sandbox-Umgebungen der Stufen 2 bis 5 aus. |
| **Status**                         | Diese Funktion wird entfernt. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.17 von Finance and Operations Apps

> [!IMPORTANT]
> Version 10.0.17 ist als Teil einer Vorschauversion verfügbar. Inhalt und Funktionsweise unterliegen Änderungen. Weitere Informationen zu Vorschauversionen finden Sie in den [FAQ zu Dienstupdates für One Version](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die neuesten Versionen von Visual Studio zu unterstützen, müssen einige Änderungen an den X ++ – Erweiterungen für Visual Studio vorgenommen werden. Diese Änderungen sind nicht kompatibel mit Visual Studio 2015. |
| **Ersetzt durch eine andere Funktion?**   | Visual Studio 2017 wird Visual Studio 2015 als bereitgestellte und erforderliche Version ersetzen. |
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet. Im Zuge des Updates werden die vorherigen X++-Tools aus Visual Studio 2015 entfernt und die aktualisierten Tools werden nicht in Visual Studio 2015 installiert. Es gibt keine Auswirkungen auf gehostete Builds. Für virtuelle Buildmaschinen muss die Buildpipeline (Builddefinition) manuell aktualisiert werden, um die Abhängigkeit von MSBuild 14.0 (Visual Studio 2015) in MSBuild 15.0 (Visual Studio 2017) zu ändern, wie in [Veraltete Pipeline in Azure Pipelines aktualisieren](../dev-tools/pipeline-msbuild-update.md) beschrieben. |

### <a name="user-avatar"></a>Benutzer-Avatar 

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Der Benutzer-Avatar, der auf der rechten Seite der Navigationsleiste angezeigt wird, wurde mithilfe einer API aus dem veralteten Dynamics 365-Kopfzeilensteuerung abgerufen. |
| **Ersetzt durch eine andere Funktion?**   | Benutzer sehen ihre Initialen stattdessen in einem Kreis in der Navigationsleiste. Dies ist das gleiche visuelle Element, das derzeit auf Entwicklungsmaschinen verwendet wird. |
| **Betroffene Produktbereiche**         | Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Entfernt ab Version 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Enterprise Portal (EP) veraltet  

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die mit Dynamicse AX 2012 Enterprise Portal (EP) verknüpften Metadatenartefakt sind veraltet, da EP in den Finance and Operations-Apps nie unterstützt wurde. |
| **Ersetzt durch eine andere Funktion?**   | Nr. |
| **Betroffene Produktbereiche**         | Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet. Der gesamte EP-Code soll in der Version vom Oktober 2021 entfernt werden. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.15 von Finance and Operations Apps

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Unterstützung für Dynamics 365 wird außer Betrieb genommen

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab Dezember 2020 wird die Unterstützung von Microsoft Internet Explorer 11 für alle Dynamics 365-Produkte veraltet sein und Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt werden.<br><br>Dies wirkt sich auf Kunden aus, die Dynamics 365-Produkte verwenden, die für die Verwendung über eine Internet Explorer 11-Schnittstelle entworfen wurden. Nach August 2021 wird Internet Explorer 11 für solche Dynamics 365-Produkte nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen den Kunden den Übergang zu Microsoft Edge.|
| **Betroffene Produktbereiche**         | Alle Dynamics 365-Produkte |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio Add-In zum Anwenden von Metadaten-Hotfixes

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Metadaten-Hotfixes werden mit den [One-Version](../../fin-ops/get-started/one-version.md)-Service-Updates, die im Juli 2018 mit Version 8.1 eingeführt wurden, nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Einzelne Metadaten-Hotfixes sind für unterstützte Versionen nicht verfügbar. Stattdessen werden kumulative Qualitätsaktualisierungen angewendet. |
| **Betroffene Produktbereiche**         | Visual Studio Add-Ins |
| **Bereitstellungsoption**              | Entwicklung virtueller Maschinen |
| **Status**                         | Ab Version 10.0.15 ist das Add-In nicht mehr in den Visual Studio-Tools enthalten. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.14 von Finance and Operations Apps

### <a name="online-users-page"></a>Seite „Onlinebenutzer“ 

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Dies ist eine Legacy-Seite, die für die vorherige Client/Server-Architektur erstellt wurde. Die Informationen auf dieser Seite sind nicht immer korrekt, was verwirrend und irreführend sein kann. |
| **Ersetzt durch eine andere Funktion?**   | Wir werden in einem zukünftigen Update eine neue Seite bereitstellen.|
| **Betroffene Produktbereiche**         | Systemverwaltung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Bis Oktober 2021 wird dieses Formular entfernt.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.13 von Finance and Operations Apps


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Benutzerdefinierter Code, der in den SSRS-Berichtseigenschaften definiert ist 

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Im Allgemeinen bietet benutzerdefinierter Code nur begrenzte Vorteile und erfordert gleichzeitig erhebliche Ressourcen und Rechenleistung für den Support. Benutzerdefinierter Code wird hauptsächlich von Berichtsautoren verwendet, um öffentliche Methoden aus einer benutzerdefinierten Codeassembly aufzurufen. Der in der Cloud gehostete Dienst unterstützt jedoch keine Verweise auf benutzerdefinierte Assemblys für SSRS-Berichte. |
| **Ersetzt durch eine andere Funktion?**   | Berichtsautoren können weiterhin öffentliche .NET-APIs für Mathematik‑, Konvertierungs‑ und Formatierungsvorgänge aus einem beliebigen Textfeldausdruck referenzieren. Weitere Informationen finden Sie unter [Code zu einem Bericht (SSRS) hinzufügen](https://docs.microsoft.comsql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Betroffene Produktbereiche**         | Teilmenge der in RDL definierten Anwendungsberichtsentwürfe, die benutzerdefinierten Code enthalten. |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Ab Version 10.0.13 gibt der Compiler eine Warnung für Fälle aus, in denen benutzerdefinierter Code in einer SSRS-Berichtsdefinition erkannt wird. Öffnen Sie die Berichtsentwurfsdefinition und entfernen Sie alle benutzerdefinierten Codeartefakte, um das Problem zu beheben. Diese Warnung wird in einem zukünftigen Update durch einen Compiler-Fehler ersetzt.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Upgrade von drei jQuery-Komponentenbibliotheken 

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Drei jQuery-Komponentenbibliotheken werden aktualisiert, um Sicherheitsupdates und die Aktualisierung der Währung zu gewährleisten.   
| **Ersetzt durch eine andere Funktion?**   | Die folgenden Bibliotheken sind betroffen: jQuery (auf Version 3.5.0 von Version 2.1.4), jQuery UI (auf Version 1.12.1 von Version 1.11.4), jQuery qTip (auf Version 3.0.3 von 2.2.1). Die Migrationsanleitung wurde online von jQuery bereitgestellt.  |
| **Betroffene Produktbereiche**         | Erweiterbare Steuerelemente, insbesondere benutzerdefinierter JavaScript-Code, der veraltete oder entfernte APIs verwendet |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Mit der Version 10.0.13/Platform Update 37 können Kunden optional zu den neuesten Bibliotheken wechseln, indem sie die Funktion Drei jQuery-Komponentenbibliotheken aktualisieren aktivieren. Die Umstellung auf die neuen Bibliotheken ist mit der Version vom April 2021 obligatorisch, damit Zeit für die Migration betroffener APIs bleibt.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Bestehende Rastersteuerungs/ForceLegacyGrid()-API

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die vorhandene Rastersteuerung wird durch die neue Rastersteuerung ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Die [neue Rastersteuerung](../..//fin-ops/get-started/grid-capabilities.md) |
| **Betroffene Produktbereiche**         | Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | In Version 10.0.13 ist die neue Rastersteuerung allgemein verfügbar und Kunden können diese Funktion optional aktivieren. Die neue Rastersteuerung wird im Release vom Oktober 2021 obligatorisch. Wenn die neue Rastersteuerung obligatorisch wird, wird die **forceLegacyGrid()**-API nicht mehr berücksichtigt. |

### <a name="personalization-without-saved-views"></a>Personalisierung ohne gespeicherte Ansichten 

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Personalisierungssubsystem wurde mit der Funktion zum Speichern gespeicherter Ansichten überarbeitet, um eine bessere Leistung und zusätzliche Funktionen zu erreichen. |
| **Ersetzt durch eine andere Funktion?**   | Gespeicherte Ansichten |
| **Betroffene Produktbereiche**         | Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | In Version 10.0.13/Plattformupdate 37 ist die Funktion für gespeicherte Ansichten allgemein verfügbar und Kunden können diese Funktion optional aktivieren. Die Funktion für gespeicherte Ansichten wird im Release vom Oktober 2021 obligatorisch. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.12 von Finance and Operations Apps

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Formularerweiterungen für Raster- oder Gruppensteuerelemente mit ungültigen Feldreferenzen

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Datengruppeneigenschaft in Raster- oder Gruppensteuerelementen wird verwendet, um automatisch alle Felder einer Feldgruppe anzuzeigen. Ein durch Erweiterung hinzugefügtes Raster- oder Gruppensteuerelement kann Felder enthalten, die in der Feldgruppe nicht mehr definiert sind, oder es fehlen möglicherweise Felder, die in der Feldgruppe definiert sind. Dies kann zur Laufzeit zu inkonsistentem Verhalten führen. Plattform-Updates für Version 10.0.12 von Finance and Operations Apps kategorisieren jetzt dieses Problem als Compiler *Warnung*. Um dieses Problem zu beheben, öffnen Sie die Formularerweiterung und speichern Sie sie.
| **Ersetzt durch eine andere Funktion?**   | Diese Compiler-Warnung wird in einem zukünftigen Update durch einen Compiler-Fehler ersetzt. |
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Eine Compiler-Warnung wird in Plattform-Updates für Version 10.0.12 von Finance and Operations Apps eingeführt. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.11 von Finance and Operations Apps

### <a name="explicit-safe-lists-for-self-service-environments"></a>Explizite sichere Listen für Self-Service-Umgebungen

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Der Prozess zum Verschieben von IP in sichere Listen hat sich geändert. Self-Service unterstützt keine IP-sichere Listen mehr. |
| **Ersetzt durch eine andere Funktion?**   | Weitere Informationen finden Sie unter [Konfigurieren von Azure Active Directory Bedingter Zugriff](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Betroffene Produktbereiche**         | Sicherheit |
| **Bereitstellungsoption**              | Cloud |
| **Status**                         | **Veraltet:** Diese Funktion ist für Self-Service-Bereitstellungen nicht mehr verfügbar. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die neuesten Versionen von Visual Studio zu unterstützen, müssen einige Änderungen an den X ++ – Erweiterungen für Visual Studio vorgenommen werden. Diese Änderungen sind nicht kompatibel mit Visual Studio 2015. |
| **Ersetzt durch eine andere Funktion?**   | Visual Studio 2017 wird Visual Studio 2015 als bereitgestellte und erforderliche Version ersetzen. |
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Virtuelle Maschinen, die in Version 10.0.13 (Plattform-Update 37) oder höher bereitgestellt werden, enthalten Visual Studio 2017. Version 10.0.16 (Plattform-Update 40) ist die endgültige Version mit Unterstützung für Visual Studio 2015. Virtuelle Maschinen nur mit Visual Studio 2015 können nicht auf Version 10.0.17 (Plattform-Update 41) aktualisiert werden. |

### <a name="field-groups-containing-invalid-field-references"></a>Feldgruppen mit ungültigen Feldreferenzen

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Feldgruppen in Tabellenmetadatendefinitionen können ungültige Feldreferenzen enthalten. Wenn diese Feldgruppen bereitgestellt werden, kann dies dieses zu Laufzeitfehlern in Financial Reporting und Microsoft SQL Server Reporting Services (SSRS) führen. Mit dem Plattform-Update 23 wurde ein Compiler *Warnung* eingeführt, der dazu führte, dass dieses Metadatenproblem adressiert wurde. Plattform-Updates für Version 10.0.11 von Finance and Operations Apps kategorisieren dieses Problem als Compiler *Fehle*.<p>Führen Sie folgende Schritte aus, um dieses Problem zu beheben.</p><ol><li>Entfernen Sie die ungültige Feldreferenz aus der Tabellenfeldgruppendefinition.</li><li>Neu kompilieren.</li><li>Stellen Sie sicher, dass alle Fehler behoben sind.</li></ol> |
| **Ersetzt durch eine andere Funktion?**   | Dieser Compilerfehler ersetzt dauerhaft die Compilerwarnung.  |
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | **Veraltet:** Die Compiler-Warnung ist ein Compiler-Fehler in Plattform-Updates für Version 10.0.11 von Finance and Operations Apps. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-Lizenzen, die mit dem SHA1-Hashing-Algorithmus erstellt wurden

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Der Prozess zum Erstellen von Lizenzen eines unabhängigen Softwareanbieters (ISV) hat sich geändert. Weitere Informationen finden Sie unter [Lizenzierung eines unabhängigen Softwareanbieters (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Ersetzt durch eine andere Funktion?**   | Ja. Verwenden Sie Windows PowerShell, um Lizenzen zu erstellen. |
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | <strong>Veraltet:</strong> ISV-Lizenzen, die mit dem SHA1-Hashing-Algorithmus erstellt wurden. Dieser Algorithmus war abhängig von Zertifikaten, die mit dem Dienstprogramm MakeCert erstellt wurden, und dieses Dienstprogramm ist veraltet.<p><strong>Veraltet:</strong> Die Verwendung von SHA1 für Sicherheits- oder Hashing-Zwecke. SHA1 wird Anfang 2021 nicht mehr funktionieren. Daher sollte es nicht mehr verwendet werden.<p><strong>Entfernt:</strong> Unterstützung für eingehende oder ausgehende TLS 1.0- und TLS 1.1-Anforderungen. |

## <a name="platform-update-32"></a>Plattformupdate 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Das Dialogfeld für die Änderung von Workflow-Anforderungen enthält nicht mehr die Dropdown-Liste für die Benutzerauswahl.
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Dies war ein Sicherheitsproblem, da die Änderungsanfrage an einen unbeabsichtigten Benutzer gesendet werden konnte. Dies war auch eine Frage der Benutzerfreundlichkeit, da der Benutzer gezwungen war, den Urheber des Workflows zu bestimmen und manuell auszuwählen.  |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Workflow |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Die Benutzerauswahl-Dropdown-Liste wurde aus dem Dialogfeld zur Änderung der Anforderung in Plattform-Update 32 entfernt. Änderungsanfragen werden automatisch wie vorgesehen an den Absender gesendet. Weitere Informationen über diese Funktionalität finden Sie unter [Aktionen in Workflow-Genehmigungsprozessen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Eingebettete Drillthrough-Links werden in paginierten Dokumenten, die vom Cloud-gehosteten Dienst gerendert werden, nicht mehr unterstützt 
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Navigations-URLs, die in vom Dienst gerenderte Dokumente eingebettet sind, können vertrauliche Geschäftsdaten enthalten. Wir entfernen die Unterstützung für eingebettete Drillthrough-Links in Dokumenten als Sicherheitsmaßnahme, um die Kundendaten weiter zu schützen. Durch diese Änderung profitieren Benutzer auch von einer verbesserten Leistung bei der interaktiven Erstellung von Dokumenten.  |
| **Ersetzt durch eine andere Funktion?**   | Nr. |
| **Betroffene Produktbereiche**         | Bericht |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Diese Funktion wird aktiv aus dem Dienst entfernt.<br><br>Der moderne Client bietet zahlreiche Optionen zum Erstellen von Ansichten, einschließlich automatisch generierter Links zur Unterstützung der Navigation in der Anwendung. Vom Dienst bereitgestellte paginierte Dokumente werden für externe Kommunikation empfohlen, die per E-Mail gesendet, archiviert und für Empfänger gedruckt werden. Wir haben die Vorschau von Dokumenten direkt im Browser verbessert, der direkten Zugriff auf lokale Drucker bietet. Weitere Informationen finden Sie unter [Vorschau von PDF-Dokumenten mit einem eingebetteten Viewer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen
Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]