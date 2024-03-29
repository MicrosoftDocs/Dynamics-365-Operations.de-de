---
title: URL in POS öffnen
description: Dieser Artikel bietet einen Überblick über die Verbesserungen der Produkt- und Debitorensuchfunktion in Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.custom: 141393
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ad82cf1039515e58d1717453ee3fb4e3dafd84fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276426"
---
# <a name="open-url-in-pos"></a>URL in POS öffnen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine Schaltfläche in der Dynamics 365 Commerce-Verkaufsstelle (POS) konfigurieren, um eine URL zu öffnen. Diese Funktion erfordert keine Codeanpassung und kann von jemandem in einer Nicht-Entwickler-Rolle konfiguriert werden. 

Diese Funktion ermöglicht die Konfiguration einer Schaltfläche in POS mithilfe des Raster-Designers, um eine URL zu öffnen. Aktuell wird diese in den folgenden Konfigurationen unterstützt:

- In neuem Fenster öffnen.
- Innerhalb von POS öffnen.
- Eine native App öffnen.

## <a name="open-in-new-window"></a>In neuem Fenster öffnen

Diese Konfiguration definiert, ob die URL in einem neuen Fenster oder innerhalb der App geöffnet werden soll. Wenn so konfiguriert wird, dass eine Web-URL innerhalb der App geöffnet wird, sind der Seitennavigationsbereich und der obere Balken der POS sichtbar und stehen zur Benutzerinteraktion zur Verfügung. Wenn so konfiguriert wird, dass in einem neuen Fenster geöffnet wird, wird die URL in einem neuen App-Fenster in Modern POS für Windows geöffnet und in einer neuen Browserregisterkarte in allen anderen POS-Clients. Um dies zu ermöglichen, müssen Sie die URL unter Auswahl der Option **In neuem Fenster öffnen** konfigurieren.

## <a name="open-within-pos"></a>Innerhalb von POS öffnen

Das Öffnen einer Web-URL innerhalb von POS wird aktuell nur für Modern POS in Windows unterstützt. In anderen Clients ist diese Fähigkeit in Entwicklung und für zukünftige Updates geplant. Um dies zu ermöglichen, müssen Sie die URL ohne Auswahl der Option **In neuem Fenster öffnen** konfigurieren.

## <a name="open-a-native-app"></a>Eine native App öffnen

Diese Funktion ermöglicht zudem, Nicht-Web-URLs anzugeben, um eine native App zu öffnen. Beispielsweise können Sie URL-Protokolle wie beispielsweise MailTo, SIP, Sofortnachricht oder MSTEAMS angeben, die dann von jeweiligen nativen Apps im Hostgerät gehandhabt werden können. Um dies zu ermöglichen, müssen Sie die URL unter Auswahl der Option **In neuem Fenster öffnen** konfigurieren.

- Zu Windows-Computern sehen Sie [Standardanwendungszuordnungen exportieren oder importieren](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), um die Standardprotokollzuordnungen festzulegen, wenn Sie Ihren Computer mithilfe von Abbildverwaltung für die Bereitstellung (DISM) einrichten.
- Wenn Sie MDM verwenden, wie Intune, um Ihre Windows-Computer zu verwalten, finden Sie Informationen unter [Richtlinien-CSP – ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Wenn Sie ein Entwickler sind, der eine benutzerdefinierte Website erstellt, finden Sie Informationen unter [Die Standard-App für eine URI starten](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Eine native App problemlos öffnen

Windows, iOS und Android ermöglichen auch das problemlosere Öffnen von Apps, basierend auf der App-Protokollzuordnung. Wenn Ihre App nicht bereits dazu konfiguriert ist, das Öffnen von einem Webbrowser aus zu handhaben, benötigen Sie möglicherweise einen Entwickler, um dies zu konfigurieren.

- Für Windows sehen Sie Informationen unter [Aktivieren von Apps für Websites mithilfe von App-URI-Handlern](/windows/uwp/launch-resume/web-to-app-linking).
- Für IOS finden Sie Informationen unter [Universelle Links für Entwickler](https://developer.apple.com/ios/universal-links/).
- Für Android finden Sie Informationen unter [Handhabung von Android-App-Links](https://developer.android.com/training/app-links/).

| Kunde                | In neuem Fenster öffnen | Native App öffnen | Innerhalb von POS öffnen | Detaildaten                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Modern POS auf Windows | ✓\*                | ✓               | ✓              | \* Wird in neuem „Modern POS”-Fenster geöffnet |
| Cloud POS             | ✓\*                | ✓               | X              | \* Wird in neuer Browserregisterkarte geöffnet        |
| Modern POS auf iOS     | ✓\*                | ✓               | X              | \* Wird in neuer Browserregisterkarte geöffnet        |
| Modern POS auf Android | ✓\*                | ✓               | X              | \* Wird in neuer Browserregisterkarte geöffnet        |

## <a name="before-you-begin"></a>Bevor Sie beginnen

Bevor Sie beginnen, überprüfen Sie, wie [Bildschirmlayouts für die Verkaufsstelle (POS)](pos-screen-layouts.md) konfiguriert werden.

## <a name="open-url-in-pos"></a>URL in POS öffnen

Um eine URL zu konfigurieren, die in POS geöffnet werden soll, führen Sie die folgenden Schritte aus.

1. Wechseln Sie in der Zentrale zu **Einzelhandel und Handel \> Kanaleinstellungen \> POS-Einstellungen \> POS \> Bildschirmlayouts**.
2. Wählen Sie **Schaltflächenraster \> Designer** aus.
3. Erstellen Sie eine neue Schaltfläche.
4. Wählen Sie die Eigenschaften **Schaltfläche** aus.
5. Wählen Sie **URL öffnen** als die Aktivität aus.
6. Geben Sie die URL ein, die Sie verwenden möchten.
7. Konfigurieren Sie, ob die URL in einem neuen Fenster geöffnet werden soll.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
