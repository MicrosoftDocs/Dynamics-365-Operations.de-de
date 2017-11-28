---
title: "Konfigurieren von Bildschirmlayouts für POS"
description: "Dieses Thema enthält Informationen zu Bildschirmlayouts für Microsoft Dynamics 365 for Retail-POS-Erfahrungen."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad425ab0848ab04003b7378cb5c488650f01c441
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurieren von Bildschirmlayouts für POS

[!include[banner](includes/banner.md)]


Dieses Thema enthält Informationen zu Bildschirmlayouts für Microsoft Dynamics 365 for Retail-POS-Erfahrungen.

Die Microsoft Dynamics 365 for Retail-POS-Benutzeroberfläche kann mithilfe einer Kombination von visuellen Profilen und Bildschirmlayouts konfiguriert werden und zu Shops, Kassen und/oder den Benutzern zugewiesen werden.

## <a name="visual-profile"></a>Visuelles Profil
Visuelle Profile werden für die Kassen zugewiesen und werden verwendet, um die Sichtelementen anzugeben, die kassenspezifisch sind und gemeinsam genutzt werden. Jeder Benutzer, der sich an der Kasse anmeldet, hat dasselbe Thema, Farben und Bilder. 

**Profilnummer** Die eindeutige Kennung für das visuelle Profil. 

**Beschreibung** - Die Beschreibung ermöglicht es Ihnen, einen beschreibenden Namen angeben, der unterstützt, das richtige Profil für in Ihrer Situation zu identifizieren.

**Thema** - Benutzer können zwischen den hellen oder dunklen Anwendungsdesigns auswählen. Diese Einstellungen wirken sich auf die gewünschten Schrift- und Hintergrundfarben der App aus.

**Akzentfarbe** - Die Akzentfarbe wird im POS verwendet, um bestimmte Sichtelemente wie Kacheln, Befehlsschaltflächen oder Links zu unterscheiden oder hervorzuheben. Diese Elemente sind in der Regel aktiv.

**Kopffarbe** - Die Kopffarbe ermöglicht dem Benutzer, die Farbe der Kopfzeile zu konfigurieren, um die Brandingbedürfnisse des Einzelhändlers zu erfüllen. Diese Funktion ist nur in Microsoft Dynamics 365 for Retail, Version 1611, verfügbar.

**Anmeldung Hintergründe** - Benutzer können ein Hintergrundbild für die Bildschirm Anmeldung angeben. Die Dateigröße von Hintergrundbildern sollte so gering wie möglich gehalten werden, da das Speichern und Hochladen großer Dateien Auswirkungen auf Das Anwendungsverhalten und -Leistung haben kann.

**Anwendungshintergrund**- Das Bild kann ein als Hintergrund in der gesamten Anwendung anstelle der ausgefüllten Themaenfarbe auch verwenden. Wie bei den Anmeldung Hintergründen ist es ratsam, es so klein wie möglich zu halten.

## <a name="screen-layouts"></a>Bildschirmlayouts
Bildschirmlayoutkonfiguration bestimmt die Aktivitäten, Inhalte und die Platzierung von Benutzeroberflächen-Steuerelementen im POS-Begrüßungsbildschirm- und -Buchungsbildschirm. 

**Begrüßungsbildschirm**- In den meisten Fällen ist der Begrüßungsbildschirm die Seite, die den Benutzern angezeigt werden, wenn sie sich in POS anmelden. Der Begrüßungsbildschirm kann einem aus Branding bild und -Schaltflächenrastern bestehen, die Zugriff auf POS-Arbeitsgängen bilden. In der Regel werden Arbeitsgänge, die nicht für die aktuellen Buchung bestimmt sind, hier platziert. 

**Buchungsbildschirm** - Der Buchungsbildschirm ist der Hauptbildschirm in POS zur Verarbeitung von Verkaufsbuchungen und Aufträgen. Der Buchungsbildschirm kann mithilfe des Bildschirmlayoutdesigners konfiguriert werden. 

**Standardanfangsbildschirm** - Einige Einzelhändler bevorzugen, dass der Kassierer direkt an den Buchungsbildschirm navigieren, nachdem er angemeldet hat. Die Standardanfangsbildschirmeinstellung ermöglicht Benutzern dieses für jedes Bildschirmlayout festzulegen.

### <a name="assignment"></a>Zuweisung

Bildschirmlayouts können Unternehmen, Kassen oder Benutzern zugeweisen werden. Die Benutzer-Zuweisung setzt die Kassen- und Shopzuweisung außer kraft, und die Kassen-Zuweisung setzt die Shopzuweisung außer kraft. In einem einfachen Szenario, wo alle Benutzer das gleiche Layout unabhängig von der Kasse oder Rolle verwenden, kann das Bildschirmlayout nur für den Shop festgelegt werden. In Fällen, in denen bestimmten Kassen oder Benutzer spezielle Layouts erfordern, können sie ihnen zugeordnet werden.

### <a name="layout-sizes"></a>Layoutgrößen

Diese Funktion ist nur in Microsoft Dynamics 365 for Retail, Version 1611, verfügbar. Da in vielen Fällen Bildschirmlayouts zu mehreren Bildgrößen und -auflösungen verwendet werden können, können Benutzer das Layout und Inhalt für jedes konfigurieren. Die POS-Anwendung wählt automatisch die nähste Layoutgröße für das Gerät zum Zeitpunkt des Starts aus. Ein Bildschirmlayout kann die Konfigurationen von Komplett- und Kompaktgeräten angeben. Diese Konfiguration ermöglicht ein einzelnes Bildschirmlayout zu einem Benutzer zuzuordnen, der mit verschiedene Größen und Formularfaktoren im Shop arbeitet. 

**Modern POS - Vollständig** - Vollständige Layouts werden verwendet für große PC-Bildschirme oder Tablets. Benutzer können auswählen, welche Benutzeroberflächenelemente einzuschließen sind, deren Größe oder Platzierung bestimmen, und der detaillierten Eigenschaften konfigurieren. Vollständige Layouts unterstützen Hochformat- und Querformatkonfigurationen. 

**Modern POS - Kompakt** - Kompakte Layouts werden verwendet für kleine Telefone oder Tablets. Designmöglichkeiten werden für kompakte Geräte beschränkt. Benutzer können die Spalten und Felder für den Zugriff und summenbereiche konfigurieren.

### <a name="screen-layout-designer"></a>Designer für Bildschirmlayout

Jede Layoutgröße innerhalb eines Bildschirmlayouts muss mithilfe des Bildschirmlayoutdesigners konfiguriert werden. Mit dem Designer können Benutzern Benutzeroberflächenelementen des Buchungsbildschirms angeben und konfigurieren. Der Bildschirmlayoutdesigner verwendet ClickOnce, um die neueste Version der Anwendung herunterzuladen (bei jedem Start). Stellen Sie sicher, dass die Browseranforderungen für die Verwendung ClickOnce erfüllt sind. Einige Browser, z.B. Chrome, benötigen Erweiterungen. 

**Nummerpad** - Das Nummerpad ist die Hauptbenutzereingabe im POS-Buchungs-Bildschirm. Es kann so konfiguriert werden, dass das gesamte Pad auf dem Bildschirm für Touchscreen sichtbar ist, oder nur das Eingabefeld anzuzeigen, das einer physischen Tastatur verwendet werden kann. Die Nummerpadeinstellungen sind nur im vollständigen Layout verfügbar. In Dynamics 365 for Retail, Version 1611, können kompakte Layouts immer das vollständige Nummernpad nutzen, das über den Buchungsbildschirm verfügbar ist.

**Gesamtbereich** - Der Gesamtbereich kann anschließend in eine ein oder zwei Spalten so konfiguriert werden, dass Zeilenzähl-Felder wie Rabattbetrag, Gebühren, Steuern Zwischensumme und anzuzeigen. In Microsoft Dynamics 365 for Retail, Version 1611, unterstützen kompakte Layouts nur eine einzelne Gesamtspalte. 

**Empfang** - Der Empfangsbereich enthält die Verkaufspositionen, die Zahlungspositionen und die Lieferinformationen für die Produkte und Dienste, die am POS verarbeitet werden. Benutzer können Spalten, Breite und Position angeben. In den kompakten Layouts in Dynamics 365 for Retail, Version 1611, können Sie auch zusätzliche Informationen konfigurieren, die in der Zeile unter der Hauptposition angezeigt wird. 

**Kundenkarte** - Die Kundenkarte zeigt Informationen bezüglich des Kunden an, der momentan der Buchung zugeordnet ist. Die Kundenkarte kann so konfiguriert werden, um zusätzliche Informationen anzuzeigen oder auszublenden. 

**Registerkartensteuerelement** – Das Registerkartensteuerelement kann auf das Bildschirmlayout platziert werden, und andere Steuerelemente wie Nummernpad, Kundenkarte oder Schaltflächenraster können innerhalb der Registerkarte platziert werden. Das Registerkartensteuerelement ist ein Container, mit dem der Benutzer mehr Inhalte auf dem Bildschirm unterbringen kann. Das Registerkartensteuerelement ist für vollständige Layouts nur verfügbar. 

**Bild**- Die Bildsteuerung kann verwendet werden, um das Shoplogo oder anderes Brandingbilder im Buchungsbildschirm anzuzeigen. Das Bildsteuerelement ist für vollständige Layouts nur verfügbar. 

**Empfohlene Produkte** - Sofern für die Umgebung konfiguriert, wird das Produktsteuerelement empfohlene Produktvorschläge auf Grundlage von Machine-Learning-Daten angezeigt. Das empfohlene Produktsteuerelement ist nur für vollständige Layouts in Dynamics 365 for Retail, Version 1611, verfügbar. ** Benuterdefiniertes Steuerelement ** - Das benutzerdefinierte Steuerlelement dient als Platzhalter innerhalb des Bildschirmlayouts das die Platzierung von benutzerdefinierten Inhalten zulässt. Das benutzerdefinierte Steuerelement ist für vollständige Layouts nur verfügbar.

<a name="see-also"></a>Siehe auch
--------

[Einrichten von Retail POS-Layoutdesigner](install-pos-layout-designer.md)




