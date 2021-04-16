---
title: Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren
description: In diesem Thema wird beschrieben, wie die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams aktiviert wird.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842668"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams aktiviert wird.

Um Teams mit Informationen aus Dynamics 365 Commerce zu versorgen und die Funktionen der Aufgabenverwaltung zwischen Teams und der Point-of-Sale-Anwendung (POS-Anwendung) zu synchronisieren, müssen Sie die Integrationsfunktionen in der Commerce-Zentralverwaltung aktivieren.

> [!NOTE]
> Wenn Sie die Teams-Integration aktivieren, stimmen Sie zu, Ihre Daten für Teams freizugeben. Daten, die mit Teams geteilt werden, befinden sich möglicherweise in einem anderen Land als Ihre Commerce-Daten und unterliegen möglicherweise anderen Compliance-Standards. Weitere Informationen dazu, finden Sie unter [Microsoft Trust Center](https://www.microsoft.com/trust-center). Informationen zu den Microsoft-Datenschutzrichtlinien finden Sie in den [Microsoft-Datenschutzbestimmungen](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Teams-Integration aktivieren

Bevor Sie die Microsoft Teams-Integration in Commerce aktivieren können, müssen Sie die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal registrieren.

Führen Sie die folgenden Schritte aus, um die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal zu registrieren.

1. Befolgen Sie die Schritte in [Schnellstart: Registrieren einer Anwendung bei Microsoft Identity Platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app), um die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal zu registrieren.
1. Kopieren Sie den Wert **Anwendungs-ID (Client-ID)** aus der Seite **Überblick** der registrierten App. Sie werden diesen Wert verwenden, um die Teams-Integration in der Commerce-Zentralverwaltung zu aktivieren.
1. Kopieren Sie den Zertifikatswert, der beim [Hinzufügen eines Zertifikats](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in Schritt 1 eingegeben wurde. Das Zertifikat wird auch als öffentlicher Schlüssel oder Anwendungsschlüssel bezeichnet. Sie werden diesen Wert verwenden, um die Teams-Integration in der Commerce-Zentralverwaltung zu aktivieren.

Führen Sie die folgenden Schritte aus, um die Teams-Integration in der Commerce-Zentralverwaltung zu aktivieren.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie die Option **Microsoft Teams-Integration aktivieren** auf **Ja** fest.
1. Geben Sie in den Feldern **Anwendungs-ID** und **Anwendungsschlüssel** die Werte ein, die Sie erhalten haben, als Sie die Teams-Anwendung im Azure-Portal registriert haben.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Die folgende Abbildung zeigt ein Beispiel für die Konfiguration der Teams-Integration in der Commerce-Zentralverwaltung.

![Konfiguration der Teams-Integration in der Commerce-Zentralverwaltung](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Teams-Integration deaktivieren

Führen Sie die folgenden Schritte aus, um die Microsoft Teams-Integration in der Commerce-Zentralverwaltung zu deaktivieren.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
3. Legen Sie die Option **Microsoft Teams-Integration aktivieren** auf **Nein** fest.
4. Löschen Sie die Werte aus den Feldern **Anwendungs-ID** und **Anwendungsschlüssel**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

> [!NOTE]
> Nachdem Sie die Teams-Integration in Commerce deaktiviert haben, werden auf den POS-Terminals keine Aufgaben mehr angezeigt, die in der Teams-Anwendung veröffentlicht wurden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick Integration Dynamics 365 Commerce und Microsoft Teams](commerce-teams-integration.md)

[Microsoft Teams aus Dynamics 365 Commerce bereitstellen](provision-teams-from-commerce.md)

[Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren](synchronize-tasks-teams-pos.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind](map-stores-existing-teams.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ](teams-integration-faq.md)
