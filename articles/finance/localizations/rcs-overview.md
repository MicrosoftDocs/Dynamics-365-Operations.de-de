---
title: Regulatory Configuration Service
description: Dieses Thema bietet einen Überblick über die Funktionen des Regulatory Configuration Service (RCS) und erläutert den Zugriff auf den Dienst.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216561"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Der Regulatory Configuration Service (RCS) ist ein eigenständiger Designer- und Lebenszyklusverwaltungsdienst für No-Code-/Low-Code-Globalisierungsfunktionen. Mit RCS können Beteiligte der Globalisierung wichtige Globalisierungsbereiche wie Steuern, elektronische Rechnungsstellung, behördliche Berichterstattung, Bank- und Geschäftsdokumente erweitern und anpassen, ohne Entwickler einbeziehen zu müssen. Dieser No-Code/Low-Code-Globalisierungsansatz macht die Globalisierung einfacher, schneller und kostengünstiger zu erstellen oder zu erweitern.

RCS bietet folgende Funktionen:

- Unterstützung aller Funktionen, die durch die elektronische Berichterstellung (EB) bereitgestellt werden.
- Voraussetzung für die Konfiguration neuer Globalisierungs-Microservices.
- Unterstützung der elektronischen Rechnungsstellung. Weitere Informationen finden Sie unter [Elektronische Rechnungsstellung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Unterstützung der Steuerberechnung. Weitere Informationen finden Sie unter [Steuerdienst](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Unterstützung für neue Funktionen für Globalisierungsfunktionen, die das Lebenszyklusmanagement von Mehrkomponentenfunktionen vereinfachen und zusätzliche Funktionen zum Konfigurieren von Aktionen und zum Einrichten von Funktionsparametern bieten. Weitere Informationen finden Sie unter [Regulatory Configuration Service – vereinfachtes Management von Globalisierungsfunktionen für Globalisierungsdienste](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Unterstützung für die zentrale Veröffentlichung, Speicherung und Freigabe von benutzerdefinierten Konfigurationen im globalen Repository, um die Konfigurationsverwaltung zu vereinfachen, ohne dass die Verwendung von Microsoft Dynamics Lifecycle Services (LCS) erforderlich ist.

## <a name="access-rcs"></a>Zugriff auf RCS

Sie können sich über die [Seite „Regulatory Configuration Service“](https://marketing.configure.global.dynamics.com/) für RCS anmelden oder sich bei RCS anmelden.

![RCS-Registrierung/-Anmeldung](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Überprüfen und akzeptieren Sie auf der Seite **Regulatory Configuration Service** die ergänzenden Nutzungsbedingungen für den Dienst und wählen Sie dann eine der folgenden Schaltflächen aus:

- **Registrieren**, wenn Sie den Dienst zum ersten Mal nutzen und eine geschäftliche E-Mail-Adresse verwenden, um Ihrem Unternehmen eine Dienstumgebung bereitzustellen
- **Anmelden**, wenn Sie sich zuvor schon für den Dienst angemeldet haben und auf Ihre Organisationsumgebung zugreifen möchten

## <a name="regional-availability"></a>Regionale Verfügbarkeit

RCS ist allgemein in folgenden Regionen verfügbar:

- Vereinigte Staaten
- Indien
- Frankreich
- Europa

Eine vollständige Liste der Regionen finden Sie unter [Dynamics 365 und Power Platform: Verfügbarkeit, Datenstandort, Sprache und Lokalisierung](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>RCS-Standardunternehmen

Die in RCS verwendete Designzeitfunktionalität wird von allen Unternehmen gemeinsam genutzt. Es gibt keine unternehmensspezifische Funktion. Daher empfehlen wir Ihnen, ein Unternehmen **DAT** in Ihrer RCS-Umgebung zu verwenden.

In einigen Szenarien möchten Sie jedoch möglicherweise, dass ER-Formate Parameter verwenden, die sich auf eine bestimmte juristische Person beziehen. Nur in diesen Szenarien sollten Sie den standardmäßigen Firmenumschalter verwenden. Ein Beispiel finden Sie unter [ER-Format zur Verwendung von Parametern konfigurieren, die pro juristischer Person angegeben werden](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Zugehörige RCS-Dokumentation

Weitere Informationen zu den zugehörigen Komponenten finden Sie in den folgenden Themen:

- **RCS:**

    - [EB-Konfigurationen in RCS erstellen und in das globale Repository hochladen](rcs-global-repo-upload.md)

- **Globales Repository:**

    - [Eine EB-Konfiguration erstellen und in das globale Repository hochladen](rcs-global-repo-upload.md)
    - [Konfiguration im globalen Repository freigeben](rcs-global-repo-share-configuration.md)
    - [Verbesserte Filterung im globalen Repository](enhanced-filtering-global-repo.md)
    - [EB-Konfigurationen aus dem globalen Repository herunterladen](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Konfigurationen im globalen Repository einstellen](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)-Speichereinstellung](rcs-lcs-repo-dep-faq.md)

- **Globalisierungsfunktion:**

    - [Regulatory Configuration Service (RCS) – Globalisierungsfunktion](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>Problembehandlung bei der RCS-Registrierung

Wenn Sie sich über die Serviceseite bei RCS anmelden, tritt möglicherweise ein Problem auf, das mit Azure Active Directory (Azure AD) zusammenhängt. Die Fehlermeldung, die Sie erhalten, weist darauf hin, dass die Registrierung für RCS derzeit deaktiviert ist und aktiviert werden muss, bevor Sie den Registrierungsprozess abschließen können.

![Fehlermeldung bei RCS-Registrierung](media/01_RCSSignUpError.jpg)

Das Problem tritt auf, weil Sie daran gehindert werden, sich für Ad-hoc-Abonnements anzumelden, und die Eigenschaft `AllowAdHocSubscriptions` in Ihrem Mandanten aktiviert sein muss. 

- Wenn Ihre IT-Abteilung die Azure-Mandanten Ihrer Organisation verwaltet, wenden Sie sich an diese Abteilung, um das Problem zu melden.
- Wenn Sie für die Verwaltung Ihrer Azure-Mandanten verantwortlich sind, können Sie die Probleme beheben, indem Sie die Schritte in [Wozu dient die Self-Service-Registrierung in Azure Active Directory?](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
