---
title: Verwenden von Microsoft Power Apps Portalen mit dem Partei-Datenmodell
description: In diesem Thema werden die Änderungen an den Webrollen für Microsoft Power Apps Portale aufgrund des Partei-Datenmodells in Duales Schreiben beschrieben.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 8242a74b8b2251a8489b772f5c4746b113fe2987
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060919"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Verwenden von Microsoft Power Apps Portalen mit dem Partei-Datenmodell

[!INCLUDE[banner](../../includes/banner.md)]



Die Duales Schreiben-Anwendungsorchestrierungslösung, Version 2.0.999.0 und höher enthält Änderungen des Datenmodells an Partei und globalem Adressbuch für die Konto- und Kontakttabellen. Die Änderungen ermöglichen Viele-zu-Viele-Beziehungen, die erweiterte Geschäftsszenarien unterstützen. Diese Änderungen werden von Portal-Webrollen, einschließlich des Kundenportals, nicht unterstützt, die standardmäßig ausgeliefert wurden oder in Ihrer Umgebung vorhanden waren, bevor Sie Duales Schreiben installiert haben. Damit die Webrollen wie erwartet funktionieren, müssen Sie mithilfe des neuen Datenmodells neue Webrollen erstellen. 

Zusammenfassend hat sich die Art und Weise, wie die Tabellen interagieren, geändert, aber die Tabellenberechtigungen im Kundenportal haben sich nicht geändert. In diesem Thema wird erläutert, wie Sie neue Webrollen erstellen, die mit dem neuen erweiterten Datenmodell funktionieren.

Dieses Diagramm zeigt die Tabellenbeziehung **ohne** das Datenmodell der Partei und des globalen Adressbuchs:

   ![ohne Parteimodell.](media/without-party-model.PNG)

Dieses Diagramm zeigt die Tabellenbeziehung **mit** dem Datenmodell der Partei und des globalen Adressbuchs:

   ![mit Parteimodell.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Erstellen einer neuen Tabellenberechtigung

Gehen Sie folgendermaßen vor, um diese neuen Tabellenberechtigungen zu erstellen:

1. Melden Sie sich bei [Power Apps](https://make.powerapps.com) an und gehen Sie zu Ihren Apps.
2. Wählen Sie Ihre Portal Management-App aus.
3. Wählen Sie in der Seitenleiste **Sicherheit > Tabellenberechtigungen** aus.

    Sie müssen drei neue Berechtigungen erstellen:

    + **Konakt** zu **Partei** Tabellenverbindung
    + **Partei** zu **Konto** Tabellenverbindung
    + **Konto** zu **Auftrag** Tabellenverbindung

4. Erstellen und speichern Sie eine neue Berechtigung für die Kontakt-zu-Partei-Verbindung, indem Sie die folgenden Parameter festlegen:

    + **Name**: **Partei** zu **Konto** Tabellenverbindung (oder Ihre Wahl)
    + **Tabellenname**: msdyn_contactforparty
    + **Website**: Kundenportal
    + **Umfang**: Kontakt
    + **Rechte**: Alles auswählen
    + **Webrollen**: Authentifizierte Benutzer, Kundenvertreter (oder Ihre Wahl)

5. Erstellen und speichern Sie eine neue Berechtigung für die Partei-zu-Konto-Verbindung, indem Sie die folgenden Parameter festlegen:

    + **Name**: Partei-zu-Konto-Verbindung (oder Ihre Wahl)
    + **Tabellenname**: Konto
    + **Website**: Kundenportal
    + **Umfang**: Übergeordnetes Element
    + **Rechte**: Alles auswählen
    + **Berechtigung für übergeordnete Tabelle**: Kontakt-zu-Partei-Verbindung

6. Erstellen und speichern Sie eine neue Berechtigung für die Konto-zu-Auftrag-Verbindung, indem Sie die folgenden Parameter festlegen:

    + **Name**: Konto-zu-Auftrag-Verbindung (oder Ihre Wahl)
    + **Tabellenname**: salesorder
    + **Website**: Kundenportal
    + **Umfang**: Übergeordnetes Element
    + **Rechte**: Alles auswählen
    + **Berechtigung für übergeordnete Tabelle**: Partei-zu-Konto-Verbindung

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
