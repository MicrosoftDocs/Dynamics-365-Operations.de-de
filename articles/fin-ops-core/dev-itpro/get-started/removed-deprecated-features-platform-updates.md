---
title: Entfernte oder veraltete Plattformfunktionen
description: Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.
author: sericks007
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 8b26ad668b6cc15d759e10952c042acd5e85bdea
ms.sourcegitcommit: 4909e55529f03310d24b7e40d52751e24d35259b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3678221"
---
# <a name="removed-or-deprecated-platform-features"></a>Entfernte oder veraltete Plattformfunktionen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.13 von Finance and Operations Apps

> [!NOTE]
> Version 10.0.13 ist eine Vorschauversion. Inhalt und Funktionsweise unterliegen Änderungen. Weitere Informationen zu Vorschauversionen finden Sie unter [Dienstupdateverfügbarkeit](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/public-preview-releases).

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
| **Status**                         | Sobald die Verfügbarkeit neuer virtueller Maschinen (VMs) mit Visual Studio 2017 angekündigt ist, müssen bestehende VMs nur mit Visual Studio 2015 durch Release Wave 1 von 2021 erneut bereitgestellt werden. |

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

