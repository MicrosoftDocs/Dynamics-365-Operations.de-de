---
title: Mobilen Arbeitsbereich für die Anlagenverwaltung einrichten
description: Dieser Artikel beschreibt, wie Sie Microsoft Dynamics 365 Supply Chain Management und die Mobile-App von Finanzen und Betrieb (Dynamics 365) festlegen, um einen Asset-Management-Arbeitsbereich auszuführen, in dem Arbeitskräfte Asset-Management-Aufgaben erledigen können.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ef4e6bf2ae59adb05c7d4aacc3f5675a5adcafc9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070052"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Mobilen Arbeitsbereich für die Anlagenverwaltung einrichten

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Microsoft Dynamics 365 Supply Chain Management und die Mobile-App von Finanzen und Betrieb (Dynamics 365) festlegen, um einen **Asset-Management**-Arbeitsbereich auszuführen, in dem Arbeitskräfte Asset-Management-Aufgaben erledigen können.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Einrichten von Benutzern als Wartungsarbeiter in Supply Chain Management

Führen Sie für jeden Benutzer, der Zugriff auf den mobilen Arbeitsbereich für die **Anlalgenverwaltung** benötigt, die folgenden Schritte aus.

1. Wechseln Sie in Supply Chain Management zu **Personalverwaltung \> Arbeitskräfte** und stellen Sie sicher, dass ein Arbeitskraftdatensatz für den Benutzer vorhanden ist, den Sie einrichten möchten. Erstellen Sie gegebenenfalls einen neuen Arbeitskraftdatensatz.
1. Wechseln Sie zu **Anlagenverwaltung \> Einrichten \> Arbeitskräfte \> Arbeitskräfte** und stellen Sie sicher, dass der Arbeitskraftdatensatz, den Sie im vorherigen Schritt gesucht (oder erstellt) haben, einem Wartungsarbeiterdatensatz zugeordnet ist. Erstellen Sie gegebenenfalls einen neuen Wartungsarbeiterdatensatz und legen Sie das Feld **Arbeiter** auf den Arbeitskraftdatensatz aus dem vorherigen Schritt fest.
1. Wechseln Sie zu **Anlagenverwaltung \> Einrichten \> Arbeitskräfte \> Wartungsarbeitergruppen** und stellen Sie sicher, dass der Wartungsarbeiterdatensatz, den Sie im vorherigen Schritt gesucht (oder erstellt) haben, einer Wartungsarbeitergruppe angehört.
1. Wechseln Sie zu **Systemverwaltung \> Benutzer**.
1. Wählen Sie den relevanten Benutzer im Raster aus.
1. Legen Sie im Inforegister **Nutzerdetails** das Feld **Person** auf das Arbeitskraftkonto fest, das Sie dem aktuellen Benutzerkonto zuordnen möchten. Dieses Arbeitskraftkonto sollte der Arbeitskraftdatensatz sein, den Sie in Schritt 1 gesucht (oder erstellt) und in Schritt 2 einem Wartungsarbeiterdatensatz zugeordnet haben.

> [!NOTE]
> Benutzerberechtigungen und Sicherheitsrollen gelten für die Funktionen des mobilen Arbeitsbereichs für die **Anlagenverwaltung** ebenso wie für die Funktionen der Benutzeroberfläche von Supply Chain Management. Daher muss jeder Benutzer, den Sie für den Zugriff auf den mobilen Arbeitsbereich für die **Anlagenverwaltung** einrichten, über die Sicherheitsrollen verfügen, die zur Ausführung ähnlicher Vorgänge direkt in Supply Chain Management erforderlich sind.

## <a name="publish-the-asset-management-mobile-workspace"></a>Mobilen Arbeitsbereich für die Anlagenverwaltung veröffentlichen

Um die Funktionen des Asset-Managements in der Mobile-App für Finanzen und Betrieb (Dynamics 365) verfügbar zu machen, müssen Sie den mobilen Arbeitsbereich **Asset-Management** veröffentlichen.

1. Wählen Sie in Supply Chain Management die Schaltfläche **Einstellungen** aus (das Zahnradsymbol oben rechts) und wählen Sie dann im Menü **Mobile App** aus.
1. Suchen Sie im Dialogfeld **Mobile App verwalten** die Kachel **Anlagenverwaltung**. Wenn sie den Text „In Metadaten – nicht veröffentlicht“ enthält, wurde der Arbeitsbereich noch nicht veröffentlicht. Wenn sie den Text „In Metadaten – veröffentlicht“ enthält, wurde der Arbeitsbereich bereits veröffentlicht und Sie können den Rest dieser Prozedur überspringen.

    ![Das Dialogfeld „Mobile App verwalten“.](media/mobile-workspaces.png "Das Dialogfeld „Mobile App verwalten“")

1. Wähle Sie die Kachel **Anlagenverwaltung** aus und wählen Sie dann auf der Symbolleiste **Veröffentlichen** aus. Nach einigen Sekunden sollten Sie eine Benachrichtigung erhalten, dass der Arbeitsbereich erfolgreich veröffentlicht wurde. Außerdem sollte sich der Text auf der Kachel in „In Metadaten – veröffentlicht“ ändern.

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Installieren und Festlegen der Mobile-App für Finanzen und Betrieb (Dynamics 365)

1. Rufen Sie einen der folgenden App-Stores auf, um die **Microsoft Finanzen und Betrieb (Dynamics 365)** App auf Ihrem mobilen Gerät zu installieren:

    - [Für Google Android-Geräte](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Für Apple iOS-Geräte](https://go.microsoft.com/fwlink/?linkid=850663)

1. Öffnen Sie die Finanzen und Betrieb (Dynamics 365) App. Die Anmeldeseite sollte angezeigt werden. Geben Sie im Feld **Anmelden** Ihre Supply Chain Management-URL ein oder wählen Sie in der Liste **Letzte Umgebungen** eine aktuelle URL aus und tippen Sie dann auf **Verbinden**.

    ![Anmeldeseite.](media/mobile-app-sign-in.png "Anmeldeseite")

1. Wenn Sie aufgefordert werden, die Verbindung zu bestätigen, aktivieren Sie das Kontrollkästchen **Verstanden** und tippen Sie anschließend auf **Verbinden**.
1. Verwenden Sie auf der Seite **Konto auswählen** Ihr Microsoft-Konto aus, um sich bei der mobilen Anwendung anzumelden.

    Die Seite **Arbeitsbereiche** wird angezeigt. Sie listet jeden mobilen Arbeitsbereich auf, der von Ihrer Supply Chain Management-Instanz veröffentlicht wurde.

    ![Liste der Arbeitsbereiche.](media/mobile-app-workspaces.png "Liste der Arbeitsbereiche")

1. Wenn Sie die juristische Person (Firma) ändern müssen, tippen Sie oben links auf die Menütaste (manchmal auch als Hamburger oder Hamburgertaste bezeichnet) und anschließend auf **Firma ändern**.

    ![Ändern der juristischen Person.](media/mobile-app-change-comp.png "Ändern der juristischen Person")

1. Wählen Sie auf der Seite **Arbeitsbereiche** den Arbeitsbereich aus, mit dem Sie arbeiten möchten, um ihn zu öffnen.

    ![Mobiler Arbeitsbereich für Anlagenverwaltung.](media/mobile-app-asset-workspace.png "Mobiler Arbeitsbereich für Anlagenverwaltung")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Arbeiten mit dem mobilen Arbeitsbereich für die Anlagenverwaltung

Weitere Informationen zum Arbeiten mit dem mobilen Arbeitsbereich für die **Anlagenverwaltung** finden Sie unter [Mobilen Arbeitsbereich für die Anlagenverwaltung nutzen](asset-management-mobile-workspace.md).

Weitere Informationen über die Finanzen und Betrieb (Dynamics 365) Mobile-App finden Sie auf der [Homepage der Mobile-App](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
