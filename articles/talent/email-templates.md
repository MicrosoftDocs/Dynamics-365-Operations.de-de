---
title: E-Mail-Vorlagen in Attract erstellen
description: 'Dieses Thema enthält Informationen zu den E-Mail-Vorlagen, die Sie in Microsoft Dynamics 365 Talent: Attract erstellen und verwenden können.'
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 55c12010cfd055ee6977f50e566b70f76a2e1682
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461241"
---
# <a name="create-email-templates-in-attract"></a>E-Mail-Vorlagen in Attract erstellen

[!include [banner](includes/banner.md)]

Mithilfe der E-Mail-Vorlagen-Bibliothek können Administratoren ein einheitliches Design und Branding für alle E-Mails erstellen, die von Microsoft Dynamics 365 Talent: Attract und Offer gesendet werden. Administratoren können auch eine Sammlung von E-Mail-Inhaltsvorlagen zusammenstellen, die von anderen E-Mail-Nutzern verwendet werden können. Das Einstellungsteam kann diese Vorlagen in ihrem Workflow verwenden, um E-Mail-Nachrichten effizienter zu senden. Einige E-Mails werden so konfiguriert, dass sie automatisch gesendet werden, und der Administrator kann die Email-Vorlagen-Bibliothek verwenden, um den Inhalt für die E-Mails anzupassen.

> [!NOTE]
> Um E-Mail-Vorlagen zu verwenden, muss die Organisation das Verständliche Einstellungsadd-on haben.

## <a name="global-template-configurations"></a>Globale Konfigurationsvorlagen

Um ein konsistentes Branding für die gesamte E-Mail-Kommunikation zu erstellen, muss der Administrator erst die globalen Kopf- und Fußzeilen für alle E-Mail-Vorlagen festlegen. Im Administratorcenter kann der Administrator auf der Registerkarte **Email-Vorlagen-Einstellungen** im Abschnitt **Kopfzeile** ein Bild hochladen, das bei allen E-Mails als Kopfzeile oder Banner verwendet werden soll. Das Bild kann ein Firmenlogo, ein Briefkopf oder jedes andere Repräsentativbild sein. Es wird empfohlen, dass die Breite zwischen 25 und 800 Pixel beträgt und die Höhe zwischen 25 und 150 Pixel, da diese Abmessungen für die meisten E-Mail-Clients wie Microsoft Outlook optimal sind. Das Bild muss eine JPEG-, JPG-, PNG- oder SVG-Datei sein, und die Dateigröße muss kleiner als 1 Megabyte (MB) sein. Nachdem ein Bild hochgeladen wurde, wird eine Vorschau der Kopfzeile generiert und angezeigt. Wenn das Kopfzeilenbild entfernt oder ersetzt werden muss, kann der Administrator die Option **Entfernen** über der Vorschau verwenden.

Im Abschnitt **Fußzeile** kann der Administrator Links zur Kommunikations-Datenschutzrichtlinie den Bedingungen des Unternehmens bereitstellen. Diese Links werden in eine Fußzeile integriert, die automatisch generiert wird. Eine Vorschau der Fußzeile wird dann angezeigt. Der Administrator kann auch eine bestimmte Sprache auswählen, in der E-Mail-Fußzeilen als Teil aller E-Mail-Nachrichten gesendet werden. Die gleiche Sprachenkonfiguration wird auch zum Zusammenfügen der Tabelle der Gesprächsszusammenfassung verwendet. 

Vergewissern Sie sich, dass Sie die Änderungen speichern, bevor Sie das Administratorcenter schließen.

> [!NOTE] 
> Die Kopf- und Fußzeilen sind globale Einstellungen für alle E-Mails. Daher werden sie in allen E-Mails angezeigt, die von über Attract gesendet werden. Wenn die Einstellungen nicht konfiguriert werden, werden die Kopf- und Fußzeilen aus allen E-Mails weggelassen.

## <a name="email-template-library"></a>E-Mail-Vorlagenbibliothek 

Nachdem die globalen Vorlagenkonfigurationen eingerichtet sind, kann der Administrator damit beginnen, Vorlagen für alle E-Mails zu erstellen und zusammenzustellen, die über Attract und Offer gesendet werden. Die Email-Vorlagenbibliothek ist nur für Administratoren verfügbar. Um die Bibliothek zu öffnen, wählen Sie im Hauptnavigationsmenü die Registerkarte **E-Mail-Vorlagen** aus. Die Bibliothek wird nach den unterschiedlichen Aktivitäten in Attract kategorisiert, für die E-Mails gesendet werden müssen, z. B. „Planung“, „Bewertung“, „Joberstellung“ und „Angebot“. Der Administrator kann eine beliebige Kategorie auswählen, um alle E-Mail-Typen anzuzeigen, die der Aktivität zugeordnet sind. Wählen Sie beispielsweise **Planung** aus, um die verschiedenen E-Mail-Typen anzuzeigen, die während des Planungsprozesses gesendet werden, und alle Vorlagen, die für jeden E-Mail-Typ verfügbar sind. Jeder Unterabschnitt in einer Kategorie stellt einen E-Mail-Typ dar.

Eine E-Mail-Typen können mehrere Empfänger haben. In der Kategorie **Planung** beispielsweise, werden die E-Mails, die gesendet werden, wenn die Gesprächsplanzusammenfassung benötigt wird, an Kandidaten und Gesprächsleiter gesendet. Jeder Abschnitt enthält zwei Hauptspalten: **Vorlagentitel** und **Empfänger**. Jede Zeile in einem Abschnitt enthält eine einzelne Vorlage für einen E-Mail-Typ. Zuerst wird ein Schlosssymbol in der Zeile für jede Vorlage angezeigt. Dieses Symbol gibt an, dass die Vorlage die Standardvorlage ist, der von Attract bereitgestellt wird, und dass sie nicht gelöscht werden kann. Für jede Vorlage kann der Administrator die Ellipsenschaltfläche (**…**) verwenden, um die Vorlage zu duplizieren, als eine Standardvorlage festzulegen oder sie zu löschen. Wenn eine Vorlage als Standardvorlage festgelegt wird, kann eine der beiden Verhaltensweisen auftreten. Das Verhalten wird durch die Kennkarte(n) angegeben, die in der Zeile für die Vorlage angezeigt werden:

- **Standard** – Diese Kennkarte gibt an, dass die Vorlage die Standardvorlage für E-Mails ist, die gesendet werden, und dass Informationen eingegeben werden, wenn ein Benutzer E-Mails dieses bestimmten Typs sendet.
- **Standard** + **Automatisch übermittelt** – Diese Kennkartenkombination on weist darauf hin, dass die Vorlage die aktive Vorlage für vom System erstellte E-Mails ist, die automatisch gesendet werden.

Um eine Vorlage zu bearbeiten, wählen Sie die Zeilen aus und nehmen Änderungen an der Vorlage vor.

> [!NOTE]
> Jeder Empfänger eines bestimmten E-Mail-Typs hat eine Standardvorlage. Alle Standardvorlage von Attract werden als Standardvorlagen festgelegt, bis der Administrator eine neue Vorlage für einen bestimmten E-Mail-Typ erstellt und als Standardvorlage festlegt.

## <a name="create-a-template"></a>Eine Vorlage erstellen

Um eine Vorlage zu erstellen, wählen Sie in der oberen rechten Ecke der Email-Vorlagenbibliothek **+ Neue Vorlage** aus. Um den E-Mail-Typ auszuwählen, für die Sie die Vorlage erstellen, wählen Sie den Empfänger, den Prozess und das Ereignis aus, für das die E-Mail gesendet werden muss. Wählen Sie dann **Erstellen** aus.

Die Vorlage wird in der Bearbeitungsansicht geöffnet, und Sie können die Vorlage benennen. Soll die Vorlage beispielsweise an Kandidaten für eine US-Universität gesendet werden, aber der Inhalt ist in Französisch, geben Sie möglicherweise den Titel **Universität\_USA\_Francais** ein. Der Titel, die Betreffzeile und der Textinhalt für jede Vorlage können Sprachen neben Englisch unterstützen.

Das Feld **Für** für eine Vorlage kann nicht geändert werden, da Sie den Empfänger bereits ausgewählt haben, als Sie die Vorlage zuerst erstellt haben.

Sie können Personen wie **Personalbeschaffungsmitarbeiter** oder **Zukünftiger Vorgesetzter** in der Kopiezeile (Cc) hinzufügen. Wird die E-Mail gesendet wird, werden diese Rollen automatisch durch die entsprechenden Benutzer ersetzt, basierend auf dem Kontext der Stelle.

Die Betreffzeile der der Textinhalt unterstützen Platzhalter. Sie können Platzhalter einfügen, indem Sie **\#** eingeben und anschließend den entsprechenden Platzhalter in der Dropdownliste für automatische Vervollständigung auswählen. Die Liste der verfügbaren Platzhalter wird rechts neben der Seite angezeigt. Wird die E-Mail gesendet, werden die Platzhalter automatisch ersetzt, basierend auf dem Kontext der Stelle und der Empfänger. Zum Beispiel beinhaltet eine Vorlage für eine E-Mail, die an Kandidaten gesendet wird, den Platzhalter \#{Kandidat\_Name}. Wird die E-Mail einem Kandidaten gesendet wird, der Cameron heißt, wird dieser Platzhalter durch den Namen von Cameron ersetzt.

Der Editor für Textinhalts ist ein Rich-Text-Editor, mit dem Sie Stil und Format des Text festlegen können. Sie können auch Links und Anker einfügen.

Nachdem eine Vorlage für einen bestimmten E-Mail-Typ erstellt wurde, wählen Sie in der Zeile für die Vorlage die Ellipsenschaltfläche (**…**) aus, und legen sie als Standardvorlage fest.

## <a name="consume-templates"></a>Vorlagen nutzen

Wenn das Einstellungsteam eine E-Mail sendet, kann es die vom Administrator erstellten Vorlagen nutzen. Wenn mehrere Vorlagen für die E-Mail erstellt wurden, die ein Benutzer sendet, wird eine Dropdownliste im E-Mail-Anordnungsworkflow angezeigt. Die Standardvorlage wird automatisch eingegeben, aber der Benutzer kann eine andere Vorlage auswählen.

> [!NOTE] 
> Für E-Mails, die automatisch gesendet werden, können mehrerer Vorlagen erstellt werden. Allerdings kann nur einer Vorlage als die aktive Vorlage festgelegt werden. Da dieser Prozess durch Ereignisse ausgelöst wird, kann nur der Administrator festlegen, welche Vorlage anhand der Kombination der Kennkarten **Standard** und **Automatisch übermittelt** in der Vorlagenbibliothek verwendet werden soll.
