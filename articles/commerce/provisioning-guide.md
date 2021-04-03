---
title: Eine Dynamics 365 Commerce-Evaluierungsumgebung bereitstellen
description: In diesem Thema wird erläutert, wie eine Evaluierungsumgebung in Microsoft Dynamics 365 Commerce bereitgestellt wird.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a57cc02c6d62f288f14b65191c2f4927a019963c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478163"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Eine Dynamics 365 Commerce-Evaluierungsumgebung bereitstellen

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie eine Evaluierungsumgebung in Microsoft Dynamics 365 Commerce bereitgestellt wird.

Bevor Sie beginnen, empfehlen wir, dass Sie einen kurzen Blick in dieses Thema werfen, um eine Vorstellung davon zu bekommen, was der Prozess erfordert.

> [!NOTE]
> Commerce-Auswertungsumgebungen sind nicht allgemein verfügbar und sie werden Partner und Kunden auf Anfrage gewährt. Für weitere Informationen wenden Sie sich an den Ansprechpartner Ihres Microsoft-Partners.

Um eine Commerce-Evaluierungsumgebung erfolgreich bereitzustellen, müssen Sie ein Projekt mit einem bestimmten Produktnamen und -Typ erstellen. Bei der Umgebung und der Commerce Scale Unit (CSU) gibt es auch einige spezifische Parameter, die Sie verwenden müssen, um später E-Commerce bereitstellen zu können. In den Anweisungen in diesem Thema werden alle Schritte, die zum Ausführen der Bereitstellung erforderlich sind, sowie die Parameter, die Sie verwenden müssen, beschrieben.

Nach der erfolgreichen Bereitstellung Ihrer Commerce-Evaluierungsumgebung müssen Sie einige Schritte nach der Bereitstellung ausführen, um Ihre Vorschauumgebung vorzubereiten. Einige Schritte sind optional, je nachdem, welche Aspekte des Systems Sie bewerten möchten. Sie können die optionalen Schritte später jederzeit ausführen.

Informationen zum Konfigurieren Ihrer Commerce-Evaluierungsumgebung nach deren Bereitstellung finden Sie unter [Konfigurieren Sie eine Commerce-Evaluierungsumgebung](cpe-post-provisioning.md). Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Evaluierungsumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Evaluierungsumgebung konfigurieren](cpe-optional-features.md).

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen müssen erfüllt sein, damit Sie Ihre Commerce-Evaluierungsumgebung bereitstellen können:

- Sie wurden in das Auswertungsprogramm aufgenommen und Ihnen wurde die Kapazität für eine Auswertungsumgebung gewährt.
- Sie haben Zugriff auf das Microsoft Dynamics Lifecycle Services-Portal (LCS).
- Sie sind ein bestehender Partner oder Kunde von Microsoft Dynamics 365 und können ein Dynamics 365 Commerce-Projekt erstellen.
- Sie haben Administratorzugriff auf Ihr Microsoft Azure-Abonnement, oder Sie stehen in Kontakt mit einem Abonnementadministrator, der Sie bei Bedarf unterstützen kann.
- Ihnen liegt Ihre Azure Active Directory-Mandanten-ID (Azure AD) vor.
- Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als E-Commerce-Systemadministrator-Gruppe verwendet wird, und Ihnen liegt deren ID vor.
- Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als Bewertungs- und Prüfungsmoderatorgruppe verwendet wird, und Ihnen liegt deren ID vor. (Diese Sicherheitsgruppe kann mit der Administratorgruppe des E-Commerce-Systems identisch sein.)

Beachten Sie, dass diese Liste nicht vollständig ist. Sollten Probleme auftreten, wenden Sie sich an Ihren Microsoft-Partner, um Unterstützung zu erhalten.

## <a name="provision-your-commerce-evaluation-environment"></a>Bereitstellen Ihrer Commerce-Evaluierungsumgebung

In diesen Verfahren wird erläutert, wie eine Commerce-Evaluierungsumgebung bereitgestellt wird. Nachdem Sie sie erfolgreich abgeschlossen haben, kann die Commerce-Evaluierungsumgebung konfiguriert werden. Alle hier beschriebenen Aktivitäten finden im LCS-Portal statt.

### <a name="create-a-new-project"></a>Neues Projekt erstellen

Gehen Sie folgendermaßen vor, um ein neues Projekt in LCS zu erstellen.

1. Wählen Sie auf der LCS-Startseite das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.
1. Führen Sie im rechten Bereich einen der folgenden Schritte aus:

    - Wenn Sie ein Partner sind, wählen Sie **Migrieren, Erstellen von Lösungen und Kennenlernen von** aus.
    - Wenn Sie ein Debitor sind, wählen Sie **Künftige Presales** aus.

1. Geben Sie einen Namen, eine Beschreibung und die Branche ein.
1. Wählen Sie im Feld **Produktname** die Option **Dynamics 365 Commerce** aus.
1. Wählen Sie im Feld **Produktversion** die Option **Dynamics 365 Commerce** aus.
1. Wählen Sie im Feld **Methode** **Dynamics Retail-Implementierungsmethode** aus.
1. Optional: Sie können Rollen und Benutzer aus einem vorhandenen Projekt importieren.
1. Wählen Sie **Erstellen** aus. Die Projektansicht wird angezeigt.

### <a name="add-the-azure-connector"></a>Azure-Connector hinzufügen

Führen Sie die folgenden Schritte aus, um den Azure Connector zu Ihrem LCS-Projekt hinzuzufügen [Schließen Sie den Onboarding-Prozess für Azure Resource Manager (ARM) ab](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).

### <a name="deploy-the-environment"></a>Bereitstellen der Umgebung

Gehen Sie folgendermaßen vor, um die Umgebung bereitzustellen.

> [!NOTE]
> Möglicherweise müssen Sie die Schritte 6, 7 und/oder 8 nicht ausführen, da Seiten mit einer einzelnen Option übersprungen werden. Wenn Sie sich in der Ansicht **Umgebungsparameter** befinden, bestätigen Sie, dass der Text **Dynamics 365 Commerce – Demo (10.0.* x* mit Plattform-Update *xx*)** direkt über dem Feld **Umgebungsname** angezeigt wird. Weitere Details finden Sie in der Abbildung, die nach Schritt 8 angezeigt wird.

1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Wählen Sie **Hinzufügen** aus, um eine Umgebung hinzuzufügen.
1. Wählen Sie im Feld **Anwendungsversion** die aktuellste Version aus. Wenn Sie aus einem bestimmten Grund eine andere Anwendungsversion als die aktuellste auswählen müssen, wählen Sie keine Version vor **10.0.14** aus.
1. Verwenden Sie im Feld **Plattformversion** die Plattformversion, die automatisch für die von Ihnen ausgewählte Anwendungsversion ausgewählt wird. 

    ![Auswählen von Anwendungs- und Plattformversionen](./media/project1.png)

1. Wählen Sie **Weiter**.
1. Wählen Sie **Demo** als Umgebungstopologie aus.

    ![Auswählen der Umgebungstopologie 1](./media/project2.png)

1. Geben Sie auf der Seite **Umgebung bereitstellen** einen Umgebungsnamen ein. Lassen Sie die erweiterten Einstellungen unverändert.

    ![Bereitstellen der Umgebungsseite](./media/project4.png)

1. Passen Sie die VM-Größe nach Bedarf an. (Wir empfehlen die VM-Lagermengeneinheit \[SKU\] **D13 v2**.)
1. Überprüfen Sie die Preis- und Lizenzbedingungen und aktivieren Sie das Kontrollkästchen, um anzuzeigen, dass Sie diesen zustimmen.
1. Wählen Sie **Weiter**.
1. Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Bereitstellen** aus. Sie werden zur Ansicht **In der Cloud gehostete Umgebungen** weitergeleitet, und Ihre Umgebung sollte in der Liste angezeigt werden.

    Ihre angeforderte Umgebung wird so angezeigt, dass sie in die Warteschlange gestellt und anschließend bereitgestellt wurde. Es wird einige Zeit dauern, bis die Arbeitsabläufe in der Umgebung abgeschlossen sind. Versuchen Sie es daher nach ungefähr sechs bis neun Stunden erneut.

1. Stellen Sie vor dem Fortfahren sicher, dass der Status Ihrer Umgebung **Bereitgestellt** lautet.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Initialisieren der Commerce Scale Unit (Cloud)

Führen Sie folgende Schritte aus, um die CSU zu initialisieren.

1. Wählen Sie in der Ansicht **In der Cloud gehostete Umgebungen** Ihre Umgebung in der Liste aus.
1. Wählen Sie in der Umgebungsansicht rechts die Option **Vollständige Details** aus. Die Ansicht zu Umgebungsdetails wird angezeigt.
1. Wählen Sie unter **Umgebungsfunktionen** die Option **Verwalten** aus.
1. Wählen Sie auf der Registerkarte **Commerce** die Option **Initialisieren** aus. Die Ansicht zu CSU-Initialisierungsparametern wird angezeigt.
1. Wählen Sie im Feld **Region** die Region aus, die mit der Region identisch ist, in der Sie die Umgebung bereitgestellt haben.
1. Lassen Sie das Feld **Version** wie es ist.
1. Wählen Sie **Initialisieren** aus.
1. Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Ja** aus. In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **Commerce** ausgewählt ist. Ihre CSU wurde für die Bereitstellung in die Warteschlange gestellt.
1. Stellen Sie vor dem Fortfahren sicher, dass Ihr CSU-Status **Erfolgreich** lautet. Die Initialisierung dauert ungefähr zwei bis fünf Stunden.

Wenn Sie den Link **Verwalten** in der Ansicht „Umgebungsdetails“ nicht finden können, wenden Sie sich an Ihren Microsoft-Kontakt, um Unterstützung zu erhalten.

Während des Bereitstellungsprozesses wird möglicherweise die folgende Fehlermeldung angezeigt:

> Auswertungsumgebungen (Demo/Test) müssen die Anwendung \<application ID\> für den Konnektor der Skalierungseinheit in der Zentralverwaltung registrieren.

Wenn die CSU-Initialisierung fehlschlägt und Sie diese Fehlermeldung erhalten, notieren Sie sich die Anwendungs-ID, bei der es sich um einen global eindeutigen Bezeichner (GUID) handelt, und befolgen Sie die Schritte im nächsten Abschnitt, um die CSU-Bereitstellungsanwendung in der Commerce-Zentralverwaltung zu registrieren.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>Registrieren Sie die CSU-Bereitstellungsanwendung in der Commerce-Zentrale (falls erforderlich)

Führen Sie folgende Schritte aus, um die CSU-Bereitstellungsanwendung in der Commerce-Zentralverwaltung zu registrieren (falls erforderlich).

1. Wechseln Sie in Commerce-Zentralverwaltung zu **Systemverwaltung \> Einrichtung \> Azure Active Directory-Anwendungen**.
1. Geben Sie in der Spalte **Kunden-ID** die Anwendungs-ID aus der CSU-Initialisierungsfehlermeldung ein, die Sie erhalten haben.
1. Geben Sie in der Spalte **Name** einen beliebigen beschreibenden Text ein (z. B. **CSU Eval**).
1. Geben Sie in der Spalte **Benutzer-UD** **RetailServiceAccount** ein.
1. Wiederholen Sie die CSU-Initialisierung und -Bereitstellung über LCS.

### <a name="initialize-e-commerce"></a>E-Commerce initialisieren

Führen Sie folgende Schritte aus, um e-Commerce zu initialisieren.

1. Prüfen Sie auf der Registerkarte **E-Commerce** die Evaluierungseinwilligung und wählen Sie dann **Einrichten** aus.
1. Geben Sie im Feld **E-Commerce-Evaluierungsname** einen Namen ein. Beachten Sie, dass dieser Name in einigen URLs sichtbar ist, die auf Ihre E-Commerce-Instanz verweisen.
1. Wählen Sie im Feld **Commerce Scale Unit Name** Ihre CSU in der Liste aus. (Die Liste sollte nur eine Option haben.)

    Das Feld **E-Commerce-Geografie** wird automatisch eingestellt.

1. Wählen Sie **Weiter** aus, um fortzufahren.
1. Geben Sie im Feld **Unterstützte Hostnamen** eine gültige Domäne, wie `www.fabrikam.com`, ein.
1. Geben Sie in das Feld **AAD-Sicherheitsgruppe für Systemadministrator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen. Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.
1.  Geben Sie in das Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen. Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.
1. Lassen Sie die Option **Bewertungs- und Prüfungsdienst aktivieren** auf **Ja** festgelegt.
1. Wählen Sie **Initialisieren** aus. In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **E-Commerce** ausgewählt ist. Die E-Commerce-Initialisierung wurde gestartet.
1. Warten Sie, bevor Sie fortfahren, bis Ihr E-Commerce-Initialisierungsstatus **Initialisierung erfolgreich** lautet.
1. Notieren Sie sich unten rechts im Bereich **Links** die URLs für die folgenden Links:

    * **E-Commerce-Website** – Der Link zum Stammverzeichnis Ihrer E-Commerce-Website.
    * **Commerce-Site-Builder** – Der Link zum Site-Management-Tool.

## <a name="next-steps"></a>Nächste Schritte

Um den Prozess zum Bereitstellen und Konfigurieren Ihrer Commerce-Evaluierungsumgebung fortzusetzen, schauen Sie sich [Konfigurieren Sie eine Commerce-Evaluierungsumgebung](cpe-post-provisioning.md) an.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Dynamics 365 Commerce-Evaluierungsumgebung – Übersicht](cpe-overview.md)

[Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung](cpe-post-provisioning.md)

[BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren](cpe-bopis.md)

[Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren](cpe-optional-features.md)

[Dynamics 365 Commerce-Evaluierungsumgebung – FAQ](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (Cloud)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-Portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
