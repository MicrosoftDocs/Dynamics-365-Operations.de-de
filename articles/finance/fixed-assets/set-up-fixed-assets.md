---
title: Anlagen einrichten
description: Dieses Thema bietet einen Überblick über das Einrichten des Anlagenmoduls.
author: moaamer
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 164f19d4b346a51d4f5d43064cb33bf0c01378dd
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726237"
---
# <a name="set-up-fixed-assets"></a>Anlagen einrichten

[!include [banner](../includes/banner.md)]

Dieses Thema bietet einen Überblick über das Einrichten des **Anlagen**-Moduls. 

Parameter steuern das allgemeine Verhalten in Anlagen. Mit Anlagengruppen können Sie Ihre Anlagen gruppieren und Standardattribute für jede Anlage definieren, die einer Gruppe zugewiesen wird. Bücher werden Anlagengruppen zugewiesen. Bücher verfolgen den Finanzwert einer Anlage im Laufe der Zeit ändern, indem die Abschreibungskonfiguration verwenden, die im Abschreibungsprofil definiert wird.

Anlagen werden bei der Erstellung einer Gruppe zugeordnet. Standardmäßig werden die Bücher, die der Anlagengruppe zugeordnet sind, dann der Anlage zugeordnet. Bücher, die konfiguriert werden, um im Hauptbuch zu buchen, sind einem Buchungsprofil zugeordnet. Sachkonten werden für jedes Buch im Buchungsprofil definiert. Sie werden verwendet, wenn Anlagentransaktionen gebucht werden.

![Anlagenkomponenten.](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Abschreibungsprofile

Abschreibungsprofile sollten zuerst eingerichtet werden. Im Abschreibungsprofil konfigurieren Sie, wie der Wert einer Anlage im Laufe der Zeit abgeschrieben wird. Sie müssen die Abschreibungsmethode, das Abschreibungsjahr (Kalenderjahr oder Geschäftsjahr) und die Häufigkeit der Abschreibung festlegen. Weitere Informationen finden Sie unter [Abschreibungsprofile einrichten und anlegen](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Bücher

Nachdem Sie das Abschreibungsprofile erstellt haben, müssen Sie die erforderlichen Bücher für die Anlagen erstellen. Jedes Abschreibungsbuch verfolgt einen unabhängigen wertmäßigen Lebenszyklus einer Anlage. Bücher können konfiguriert werden, um zugehörige Buchungen im Hauptbuch zu buchen. Diese Konfiguration ist die Standardeinstellung, da sie in der Regel für Unternehmensrechnungslegung verwendet wird. Bücher, die nicht im Hauptbuch gebucht werden, werden nur in den Anlagenuntersachkonten gebucht und werden in der Regel für die Steuerberichterstattung verwendet.

Ein primäres Abschreibungsprofil wird jedem Buch zugewiesen. Bücher haben auch ein alternatives oder wechselbares Abschreibungsprofil, wenn diese Art des Profils anwendbar ist. Um das Anlagenbuch in den Abschreibungsausführungen automatisch einzubeziehen, müssen Sie die Option **Berechnen der Abschreibung** aktivieren. Wenn diese Option nicht für eine Anlage aktiviert ist, überspringt der Abschreibungsvorschlag die Anlage.

Sie können auch abgeleitete Bücher einrichten. Die angegebenen abgeleiteten Transaktionen werden in den abgeleiteten Büchern als genaue Kopie der primären Transaktion gebucht. Daher werden normalerweise die abgeleitete Buchungen für Anschaffungen und Abgänge und nicht für Abschreibungsbuchungen eingerichtet. Weitere Informationen finden Sie unter [Wertmodelle einrichten](tasks/set-up-value-models.md).

Über eine Option auf der Seite **Anlagenparameter** können Sie die Sperrfunktion ein- oder ausschalten. Diese Funktion wird in **Arbeitsbereich der Funktionsverwaltung** aktiviert.

## <a name="fixed-asset-posting-profiles"></a>Anlagenbuchungsprofile

Nachdem das Buch eingerichtet wurde, können Sie das Buchungsprofil erstellen. Das Buchungsprofil muss nach Buch definiert werden, allerdings kann es auf einer detaillierteren Ebene definiert werden. Beispielsweise können Sie das Buchungsprofil für die Kombination eines Buchs und der Anlagengruppe oder sogar für ein einzelnes Anlagenbuch definieren. Standardmäßig werden die Sachkonten verwendet, die für Verwendung der Anlagenbuchungen definiert wurden.

Sie müssen zunächst die Sachkonten definieren, die während der Abgangsprozesse, Abgangsvertrieb und Abgangsausschüsse verwendet werden. Zum Zeitpunkt des Abgangs werden die Anlagentransaktionen, die zuvor gebucht wurden, aus den ursprünglichen Konten storniert. Die Nettobeträge werden dann in das entsprechende Konto für Gewinn und Verlust für Anlagenabgang verschoben. Um sicherzustellen, dass Buchungen korrekt storniert werden, müssen Sie ein Kreditorenkonto für alle Buchungstypen, die in Ihrem Unternehmen verwendet werden, erstellen. Das "Hauptkonto" sollte das ursprüngliche Hauptkonto für diesen Transaktionstyp im Buchungsprofil sein, während das "Gegenkonto" das Gewinn- und Verlustkonto sein sollte. Die Ausnahme ist der Nettobuchwert. In diesem Fall sollten das Hauptkonto und das Gegenkonto in den Gewinn und Verlust für das Abgangskonto festgelegt werden. Weitere Informationen finden Sie unter [Anlagenbuchungsprofile einrichten](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Anlagengruppen

Das Feld **Anlagengruppe** ist das einzige Pflichtfeld beim Erstellen einer Anlage. Der Wert dieses Felds bestimmt den Standardwert mehrerer Informationsfelder für die Anlage. Bücher werden eingerichtet, damit ein Standardbuch jeder Anlage einer Gruppe zugeordnet ist. Hierdurch können Attribute, die Sie für die Bücher festlegen, für eine Gruppe von Anlagen spezifisch sein. Diese Attribute umfassen Nutzungsdauer und die Abschreibungskonvention.

Sie können Sonderabschreibungsbeträge oder Bonusabschreibungen für eine bestimmte Kombination von festen Anlagengruppen und einem Buch definieren. Sie müssen eine Priorität für die Sonderabschreibung zuweisen, um die Reihenfolge anzugeben, in der die Zulagen berechnet werden, wenn mehrere Zulagen zu einem Buch zugewiesen werden. Weitere Informationen finden Sie unter [Anlagengruppen einrichten](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Journale

Auf der Seite **Erfassungsnamen** müssen Sie die Erfassungsnamen erstellen, die mit der Anlagenerfassung verwendet werden sollte. Sie müssen das Feld **Erfassungstyp** auf **Anlagevermögen buchen** festlegen. Legen Sie das Feld **Belegnummern** fest, sodass die Erfassungsnamen für die Anlagenerfassung verwendet werden. Von Anlagenerfassungen sollte nicht die Einstellung **Nur eine Belegnummer** verwendet werden, da eine eindeutige Belegnummer für mehrere automatisierte Prozesse erforderlich ist, wie Übertragungen und Teilungen.

## <a name="fixed-asset-parameters"></a>Anlagenparameter

Der letzte Schritt ist, das Aktualisieren der Anlagenparameter.

Das Feld **Aktivierungsschwelle** bestimmt die Anlagen, die abgeschrieben werden. Wenn eine Bestellposition als Anlage ausgewählt wird, aber nicht den angegebenen Aktivierungsschwellenwert erreicht, ist eine Anlage noch erstellt oder aktualisiert, wobei die Option **Berechnung der Abschreibung** auf **Nein** festgelegt ist. Daher wird die Anlage nicht automatisch im Rahmen der Abschreibungsvorschläge abgeschrieben.

Eine wichtige Option ist **Automatisch Abschreibungsregulierungsbeträge mit Abgang erstellen** genannt. Wenn Sie diese Option auf **Ja** festlegen, wird die Anlagenabschreibung automatisch angepasst, basierend auf den Abschreibungseinstellungen zum Zeitpunkt des Anlagenabgangs. Eine weitere Option ist es, Skonti vom Anschaffungsbetrag abzuziehen, wenn Sie Anlagen erwerben, indem Sie eine Kreditorenrechnung verwenden.

Mit dem Parameter **Anlagenbücher in einem Abschreibungsjournal sperren** können Sie Anlagenbücher in einem Abschreibungsjournal sperren. Wenn Abschreibungsbuchungen gebucht werden, überprüft das System, dass dasselbe Anlagenbuch nicht mehr als einem Abschreibungsjournal hinzugefügt wurde. Ist dies der Fall, wird dieses Anlagenbuch gesperrt und die Buchung wird gestoppt. Wenn sich eine Anlagenbuch-ID in einem gesperrten Journal befindet, wird es automatisch entsperrt, wenn die Buchung für das ursprüngliche Journal abgeschlossen ist. Sie können das Journal auch manuell entsperren. 

Im Inforegister **Bestellung** können Sie konfigurieren, wie Anlagen als Teil des Einkaufsprozesses erstellt werden sollen. Die erste Option wird **Anlagenanschaffung aus Einkauf zulassen** genannt. Wenn Sie diese Option auf **Ja** festlegen, erfolgt die Anlagenanschaffung, wenn die Rechnung gebucht wird. Wenn Sie diese Option auf **Nein** festlegen, können Sie immer noch eine Anlage in eine Bestellung (PO) und Rechnung geben, aber die Anschaffung wird nicht gebucht werden. Die Buchung muss als separater Schritt aus der Anlagenerfassung ausgeführt werden. Mithilfe der Option **Anlage bei Buchung von Produktzugang oder Rechnung erstellen** können Sie eine neue Anlage bei der Buchung „spontan” erstellen. Daher muss die Anlage nicht als Anlage vor der Transaktion eingerichtet werden. Die letzte Option **Während Positionseingabe auf Anlagenerstellung überprüfen**, bezieht sich nur auf Bestellanforderungen.

Sie können Ursachencodes konfigurieren, damit sie für Änderungen an einer Anlage oder für bestimmte Anlagenbuchungen erforderlich sind.

Schließlich definieren Sie auf der Registerkarte **Nummernkreise** die Nummernkreise für Anlagen. Der Nummernkreis der **Anlagen** kann vom Nummernkreis der **Anlagengruppe** überschrieben werden, wenn er angegeben wurde.

Weitere Informationen finden Sie unter [Anlage erstellen](tasks/create-fixed-asset.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
