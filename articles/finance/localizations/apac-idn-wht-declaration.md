---
title: Quellensteuerbericht für Indonesien
description: In diesem Artikel wird erläutert, wie Sie die Quellensteuererklärungen für Indonesien konfigurieren und generieren.
author: AdamTrukawka
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.search.scope: ''
ms.openlocfilehash: 732db563532ebc46c7b9fc69c2aaa128640084f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282434"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Quellensteuerbericht für Indonesien (ID-00005)

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie die PPH-Quellensteuerdatei einrichten und generieren, die juristische Personen in Indonesien verwenden, um Quellentransaktionen in der e-Bupot-Anwendung zu melden.

Die indonesische Steuerbehörde (DGT) bestimmt, dass steuerpflichtige Unternehmer (PKP), die bei KPP Pratama als Steuereinbehalter/Eintreiber der Einkommensteuer (PPh) registriert sind, Artikel 23 und/oder Artikel 26 elektronisch melden müssen, indem sie die Einkommensteuererklärung Artikel 23 und 26 unter Verwendung von die e-Bupot-Anwendung. 

- **Artikel 23** – Der Bericht umfasst alle Quellensteuertransaktionen von Lieferanten, bei denen der Länder-/Regionscode der primären Adresse der Code für Indonesien ist.
- **Artikel 26** – Der Bericht umfasst alle Quellensteuertransaktionen von Lieferanten, bei denen der Länder-/Regionscode der primären Adresse nicht der Code für Indonesien ist.

## <a name="prerequisites"></a>Voraussetzungen

- Die primäre Adresse der juristischen Person muss in Indonesien liegen.
- Die Funktion **Vergütungsaufstellung** muss im Arbeitsbereich **Globale Quellensteuer** aktiviert werden. Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="download-electronic-reporting-configurations"></a>Elektronische Berichtskonfigurationen herunterladen

Die Generierung einer Importdatei basiert auf Konfigurationen des elektronischen Berichtswesens (ER). Weitere Informationen zu den Funktionen und Konzepten der konfigurierbaren Berichterstellung finden Sie unter [Elektronische Berichterstattung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Befolgen Sie für Produktions- und UAT-Umgebungen (Benutzerakzeptanztest) die Anweisungen im Thema: [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Um die Importdatei zu generieren, laden Sie die folgenden Konfigurationen aus dem Repository hoch:

- **Steuererklärung model.version.93.xml** oder eine neuere Version
- **Steuererklärungsmodell mapping,version.93.153.xml** oder eine neuere Version
- **WHT PPh-Schemaimport (ID).Version.93.14** oder eine neuere Version

## <a name="set-up-general-ledger-parameters"></a>Einrichten der Hauptbuchparameter

1. Wechseln Sie zu **Steuer** \> **Einrichtung** \> **Allgemeine Ledger-Parameter**.
2. Auf der **Quellensteuer**-Registerkarte im Feld **Quellensteuer-Erklärungsformularzuordnung** wählen Sie **WHT PPh Schemaimport (ID)** aus. 
3. Gehen Sie zu **Steuer** \> **Konfiguration** \> **Quellensteuer** \> **Arten von Quellensteuereinnahmen**, um **Kode Bukti Potong** Quellensteuerertragsart einzurichten und ordnen Sie dann die Codes den zugehörigen Quellensteuergruppen zu. Die Codes werden benötigt, um die Integrationsdatei mithilfe der e-Bupot-Anwendung zu generieren. 

## <a name="generate-the-withholding-import-file"></a>Generieren Sie die Quellensteuerimportdatei

Der Prozess der Erstellung und Erstellung der e-Bupot-Datei für einen bestimmten Zeitraum basiert auf den Quellensteuertransaktionen, die während des Abrechnungs- und Nachzahlungssteuerauftrags gebucht wurden.

Folgen Sie diesen Schritten, um die Datei zu generieren.

1. Gehen Sie zu **Steuer** \> **Erklärungen** \> **Quellensteuer** \> **PPH-Importdatei e-bupot 23 und 26**.
2. Wählen Sie den Abrechnungszeitraum und das Anfangsdatum für den Bericht aus.
3. Geben Sie das Transaktionsdatum ein, und wählen Sie **OK** aus.
4. Wählen Sie die Sprache aus. Alle Berichte sind ins US-Englisch übersetzt (**en-us**) und Indonesisch (**ID**).
5. Wählen Sie den Geschäftstyp aus und geben Sie die Scheck- und Belegnummern ein. 
6. Prüfen Sie, ob der Bericht vom Manager unterzeichnet wurde. Diese Informationen werden in den Bericht der Datei einbezogen. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
