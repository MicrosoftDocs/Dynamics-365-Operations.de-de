---
title: Konfigurieren Sie die Azure Active Directory-Authentifizierung für die POS-Anmeldung
description: Dieses Thema erklärt, wie Sie Azure Active Directory als Authentifizierungsmethode in Microsoft Dynamics 365 Commerce Point of Sale (POS) konfigurieren.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 14d8ac93241d05245ad989bcb3cb35aaf8969164d6cfc6010a8e9d426987a1ca
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716299"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Konfigurieren Sie die Azure Active Directory-Authentifizierung für die POS-Anmeldung

[!include [banner](includes/banner.md)]

Dieses Thema erklärt, wie Sie Azure Active Directory (Azure AD) als Authentifizierungsmethode in Microsoft Dynamics 365 Commerce Point of Sale (POS) konfigurieren.

Einzelhändler, die Dynamics 365 Commerce zusammen mit anderen Microsoft Cloud-Diensten wie Microsoft Azure, Microsoft 365 und Microsoft Teams verwenden, möchten in der Regel Azure AD für die zentrale Verwaltung von Anmeldeinformationen für eine sichere und nahtlose Anmeldung in allen Anwendungen verwenden. Um die Azure AD-Authentifizierung für Commerce POS zu verwenden, müssen Sie zuerst Azure AD als Authentifizierungsmethode in der Commerce-Zentrale konfigurieren.

## <a name="configure-pos-authentication-method"></a>Konfigurieren Sie die POS-Authentifizierungsmethode

Um die POS-Authentifizierungsmethode in der Commerce-Zentrale zu konfigurieren, führen Sie diese Schritte aus.
    
1. Gehen Sie zu **Retail und Commerce \> Kanalkonfiguration \> POS-Konfiguration \> POS-Profile \> Funktionalitätsprofile** und wählen Sie ein Funktionalitätsprofil zum Ändern.
1. Wählen Sie im Abschnitt **Anmeldung von POS-Mitarbeitern** auf der Registerkarte **Funktionen** eine gewünschte Option für die Authentifizierungsmethode aus der Dropdown-Liste **Authentifizierungsmethode für die Anmeldung**.

    Die **Anmelde-Authentifizierungsmethode** hat drei Optionen:
    
    - **Personal-ID und Kennwort** – Diese Standardoption erfordert, dass POS-Benutzer eine Personal-ID und ein Kennwort eingeben, um sich am POS anzumelden und um auf die Manager-Überschreibungsfunktion zuzugreifen.
    - **Azure AD ohne Single Sign-On** – Bei dieser Option müssen POS-Benutzer Azure AD-Anmeldeinformationen verwenden, um sich an der Kasse anzumelden und auf die Manager-Override-Funktionalität zuzugreifen. Wenn der POS Client aktualisiert oder neu geöffnet wird, muss der POS-Benutzer Anmeldeinformationen Azure AD angeben, um sich erneut anzumelden.
    - **Azure AD mit Single Sign-On** – Wenn diese Option ausgewählt ist, können sich POS-Benutzer bei Cloud POS (CPOS) mit aktiven Anmeldeinformationen Azure AD anmelden, die von anderen Webanwendungen im selben Webbrowser verwendet werden, oder sich bei Modern POS (MPOS) mit Anmeldeinformationen Azure AD anmelden, die bei Windows angemeldet sind. Beide Methoden lassen die Anmeldung zu, ohne dass die Anmeldeinformationen Azure AD auf dem POS-Anmeldebildschirm eingegeben werden müssen. Für den Zugriff auf die Überschreibungsfunktion des POS-Managers ist jedoch immer noch eine Anmeldung mit Anmeldeinformationen Azure AD erforderlich.

1. Gehen Sie zu **Retail und Commerce > Retail und Commerce IT > Verteilungsplan** und führen Sie den Job **1070 (Kanalkonfiguration)** aus, um die neuesten Einstellungen des Funktionalitätsprofils mit den POS Clients zu synchronisieren.

> [!NOTE]
> - Die Option **Azure AD ohne Single Sign-On** Authentifizierungsmethode ersetzt die Option **Azure Active Directory** in Commerce Version 10.0.18 und früher.
> - Die Azure AD-Authentifizierung erfordert eine aktive Internetverbindung und funktioniert nicht, wenn der POS offline ist.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Verknüpfen Sie Azure AD-Konten mit POS-Benutzern

Um Azure AD als POS-Authentifizierungsmethode zu verwenden, müssen Sie Azure AD-Konten mit POS-Benutzern in der Commerce-Zentrale verknüpfen. 

Um Azure AD-Konten mit POS-Benutzern in der Commerce-Zentrale zu verknüpfen, führen Sie diese Schritte aus.
    
1. Gehen Sie zu **Retail und Commerce > Mitarbeiter > Arbeitskräfte** und öffnen Sie einen Datensatz für eine Arbeitskraft.
1. Wählen Sie im Aktivitätsbereich die Registerkarte **Commerce** und dann unter **Externe Identität** die Option **Vorhandene Identität zuordnen**. 
1. Wählen Sie im Dialogfeld **Existierende externe Identität verwenden** **Mit E-Mail** suchen, geben Sie eine E-Mail-Adresse Azure AD ein und wählen Sie dann **Suchen**.
1. Wählen Sie das Azure AD-Konto, das zurückgegeben wird, und wählen Sie dann **OK**.

Nach den obigen Konfigurationsschritten werden die Felder **Alias**, **UPN** und **Externer Unterbezeichner** auf der Registerkarte **Commerce** der Detailseite des Workers ausgefüllt.

Sie müssen den Job **1060 (Mitarbeiter)** in **Retail und Commerce > Retail und Commerce IT > Verteilungsplan** ausführen, um die neuesten POS-Benutzer- und Azure AD-Kontodaten mit dem Kanal zu synchronisieren.

> [!NOTE]
> Als bewährtes Verfahren wird dringend empfohlen, nach der Aktualisierung von worker-Informationen wie Kennwort, POS-Berechtigung, zugehöriges Azure AD-Konto oder Mitarbeiter-Adressbuch in der Commerce-Zentrale den Auftrag **1060 (Mitarbeiter)** auszuführen, um die neuesten worker-Informationen mit dem Channel zu synchronisieren. Der POS Client kann dann die richtigen Daten für die Benutzerauthentifizierung und die Berechtigungsprüfung abrufen.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>POS-Sperrregister und Abmeldung mit Azure AD-Authentifizierung

Folgendes geschieht, wenn POS so konfiguriert ist, dass die Authentifizierungsmethode Azure AD verwendet wird:

- Die Funktion **Register sperren** wird in der POS-Anwendung nicht verfügbar sein. 
- Die Funktion **Automatisch sperren** verhält sich genauso wie die Funktion **Automatisch abmelden**.
- Wenn der POS-Benutzer **Abmelden** wählt, wird der Benutzer beim nächsten Start des POS aufgefordert, sich mit Anmeldeinformationen Azure AD anzumelden, unabhängig davon, ob die Einzelanmeldung aktiviert ist.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Manager-Überschreibungsfunktionalität mit Azure AD-Authentifizierung

Wenn die Kasse so konfiguriert ist, dass sie die Azure AD-Authentifizierung verwendet, öffnet die Manager-Überschreibungsfunktion ein Dialogfeld, in dem die Azure AD-Anmeldeinformationen des Manager-Benutzers abgefragt werden. Nachdem die Anmeldung des Managers genehmigt wurde, werden die Azure AD-Anmeldeinformationen des Managers nicht mehr verwendet und die Anmeldeinformationen des vorherigen Azure AD-Benutzers werden für die nachfolgenden Vorgänge am POS verwendet.

> [!NOTE]
> - In Commerce-Versionen 10.0.18 und früher unterstützt die Manager-Überschreibungsfunktion nicht die Azure AD. Eine Personal-ID und ein Kennwort sind auch dann erforderlich, wenn die Kasse so konfiguriert ist, dass sie die Authentifizierungsmethode Azure AD verwendet.
> - Wenn Sie CPOS mit dem Safari-Webbrowser auf einem Apple iOS-Gerät verwenden, müssen Sie zuerst **Pop-ups blockieren** in den Safari-Einstellungen deaktivieren, damit die Manager-Override-Funktion mit der Azure AD-Authentifizierung funktioniert. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Bewährte Verfahren zur Sicherheit für Azure AD-POS-Authentifizierung auf gemeinsam genutzten Geräten

Viele Einzelhändler legen ihre Umgebung im Ladengeschäft so fest, dass mehrere Benutzer von einem gemeinsamen physischen Gerät auf die POS-Anwendung zugreifen müssen. In diesem Zusammenhang bietet die einmalige Anmeldung zwar eine bequeme und nahtlose Authentifizierung, sie kann aber auch eine Sicherheitslücke erstellen, bei der der aktuelle POS-Benutzer möglicherweise nicht erkennt, dass die Anmeldeinformationen eines anderen Benutzers verwendet werden, um Transaktionen oder Vorgänge im POS durchzuführen. Bevor Sie die Kasse so konfigurieren, dass sie die Azure AD-Authentifizierungsmethode verwendet, sollten Sie unbedingt Ihre Sicherheitsrichtlinien und die Anmeldeeinstellungen des gemeinsamen Geräts überprüfen, um zu entscheiden, welche Option am besten geeignet ist.

- Wenn Ihre Einzelhandelsumgebung ein gemeinsames Konto (z.B. ein lokales Konto) für die Anmeldung am physischen Gerät verwendet, wird empfohlen, die Option **Azure AD ohne Single Sign-On** zu verwenden. Dadurch wird sichergestellt, dass jeder POS-Benutzer explizit Anmeldeinformationen Azure AD angibt, um sich am POS anzumelden.
- Wenn Ihre Einzelhandelsumgebung erfordert, dass die Mitarbeiter ihre eigenen Azure AD-Konten verwenden, um sich an der Kasse und dem zugehörigen physischen Gerät anzumelden, wird empfohlen, die Option **Azure AD mit Single Sign-On** zu verwenden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine Arbeitskraft konfigurieren](tasks/worker.md)

[Ein Einzelhandelsfunktionsprofil erstellen](retail-functionality-profile.md)


[Erweiterte Anmeldungsfunktionen für MPOS und Cloud POS einrichten](extended-logon.md)

[Bewährte Verfahren zur Sicherheit von Cloud POS in gemeinsam genutzten Umgebungen](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
