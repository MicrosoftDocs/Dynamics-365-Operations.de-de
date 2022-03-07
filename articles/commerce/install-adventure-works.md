---
title: Adventure Works-Design installieren
description: In diesem Thema wird beschrieben, wie Sie das Adventure Works-Design in Microsoft Dynamics 365 Commerce installieren.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ad704c6c3b95abcfd52e449a0ffbb4b82b236498ae8d2775c4e65811de3ef503
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763835"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works-Design installieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie das Adventure Works-Design in Microsoft Dynamics 365 Commerce installieren. 

> [!IMPORTANT]
> Das Adventure Works-Design und die neuen Module stehen ab der Dynamics 365 Commerce-Version 10.0.20 zur Verfügung. Sie sind erhältlich ab Microsoft AppSource.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie das Adventure Works-Design installieren, müssen Sie über eine Dynamics 365 Commerce Umgebung (Commerce Version 10.0.20 oder höher) verfügen, die Retail Cloud Scale Unit (RCSU), das Commerce Online Software Development Kit (SDK) und die Commerce-Modulbibliothek enthält. Informationen zur Installation des Commerce SDK und der Modulbibliothek finden Sie unter [SDK- und Modulbibliothek-Updates](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Installationsschritte

### <a name="install-the-adventure-works-theme-in-your-application"></a>Installieren Sie das Adventure Works-Design in Ihrer Anwendung

Das Adventure Works-Themenpaket steht im **dynamics365-Commerce** Feed als **@msdyn365-commerce-theme/adventureworks-theme-Kit** zur Verfügung. Obwohl das Adventure Works-Designpaket Teil dieses Feeds ist, befindet es sich jedoch unter einem anderen Namespace. Daher müssen Sie diese Schritte ausführen, um Registrierungseinträge für den Namespace hinzuzufügen.

1. Aktualisieren Sie die **.npmrc** Datei so, dass sie den folgenden Registrierungseintrag enthält (falls der Eintrag nicht bereits enthalten ist):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Aktualisieren Sie die **.yarnrc** Datei so, dass sie den folgenden Registrierungseintrag enthält (falls der Eintrag nicht bereits enthalten ist):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Führen Sie den folgenden Befehl an der Eingabeaufforderung aus, um das Paket in Ihrer lokalen Umgebung zu installieren. Dieser Befehl aktualisiert automatisch die Datei package.json, sodass sie die Abhängigkeit enthält.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

In der **package.json** Datei sollten Sie die Theme-Version auf eine bestimmte Version aktualisieren.

> [!IMPORTANT]
> - Die Designversion sollte mit der Version der Modulbibliothek übereinstimmen, um sicherzustellen, dass alle Funktionen wie erwartet funktionieren. 
> - Die Mindestversion für die Commerce-Modulbibliothek und das SDK sollte 10.0.20 (9.31) sein. 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Fügen Sie die Schriftartdateien für das Adventure Works-Design hinzu

Nachdem das Adventure Works-Design in Ihrer App installiert wurde, müssen Sie die dafür erforderlichen Schriftartdateien hinzufügen. Um diesen Schritt abzuschließen, kopieren Sie alle Schriftartdateien von **\node_modules@msdyn365-commerce-theme\adventureworks-theme-Kit\src\modules\adventureworks\public\webfonts** zum öffentlichen Verzeichnispfad der Partneranwendung **\öffentlich\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Legen Sie die Ressourcen für das AdventureWorks-Design fest

Der nächste Schritt besteht darin, die erforderliche Standardressource für das Design zu aktualisieren. Um diesen Schritt abzuschließen, kopieren Sie den Inhalt aus der Datei global.json unter **\node_modules@msdyn365-commerce-theme\adventureworks-theme-Kit\src\modules\adventureworks\r Ressourcen\Module** zur Partneranwendung global.json Datei unter **\src\resources\modules**. Wenn das **\src\resources** Zielverzeichnis nicht vorhanden ist, kann es vollständig aus dem **\node_modules@msdyn365-commerce-theme\adventureworks-theme-Kit\src\modules\adventureworks** Quellverzeichnis zum **\src** Zielverzeichnis kopiert werden.

### <a name="pull-updates-and-validate-the-theme"></a>Ziehen Sie Updates und validieren Sie das Thema

Informationen zum Abrufen des neuesten SDKs, der Modulbibliothek und anderer Abhängigkeitsupdates finden Sie im Abschnitt Updates abrufen unter [SDK- und Modulbibliothek-Updates](e-commerce-extensibility/sdk-updates.md#pull-updates).

Nachdem die neuesten Abhängigkeiten heruntergezogen wurden, können Sie den **yarn start** Befehl ausfühen, um den Knoten-Server in Ihrer Entwicklungsumgebung zu starten und das neue Adventure Works-Design zu testen. Durchsuchen Sie die Anwendung lokal mithilfe des Abfragezeichenfolgenparameters `?theme=adventureworks` (zum Beispiel,`https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[AdventureWorks-Design](adventure-works-theme.md)

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[SDK- und Modulbibliotheksupdates](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
