---
title: Entfernte oder veraltete Plattformfunktionen
description: Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.
author: sericks007
manager: AnnBe
ms.date: 04/17/2020
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
ms.openlocfilehash: f6365d42de5d19d960641f188cb6052ef07d721f
ms.sourcegitcommit: 6d6aa016c4971b0673d461b82fd80b060ae5f7a1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3268746"
---
# <a name="removed-or-deprecated-platform-features"></a>Entfernte oder veraltete Plattformfunktionen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Plattform-Updates für Version 10.0.11 von Finance and Operations Apps

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

