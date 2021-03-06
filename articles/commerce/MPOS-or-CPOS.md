---
title: Zwischen Modern POS (MPOS) und Cloud POS wählen
description: In diesem Thema werden die wesentlichen Unterschiede zwischen Modern POS und Cloud POS erklärt. Außerdem werden verschiedene Faktoren beschrieben, die Einzelhändler, die Dynamics 365 Commerce implementieren, bedenken müssen, um die beste Wahl für ihre Anforderungen zu treffen.
author: jblucher
ms.date: 10/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f19506d66aef22099dae9396fd345c293bf559b7
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193070"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a>Zwischen Modern POS (MPOS) und Cloud POS wählen

[!include [banner](includes/banner.md)]

Dieses Thema gibt Implementierern zusätzliche Hintergrundinformationen, Tipps und Orientierungshilfe für Faktoren, die sie berücksichtigen sollten, wenn sie Dynamics 365 Commerce bereitstellen. Indem diese Anleitung überprüft und befolgt wird als Teil des Bereitstellungsprozesses, können Implementierer Abgänge vermeiden, die möglicherweise die Zufriedenheit oder Leistung der Benutzer beeinträchtigt hat.

## <a name="insights"></a>Einblicke

Commerce bietet eine breite Palette von Bereitstellungs- und Topologieoptionen. Daher können Einzelhändler die Komponenten und die gewünschte Konfiguration auswählen, die in ihrer Geschäfts- und Technologiebedingungen erfüllt werden. Ein Aspekt der Implementierung, der Überlegung voraussetzt, erfordert, ist die Auswahl einer Plattform und des Formularfaktors für die Verkaufsstellen (POS)- Komponente.

### <a name="pos-platform-and-form-factor-considerations"></a>POS-Plattform- und -Formularfaktorüberlegungen

Commerce unterstützt die folgenden: POS-Optionen

- Modern POS (MPOS)  für Microsoft Windows
- MPOS für Microsoft Windows Phone
- MPOS für Apple iPad oder Google Android-Tablet
- Cloud POS (CPOS) mit Unterstützung von Microsoft Edge-, Internet Explorer- und Google Chrome-Browsern

In allen Fällen teilt POS (MPOS und CPOS) den gleichen Kernanwendungscode. Dieser Schritt ist wichtig für folgende Gründe:

- Die Benutzeroberfläche (UI) ist, ungeachtet der Plattform oder den Formularfaktor einheitlich.
- Die meisten funktionalen Funktionen sind identisch, dies unabhängig von der Plattform oder dem Formularfaktor. Jedoch gibt es mehrere wichtige Unterschiede. Die Unterschiede werden in diesem Thema vermerkt.
- In einem bestimmten Shop können die POS-Abweichungen kombiniert und gleichzeitig ausgeführt werden. Für die Hauptregister kann ein MPOS Einzelhändler MPOS beispielsweise auf Computern verwenden, die unter Windows ausgeführt werden. Allerdings kann der Einzelhändler die Terminals oder Register mit browserbasierten mobilen Geräten ergänzen.
- Anpassungen und Erweiterungen können über Formularfaktoren Plattformen leicht verwendet werden. Da der Kernanwendungscode freigegeben wird, können die meisten Anpassungen einmal anstelle mehrmals implementiert werden.

### <a name="mpos-vs-cpos"></a>MPOS und CPOS

Obwohl MPOS und CPOS von der Komplexität identisch sind, gibt es mehrere wichtige Unterschiede, die Sie verstehen müssen.

#### <a name="mpos"></a>MPOS

MPOS auf einem Windows-, iOS- oder Android-Gerät ist eine Anwendung, die auf dieses Gerät verpackt, eingerichtet und gewartet wird.

- **Windows** – Die MPOS für Windows-Anwendung enthält den gesamten Anwendungscode und die eingebette Commerce Runtime (CRT). 
- **iOS/Android** – Auf diesen Plattformen dient die Anwendung als Host für den CPOS-Anwendungscode. Das bedeutet, der Anwendungscode stammt von dem CPOS-Server auf Microsoft Azure oder der Commerce Scale Unit. Weitere Informationen finden Sie unter [Commerce Scale Unit-Übersicht](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Da CPOS in einen Browser ausgeführt wird, wird die Anwendung nicht im Gerät eingerichtet. Stattdessen greift der Browser auf den Anwendungscode vom CPOS-Server zu. Daher können CPOS nicht direkt POS-Hardware zugreifen oder offline in einem Bundesland arbeiten.

### <a name="store-deployment-considerations"></a>Shopbereitstellungsüberlegungen

Neben einer Plattform und einem Formularfaktor müssen Einzelhändler eine Bereitstellungsoption auch im Unternehmen auswählen. Die folgenden Tabelle zeigt die Konfiguration, die für jede POS-Option verfügbar ist.

| POS-Bewerbung         | Commerce Scale Unit | Verfügbar offline |
|-------------------------|---------------|-------------------|
| MPOS für Windows        | Cloud oder RSSU | Ja               |
| MPOS für iOS oder Android | Cloud oder RSSU | Nein                |
| Cloud POS               | Cloud oder RSSU | Nein                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Die Commerce Scale Unit ist eine Komponente, die das CRT hostet. Das gesamte CRT enthält die Geschäftslogik, die vom POS verwendet wird und es bietet Zugriff auf die Kanaldatenbank. Sobald sie online ist, nutzen alle POS-Kunden im Shop die Commerce Scale Unit. Die Commerce Scale Unit kann entweder in der Cloud oder im Shop bereitgestellt werden.

#### <a name="offline-mode"></a>Offlinemodus

MPOS für Windows unterstützt Offline-Modus. Im Offline-Modus kann der POS weiter Verkäufe verarbeiten, selbst wenn er von der Commerce Scale Unit getrennt ist. Sie kann mit der Kanaldatenbank dann synchronisiert werden, sofern die Konnektivität zurückgesetzt wird. MPOS verwendet eine eigene eingebettete Instanz des CRT und verwendet vorübergehend eine eigene lokale Datenquelle (offline SQL Server-Datenbank). Weitere Informationen finden Sie unter [POS Offline-Funktionalität](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>POS-Peripheriegeräte-/-Hardwareüberlegungen

Einzelhändler müssen auch entscheiden, wie der POS auf Geräte wie Drucker, Bargeldladen und Zahlungsterminals zugreift. Nur MPOS für Windows unterstützt direkte Kommunikation mit diesen Geräten. MPOS für Windows Phone, IOS oder Android und Cloud POS benötigen eine Hardwarestation, um auf diese Geräte zuzugreifen. Hardwarestationen können einem POS-Register zugewiesen werden oder unter den Kassen in einer Filiale verwendet werden. Weitere Informationen dazu, wie die Hardwarestation installiert wird, finden Sie unter [Retail-Hardwarestation-Konfiguration und -Installation](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Implementierungsüberlegungen

Berücksichtigen Sie die folgenden Informationen, wie Sie die POS-Implementierung in den Ladengeschäften planen:

- **Funktionsanforderungen** – Die Kerngeschäftsprozesse und - funktionen sind gleich, unabhängig von der Plattform, dem Forularfaktor oder der Bereitstellungstopologie. Daher müssen Einzelhändler die meisten Funktionsanforderungen nicht berücksichtigten, wenn sie ihre Implementierung planen.
- **Konnektivität** - Netzwerkverfügbarkeit (Fernnetz \[WAN\] und lokale Netzwerke \[LAN\]) ist der größte Faktor, der vorsichtige Überlegung voraussetzt. Sämtliche Vorteile, die ein Null-Bedarf, Cloud-gehostete Lösung in Bezug auf Kosten- und Einfachheit bringt, ist verloren, wenn das System nicht für unternehmenswichtige Prozesse verfügbar ist.

    Sofern die Konnektivität für ein gegebenes Gerät sehr zuverlässig und elastisch ist oder wenn ein bestimmter Betrag von Ausfallzeiten für den Einzelhändler akzeptabel ist, wird eine der folgenden Optionen empfohlen:

    - Verwenden Sie MPOS in Windows, und ermöglichen Sie den Offline-Modus.
    - Stellen Sie eine lokale Commerce Scale Unit bereit.

    Diese beiden Optionen sind nicht einheitlich exklusiv. Für die zuverlässigste Topologie, können Einzelhändler eine lokale RSSU bereitstellen, um die Abhängigkeit für die Internet-Konnektivität oder Azure-Verfügbarkeit zu reduzieren, und sie können auch POS-Register bereitstellen, in denen der Offline-Modus aktiviert wird, wenn ein Problem mit dem lokalen Server oder im Netzwerk vorhanden ist.

- **Hardwaregeräte/Peripheriegeräte** – Ein wichtiger Aspekt eines Retail POS-Systems ist die Möglichkeit, Drucker, Geldladen und Zahlungsterminals zu verwenden. Obwohl alle verfügbaren POS-Optionen Peripheriegeräte verwenden, können nur MPOS für Windows diese direkt unterstützen. Bei allen anderen Anwendungen ist eine oder mehrere Hardwarestationen erforderlich. Obwohl dieser Ansatz Flexibilität hinzufügt, müssen zusätzliche Komponenten bereitgestellt, konfiguriert und verwaltet werden.
- **Systemanforderungen** – Die Systemanforderungen für die POS-Anwendung unterscheiden sich. Stellen Sie sicher, die neuesten Informationen zu überprüfen, bevor Sie Ihre Auswahl treffen. Weil CPOS beispielsweise in einen Browser ausgeführt wird, unterstützt sie einen breiteren Bereich von Betriebssystemen. Weitere Informationen zu den Systemanforderungen finden Sie unter [Systemanforderungen für Cloud-Bereitstellung](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Bereitstellung und Verwalten** – Die Komplexität der Bereitstellung und Wartungsanforderungen kann unterschiedlich sein, abhängig von der Anwendungen und der Bereitstellungs-Auswahlen. Beispiel für eine Cloud-gehostete CPOS-Bereitstellung ist, dass Sie nicht jedes Gerät installieren und aktualisieren müssen. Daher verringert dieser Ansatz Komplexität und Kosten. Wenn Sie jedoch MPOS für jedes Register bereitstellen und den Offline-Modus aktivieren, und Sie auch geteilte Hardware-Stationen bereitstellen, erhöhen Sie die Anzahl von Endpunkten, die verwaltet werden müssen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]