---
title: Spediteure einrichten
description: In diesem Thema erfahren Sie, wie Sie einen Spediteur einrichten und Details wie Service, Versandart, Transportausschreibung, Transportbeschränkungen und Frachtrate definieren.
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb39d58336e7f867e19d7ba6d9f801200de5a0aa
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148554"
---
# <a name="set-up-shipping-carriers"></a>Spediteure einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema erfahren Sie, wie Sie einen Spediteur einrichten und Details wie Service, Versandart, Transportausschreibung, Transportbeschränkungen und Frachtrate definieren. Ein Transportkoordinator kann dann einen Spediteur einer ein- und ausgehenden Ladung zuweisen.


## <a name="create-a-new-shipping-carrier"></a>Neuen Spediteur erstellen
1. Gehen Sie zu **Navigationsbereich > Module > Transportmanagement > Einrichtung > Spediteur > Spediteur > Spediteur**.
2. Wählen Sie **Neu** im Aktionsbereich.
3. Geben Sie in das Feld **Spediteur** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie im Feld **Modus** eine Option aus dem Dropdown-Menü aus.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Füllen Sie die allgemeinen Informationen für den Spediteur aus
1. Schaltet die Erweiterung des Abschnitts **Übersicht** um.
2. Aktivieren oder deaktivieren Sie das Kontrollkästchen **Spediteur aktivieren**.
3. Wählen Sie im Feld **Lieferantenkonto** eine Option aus dem Dropdown-Menü. Wählen Sie das Kreditorenkonto aus, das dem Spediteur zugeordnet werden soll.  
4. Wählen Sie im Feld **Transportausschreibungstyp** eine Option aus. Wählen Sie **Manuell**, um die Seite Transportausschreibung zu verwenden, oder wählen Sie **EDI**, um die Ausschreibung über Electronic Data Interchange (EDI) zu aktualisieren.  
5. Aktivieren oder deaktivieren Sie das Kontrollkästchen **Spediteur-Rating aktivieren**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Erstellen Sie die erforderlichen Dienstleistungen für den Spediteur
1. Schaltet die Erweiterung des Abschnitts **Dienste** um.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Spediteurservice** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie im Feld **Transportmethode** eine Option aus dem Dropdown-Menü.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Richten Sie die Adresse für den Spediteur ein (optional)
1. Schaltet die Erweiterung des Abschnitts **Adressen** um.
2. Wählen Sie **Neu** aus.
3. Geben Sie in das Feld **Name oder Beschreibung** einen Wert ein.
4. Wählen Sie im Feld **Land/Region** eine Option aus dem Dropdown-Menü.
5. Wählen Sie im Feld **ZIP/Postleitzahl** eine Option aus dem Dropdown-Menü.
6. Geben Sie im Feld **Straße** einen Wert ein.
7. Wählen Sie **OK**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Richten Sie das Bewertungsprofil für den Spediteur ein.
1. Schaltet die Erweiterung des Abschnitts **Bewertungsprofile** ein.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Bewertungsprofil** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie im Feld **Lagerort** eine Option aus dem Dropdown-Menü.
6. Wählen Sie im Feld **Lager** eine Option aus dem Dropdown-Menü.
7. Wählen Sie im Feld **Rate-Engine** eine Option aus dem Dropdown-Menü aus. Wählen Sie das Tarifmodul aus, das in Übereinstimmung mit dem Vertrag steht, den Sie mit dem Spediteur haben.  
8. Wählen Sie im Feld **Rate-Master** eine Option aus dem Dropdown-Menü.
9. Wählen Sie im Feld **Transitzeit-Engine** eine Option aus dem Dropdown-Menü.
10. Wählen Sie **Speichern**.

