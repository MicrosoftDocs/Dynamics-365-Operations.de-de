---
title: Automatisierung des Inkassoverfahrens
description: In diesem Artikel wird das Einrichten von Inkassoprozessstrategien beschrieben, mit denen Debitorenrechnungen automatisch identifiziert werden, für die eine E-Mail-Erinnerung, eine Inkassoaktivität oder ein Mahnschreiben an den Debitoren gesendet werden müssen.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9ec749db197b4d04ee2e99ac7a16f4f2120c6707
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946177"
---
# <a name="collections-process-automation"></a>Automatisierung des Inkassoverfahrens

[!include [banner](../includes/banner.md)]

In diesem Artikel wird das Einrichten von Inkassoprozessstrategien beschrieben, mit denen Debitorenrechnungen automatisch identifiziert werden, für die eine E-Mail-Erinnerung, eine Inkassoaktivität (z. B. ein Telefonanruf) oder ein Mahnschreiben an den Debitoren gesendet werden müssen. 

Unternehmen verbringen häufig viel Zeit damit, alte Kontostandberichte, Debitorenkonten und offene Rechnungen zu recherchieren, um festzustellen, welche Debitoren wegen einer offenen Rechnung oder eines offenen Kontostands kontaktiert werden sollten. Diese Recherche nimmt Zeit in Anspruch, die ein Inkassobüro für die Kommunikation mit Debitoren benötigt, um überfällige Salden einzuziehen oder Rechnungsstreitigkeiten beizulegen. Mit der Automatisierung von Inkassoprozessen können Sie einen strategiebasierten Ansatz für Ihren Inkassoprozess festlegen. Auf diese Weise können Sie Inkassoaktivitäten konsistent anwenden, indem Sie benutzerdefinierte E-Mail-Erinnerungen oder einen programmierten Prozess zum Senden von Mahnschreiben bereitstellen. 

## <a name="collections-process-setup"></a>Inkassoprozesseinrichtung
Sie können die **Inkassoprozesseinrichtung**-Seite (**Kredit und Inkasso > Einrichtung > Inkassoprozesseinrichtung**) verwenden, um einen automatisierten Inkassoprozess zu erstellen, der Aktivitäten plant, E-Mail-Nachrichten sendet und Debitorenmahnschreiben erstellt und veröffentlicht. Die Prozessschritte basieren auf der führenden oder ältesten offenen Rechnung. Jeder Schritt verwendet diese Rechnung, um zu bestimmen, welche Kommunikation oder Aktivität mit einem bestimmten Debitor stattfinden soll.  

Inkassoteams senden in der Regel eine frühzeitige Benachrichtigung zu jeder ausstehenden Rechnung, damit ein Kunde benachrichtigt wird, wenn die Rechnung fällig wird. Die Auswahl **Vormahnung** kann so eingestellt werden, dass für jede Rechnung ein Schritt in jeder Prozesshierarchie ausgeführt werden kann, wenn der Rechnungszeitpunkt diesen Schritt erreicht.

### <a name="process-hierarchy"></a>Prozesshierarchie
Jeder Debitorenpool kann nur einer Prozesshierarchie zugeordnet werden. Der Hierarchierang dieses Schritts gibt an, welcher Prozess Vorrang hat, wenn ein Debitor in mehr als einem Pool enthalten ist, dem eine Prozesshierarchie zugewiesen ist. Die Pool-ID bestimmt, welche Debitoren dem Prozess zugewiesen werden. Jede eingerichtete Hierarchie kann nur einer Prozessautomatisierung zugewiesen werden.

Die Ruhetage werden verwendet, um sicherzustellen, dass ein Debitor durch den automatisierten Prozess nicht zu häufig kontaktiert wird. Wenn beispielsweise die Ruhetage auf zwei festgelegt sind, wird ein Debitor mindestens zwei Tage lang nicht durch den automatisierten Prozess kontaktiert, selbst wenn die ursprüngliche Hauptrechnung vollständig beglichen wurde. 

Um Kunden von der Prozessautomatisierung auszuschließen, wenn der Fälligkeitssaldo des Kunden oder der Rechnungsbetrag unter einem definierten Wert liegt, wählen Sie **Guthaben der Debitorenfälligkeit kleiner als** oder **Rechnungsbetrag kleiner als** in dem Feld **Vom Prozess ausschließen** aus, und geben sie den Betragswert ein.

Markieren Sie **Vorhersage verwenden**, um Inkassoaktivitäten mit Vorhersagen zu Kundenzahlungen zu erstellen. Die erstellten Aktivitäten verwenden die Aktivitätsvorlage von **Zahlungsvorhersagen** auf der Seite **Debitorenparameter**, auf der Registerkarte **Automatisierung des Inkassoprozesses**. 

### <a name="process-details"></a>Prozessdetails
Klicken Sie auf **Neu**, um der Hierarchie neue Prozessdetails hinzuzufügen. Die **Beschreibung** wird verwendet, um den Zweck oder Namen des Schritts in der Hierarchie zu identifizieren. Wählen Sie den **Aktionstyp** aus, um den Schritt zu definieren, der, eine E-Mail sendet oder ein Mahnschreiben erstellt. 

- Das **Geschäftsdokument** definiert die Vorlage, die zum Erstellen des Aktionstyps verwendet wird. Dieses Dokument kann eine Aktivitätsvorlage, eine E-Mail-Vorlage oder ein Mahnschreiben sein, dass an jeden Debitor gesendet wird. Die Inkasso-Prozessautomatisierung erstellt nur Inkassobriefe pro Kunde, unabhängig davon, wie andere Inkassoparameter eingestellt sind.
- **Wann** definiert den Prozessschritt, der vor oder nach dem führenden (ältesten) Fälligkeitsdatum der Rechnung stattfindet, und wird zusammen mit der in der Spalte **Tage in Bezug auf das Fälligkeitsdatum der Rechnung** angezeigten Zahl verwendet. 
- Markieren Sie die Option **Vorausmahnung**, um eine Aktion für jede Rechnung in einem Schritt in einer Prozesshierarchie zu erstellen. Aktionen zu Vorausmahnungen beinhalten in der Regel eine frühzeitige Benachrichtigung zu ausstehenden Rechnungen, damit ein Kunde benachrichtigt werden kann, wenn die Rechnung fällig wird. Die Vorausmahnung kann nur für einen Vorgang pro Hierarchie markiert werden. Wenn Sie einen E-Mail-Aktionstyp auswählen, wird anhand des Empfängers definiert, ob die E-Mail-Nachricht an einen Debitor-, Verkaufsgruppen- oder Inkassovermittler gesendet wird. 
- Der Wert im Feld **Kontakt zu Geschäftszwecken** bestimmt dann, welcher Kontakt von diesem Debitorenkonto die Mitteilung erhält.

### <a name="business-document-details"></a>Einzelheiten des Geschäftsdokuments
Die Einzelheiten des Geschäftsdokuments variieren je nach Aktionstyp, der in den Prozessdetails ausgewählt wurde. Wenn der Aktionstyp eine Aktivität ist, werden die Details der Aktivitätsvorlage angezeigt. Zu diesen Details gehören der Name der Aktivitätsvorlage, die Art der zu erstellenden Aktivität, der Zweck der Aktivität, die Anzahl der Tage, die für den Abschluss der Aktivität geplant sind, und die Details der Aktivität. Diese Aktivität wird dann mit der führenden Rechnung verknüpft, die den Empfänger die Aktion mitteilt, die zum Abschließen der Aktivität erforderlich ist.

Wenn der Aktionstyp eine E-Mail in den Prozessdetails ist, enthält dieser Abschnitt zwei Inforegister. Die erste wird verwendet, um die Vorlagen-ID, die E-Mail-Beschreibung, die Standardsprache, den Benutzernamen, der automatisch gesendeten E-Mail-Nachrichten zugewiesen wird, und die E-Mail-Adresse des zugeordneten Absenders zu definieren. Mit der zweiten Option kann der Text der E-Mail nach den Werten in den Feldern **Sprache** und **Betreff** der E-Mail durch Auswahl von **Bearbeiten** gespeichert werden. Dies öffnet ein Fenster, in dem HTML-Inhalte hochgeladen werden können. 

> [!Note]
> Sie können eine Outlook-E-Mail-Nachricht speichern, die den Nachrichtentext im HTML-Format enthält. Anschließend können Sie den Nachrichteninhalt hochladen, um die Vorlage zu implementieren. <br> <br> Wenn der Aktionstyp des Mahnschreibens ausgewählt ist, wird auf der Einrichtungsseite kein Abschnitt mit Geschäftsdokumentdetails angezeigt.

Verwenden Sie die Schaltfläche **Historie des Inkassoprozesses**, um die aktuelle Historie für die ausgewählte Prozesshierarchie anzuzeigen. 

Klicken Sie auf die Aktion **Inkassoprozesszuweisung**, um Kunden anzuzeigen, die einem Inkassoprozess zugewiesen sind. Verwenden Sie **Vorschau der Debitorenzuweisung**, um die Hierarchie anzuzeigen, dass ein bestimmter Kunde zugewiesen ist. Verwenden Sie **Vorschau der Prozesszuweisung**, um eine Vorschau der Kunden anzuzeigen, die einer Hierarchie zugewiesen werden, wenn diese ausgeführt wird. Klicken Sie auf **Manuelle Zuweisung**, um Kunden anzuzeigen, die einem Prozess manuell zugewiesen wurden, oder wählen Sie Kunden aus, die einem Prozess zugewiesen werden sollen.

Klicken Sie auf die Aktion **Prozesssimulation**, um die Aktionen in der Vorschau anzuzeigen, die erstellt werden, wenn die ausgewählte Prozessautomatisierung zu diesem Zeitpunkt ausgeführt wird. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
