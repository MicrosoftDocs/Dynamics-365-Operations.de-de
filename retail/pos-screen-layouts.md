---
title: "Konfigurieren Sie Bildschirmlayouts für POS"
description: "Dieses Thema enthält Informationen zu Bildschirmlayouts für das Microsoft Dynamics 365 für Arbeitsgänge - Kleinverkaufsstelle (POS)- Erfahrungen bereit."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurieren Sie Bildschirmlayouts für POS

Dieses Thema enthält Informationen zu Bildschirmlayouts für das Microsoft Dynamics 365 für Arbeitsgänge - Kleinverkaufsstelle (POS)- Erfahrungen bereit.

Das Microsoft Dynamics 365 für Arbeitsgänge Kleinverkaufsstelle (POS)- - Benutzeroberfläche kann mithilfe einer Kombination von visuellen Profilen und von Bildschirmlayouts konfiguriert werden, werden den Shops zugewiesen, den Kassen und/oder den Benutzer.

## <a name="visual-profile"></a>Visuelles Profil
Visuelle Profile werden für die Register zugewiesen und werden verwendet, um den Sichtelementen anzugeben, die Registerbesondere sind und freigegeben zu Benutzern. Jeder Benutzer, der in das Register protokolliert hat, dasselbe Thema, Farben und Bilder. ** Profilnummer ** Profilnummer - Die eindeutige Kennung ist der für das visuelle Profil. ** ** Beschreibung - Die Beschreibung ermöglicht es Ihnen, einen beschreibenden Namen angeben, der unterstützt, das richtige Profil für in Ihrer Situation zu identifizieren. ** Thema ** - Benutzer kann zwischen den hellen oder dunklen Bewerbungsthemen auswählen. Diese Einstellungen sich die gewünschten Schrift- und Hintergrundfarben während der Zeit-App aus. ** Akzentfarbe ** - Die Akzentfarbe werden während des POS verwendet, um bestimmte Sichtelemente wie Kacheln, Befehlsschaltflächen oder Links zu unterscheiden oder hervorzuheben. Diese Elemente sind in der Regel verklagbar. ** Kopffarbe ** - Die Kopffarbe ermöglicht dem Benutzer, um die Farbe der Kopfzeile zu konfigurieren, um die Brandingbedürfnisse des Einzelhändlers zu erfüllen. Diese Funktion ist in Dynamics 365 für Arbeitsgangsversion 1611 nur verfügbar. ** Anmeldung Hintergründe ** - Benutzer können ein Hintergrundbild für den Bildschirm Anmeldung angeben. Die Dateigröße von Hintergrundbildern sollte so gering wie möglich gehalten werden, als, Speichern und Hochladen großer Dateien Auswirkungen auf den Bewerbungsverhalten und -Leistung haben kann. ** Anwendungshintergrund ** POS - Das Bild kann ein als Hintergrund in der gesamten Anwendung anstelle der ausgefüllten Themaenfarbe auch verwenden. Wie bei der Anmeldung Hintergründen, es wird darüber informiert, um die zulässige Mindest- beizubehalten, so wie möglich.

## <a name="screen-layouts"></a>Bildschirmlayouts
Bildschirmlayoutkonfiguration bestimmt die Aktivitäten, Inhalts- und die Platzierung von Benutzeroberflächen-Kontrollen im POS-Begrüßungsbildschirm- und -Buchungsbildschirm. ** Begrüßungsbildschirm ** - in den meisten Fällen ist der Begrüßungsbildschirm die Seite, den Benutzer angezeigt werden, wenn sie zuerst in POS sperren</b> protokollieren. Der Begrüßungsbildschirm kann einem aus Branding bild und -Schaltflächenrastern bestehen, die Zugriff auf POS-Arbeitsgängen bilden. In der Regel werden Arbeitsgänge, die nicht mit der aktuellen Buchung bestimmt sind hier, erteilt. ** Buchungsbildschirm ** - Der ist der Buchungsbildschirm Hauptbildschirm in POS zur Verarbeitung von Verkaufsbuchungen und Aufträgen. Der Buchungsbildschirm kann mithilfe des Bildschirmlayoutdesigners konfiguriert werden. ** Standardanfangsbildschirm ** - Einige Banken bevorzugen Einzelhändler, dass der Kassierer direkt an den Buchungsbildschirm navigieren, nachdem er angemeldet hat. Die Standardanfangsbildschirmeinstellung ermöglicht Benutzern gestattet, dieses für jedes Bildschirmlayout festzulegen.

### <a name="assignment"></a>Zuweisung

Bildschirmlayouts können im Unternehmen zugewiesen werden, Register oder Benutzerebene. Die Benutzer-Zuweisung setzt die Register- und Filialzuweisung, und die Register-Zuweisung setzt die Filialzuweisung. In einem einfachen Szenario, wo alle Benutzer das gleiche Layout unabhängig davon Register oder Rolle verwenden, kann das Bildschirmlayout nur in Ihrem Unternehmen festgelegt werden. In denen auf bestimmten Registern oder Benutzer spezielle Layouts erfordern, können sie zum zugeordnet werden.

### <a name="layout-sizes"></a>Layoutgrößen

Diese Funktion kommt nur auf Dynamics 365 für Arbeitsgangsversion 1611 zu. Da in vielen Fällen Bildschirmlayouts zu mehreren Bildumfang und Lösungen verwendet werden können, können Benutzer das Layout und Inhalt für jedes konfigurieren. Die POS-Bewerbung wählt automatisch die nähste Layoutgröße für das Gerät zum Zeitpunkt des Starts aus. Ein Bildschirmlayout kann für Konfigurationen vollständiger und Vertragsgeräte angeben. Diese Konfiguration ermöglicht einen einzelnem Bildschirmlayout zuzuordnenden Benutzer, das Arbeiten über verschiedene Größen und Formularfaktoren in der Filiale. ** Modernes POS - Voll ** - Voll Layouts ist verwendet für wie PC-Bildschirme größere Anzeigen oder -Tablets normalerweise die. Benutzer können auswählen, die die Benutzeroberflächen dem elemente einzuschließen, deren Größe oder Platzierung zu bestimmen, und der detaillierten Eigenschaften zu konfigurieren. Vollständige Layouts unterstützen Hochformat- und Querformatkonfigurationen. ** Modernes POS - Vertrag ** - kompakte Layouts ist verwendet für kleine Telefone oder Tablets normalerweise die. Designmöglichkeiten werden für kompakte Geräte beschränkt. Benutzer können die Spalten den Feldern und für den Zugriff konfiguriert summiert und Bereiche auf.

### <a name="screen-layout-designer"></a>Designer für Bildschirmlayout

Jede Layoutgröße innerhalb eines Bildschirmlayouts muss mithilfe des Bildschirmlayoutdesigners konfiguriert werden. Der Designer können Benutzern, um den Benutzeroberflächenelementen des Buchungsbildschirms anzugeben und zu konfigurieren. Der Bildschirmlayoutdesigner verwendet ClickOnce, um die neueste Version der Anwendung herunterzuladen, und jedes Mal zu starten die Benutzer Zugriffe es. Stellen Sie sicher, Browseranforderungen für die Verwendung ClickOnce-einiger Browser, z Chrome sicherzustellen, benötigen Sie Erweiterungen. ** Nummerauflage ** - Die Nummerauflage ist die Hauptbenutzereingabe im POS-Buchungs-Bildschirm. Sie kann so konfiguriert werden, dass die gesamte Auflage, die auf dem Bildschirm für Touchscreen ideal ist, oder nur das Eingabefeld anzuzeigen, das einer physischen Tastatur verwendet werden kann. Die Nummerauflageneinstellungen sind nur im vollständigen Layout verfügbar. In Dynamics 365 für Arbeitsgangsversion 1611, können kompakte Layouts immer die vollständige Nummerauflage, die vom Buchungsbildschirm verfügbar ist. ** Gesamtbereich ** - Der Gesamtbereich kann anschließend in eine ein oder zwei Spalten so konfiguriert werden, dass Zeilenzähl- Felder wie, Rabattbetrag, Gebühren, Steuern Zwischensumme und anzuzeigen. In Dynamics 365 für Arbeitsgangsversion 1611 unterstützen, kompakte Layouts nur eine einzelne Gesamtspalte. ** ** Zugang - ** ** der Zugangsbereich enthält die Verkaufspositionen, die Zahlungspositionen und die Lieferinformationen für die Produkte und Dienste, die am Point-of-Sale verarbeitet werden. Benutzer können Spalten, Breite und Position angeben. In den kompakten Layouts in Dynamics 365 für Arbeitsgangsversion 1611, können Sie zusätzliche Informationen auch mit dem konfigurieren, die in der Zeile mit der Hauptlinie wird. ** Debitorenkarte ** - Die Debitorenkarte zeigt Informationen bezüglich des Debitors angezeigt, der momentan der Buchung zugeordnet ist. Die Debitorenkarte kann so konfiguriert werden, um zusätzliche Informationen anzuzeigen oder auszublenden. ** Registerkartensteuerelement ** - das Registerkartensteuerelement kann auf das Bildschirmlayout erteilt werden, und andere Steuerelemente wie die Nummerauflage, die Debitoren karte oder Die Schaltflächenraster können innerhalb der Registerkarte erteilt werden. Das Registerkartensteuerelement ist ein gültiger Container, die dieser Benutzer zufriedeneres im Bildschirm anpassen. Das Registerkartensteuerelement ist für vollständige Layouts nur verfügbar. ** Bild ** - Die Bildsteuerung kann verwendet werden, um das Shoplogo oder anderes Brandingbild im Feld Buchungsbildschirm anzuzeigen. Die Bildsteuerung ist für vollständige Layouts nur verfügbar. ** Empfohlene Produkte ** - sofern für die Umgebung konfiguriert ist, wird das Produktsteuerelement empfohlene Produktvorschläge auf Grundlage Lernfähigkeit einer Maschine angezeigt. Das empfohlene Produktsteuerelement ist für vollständige Layouts in Dynamics 365 für Arbeitsgangsversion 1611 nur verfügbar. ** Zollkontrolle ** - Die Zollkontrolle dient als Platzhalter ein, innerhalb des Bildschirmlayouts Benutzer zum Rücklage platz benutzerdefinierten Inhalt zulässt. Die Zollkontrolle ist für vollständige Layouts nur verfügbar.

<a name="see-also"></a>Siehe auch
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


