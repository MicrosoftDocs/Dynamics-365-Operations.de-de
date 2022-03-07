---
title: Verkaufsstellen-(POS)-Anwendung und Benutzerspracheinstellungen
description: In diesem Thema wird beschrieben, wie Spracheinstellungen in Modern POS (MPOS) und Cloud POS geändert werden.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 099d16f63e03ecbc8bf911fe4385b35fac7c67f763c17379cdc6b6229abdea16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774532"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Verkaufsstellen-(POS)-Anwendung und Benutzerspracheinstellungen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Spracheinstellungen in Modern POS (MPOS) und Cloud POS geändert werden.

## <a name="overview"></a>Übersicht
Modern POS (MPOS) und Cloud POS unterstützen Umgebung, in denen Spracheinstellungen und -übersetzungen zwischen die Filiale und die Benutzereinstellungen variieren können. Beispielsweise kann sich der Shop in einer Region befinden, der in Englisch die gängigsten für seine Kunden ist, manche Arbeitskräfte ziehen sie vor, die Anwendung mit französischen Übersetzungen zu verwenden.

## <a name="data-language"></a>Sprache der Daten

Unabhängig von der Einstellungen des Benutzers verwendet MPOS und Cloud POS immer die Spracheinstellungen des Shops, um die Übersetzungen bestimmt, die für Daten verwendet werden. Dadurch wird sichergestellt, dass alle Benutzer und Debitoren eine konsistente Erfahrung haben. Beispiele zu Daten sind:

- Produkte
- Attribute und Werte
- Kategorienamen
- Gedruckte oder per E-Mail übermittelte Transaktionsbelege
- Namen der Zahlungsmethoden
- Zeilenanzeigemeldungen

Die Sprache der Filiale wird auch für den POS-Haupt-Anmelden Bildschirm verwendet, da der Benutzer nicht bekannt, vor dem Anmelden. Wenn eine Übersetzung nicht für die Sprache der Filiale verfügbar ist, stellt der Betrag vom POS der Sprache des Unternehmens wieder her.

### <a name="configuring-the-stores-language-setting"></a>Konfigurieren der Spracheinstellung des Shops

Die Spracheinstellung eines Shops wird über **Alle Einzelhandelsgeschäfte** auf der Seite **Shop** unter **Allgemein &gt; Regionaleinstellungen &gt; Sprache** festgelegt. Verwenden Sie die Dropdownliste, um eine Sprache für jeden Shop auszuwählen.

## <a name="user-interface-language"></a>Benutzeroberflächensprache

Die Einstellung des POS- Benutzers werden die Übersetzungen, die in der Bewerbungsbenutzeroberfläche verwendet werden. Dies umfasst alle Beschriftungen, Menüs und Listen ein, die nicht als Daten anwenden. Eine Ausnahme ist der Text, der in POS-Schaltflächenrastern angezeigt wird. Die Schaltflächenraster nicht unterstützt Übersetzungen, sodass die Konten immer Text anzeigen, wie auf der Schaltfläche definiert. Um zu unterstützen übersetzte Schaltflächen, müssen Sie separate Schaltflächenraster kopieren und verwalten und diese den entsprechenden Benutzer zuweisen.

### <a name="configuring-the-users-language-setting"></a>Konfigurieren der Spracheinstellung der Benutzers

Die Spracheinstellung des POS-Benutzers wird unter **Alle Arbeitskräfte** auf der Seite **Arbeitskraft** unter **Einzelhandel und Commerce &gt;  Sprache** festgelegt. Sie wird nicht auf der Hauptregisterkarte „Profil“ festgelegt. Diese Einstellung wird nicht durch POS verwendet. Wenn die Sprache des Benutzers nicht festgelegt wird oder sie auf eine Sprache festgelegt wird, in der Übersetzungen nicht verfügbar sind, stellt das POS die Sprache des Shops wieder her.

| &nbsp;      | Sprache der Benutzeroberfläche                  | Datensprache (Produkte, Bonlayouts, Zeilenanzeige usw.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Unternehmen** | Standard                    | Standard                                                       |
| **Shop**   | Überschreibt Unternehmen          | Überschreibt Unternehmen                                             |
| **Benutzer**    | Überschreibt Shop oder Unternehmen | Nie                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]