---
title: Einen Callcenterkanal einrichten
description: In diesem Artikel wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.
author: samjarawan
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 219c84eb9a8c3b53467ed48c13775106c82dac63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864954"
---
# <a name="set-up-a-call-center-channel"></a>Einen Callcenterkanal einrichten


[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.

## <a name="overview"></a>Übersicht


In Dynamics 365 Commerce ist ein Callcenter ein Commerce Channel, der in der Anwendung definiert werden kann. Durch das Definieren eines Kanals für Ihre Callcenter-Entitäten kann das System bestimmte Daten und Auftragsverarbeitungsstandards mit Aufträgen verknüpfen. Während ein Unternehmen mehrere Call-Center-Kanäle in Commerce definieren kann, ist es wichtig zu beachten, dass ein einzelner Benutzer nur mit einem Call-Center-Kanal verbunden sein darf. 

Bevor Sie einen neuen Callcenter-Kanal anlegen, stellen Sie sicher, dass Sie die Voraussetzungen [Kanal-Einrichtung](channels-prerequisites.md) erfüllt haben.

## <a name="create-and-configure-a-new-call-center-channel"></a>Einen neuen Callcenterkanal erstellen und konfigurieren

Um einen Callcenterkanal zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie im Navigationsbereich zu **Retail and Commerce \> Kanäle \> Callcenter \> Alle Callcenter**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.
1. Wählen Sie aus der Dropdown-Liste die entsprechende **Juristische Person** aus.
1. Wählen Sie aus der Dropdown-Liste den entsprechenden **Lager** Lagerplatz aus. Dieser Standort wird als Standard bei Kundenaufträgen verwendet, die für diesen Call-Center-Kanal angelegt werden, es sei denn, auf Kunden- oder Artikelebene wurden andere Standardeinstellungen definiert.
1. Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an. Diese Daten werden für die Unterstützung der automatischen Bestückung mit Standardeinstellungen verwendet, wenn neue Kundendatensätze angelegt werden. Beim Anlegen von Callcenter-Aufträgen ist es nicht ratsam, Aufträge für den Standardkunden anzulegen.
1. Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein. Beim Anlegen und Verarbeiten von Callcenter-Aufträgen wird das E-Mail-Benachrichtigungsprofil verwendet, um automatische E-Mail-Benachrichtigungen an Kunden mit Informationen über ihren Auftragsstatus auszulösen.
1. Geben Sie einen Infocode **Preisüberschreibung** an. Dazu müssen Sie möglicherweise zuerst einen Info-Code anlegen. Dieser Infocode enthält eine Reihe von Begründungscodes, aus denen der Benutzer bei der Verwendung der Funktion zur Preisüberschreibung bei einer Call-Center-Bestellung aufgefordert wird, eine Auswahl zu treffen.
1. Geben Sie einen Infocode **Code halten** ein. Dazu müssen Sie möglicherweise zuerst einen Info-Code anlegen. Dieser Infocode enthält eine Reihe von optionalen Begründungscodes, aus denen der Benutzer bei der Platzierung einer zurückgestellten Bestellung zur Auswahl aufgefordert wird.
1. Geben Sie einen Infocode **Haben** ein. Dazu müssen Sie möglicherweise zuerst einen Info-Code anlegen. Dieser Infocode stellt die Menge der Begründungscodes zur Verfügung, aus denen der Benutzer wählen kann, wenn er die Auftragskreditfunktion des Call Centers verwendet, um dem Kunden aus Gründen des Kundendienstes verschiedene Rückerstattungen zu gewähren.
1. Optional: Richten Sie die finanziellen Dimensionen auf der Registerkarte **Finanzielle Dimensionen** ein. Die hier eingegebenen Dimensionen werden bei jedem Kundenauftrag, der in diesem Callcenter-Kanal angelegt wird, als Standardeinstellung verwendet.
1. Klicken Sie auf **Speichern**.

Das folgende Bild zeigt die Erstellung eines neuen Callcenterkanals.

![Neuer Callcenterkanal.](media/channel-setup-callcenter-1.png)

Das folgende Bild zeigt ein Beispiel für einen Callcenterkanal.

![Beispiel eines Callcenterkanals.](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Einrichtung eines zusätzlichen Kanals

Zusätzliche Aufgaben, die für das Einrichten des Callcenterkanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden und Lieferarten.

Die folgende Abbildung zeigt **Lieferarten** und **Zahlungsmethoden** Einrichtungsoptionen auf der Registerkarte **Einrichten**.

![Zusätzliche Aktionen zum Einrichten von Callcenterkanälen.](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Einrichten von Zahlungsmethoden

Um die Zahlungsmethoden einzurichten, befolgen Sie diese Schritte für jede in diesem Kanal unterstützte Zahlungsart. Die Benutzer müssen aus vordefinierten Zahlungsmethoden auswählen, um sie mit dem Call-Center-Kanal zu verknüpfen. Bevor Sie Ihre Call-Center-Zahlungsmethoden einrichten, richten Sie zunächst Ihre Hauptzahlungsmethoden unter **Retail and Commerce \> \> Zahlungsmethoden \> Zahlungsmethoden** ein.

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Navigationsfenster eine Zahlungsmethode aus den vordefinierten verfügbaren Zahlungen aus.
1. Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart. Für Kreditkarten, Geschenkkarten oder Kundenkarten ist eine zusätzliche Einrichtung erforderlich, indem Sie die Funktion **Karteneinrichtung** wählen. 
1. Konfigurieren Sie die richtigen Buchungskonten für die Zahlungsart im Abschnitt **Buchung**.
1. Klicken Sie im Aktionsfenster auf **Speichern**.

Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.

![Beispielzahlungsmethoden.](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Lieferarten einrichten

Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.  

Um eine dem Call-Center-Kanal zuzuordnende Zustellungsart zu ändern oder hinzuzufügen, gehen Sie wie folgt vor.

1. Wählen Sie im Call-Center-Zustellungsmodi-Formular **Zustellungsmodi verwalten**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.
1. Klicken Sie in der Sektion **Einzelhandelskanäle** auf **Zeile hinzufügen**, um den Call-Center-Kanal hinzuzufügen. Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.
1. Vergewissern Sie sich, dass der Zustellungsmodus mit Daten über **Produkte** und **Adressen** konfiguriert wurde. Wenn keine Produkte oder Lieferadressen für die Lieferart gültig sind, führt die Auswahl der Lieferart bei der Auftragserfassung zu Fehlern.
1. Nachdem Änderungen an den Call-Center-Lieferartenkonfigurationen vorgenommen wurden, muss der Job **Lieferarten bearbeiten** ausgeführt werden, um die Änderungsmatrix aufzulösen. Diesen Job finden Sie, indem Sie zu **Retail and Commerce \> Retail and Commerce IT \> Prozesslieferungsarten** navigieren.

Das folgende Bild zeigt ein Beispiel für eine Lieferart.

![Lieferarten einrichten.](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Channel-Benutzer einrichten

Um einen Kundenauftrag anzulegen, der mit dem Call-Center-Kanal vpm Commerce Headquarters verknüpft ist, muss der Benutzer, der den Kundenauftrag anlegt, mit dem Call-Center-Kanal verknüpft sein. Der Benutzer kann einen in Commerce Headquarters angelegten Kundenauftrag nicht manuell mit dem Kanal Call Center verknüpfen. Die Verknüpfung ist systematisch und basiert auf dem Benutzer und seiner Beziehung zum Channel Call Center. Ein Benutzer kann nur mit einem Callcenter-Channel verknüpft werden.

1. Wählen Sie im Aktionsbereich die Registerkarte **Kanal** und dann **Benutzer des Kanals**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie aus der Dropdown-Auswahlliste eine vorhandene **Benutzer-ID**, um diesen Benutzer mit dem Callcenter-Kanal zu verknüpfen.

Nachdem die Einrichtung des Kanalbenutzers abgeschlossen ist und der Benutzer einen neuen Kundenauftrag in der Handelszentrale erstellt hat, wird der Kundenauftrag mit dem zugehörigen Callcenter-Kanal verknüpft. Alle Konfigurationen für diesen Kanal werden systematisch auf den Kundenauftrag angewendet. Ein Benutzer kann bestätigen, mit welchem Callcenter-Kanal der Kundenauftrag verknüpft ist, indem er die Referenz des Kanalnamens im Auftragskopf anzeigt.


### <a name="set-up-price-groups"></a>Einrichten von Preisgruppen

Preisgruppen sind optional, können aber, wenn sie verwendet werden, steuern, welche Verkaufspreise den Kunden, die Aufträge im Callcenter-Kanal erteilen, angeboten werden. Wenn für den Kunden keine Preisgruppe konfiguriert wurde oder wenn Katalogpreisgruppen nicht auf den Kundenauftrag angewendet werden (über das Feld **Quellcode-ID** im Auftragskopf des Callcenters), wird die Kanalpreisgruppe zur Ermittlung von Artikelpreisen verwendet. Wenn eine Preisgruppe im Kanal des Callcenters nicht gefunden wird, werden die Standardartikelstammpreise verwendet. 

Um eine Preisgruppe einzurichten, gehen Sie wie folgt vor.

1. Klicken Sie im Aktionsbereich auf die Registerkarte **Kanal**, und wählen Sie dann **Preisgruppen**.
1. Klicken Sie im Aktivitätsbereich auf **Neu**.
1. Wählen Sie aus der Dropdown-Auswahlliste eine **Einzelhandelspreisgruppe**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)

[Callcenter-Vertriebsfunktionen](call-center-functionality.md)

[Callcenter-Auftragsabwicklungsoptionen einrichten](set-up-order-processing-options.md)

[Callcenterkataloge](call-center-catalogs.md)

[Einrichten und Verwenden von Betrugswarnungen](set-up-fraud-alerts.md)

[Einrichten von Anschlussprogrammen für Callcenter](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]