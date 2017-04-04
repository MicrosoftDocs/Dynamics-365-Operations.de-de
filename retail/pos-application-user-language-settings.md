---
title: "Anwendungs- und Benutzerspracheneinstellungen für POS"
description: "In diesem Thema wird beschrieben, wie modernem Spracheinstellungen in KleinPOS (MPOS) ändert und bewölkt POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>Anwendungs- und Benutzerspracheneinstellungen für POS

In diesem Thema wird beschrieben, wie modernem Spracheinstellungen in KleinPOS (MPOS) ändert und bewölkt POS.

<a name="overview"></a>Überblick
========

Moderne KleinUmgebung POS (MPOS) und der Cloud POS Stütz der, in Spracheinstellungen und -übersetzungen zwischen die Filiale und die Benutzer einstellungen variieren können. Beispielsweise kann sich der Shop in einer Region befinden, der in Englisch die gängigsten für seine Kunden ist, manche Arbeitskräfte ziehen sie vor, die Anwendung mit französischen Übersetzungen zu verwenden.

## <a name="data-language"></a>Sprache der Daten
Unabhängig von der Einstellungen des Benutzers verwendet MPOS und Cloud POS immer die Spracheinstellungen des Shops, um die Übersetzungen bestimmt, die für Daten verwendet werden. Dadurch wird sichergestellt, dass alle Benutzer und Debitoren eine konsistente Erfahrung haben.  Beispiele der Daten verfügen:

-   Produkte
-   Attribute und Werte
-   Kategorienamen
-   Gedruckte oder per E-Mail übermittelte Transaktionsbelege
-   Namen der Zahlungsmethoden
-   Zeilenanzeigemeldungen

Die Sprache der Filiale wird auch für den Haupt-Anmelden Bildschirm POS verwendet, da der Benutzer nicht bekannt, vor dem Anmelden. Wenn eine Übersetzung nicht für die Sprache der Filiale verfügbar ist, stellt der Betrag vom POS der Sprache des Unternehmens wieder her.

### <a name="configuring-the-stores-language-setting"></a>Konfigurieren der Spracheinstellung des Shops

Die Spracheneinstellung der Filiale ist von ** alle Einzelhandelsgeschäfte ** auf die Seite auf Shop Lagermanagement ** ** unter ** allgemeine regionale Einstellungs-Sprache &gt; festgelegt. ** Verwenden Sie die Dropdownauswahl, um die Sprache für jede Filiale aus.

## <a name="user-interface-language"></a>Benutzeroberflächensprache
Die Einstellung des POS- Benutzers werden die Übersetzungen, die in der Bewerbungsbenutzeroberfläche verwendet werden. Dies umfasst alle Beschriftungen, Menüs und Listen ein, die nicht als Daten anwenden. Eine Ausnahme ist der Text, der in POS-Schaltflächenrastern angezeigt wird. Die Schaltflächenraster nicht unterstützt Übersetzungen, sodass die Konten immer Anzeigen - text, wie auf der Schaltfläche definiert. Um zu unterstützen übersetzte Schaltflächen, müssen Sie separate Schaltflächenraster kopieren und verwalten und diese den entsprechenden Benutzer zuweisen.

### <a name="configuring-the-users-language-setting"></a>Konfigurieren der Spracheinstellung der Benutzers

Die Einstellung des POS- Benutzers wird aus ** alle Arbeitskräfte ** ** ** Arbeitskraft auf die Seite Kleinsprache &gt; ** ** unter festgelegt.  Sie ist nicht auf die Hauptprofilregisterkarte festgelegt.  Diese Einstellung wird nicht nach POS verwendet. Wenn die Sprache des Benutzers nicht festgelegt wird oder sie auf eine Sprache festgelegt wird, in der Übersetzungen nicht verfügbar sind, stellt das POS die Sprache des Shops wieder her.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | ** Benutzeroberflächensprache ** ** **      | **Datensprache (Produkte, Bonlayouts, Zeilenanzeige usw.)** |
| **Unternehmen** | Standard                    | Standard                                                           |
| **Shop**   | Überschreibt Unternehmen          | Überschreibt Unternehmen                                                 |
| **User**    | Überschreibt Shop oder Unternehmen | Nie                                                             |




