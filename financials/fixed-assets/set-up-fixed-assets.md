---
title: Einstellungsanlagen
description: "Dieses Thema bietet einen Überblick über Anlagen-Moduleinstellung."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: dde8053df96d03c8c8e52fa6d2fdf7f74e95ec92
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fixed-assets"></a>Einstellungsanlagen

Dieses Thema bietet einen Überblick über Anlagen-Moduleinstellung.

<a name="overview"></a>Überblick
--------
Parameter steuern das allgemeine Verhalten in Anlagen.

Mit Anlagengruppen können Sie Ihre Anlagen gruppieren und Standardattribute für jede Anlage definieren, die einer Gruppe zugewiesen wird. Bücher werden Anlagengruppen zugewiesen. Bücher verfolgen den Finanzwert einer Anlage im Laufe der Zeit ändern, indem die Abschreibungskonfiguration verwenden, die im Abschreibungsprofil definiert wird.

Anlagen werden bei der Erstellung einer Gruppe zugeordnet. Standardmäßig werden die Bücher, die der Anlagengruppe zugeordnet sind, dann der Anlage zugeordnet. Bücher, die konfiguriert werden, um im Hauptbuch zu buchen, sind einem Buchungsprofil zugeordnet. Sachkonten werden die pro Buch im Buchungsprofil angegeben und verwendet, wenn Anlagenposten gebucht werden. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Abschreibungsprofile
Abschreibungsprofile sollten zuerst eingerichtet werden. Im Abschreibungsprofil konfigurieren Sie, wie der Wert einer Anlage im Laufe der Zeit abgeschrieben wird. Sie müssen die Abschreibungsmethode, das Abschreibungsjahr (Kalenderjahr oder Geschäftsjahr) und die Häufigkeit der Abschreibung festlegen.

## <a name="books"></a>Bücher
Nachdem Sie das Abschreibungsprofile erstellt haben, müssen Sie die erforderlichen Bücher für die Anlagen erstellen. Jedes Abschreibungsbuch verfolgt einen unabhängigen wertmäßigen Lebenszyklus einer Anlage. Bücher können konfiguriert werden, um zugehörige Buchungen im Hauptbuch zu buchen. Diese Konfiguration ist die Standardeinstellung, da sie in der Regel für Unternehmensrechnungslegung verwendet wird. Bücher, die nicht dem Hauptbuchbeitrag nur dem Anlagenuntergeordneten Sachkonto buchen und normalerweise für die Steuererklärung, verwendet werden soll.

Ein primäres Abschreibungsprofil wird jedem Buch zugewiesen. Bücher haben auch ein alternatives oder wechselbares Abschreibungsprofil, wenn diese Art des Profils anwendbar ist. Um das Anlagenbuch in den Abschreibungsausführungen automatisch einzubeziehen, müssen Sie die Option Berechnen der Abschreibung aktivieren. Wenn diese Option nicht für eine Anlage ausgewählt wird, übersprungen werden der Abschreibungsvorschlag die Anlage.

Sie können auch abgeleitete Bücher einrichten. Die angegebenen abgeleiteten Transaktionen werden als genaue Kopie der primären Transaktion in den abgeleiteten Büchern gebucht. Daher werden normalerweise die abgeleitete Buchungen für Anschaffungen und Abgänge und nicht für Abschreibungsbuchungen eingerichtet.

## <a name="fixed-asset-posting-profiles"></a>Anlagenbuchungsprofile
Nachdem das Buch eingerichtet wurde, können Sie das Buchungsprofil erstellen. Das Buchungsprofil muss nach Buch definiert werden, allerdings kann es auf einer detaillierteren Ebene definiert werden. Beispielsweise können Sie das Buchungsprofil für die Kombination eines Buchs und der Anlagengruppe oder sogar für ein einzelnes Anlagenbuch definieren. Standardmäßig werden die Sachkonten verwendet, die für Verwendung der Anlagenbuchungen definiert wurden.

Sie müssen zunächst die Sachkonten definieren, die während der Abgangsprozesse, Abgangsvertrieb und Abgangsausschüsse verwendet werden. Zum Zeitpunkt des Abgangs werden die Anlagenbuchungen, die zuvor gebucht wurden aus den ursprünglichen Konten storniert und die Nettobeträge werden in die entsprechenden Konten für Gewinne und Verluste für Anlagenbeseitigungen verschoben. Um sicherzustellen, dass Buchungen korrekt storniert werden, müssen Sie ein Kreditorenkonto für alle Buchungstypen, die in Ihrem Unternehmen verwendet werden, erstellen. Das "Hauptkonto" sollte das ursprüngliche Hauptkonto für diesen Transaktionstyp im Buchungsprofil sein, während das "Gegenkonto" das Gewinn- und Verlustkonto sein sollte. Die Ausnahme ist der Nettobuchwert. In diesem Fall sollten das Hauptkonto und das Gegenkonto in den Gewinn und Verlust für das  Abgangskonto festgelegt werden.

## <a name="fixed-asset-groups"></a>Anlagengruppen
Anlagengruppe ist das einzige Pflichtfeld, beim Erstellen einer Anlage. Der Wert dieses Felds bestimmt den Standardwert mehrerer Informationsfelder für die Anlage. Bücher werden eingerichtet, damit ein Standardbuch jeder Anlage einer Gruppe zugeordnet ist. Sie können Attribute für die Bücher dann festlegen, die spezifisch für eine Anlagengruppe sind, wie beispielsweise Nutzungsdauer und Abschreibungskonvention.

Sie können Sonderabschreibungsbeträge oder Bonusabschreibungen für eine bestimmte Kombination von festen Anlagengruppen und einem Buch definieren. Sie müssen eine Priorität für die Sonderabschreibung zuweisen, um die Reihenfolge anzugeben, in der die Zulagen berechnet werden, wenn mehrere Zulagen zu einem Buch zugewiesen werden.

## <a name="fixed-asset-parameters"></a>Anlagenparameter
Der letzte Schritt ist, das Aktualisieren der Anlagenparameter.

Das Feld Aktivierungsschwelle bestimmt die Anlagen, die abgeschrieben werden. Wenn eine Bestellposition als Anlage aktiviert, aber nicht den angegebenen Aktivierungsschwellenwert erreicht, ist eine Anlage noch erstellt oder aktualisiert, wobei die berechnensabschreibungsoption wird auf "Nein" festgelegt. Daher wird die Anlage nicht automatisch im Rahmen der Abschreibungsvorschläge abgeschrieben.

Eine wichtige Option ist Automatisch Abschreibungsregulierungsbeträge mit Abgang erstellen. Wenn Sie diese Option auf Ja festlegen, wird die Anlagenabschreibung automatisch angepasst, basierend auf den Abschreibungseinstellungen zum Zeitpunkt der Anlagenbeseitigung. Eine weitere Option ist es, Skonti von Ihrem Anschaffungsbetrag abzuziehen, wenn Sie Anlagen erwerben, indem Sie eine Kreditorenrechnung verwenden.

Im Inforegister Bestellung können Sie konfigurieren, wie Anlagen als Teil des Einkaufsprozesses erstellt werden sollen. Die erste Option ist Anlagenanschaffung aus Einkauf zulassen. Wenn Sie diese Option auf Ja festlegen, erfolgt die Anlagenanschaffung, wenn die Rechnung gebucht wird. Durch Festlegen dieser Option auf Nein, Ihnen eine Anlage auf eine Bestellung (PO) und Rechnung, wohingegen, noch aufnehmen können die Anschaffung wird nicht gebucht. Die Buchung muss als separater Schritt aus der Anlagenerfassung ausgeführt werden. Die erstellensanlage während der Produktzugangs- oder Rechnungsbuchungsoption können Sie eine neue Anlage bei der Buchung " spontan" erstellen,sodass diese nicht als Anlage vor der Buchung eingerichtet werden muss. Die letzte Option Während Positionseingabe auf Anlagenerstellung überprüfen, bezieht sich nur auf Bestellanforderungen.

Sie können Ursachencodes konfigurieren, damit sie für Änderungen an einer Anlage oder für bestimmte Anlagenbuchungen erforderlich sind.

Schließlich definieren Sie auf der Registerkarte Nummernkreise den Nummernkreis für Anlagen. Der Anlagennummernkreis kann von der Anlagengruppe überschrieben werden, wenn er angegeben wurde.


