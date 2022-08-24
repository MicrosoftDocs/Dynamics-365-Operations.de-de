---
title: Zwischen Store Commerce und Cloud POS auswählen
description: In diesem Artikel werden die wichtigsten Unterschiede zwischen Store Commerce und Cloud POS erläutert und verschiedene Faktoren beschrieben, die Einzelhändler, die Dynamics 365 Commerce implementieren, berücksichtigen sollten, um ihnen dabei zu helfen, die beste Wahl für ihre Anforderungen zu treffen.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: bbb5f3d4c61907243bed404f3ab7bea05c78b1c0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276453"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Zwischen Store Commerce und Cloud POS auswählen

[!include [banner](includes/banner.md)]

In diesem Artikel werden die wichtigsten Unterschiede zwischen Store Commerce und Cloud POS erläutert und verschiedene Faktoren beschrieben, die Einzelhändler, die Dynamics 365 Commerce implementieren, berücksichtigen sollten, um ihnen dabei zu helfen, die beste Wahl für ihre Anforderungen zu treffen. Es gibt Implementierern zudem zusätzliche Hintergrundinformationen, Tipps und Orientierungshilfe für Faktoren, die sie berücksichtigen sollten, wenn sie Dynamics 365 Commerce bereitstellen. Indem diese Anleitung überprüft und befolgt wird als Teil des Bereitstellungsprozesses, können Implementierer Abgänge vermeiden, die möglicherweise die Zufriedenheit oder Leistung der Benutzer beeinträchtigt hat.

## <a name="insights"></a>Einblicke

Commerce bietet eine breite Palette von Bereitstellungs- und Topologieoptionen. Daher können Einzelhändler die Komponenten und die gewünschte Konfiguration auswählen, die in ihrer Geschäfts- und Technologiebedingungen erfüllt werden. Ein Aspekt der Implementierung, der Überlegung voraussetzt, erfordert, ist die Auswahl einer Plattform und des Formularfaktors für die Verkaufsstellen (POS)- Komponente.

### <a name="pos-platform-and-form-factor-considerations"></a>POS-Plattform- und -Formularfaktorüberlegungen

Commerce unterstützt die folgenden: POS-Optionen

- Store Commerce für Microsoft Windows
- Store Commerce für iOS und Android
- Cloud POS (CPOS) mit Unterstützung von Microsoft Edge- und Google Chrome-Browsern
- Modern POS (MPOS) für Microsoft Windows (MPOS wird im Oktober 2023 eingestellt.) 

In allen Fällen teilt POS (Store Commerce und CPOS) den gleichen Kernanwendungscode. Dieser Schritt ist wichtig für folgende Gründe:

- Die Benutzeroberfläche (UI) ist, ungeachtet der Plattform oder den Formularfaktor einheitlich.
- Die meisten funktionalen Funktionen sind identisch, dies unabhängig von der Plattform oder dem Formularfaktor. Jedoch gibt es mehrere wichtige Unterschiede. Die Unterschiede werden in diesem Artikel vermerkt.
- In jedem Shop können die POS-Abweichungen kombiniert und gleichzeitig ausgeführt werden. Für die Hauptregister kann ein Einzelhändler Store Commerce beispielsweise auf Computern verwenden, die unter Windows ausgeführt werden. Allerdings kann der Einzelhändler die Terminals oder Register mit browserbasierten mobilen Geräten ergänzen.
- Anpassungen und Erweiterungen können über Formularfaktoren Plattformen leicht verwendet werden. Da der Kernanwendungscode freigegeben wird, können die meisten Anpassungen einmal anstelle mehrmals implementiert werden.

### <a name="store-commerce-vs-cpos"></a>Store Commerce im Vergleich zu CPOS

Obwohl Store Commerce und CPOS weitgehend identisch sind, gibt es mehrere wichtige Unterschiede, die Sie verstehen müssen.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce ist eine Desktop-Anwendung, die auf einem Gerät installiert und gewartet wird.

- **Windows** – Die Store Commerce-Anwendung für Windows enthält den gesamten Anwendungscode, Commerce Runtime (CRT) und Hardware Station (HWS).
- **iOS/Android** – Auf diesen Plattformen dient die Anwendung als Host für den CPOS-Anwendungscode. Das bedeutet, der Anwendungscode stammt von dem CPOS-Server der auf Commerce Scale Unit gehostet wird. Weitere Informationen finden Sie unter [Commerce Scale Unit-Übersicht](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Da CPOS in einen Browser ausgeführt wird, wird die Anwendung nicht im Gerät eingerichtet. Stattdessen greift der Browser auf den Anwendungscode vom CPOS-Server zu. Daher können CPOS nicht direkt POS-Hardware zugreifen oder offline in einem Bundesland arbeiten.

### <a name="store-deployment-considerations"></a>Shopbereitstellungsüberlegungen

Neben einer Plattform und einem Formularfaktor müssen Einzelhändler eine Bereitstellungsoption auch im Unternehmen auswählen. Die folgenden Tabelle zeigt die Konfiguration, die für jede POS-Option verfügbar ist.

| POS-Bewerbung            | Commerce Scale Unit | Verfügbar offline | Lokale HWS-Unterstützung |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce für Windows | Cloud oder RSSU       | Ja               | Ja               |
| Store Commerce für Android | Cloud oder RSSU       | Nein                | Ja               |
| Store Commerce für iOS     | Cloud oder RSSU       | Nein                | Nein                |
| Cloud POS                  | Cloud oder RSSU       | Nein                | Nein                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Die Commerce Scale Unit ist eine Komponente, die das CRT hostet. Das gesamte CRT enthält die Geschäftslogik, die vom POS verwendet wird und es bietet Zugriff auf die Kanaldatenbank. Sobald sie online ist, nutzen alle POS-Kunden im Shop die Commerce Scale Unit. Die Commerce Scale Unit kann entweder in der Cloud oder im Shop bereitgestellt werden.

#### <a name="offline-mode"></a>Offlinemodus

Der Offlinemodus wird bei Store Commerce für Windows unterstützt. Im Offline-Modus kann der POS weiter Verkäufe verarbeiten, selbst wenn er von der Commerce Scale Unit getrennt ist. Sie kann mit der Kanaldatenbank dann synchronisiert werden, sofern die Konnektivität zurückgesetzt wird. Store Commerce verwendet eine eigene eingebettete Instanz des CRT und verwendet vorübergehend eine eigene lokale Datenquelle (offline SQL Server-Datenbank). Weitere Informationen finden Sie unter [POS Offline-Funktionalität](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>POS-Peripheriegeräte-/-Hardwareüberlegungen

Einzelhändler müssen auch entscheiden, wie der POS auf Geräte wie Drucker, Bargeldladen und Zahlungsterminals zugreift. Hardwarestationen können einem POS-Register zugewiesen werden oder unter den Kassen in einer Filiale verwendet werden.

| POS-Bewerbung            | Lokaler HWS OPOS | Netzwerkperipheriegeräte | Gemeinsame HWS-Unterstützung |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce für Windows | Ja            | Ja                 | Ja                |
| Store Commerce für Android | Nein             | Ja                 | Ja                |
| Store Commerce für iOS     | Nein             | Nein                  | Ja                |
| Cloud POS                  | Nein             | Nein                  | Ja                |

Weitere Informationen dazu, wie die Hardwarestation installiert wird, finden Sie unter [Retail-Hardwarestation-Konfiguration und -Installation](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Implementierungsüberlegungen

Berücksichtigen Sie die folgenden Informationen, wie Sie die POS-Implementierung in den Ladengeschäften planen:

- **Funktionsanforderungen** – Die Kerngeschäftsprozesse und - funktionen sind gleich, unabhängig von der Plattform, dem Forularfaktor oder der Bereitstellungstopologie. Daher müssen Einzelhändler die meisten Funktionsanforderungen nicht berücksichtigten, wenn sie ihre Implementierung planen.
- **Konnektivität** - Netzwerkverfügbarkeit (Fernnetz \[WAN\] und lokale Netzwerke \[LAN\]) ist der größte Faktor, der vorsichtige Überlegung voraussetzt. Sämtliche Vorteile, die ein Null-Bedarf, Cloud-gehostete Lösung in Bezug auf Kosten- und Einfachheit bringt, ist verloren, wenn das System nicht für unternehmenswichtige Prozesse verfügbar ist.

    Sofern die Konnektivität für ein gegebenes Gerät sehr zuverlässig und elastisch ist oder wenn ein bestimmter Betrag von Ausfallzeiten für den Einzelhändler akzeptabel ist, wird eine der folgenden Optionen empfohlen:

    - Verwenden Sie Store Commerce in Windows, und aktivieren Sie den Offline-Modus.
    - Stellen Sie eine lokale Commerce Scale Unit bereit.

    Diese beiden Optionen sind nicht einheitlich exklusiv. Für die zuverlässigste Topologie, können Einzelhändler eine lokale RSSU bereitstellen, um die Abhängigkeit für die Internet-Konnektivität oder Azure-Verfügbarkeit zu reduzieren, und sie können auch POS-Register bereitstellen, in denen der Offline-Modus aktiviert wird, wenn ein Problem mit dem lokalen Server oder im Netzwerk vorhanden ist.

- **Hardwaregeräte/Peripheriegeräte** – Ein wichtiger Aspekt eines Retail POS-Systems ist die Möglichkeit, Drucker, Geldladen und Zahlungsterminals zu verwenden. Obwohl alle verfügbaren POS-Optionen Peripheriegeräte verwenden können, unterstützt nur Store Commerce für Windows diese direkt. Bei allen anderen Anwendungen ist eine oder mehrere Hardwarestationen erforderlich. Obwohl dieser Ansatz Flexibilität hinzufügt, müssen zusätzliche Komponenten bereitgestellt, konfiguriert und verwaltet werden.
- **Systemanforderungen** – Die Systemanforderungen für die POS-Anwendung unterscheiden sich. Stellen Sie sicher, die neuesten Informationen zu überprüfen, bevor Sie Ihre Auswahl treffen. Weil CPOS beispielsweise in einen Browser ausgeführt wird, unterstützt sie einen breiteren Bereich von Betriebssystemen. Weitere Informationen zu den Systemanforderungen finden Sie unter [Systemanforderungen für Cloud-Bereitstellung](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Bereitstellung und Verwalten** – Die Komplexität der Bereitstellung und Wartungsanforderungen kann unterschiedlich sein, abhängig von der Anwendungen und der Bereitstellungs-Auswahlen. Beispiel für eine Cloud-gehostete CPOS-Bereitstellung ist, dass Sie nicht jedes Gerät installieren und aktualisieren müssen. Daher verringert dieser Ansatz Komplexität und Kosten. Wenn Sie jedoch Store Commerce für jedes Register bereitstellen und den Offline-Modus aktivieren, und Sie auch geteilte Hardware-Stationen bereitstellen, erhöhen Sie deutlich die Anzahl von Endpunkten, die verwaltet werden müssen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
