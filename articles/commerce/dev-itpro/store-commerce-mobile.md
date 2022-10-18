---
title: Store Commerce-App für mobile Plattformen
description: Dieser Artikel beschreibt die ersten Schritte mit der Store Commerce-App von Microsoft Dynamics 365 Commerce für Android und iOS.
author: stuharg
ms.date: 10/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: 1f07a130629863ebd9d036378436cf360e90ac26
ms.sourcegitcommit: 98231ff810f41f9fcdc6b536d87e453028aa6db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/07/2022
ms.locfileid: "9642339"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce-App für mobile Plattformen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die ersten Schritte mit den Store Commerce-Apps von Microsoft Dynamics 365 Commerce für Android und iOS.

Die mobilen Dynamics 365 Commerce-Apps für Android und iOS machen den Prozess der Bereitstellung voll ausgestatteter mobiler Verkaufsstellengeräte (POS-Geräte) für Ihre Einzelhandelsumgebung unkompliziert und einfach. Die mobilen Apps von Store Commerce bieten alle Funktionen und Vorteile der [Store Commerce-App für Windows](store-commerce.md) auf Telefon- und Tablet-Formfaktoren. Die mobilen Store Commerce-Apps können direkt aus den Apple- und Google Play-App-Stores installiert werden und erfordern nicht, dass ein Entwickler ein neues Anwendungspaket erstellt, um sie bereitzustellen oder zu aktualisieren. 

Die mobilen Store Commerce-Apps behalten die volle Funktionsparität mit aktuellen Retail-Hybrid-Apps bei. Darüber hinaus umfasst Store Commerce für iOS Unterstützung für eine dedizierte Hardwarestation, sodass iOS-Geräte mit vernetzten Zahlungsterminals, Belegdruckern und Kassenschubladen kommunizieren können, ohne dass eine gemeinsam genutzte Hardwarestation bereitgestellt werden muss. 

> [!IMPORTANT]
> Die Store Commerce-Apps für Windows, Android und iOS sind die nächste Generation von POS-Anwendungen für Dynamics 365 Commerce. Die aktuelle Modern POS (MPOS)-Anwendung und die [Retail-Hybrid-Apps](hybridapp.md) für Mobilgeräte werden im Oktober 2023 eingestellt. Microsoft empfiehlt, dass Sie Store Commerce oder Cloud POS (CPOS) für alle neuen POS-Bereitstellungen verwenden. Bestehende Kunden sollten eine Migration von der Retail-Hybrid-App zu Store Commerce planen. Weitere Informationen zum Zeitplan der Einstellung für MPOS und die Retail-Hybrid-Apps finden Sie unter [Modernisierung des Technologie-Stacks für Dynamics 365 Commerce im Geschäft](https://www.microsoft.com/download/details.aspx?id=103896). 

## <a name="app-architecture"></a>App-Architektur

Die mobilen Store Commerce-Apps verwenden dieselbe Topologie wie die Store Commerce-App für Windows, wenn sie im Hybridmodus bereitgestellt werden. Die mobilen Apps von Store Commerce sind Shell-Anwendungen, die CPOS direkt von der Commerce Scale Unit (CSU) rendern und über die CSU eine Verbindung zu Monitorloser Commerce und Commerce headquarters herstellen. Das Shell-Anwendungsmodell ermöglicht es Store Commerce-Apps, eine dedizierte Hardwarestation für die direkte Integration in ein Zahlungsterminal, einen Drucker, eine Kassenschublade und andere Peripheriegeräte zu unterstützen. Sie müssen keine gemeinsam genutzte Hardwarestation einrichten, um Hardwaregeräte zu verwenden. 

Um eine mobile Store Commerce-App zu aktualisieren, aktualisieren Sie einfach die CSU. Alle neuen POS-Funktionen und -Features werden automatisch von der App übernommen. Weitere Informationen zum Aktualisieren der CSU finden Sie unter [Anwenden von Updates und Erweiterungen auf Commerce Scale Unit (Cloud)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Die Shell-Apps werden über App Store-Updates gewartet. Wenn eine Nebenversion die allgemeine Verfügbarkeit (GA) erreicht, veröffentlicht Microsoft sie in den App Stores. Microsoft kann zwischen Nebenversionsupdates auch Patches veröffentlichen, um Fehlerbehebungen mit hoher Priorität zu veröffentlichen.

## <a name="prerequisites"></a>Voraussetzungen

Die mobilen Store Commerce-Apps erfordern Dynamics 365 Commerce, insbesondere Commerce headquarters und die CSU-Komponenten. In der folgenden Tabelle sind die Mindestversionen des Betriebssystems (OS) und der CSU aufgeführt, die für die mobilen Android- und iOS-Apps erforderlich sind. 

| Voraussetzung | Android      | iOS  |
| ------------ | ------------ | ---- |
| Betriebssystemversion   | 7.0          | 15.0 |
| CSU-Version  | 9.38.22266.8 | TBD  |

## <a name="install-the-app"></a>App installieren

Sie können die mobilen Apps von Store Commerce direkt aus dem Google Play Store oder dem Apple App Store installieren. 

- [Store Commerce-App für Android](https://aka.ms/storecommerceandroid)
- Store Commerce-App für iOS (bald verfügbar)

Die Android-App-Pakete (.apk) und die Apple-App-Pakete (.ipa) können auch aus der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services heruntergeladen werden. 

## <a name="device-and-register-setup"></a>Geräte- und Kasseneinrichtung

Bevor eine Kasse in den mobilen Apps von Store Commerce aktiviert werden kann, müssen Sie ein Gerät und eine Kasse in Commerce headquarters einrichten. Weitere Informationen finden Sie unter [Geräte und Kassen](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Geräteeinrichtung

Gehen Sie folgendermaßen vor, um ein neues Gerät zu erstellen und einzurichten.

1. Gehen Sie in Commerce headquarters zu **Einzelhandel und Handel \> Kanaleinstellungen \> POS-Einrichtung \> Geräte**. 
1. Erstellen Sie ein neues Gerät, und wählen Sie entweder **Modern POS – Android** oder **Modern POS – iOS** als Anwendungstyp, abhängig von der mobilen App, die Sie bereitstellen. 

    > [!NOTE] 
    > Die **Modern POS – Android**- und **Modern POS – iOS**-Anwendungstypen werden auch verwendet, um die aktuellen Hybrid-Apps für Android und iOS bereitzustellen. Nach der Einstellung von MPOS werden die Bezeichnungen für diese Anwendungstypen auf **Store Commerce – Android** und **Modern POS – iOS** aktualisiert. 

### <a name="register-setup"></a>Kasseneinrichtung

Sie können eine neue Kasse erstellen und sie mit dem von Ihnen erstellten Gerät verknüpfen oder eine vorhandene Kasse mit Ihrem neuen Gerät verknüpfen. Weitere Informationen zu Kassen finden Sie unter [Erstellen und verknüpfen von Kassen](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Bildschirmlayouteinrichtung

Wenn Sie ein Bildschirmlayout wiederverwenden, das in den Demodaten enthalten ist, die mit Ihrer Dynamics 365 Commerce-Lizenz bereitgestellt werden, wählt die Store Commerce App automatisch das enthaltene kompakte Layout, wenn die Bildschirmauflösung Ihres Geräts im Hochformat weniger als 480 &times; 853 Pixel beträgt. Wenn Sie jedoch ein Bildschirmlayout von Grund auf neu erstellen oder Ihr mobiles Gerät eine höhere Auflösung verwendet, als das kompakte Layout unterstützt, stellen Sie sicher, dass Sie eine Auflösung und zugehörige Schaltflächenraster erstellen, die für das Telefon oder Tablet geeignet sind, für das Sie bereitstellen möchten. Weitere Informationen zu Bildschirmlayoutkonfigurationen finden Sie unter [Visuelle Konfigurationen der POS-Benutzeroberfläche](../pos-screen-layouts.md). 

Nachdem Geräte und Kassen konfiguriert wurden, gehen Sie in Commerce headquarters zu **Einzelhandel und Handel \> Einzelhandel und Handel-ID \> Verteilungspläne**, und führen Sie die Kassenaugabe aus.

## <a name="activate-a-device"></a>Ein Gerät aktivieren

Führen Sie die folgenden Schritte aus, um ein Gerät in einer mobilen Store Commerce-App zu aktivieren.

1. Öffnen Sie die App auf dem mobilen Gerät.
1. Geben Sie die CPOS-URL ein, die Sie auf der Seite mit den Umgebungsdetails in Lifecycle Services oder auf der Seite **Kanalprofile** in Commerce headquarters finden (**Einzelhandel und Handel \> Kanaleinstellung \> Kanalprofile**).
1. Melden Sie sich mit den Anmeldedaten eines Mitarbeiters an, der die Berechtigung zum Verwalten von Geräten hat.
1. Wählen Sie das Geschäft aus, das mit der Kasse verknüpft ist, das Sie in Commerce headquarters erstellt oder wiederverwendet haben.
1. Wählen Sie die Kasse aus, die Sie dem Gerät zugeordnet haben, das Sie in Commerce headquarters erstellt haben.
1. Ihr Gerät sollte jetzt aktiviert sein. Sie können sich bei der Kasse anmelden, indem Sie die Bediener-ID und das Passwort eines Mitarbeiters verwenden, der dem von Ihnen ausgewählten Geschäft zugeordnet ist. 

Weitere Informationen zur Geräteaktivierung finden Sie unter [Aktivierung von Verkaufsstellengeräten (POS-Geräten)](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Featureparität mit Store Commerce für Windows

In der folgenden Tabelle werden die Funktionen der Store Commerce-App unter Windows, Android und iOS-Plattformen verglichen.

| Funktion                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Deditzierte Hardwarestation                                                            | Ja     | Ja     | Ja |
| Freigegebene Hardwarestation                                                               | Ja     | Ja     | Ja |
| Kommunikation mit vernetzten Peripheriegeräten (Zahlungsterminal, Drucker und Kassenschublade) | Ja     | Ja     | Ja |
| Peripheriegeräte für OLE für Verkaufsstellen (OPOS) über eine lokale Hardwarestation             | Ja     | Nein      | Nein  |
| Offlinemodus                                                                          | Ja     | Nein      | Nein  |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Store Commerce-App](store-commerce.md)

[Zwischen Store Commerce und Cloud POS auswählen](../mpos-or-cpos.md)

[Fehlerbehebung bei Einrichtungs- und Installationsproblemen von Store Commerce](../troubleshoot/store-commerce-setup-installation.md)
