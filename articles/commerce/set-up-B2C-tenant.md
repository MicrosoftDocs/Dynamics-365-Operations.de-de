---
title: Einen B2C Mandanten in Commerce einrichten
description: In diesem Artikel wird beschrieben, wie Sie Ihren Azure Active Directory (Azure AD) Business-to-Consumer-Mandanten (B2C) für die Authentifizierung von Benutzerseiten in Microsoft Dynamics 365 Commerce einrichten.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785136"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Einen B2C Mandanten in Commerce einrichten

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Ihren Azure Active Directory (Azure AD) Business-to-Consumer-Mandanten (B2C) für die Authentifizierung von Benutzerseiten in Dynamics 365 Commerce einrichten.

Dynamics 365 Commerce Verwendet Azure AD B2C zur Unterstützung von Benutzeranmeldeinformationen und Authentifizierungsabläufen. Ein Benutzer kann sich über diese Flows anmelden, sich anmelden und sein Kennwort zurücksetzen. Azure AD B2C speichert vertrauliche Benutzerauthentifizierungsinformationen wie Benutzername und Kennwort. Der Benutzerdatensatz im B2C-Mandanten speichert entweder einen lokalen B2C-Kontodatensatz oder einen B2C-Datensatz für Anbieter sozialer Identität. Diese B2C-Datensätze werden mit dem Kundendatensatz in der Commerce-Umgebung verknüpft.

> [!WARNING] 
> Azure AD B2C stellt alte (veraltete) Benutzerströme bis zum 1. August 2021 ein. Daher sollten Sie planen, Ihre Benutzerflows auf die neue empfohlene Version zu migrieren. Die neue Version bietet Featureparität und neue Funktionen. Die Modulbibliothek für die Commerce-Version 10.0.15 oder höher sollte mit den empfohlenen B2C-Benutzerflows verwendet werden. Weitere Informationen finden Sie unter [Benutzerflows in Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce-Evaluierungsumgebungen sind zu Demonstrationszwecken mit einem vorinstallierten Azure AD B2C-Mandanten ausgestattet. Für Evaluierungsumgebungen müssen Sie Ihren eigenen Azure AD B2C-Mandanten nicht wie unten beschrieben herunterladen.

> [!TIP]
> Mit Azure AD Identitätsschutz und bedingtem Zugriff können Sie die Benutzer Ihrer Website weiter schützen und die Sicherheit Ihrer Azure AD B2C Mandanten erhöhen. Um die Funktionalitäten zu überprüfen, die für Azure AD B2C Premium P1 und Premium P2 Mandanten verfügbar sind, siehe [Identitätsschutz und bedingter Zugriff für Azure AD B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Voraussetzungen für die dynamische Umgebung

Bevor Sie beginnen, stellen Sie sicher, dass Ihre Dynamics 365 Commerce Umgebung und der E-Commerce-Kanal entsprechend konfiguriert werden, indem die folgenden Voraussetzungen erfüllt sind.

- Legen Sie die POS-Operationen **AllowAnonymousAccess** Wert auf 1 in der Commerce headquarters fest:
    1. Gehen Sie zu **POS Vorgänge**.
    1. Im Vorgangsraster klicken Sie mit der rechten Maustaste auf das Raster und wählen **Personalisieren**.
    1. Wählen Sie **Feld hinzufügen zu**.
    1. Wählen Sie in der Liste der verfügbaren Spalten die **AllowAnonymousAccess** Spalte, um es hinzuzufügen.
    1. Wählen Sie **Aktualisieren**.
    1. Für den **612** Vorgang Kunden hinzufügen ändern Sie **AllowAnonymousAccess** auf 1.
    1. Führen Sie den **1090 (Register)** Einzelvorgang aus.
- Legen Sie das Nummernkreis-Kundenkonto Attribut **Manuell** auf **Nein** in der Handelszentrale fest:
    1. Gehen Sie zu **Einzelhandel und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Commerce-Parameter**.
    1. Wählen Sie **Nummernkreise**.
    1. In der **Kundenkonto** Zeile, doppelklicken Sie auf den **Nummernfolgecode** Wert.
    1. Im Inforegister **Allgemein** der Zahlenfolge legen Sie **Manuell** auf **Nein** fest.

Nach der Bereitstellung Ihrer Dynamics 365 Commerce Umgebung wird auch empfohlen, in der Umgebung die [Seed-Daten zu initialisieren](enable-configure-retail-functionality.md).

## <a name="next-steps"></a>Nächste Schritte

Um mit dem Einrichten eines B2C-Mandanten in Commerce fortzufahren, fahren Sie fort mit [Erstellen oder verknüpfen Sie mit einem vorhandene Azure AD B2C-Mandant im Azure-Portal](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erstellen oder Verknüpfen eines vorhandenen Azure AD B2C-Mandanten im Azure-Portal](create-link-aad-b2c-tenant.md)

[B2C Anwendungen erstellen](create-b2c-app.md)

[Benutzerflussrichtlinien erstellen](create-user-flow-policies.md)

[Anbieter sozialer Identität hinzufügen (optional)](add-social-identity-providers.md)

[Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md)

[Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Weitere B2C Informationen](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
