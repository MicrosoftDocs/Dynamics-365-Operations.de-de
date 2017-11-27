---
title: Einrichten zentralisierter Zahlungen
description: Mithilfe dieses Verfahrens wird die Verarbeitung von Zahlungen einer juristischen Person vorbereitet, die im Auftrag anderer juristischer Personen innerhalb der Organisation abgewickelt werden.
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2e309655bbc1d0fe7a088062b90fab34c642ab29
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-centralized-payments"></a>Einrichten zentralisierter Zahlungen

[!include[banner](../includes/banner.md)]


Mithilfe dieses Verfahrens wird die Verarbeitung von Zahlungen einer juristischen Person vorbereitet, die im Auftrag anderer juristischer Personen innerhalb der Organisation abgewickelt werden. Zunächst müssen jedoch die folgenden Einrichtungsverfahren ausgeführt werden:

-   Erstellen Sie juristische Personen.
-   Richten Sie die Hauptbuchparameter und -Kontenpläne ein.
-   Richten Sie Kreditorenparameter und Debitorenparameter ein (abhängig von den Modulen, die zentralisierte Zahlungen verwenden).
-   Richten Sie die Verrechnung ein.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Einrichten einer Organisationshierarchie für zentralisierte Zahlungen
Für zentralisierte Zahlungen muss eine Organisationshierarchie eingerichtet werden. Diese Organisationshierarchie wird für die Verarbeitung zentralisierter Kreditorenzahlungen und für die Verarbeitung zentralisierter Debitorenzahlungen verwendet. **Hinweis:** Die Struktur der Hierarchie ist für zentralisierte Zahlungen unerheblich. Jede juristische Person in der Hierarchie kann Zahlungen im Auftrag anderer juristischer Personen in der Hierarchie verarbeiten. Auf der Seite **Organisationshierarchien** können Sie eine neue Organisationshierarchie erstellen. Im Feld **Zweck** müssen Sie **Zentralisierte Zahlungen** auswählen. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Einrichten eines Verrechnungskontos für zentralisierte Zahlungen
Beim Ausgleich von Zahlungsbuchungen der aktuellen juristischen Person durch Rechnungen anderer juristischer Personen werden für jede einzelne juristische Person die entsprechenden Buchungen vom Typ "Fällig bis" und "Fällig von" erstellt. Geben Sie die juristische Person für die Buchung realisierter Skonti sowie für die Buchung realisierter Gewinne/Verluste an. Entscheiden Sie zunächst, welche juristische Person zum Verarbeiten von Kreditoren- und Debitorenzahlungen verwendet werden soll. Wenn eine juristische Person Kreditorenzahlungen verarbeitet, aber eine andere juristische Person Debitorenzahlungen verarbeitet, müssen Sie zu jeder juristischen Person wechseln. Wählen Sie einen **Intercompany-Beziehungsdatensatz** für eine juristische Person aus, in deren Auftrag Zahlungen verarbeitet werden sollen. 

Wählen Sie auf der Registerkarte **Zentralisierte Zahlungen** aus, ob Skonti auf die juristische Person für die Zahlung (oder einer anderen Buchung, durch die sich der Saldo des Kreditorenkontos verringert) oder auf die juristische Person für die Rechnung (oder einer anderen Buchung, durch die sich der Saldo des Kreditorenkontos erhöht) gebucht werden sollen. Diese Auswahl funktioniert zusammen mit dem Feld **Skontoverwaltung** und den Seiten **Kreditorenparameter** und **Debitorenparameter**. Bei Überzahlungen und Centdifferenztoleranzen wird die Einstellung der juristischen Person für die Zahlung verwendet. Bei Unterzahlungen und Centdifferenztoleranzen wird die Einstellung der juristischen Person für die Rechnung verwendet.

## <a name="map-vendor-accounts-across-legal-entities"></a>Zuordnen von Kreditorenkonten zu verschiedenen juristischen Personen
Wenn ein Kreditor von einer juristischen Person bezahlt wird und Sie Rechnungen für diesen Kreditor auch in anderen juristischen Personen auswählen möchten, muss sichergestellt sein, dass für alle entsprechenden Kreditorenkonten in den einzelnen juristischen Personen die gleiche Adressbuchkennung verwendet wird. Gehen eine Zahlung eines Debitors, der Rechnungen in mehreren juristischen Personen begleicht, muss sichergestellt werden, dass für alle entsprechenden Debitorenkonten in den einzelnen juristischen Personen die gleiche Adressbuchkennung verwendet wird.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Einrichten von Buchungsprofilen für zentralisierte Zahlungen
Beim Erstellen einer Zahlung durch eine juristische Person, von der Rechnungen anderer juristischer Personen ausgeglichen werden, muss in beiden juristischen Personen die gleiche Buchungsprofilkennung verwendet werden. Richten Sie zu jeder juristischen Person für die Rechnung ein Buchungsprofil ein, das dem Buchungsprofil der juristischen Person für die Zahlung entspricht, um eine ordnungsgemäße Zahlungserstellung sicherzustellen. Wechseln Sie zur ersten juristischen Person für die Rechnung. Dann können Sie auf der Seite **Kreditoren-Buchungsprofile** eine neues Buchungsprofil erstellen oder eine vorhandene Buchungsprofil bearbeiten. Die für das Buchungsprofil der juristischen Person für die Rechnung ausgewählten Optionen müssen nicht den Einstellungen des Buchungsprofils der juristischen Person für die Zahlung entsprechen.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Einrichten von Zahlungsmethoden für zentralisierte Zahlungen
Beim Erstellen einer Zahlung durch eine juristische Person, von der Rechnungen anderer juristischer Personen ausgeglichen werden, muss in beiden juristischen Personen die gleiche Zahlungsmethodenkennung verwendet werden. Richten Sie zu jeder juristischen Person für die Rechnung eine Zahlungsmethode ein, die der Zahlungsmethode der juristischen Person für die Zahlung entspricht, um eine ordnungsgemäße Zahlungserstellung sicherzustellen. Wechseln Sie zur ersten juristischen Person für die Rechnung. Dann können Sie auf der Seite **Zahlungsmethoden** eine neue Zahlungsmethode erstellen oder eine vorhandene Zahlungsmethode bearbeiten. Die für die Zahlungsmethode der juristischen Person für die Rechnung ausgewählten Optionen müssen nicht den Einstellungen der Zahlungsmethode der juristischen Person für die Zahlung entsprechen.

## <a name="set-up-default-descriptions"></a>Einrichten von Standardbeschreibungen
Sie können Standardbeschreibungen für Intercompany-Ausgleichsbelege definieren. Die Standardbeschreibung wird im Rahmen des unternehmensübergreifenden Ausgleichsprozesses in Buchungen vom Typ "Fällig bis" und "Fällig von" eingefügt. Auf der Seite **Standardbeschreibungen** können Sie neue Beschreibungen für **Intercompany-Debitorenausgleich** und **Intercompany-Kreditorenausgleich** erstellen, indem Sie eine Sprache auswählen und dann Text eingeben.




