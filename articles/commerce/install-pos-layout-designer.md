---
title: POS-Layoutdesigner installieren
description: Sie können den One-Click-Designer verwenden, um unterschiedliche Modern POS (MPOS) und Cloud POS Layouts entweder im Querformat oder im Hochformat, für Shops, Kassen, Kassierer und Vorgesetzte zu entwerfen.
author: athinesh99
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7ac1495f12a51d72a90ad88fc2d8e0a574418467
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345133"
---
# <a name="install-the-pos-layout-designer"></a>POS-Layoutdesigner installieren

[!include [banner](includes/banner.md)]

Sie können den One-Click-Designer verwenden, um unterschiedliche Modern POS (MPOS) und Cloud POS Layouts entweder im Querformat oder im Hochformat, für Shops, Kassen, Kassierer und Vorgesetzte zu entwerfen.

Der grafische Entwurf der Schnittstelle für MPOS oder Cloud-POS wird durch das Kassenlayout gesteuert. Ein Layout bestimmt die Position der verschiedenen Objekte. Beispiele sind Gesamtlayout, Layout für Artikelraster, Debitorenlayout und Zahlungslayout sowie das Layout von verschiedenen Menüschaltflächen. Layouts beinhalten auch die allgemeine Darstellung der Verkaufsschnittstelle, die den Mitarbeitern präsentiert wird.

## <a name="install-the-one-click-designer"></a>Installieren Sie den One-Click-Designer

1. Verwenden Sie in Commerce das Menü oben links, um zu **Einzelhandel und Commerce** &gt; **Kanaleinstellung** &gt; **POS-Einstellung** &gt; **POS** &gt; **Bildschirmlayouts** zu navigieren.
2. Wählen Sie ein beliebiges Layout, das einen Bewerbungstyp aus **Modern POS for Windows** oder **Cloud POS** hat und klicken Sie dann auf **Layout Designer**.
3. Klicken Sie auf der Benachrichtigungsleiste, die unten im Internet Explorer-Fenster angezeigt wird, auf **Öffnen**, um den Ein-Klick-Designer zu installieren. (Die Benachrichtigungsleiste wird möglicherweise in anderen Browsern an einer anderen Stelle angezeigt.)
4. Im Meldungsfeld **Anwendung ausführen - Sicherheitswarnung**, das angezeigt wird, klicken Sie auf **Ausführen**, um den Einzelhandel-Designerhost einzurichten. In der Statusleiste wird der Status des Installationsvorgangs angezeigt.
5. Nachdem die Installation abgeschlossen ist, geben Sie auf der Seite **Anmelden** den Commerce Benutzernamen und das Kennwort ein, und klicken Sie auf **Anmelden**, um den Designer zu starten.
6. Nachdem die Anmeldeinformationen validiert und der Designer gestartet wurde, können Sie damit beginnen, Ihr eigenes Layout zu entwerfen oder ein vorhandenes Layout zu ändern.

    [![Layout im One-Click Designer.](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Lösen Sie Probleme bei der Installation des Layoutdesigners

- Wenn Sie auf **Designer** klicken, erscheint die entsprechende Meldung, um das Installationsprogramm herunterzuladen (oder auszuführen) nicht oder Ihre aktuellen Sicherheitseinstellungen lassen kein Herunterladen der Datei zu. 

    **Lösungen:**

    - Stellen Sie im Internet Explorer sicher, dass die Popupblocker für diese Site deaktiviert sind. Klicken Sie auf **Einstellungen** &gt; **Optionen** &gt; **Datenschutz** &gt; **Popupblocker** suchen und ändern Sie die Einstellung, wenn eine Änderung erforderlich ist.
    - Fügen Sie in Internet Explorer die Commerce-URL zu den vertrauenswürdigen Sites hinzu. Klicken Sie auf **Einstellungen** &gt; **Optionen** &gt; **Sicherheit** &gt; **Vertrauenswürdige Standorte** &gt; **Standorte** &gt; **Hinzufügen**..

- Das Programm startet nicht und Sie werden aufgefordert, sich mit dem Kreditor in Verbindung zu setzen.

    **Lösung:** Fügen Sie in Internet Explorer die Commerce-URL zu den vertrauenswürdigen Sites hinzu. Klicken Sie auf **Einstellungen** &gt; **Optionen** &gt; **Sicherheit** &gt; **Vertrauenswürdige Standorte** &gt; **Standorte** &gt; **Hinzufügen**..

**Bekanntes Problem:** Der Designer funktioniert nicht ordnungsgemäß in Google Chrome- und Mozilla Firefox-Browsern. Wir sind daran, dieses Problem zu beheben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Konfigurieren, Installieren und Aktivieren von Retail Modern POS (MPOS)](retail-modern-pos-device-activation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]