---
title: Eine Anlage erstellen
description: In diesem Thema wird beschrieben, wie eine Anlage in der Anlageverwaltung erstellt wird.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e9c2b81e97a7b08dfdb596fbf6822ac94c7358dccd0b92c0677467dbc0c2e26
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721510"
---
# <a name="create-an-asset"></a>Eine Anlage erstellen

[!include [banner](../../includes/banner.md)]

 

In diesem Thema wird beschrieben, wie eine Anlage in der Anlageverwaltung erstellt wird.

1. Klicken Sie auf **Anlagenverwaltung** > **Gemeinsam** > **Anlagen** > **Alle Anlagen** oder **Aktive Anlagen**.
2. Klicken Sie auf die Schaltfläche **Neu**.
3. Im Dialogfeld **Anlagen erstellen** geben Sie die DAten zu **Anlagen** (Die Anlagen-Kennung) und den Anlagennamen ein. Wählen Sie das Datum und die Zeit für die Anlage im Feld **Effektiv**. Ab diesem Datum sind Sie in der Lage, die Anlage auf einem funktionalen Stnadort zu installieren und Die Anlage in der Anlagenstruktur zu verschieben oder zu ersetzen.
4. Im Feld **Anlagentyp** wählen Sie den Anlagentyp für die Anlage aus (Pflichtfeld). Bei Bedarf wählen Sie **Anlagenhersteller** und **Anlagenmodell** für die Anlage aus. Wenn nur ein Produkt eingerichtet wurde, wird dieses Produkt automatisch im Feld **Anlagenhersteller** ausgewählt. Die Auswahl, die in den Feldern **Anlagenhersteller** und **Anlagenmodell** verfügbar ist, hängt von der Einstellung in [Anlagenhersteller und -Modelle](../setup-for-objects/product-and-model.md) ab.
5. In der Gruppe ist **Übergeordnete Anlage** ist das Feld **Aktivposten** als Standardwert leer. Bei Bedarf können Sie eine übergeordnete Anlage auswählen, und anschließend werden alle Felder in der Gruppe **Übergeordnete Anlage** automatisch aufgefüllt.
    >[!NOTE]  
    >Wenn Sie andererseits eine übergeordnete Anlage ausgewählt haben, stehen zwei oder drei Registerkarten zur Verfügung: Die Registerkarte **Meine Anlagen** enthält die Anlagen, die den funktionalen Standorten zugeordnet sind, auf denen möglicherweise Sie (der Wartungsarbeiter, der beims System angemeldet ist), zugeordnet werden. Wenn keine funktionalen Standorte für einen Wartungsarbeiter im Formular [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md) eingerichtet werden, wird die Registerkarte **Meine Anlagen** nicht angezeigt. Die Registerkarte **Aktive Anlagen** enthält eine Liste aller Anlagen mit dem Anlagenlebenszyklusstatus „Aktiv“. Die Registerkarte **Anlagenansicht** enthält eine Strukturansicht der funktionalen Standorte und Anlagen, die für diese Standorte installiert sind.

6. Der funktionale Standardstandort, den Sie eingerichtet haben, wird für die Anlage in der Gruppe **Anlagen** > im Feld **Funktionaler Standort** vorgeschlagen. Wählen Sie bei Bedarf einen anderen, funktionalen Standort aus.

    >[!NOTE]
    >Sobald Soe eine Anlage erstellt haben, können Sie auf einem anderen funktionalen Standort installieren, falls erforderlich. Nur Anlagen der obersten Ebene (Anlagen ohne eine übergeordnete Anlage) können auf einen funktionalen Standort installiert werden. Das bedeutet, dass Sie die übergeordnete Ebene sowie sämtliche untergeordneten Anlagen im ausgewählten funktionalen Standorten einrichten. Lesen Sie mehr über das Installieren von Anlagen auf funktionalen Standorten in [Einführung in funktionale Standorte](../functional-locations/introduction-to-functional-locations.md).

7. Klicken Sie auf **OK**.
8. Wählen Sie die Anlage in der Liste **Alle Anlagen** aus und klicken Sie auf die Schaltfläche **Bearbeiten**, um weitere Informationen zur Anlage hinzuzufügen.

## <a name="general-information"></a>Allgemeine Angaben

Der funktionale Standort, dem die Anlage zugeordnet ist, wird im Feld **Funktionaler Standort** angezeigt. Wenn die Anlage eine übergeordnete Anlage ist, ist die Anzahl von untergeordneten Elementen, die der Anlage zugeordnet sind, im Feld **Untergeordnet** angezeigt. Wenn die Anlage eine untergeordnete Anlage ist, wird die Kennzeichnung der übergeordneten Elementen im Feld **Übergeordnet** angezeigt.

Sie können **Anlagenhersteller** und **Anlagenmodell** Informationen zur Anlage bearbeiten, die verwendet wird, um Ersatzteile, alternative Ersatzteile und Stellentypenstandards zu verwalten. Weitere Informationen finden Sie unter [Anlagenhersteller und -modelle](../setup-for-objects/product-and-model.md). Sie können auch Informationen über **Modelljahr** und **Seriennummer** hinzufügen, falls erforderlich.

**Aktueller Lebenszyklusstatus** wird verwendet, um festzulegen, ob die Anlage aktiv oder inaktiv ist. Wenn eine Anlage erstellt wird, ist die Phase immer auf der ersten Phase in der Anlagenphasengruppe festgelegt. Wenn Sie bereit sind, eine Anlage zu aktivieren, klicken Sie **Aktualisierungsanlagenstatus** und wählen Sie den Lebenszyklusstatus, den Sie als „aktive Anlage“ festgelegt haben und klicken Sie auf **OK**

**Hinweis:** Wenn eine Anlage auf „inaktiv“ festgelegt ist, ist es nicht mehr möglich, Arbeitsaufträge für die Anlage zu erstellen. Außerdem können Sie keine vorbeugenden Wartungsaufträge für eine inaktive Anlage planen.

Die Felder **Leistungsebene** und **Risiko** beziehen sich auf die Arbeitsaufträge, die für die Anlage erstellt werden. Die Felder enthalten die Nummern **Leistungsebene** und **Priorität**, die für die aktuellen Einstellungen für die Anlage berechnet werden. Weitere Informationen zum Einrichten dieser Werte finden Sie unter [Anlagenservicelevel](../setup-for-objects/object-priorities.md) und [Typen kritischer Werte für Anlagen](../setup-for-objects/object-criticalities.md).

## <a name="asset"></a>Anlage

Sie können **Ressource** für die Anlage auswählen. Die Ressourcen-Auswahl bestimmt, welcher Kalender für die Arbeitsauftragsplanung verwendet wird. Ressourcen-Auswahl wird häufig für Anlagen verwendet. Ressourcen und Ressourcengruppen werden in **Organisationsverwaltung** > **Ressourcen** > **Ressourcengruppen** oder **Ressourcen** eingerichtet.

Im Feld **Anlagennummer** können Sie eine Anlage auswählen, die der Anlage zugeordnet wird. Dies ist von Bedeutung, wenn Ihre Anlage einem Investitionsprojekt zugeordnet ist.

- Wenn die Anlage einem Anlagevermögen zugeordnet ist, können Sie einen Arbeitsauftragstyp verwenden, der für den Arbeitsauftrag verwendet wird, der einem Investitionsprojekt zugeordnet wird. 
- Informationen zu Anlagen für eine Anlage werden dem Modul **Anlagevermögen** in Dynamics 365 Supply Chain Management zugeordnet. Dies bedeutet, dass in **Anlagen** > **Anlagen** > **Anlagen** Sie eine Übersicht über die Anlagenverwaltungsprojekte erhalten, die einer Anlage zugeordnet werden, indem Sie die Anlage in der Liste auswählen und den Inhalt im Bereich **Zugehörige Informationen** > im Abschnitt **Zugeordnete Projekte** anzeigen.


## <a name="details"></a>Detaildaten

Im Feld **Aktiv ab** wird das Datum angezeigt, an dem Sie den Anlagenlebenszyklusstatus für einen aktiven Status aktualisiert haben (vgl. [Anlagenlebenszyklusstatus](../setup-for-objects/object-stages.md) bezüglich Einrichtung von Anlagenlebenszyklus). Wenn die Anlage nicht mehr aktiv ist und Sie den Anlagenlebenszyklusstatus für einen inaktiven Lebenszyklus aktualisiert haben, wird das Datum, ab dem die Anlage inaktiv ist, im Feld **Aktiv bis** angezeigt. Diese Daten können Sie bei Bedarf manuell ändern.

Bei Bedarf können Sie ein erwartetes Datum für den Ersatz der Anlage im Feld **Wiederbeschaffungsdatum** einfügen. Der vorkalkulierte Wert für das Ersetzen der Anlage kann in das Feld **Wiederbeschaffungswert** eingefügt werden. Beispiel: Sie können Ersatzinformationen verwenden, um sie mit den Kosten für die das Beibehalten einer Anlage zu vergleichen, um anschließend eine Entscheidung für den Kauf einer neuen Anlage zu fällen, wenn die Wartungskosten der bestehenden Anlage rasch steigen.

## <a name="notes"></a>Notizen

Sie können Hinweise hinzufügen, die der Anlage auf dem Inforegister **Hinweise** zugeordnet werden. Klicken Sie auf die Schaltfläche **Zeitstempel hinzufügen**, bevor Sie den Hinweis schreiben, wenn Sie Benutzerinformationen und Datum/Uhrzeit dem Hinweis hinzufügen möchten.

## <a name="attributes"></a>Attribute

Auf diesem Inforegister können Sie Werte für Anlagenattribute festlegen. Diese Attribute können verwendet werden, um zweckdienlich Eigenschaften oder Merkmale der Anlage wie, Größe, Gewichtung oder Maschinenkonfiguration zu beschreiben.

Klicken Sie **Position hinzufügen** und wählen Sie den Attributtyp aus. Danach fügen Sie den **Wert** ein, der mit dem Attributtyp verknüpft ist und speichern den Datensatz.

>[!NOTE] 
>Sie können sich einen Überblick über Anlagenattributtypen und ihre Beziehung zu den Anlagen in **Anlagenattribut** und **Anlagenattributüberblick** verschaffen. Weitere Informationen finden Sie unter [Anlagenattributübersicht](../objects/object-specification-overview.md).

## <a name="vendor"></a>Lieferant

Auf dem Inforegister **Lieferant** aktivieren Sie einen Lieferant für die Anlage aus. Falls eine Lieferantengarantie erteilt wurde, können Sie Garantieinformationen hier einfügen.

## <a name="address"></a>Anschrift

Auf dem Inforegister **Adresse** können Sie die Adresse der Ausrüstung einfügen. Wenn keine Adresse aus der Anlage eingefügt wird, verwendet die Anlage die Adresse einer übergeordneten Anlage, wenn die Anlage eine übergeordnete Adresse hat. Wenn keine Adresse den Anlagen- oder beliebigen Elementen in der Anlagenhierarchie zugeordnet ist, wird die Adresse des funktionalen Standorts verwendet, an dem die Anlage eingerichtet ist. Wenn dieser funktionale Standort keine Adresse hat, die ihm zugeordnet ist, wird die Adresse des funktionalen Standortes für die Anlage verwendet.

## <a name="asset-management-plans"></a>Anlagenverwaltungspläne

Wartungspläne werden für die vorbeugenden Wartungsaufträge für Analgen in regelmäßigen Zeitabständen verwendet. Auf diesem Inforegister können Sie Wartungsplanpositionen für ausgewählte Anlagen einrichten. Wartungsdurchgänge können für verschiedene Anlagen eingerichtet werden, in denen ähnliche Aufgaben in regelmäßigen Abständen ausgeführt werden müssen. Auf der Registerkarte **Funktionale Standortwartungspläne** sehen Sie die Wartungspläne, die dem funktionalen Standort zugewiesen sind, auf dem die Anlage installiert ist.

>[!NOTE]
>Wenn Sie einen Wartungsplan oder einen Wartungsdurchgang löschen, der einer Anlage unter **Alle Anlage** zugeordnet ist, löschen Sie auch automatisch alle Wartungspläne mit dem Status „Erstellt“, die basierend auf diesem Wartungsplan oder Wartungsdurchgang erstellt wurden.

## <a name="functional-location-maintenance-plans"></a>Wartungspläne für funktionale Standorte

Auf diesem Inforegister erhalten Sie einen Überblick über die Wartungspläne, die dem funktionalen Standort zugewiesen sind, auf dem die Anlage installiert ist.

## <a name="maintenance-rounds"></a>Wartungsdurchgänge

Auf diesem Inforegister können Sie die Wartungsdurchgänge hinzufügen oder entfernen, die der Anlage zugeordnet sind.

## <a name="financial-dimensions"></a>Finanzdimensionen

Sie können die Finanzdimensionen für die Anlagen auswählen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]