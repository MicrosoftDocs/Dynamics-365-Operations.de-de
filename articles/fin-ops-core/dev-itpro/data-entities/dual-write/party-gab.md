---
title: Partei und globales Adressbuch
description: In diesem Thema wird die Partei- und globale Adressbuchfunktionalität von Duales Schreiben beschrieben.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: c62290506d32579d926ad1a1d6f090845c0d0f26
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216611"
---
# <a name="party-and-global-address-book"></a>Partei und globales Adressbuch

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

*Partei* und *globales Adressbuch* sind Konzepte in Finance and Operations-Anwendungen. Eine Partei kann eine Organisation oder eine Person sein. Es ist praktisch, Eigenschaften einer Partei global zu speichern und zu verwalten, z. B. den Namen, die Sprache, Kontakte und Adressen. Wenn dann ein Eigenschaftswert an einer Stelle geändert wird, wird die Änderung an allen Stellen, an denen die Partei beteiligt ist, berücksichtigt.

## <a name="party"></a>Partei

Eine Partei ist eine Person oder eine Organisation, die an einem Geschäft beteiligt ist. Wenn das Parteikonzept verwendet wird, kann eine Person oder eine Organisation mehr als eine Rolle in einem Geschäft spielen (z. B. Arbeitskraft, Kunde, Kreditor oder Kontakt). Die Rolle basiert auf dem Kontext und dem Zweck. Hier sind einige Beispiele für Rollen von zwei fiktiven Firmen, Contoso und Fabrikam:

+ **Arbeitskraft** – Ein Mitarbeiter. Ein Beispiel ist ein Mitarbeiter von Contoso.
+ **Lieferant** – Eine Lieferantenorganisation oder ein Einzelunternehmer, der Waren oder Dienstleistungen an ein Unternehmen liefert. Wenn Fabrikam zum Beispiel Verbrauchsmaterial an Contoso verkauft, ist Fabrikam ein Kreditor von Contoso.
+ **Ansprechpartner** – Eine Person, die zu kontaktieren ist. Wenn z. B. Contoso Verbrauchsmaterial bei Fabrikam kauft, wenden sich die Mitarbeiter von Contoso an den Kontakt bei Fabrikam.
+ **Kunde** – Eine Person oder Firma, die Dinge von einer Firma kauft. Wenn z. B. Contoso Vorräte bei Fabrikam kauft, ist Contoso ein Debitor von Fabrikam.

Das Parteienmodell wird häufig verwendet, um mittlere bis komplexe Beziehungen zwischen Organisationen und Personen darzustellen, insbesondere wenn eine Partei mehr als eine Rolle spielt. Im Folgenden finden Sie einige allgemeine Beispiele hierfür:

+ Eine Partei kann sowohl Kunde als auch Verkäufer sein. Zum Beispiel verkauft Fabrikam in Nordamerika elektrische Drähte an Contoso und kauft montierte Lautsprecher von Contoso. In Europa verkauft Fabrikam Teile an Contoso, aber es kauft nichts von Contoso.
+ Eine Partei kann sowohl Mitarbeiter als auch Kunde sein. Zum Beispiel kauft ein Mitarbeiter von Contoso Elektronik von Contoso für den persönlichen Gebrauch.
+ Es kann eine many-to-many (N:N) Beziehung zwischen einer Person und einer Organisation bestehen. Beispiel: Fabrikam stellt Servicespezialisten zur Verfügung und beschäftigt einen Vermittlungskoordinator. Der Vermittlungskoordinator gleicht Service-Spezialisten mit Arbeitsanforderungen von mehreren Debitor von Fabrikam ab. Contoso ist einer der Kunden von Fabrikam. Wenn Contoso einen Service-Spezialisten benötigt, kontaktiert es den Vermittlungskoordinator, der dann die Anfrage vermittelt. Da der Platzierungskoordinator Anfragen für alle Kunden bearbeitet, handelt es sich um eine N:N-Beziehung.

Die folgende Abbildung zeigt das Datenmodell für Partei.

![Datenmodell für Partei](media/party-gab-image1.png)

> [!TIP]
> Wenn Sie versuchen, einen neuen Kontodatensatz zu erstellen, verwenden Sie das Feld **Partei**, um den Datensatz nach Namen zu suchen. Wenn Sie auf diese Weise den Datensatz finden, müssen Sie ihn nur noch auswählen. Das System füllt dann automatisch alle Daten der Partei aus. Sie müssen nicht alle erforderlichen Felder manuell festlegen. Dieses Verhalten ist auf den Seiten **Konto**, **Kontakt** und **Kreditor** standardmäßig zu finden.

Dual-Write unterstützt nicht alle Partei-Rollen von Finance and Operations-Apps. Eine vollständige Liste der Parteirollen finden Sie unter [Überblick über globale Adressbücher](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globales Adressbuch

Das globale Adressbuch ist ein Verzeichnis mit postalischen und elektronischen Adressen der Organisationen und Personen, die an einem Unternehmen beteiligt sind.

Das globale Adressbuch speichert und verwaltet so viele postalische und elektronische Adressen wie nötig. Beispiel: Fabrikam hat Tankstellen an 50 Lagerplätzen. Jeder Lagerplatz hat eine andere Postadresse, E-Mail-Adresse und Telefonnummer. Alle geschäftlichen Käufe werden der Haupttankstelle in Rechnung gestellt, aber direkt an die spezifische Tankstelle versandt, die den Kauf angefordert hat. Das globale Adressbuch speichert die Haupttankstelle als Rechnungsadresse für Fabrikam und speichert jede Tankstelle als Lieferadresse. Die Adressen können einmalig gespeichert und dann abgerufen werden, wenn sie für Angebote und Aufträge benötigt werden.

Je nach Geschäftskontext kann eine Person oder eine Organisation mehr als eine Rolle spielen, und für alle Rollen kann dieselbe Postadresse und elektronische Adresse verwendet werden. In diesem Fall sollte eine Änderung der Adresse in einer Rolle in allen anderen Rollen erscheinen. Das globale Adressbuch speichert und verarbeitet Adressen global.

Die folgende Abbildung zeigt das Datenmodell für das globale Adressbuch.

![Datenmodell für das globale Adressbuch](media/party-gab-image2.png)

## <a name="contact"></a>Kontakt

In Customer-Engagement-Apps ist ein Kontakt eine Person. Die Tabelle **Kontakt** wurde jedoch überladen, um eine Person, einen Portalbenutzer, einen business-to-consumer (B2C) Debitor oder einen Kreditor darzustellen. Die Darstellung ist implizit, und Sie können den Unterschied nicht erkennen, es sei denn, Sie untersuchen die zugehörigen Transaktionen. Die Tabelle **Kontakt** ist auf eine Eins-zu-Eins-Beziehung (1:1) mit der Tabelle **Konto** beschränkt. Als Teil des Modells für Parteien und globale Adressbücher führt Dual-Write explizite Eigenschaften für die Klassifizierung ein und lässt N:N-Beziehungen zwischen einem Kontakt, der eine Person ist, und einer Organisation (**Konto** oder **Anbieter** Entität) zu.

Es gibt zwei Typen von **Kontakt**-Zeilen:

+ **Zusammengefasster Kontakt** – Eine **Kontakt**-Zeile, in der das Feld **Firma** einen obligatorischen Wert hat.
+ **Unzusammengefasster Kontakt** – Eine **Kontakt**-Zeile, bei der das Feld **Firma** leer ist.

Die Tabelle **Kontakt** kann die folgenden Arten von Zeilen speichern.

| Zeilentyp | Beschreibung |
|----------|-------------|
| Eine Person, die ein Kunde ist (z. B. ein verkaufsfähiger Kontakt oder ein B2C-Kunde) | Ein zusammengefasster Kontakt-Datensatz, bei dem das Feld **Firma** nicht leer ist und das Feld **Ist Kunde** auf **Ja** festgelegt ist. |
| Eine Person, die ein Lieferant ist (z. B. ein Einzelunternehmer wie ein Verkäufer) | Ein zusammengefasster Datensatz, bei dem das Feld **Firma** nicht leer ist und das Feld **Lieferant** auf **Ja** festgelegt ist. |
| Eine Person, die sowohl ein Kunde als auch ein Lieferant ist | Ein zusammengefasster Datensatz, bei dem das Feld **Firma** nicht leer ist, das Feld **Ist Kunde** auf **Ja** festgelegt ist und das Feld **Ist Lieferant** auf **Ja** festgelegt ist. Eine Person kann sowohl Produzent für ein Produkt als auch Verbraucher für ein anderes Produkt sein. Beide, Finance and Operations-Apps und Duales Schreiben, unterstützen diese Beziehung. |
| Eine Person, die eine Kontaktperson für eine Organisation ist, aber kein Kunde oder Lieferant ist | Ein nicht zusammengefasster Kontakt-Datensatz, bei dem das Feld **Firma** leer ist, das Feld **Ist Kunde** auf **Nein** festgelegt ist und das Feld **Ist Lieferant** auf **Nein** festgelegt ist. |

## <a name="contact-for-party-table"></a>Kontakt für die Tabelle Partei

Die Tabelle **Kontakt für Partei** speichert und behandelt N:N-Beziehungen zwischen **Konto**-Zeilen und **Kontakt**-Zeilen. Es kann die nicht zusammengefassten **Kontakt**-Zeilen aus den nicht zusammengefassten Zeilen herausfiltern und nur die nicht zusammengefassten **Kontakt**-Zeilen mit **Konto** oder **Kreditor**-Zeilen verknüpfen.

Zum Beispiel sind Natasha Jones und Miguel Reyes Tierärzte, die Farmen in ihren Gebieten versorgen. Natasha bedient das Gebiet um Seattle und Miguel das Gebiet um Kent. In der Customer-Engagement-App werden die Betriebe als Kunden und die Tierärzte als Ansprechpartner dargestellt. Ein einziger **Kontakt**-Datensatz für Natasha ist allen Farmen zugeordnet, mit denen Natasha zusammenarbeitet. Ebenso ist ein einzelner **Kontakt** Datensatz für Miguel mit allen Farmen verbunden, mit denen Miguel arbeitet.

Diese Beziehungen werden in der Tabelle **Kontakt für Partei** gespeichert. Sie finden die Informationen auf den standardmäßigen Seiten **Konto**, **Kontakt** und **Kreditor**:

+ Auf der Seite **Konto** können Sie die Registerkarte **Zugehörige Kontakte** verwenden, um einen oder mehrere Kontakte mit der Zeile **Konto** zu verknüpfen. Auf diese Weise ordnen Sie Ansprechpartner für eine Organisation zu. Sie können dann einen Kontakt als Hauptkontakt für das Konto auswählen. Wenn Sie die Seite **Schnell erstellen** verwenden, können Sie nur eine Kontaktperson auswählen. Das Verhalten ist das gleiche, wenn Sie die Seite **Kreditor** verwenden und der Datensatztyp **Organisation** ist.
+ Auf der Seite **Kontakt**, wenn die Zeile ein Debitor, ein Kreditor oder beides ist (ein zusammengefasster Kontakt), können Sie die Registerkarte **Zugehörige Kontakte** verwenden, um einen oder mehrere Kontakte zuzuordnen. Auf diese Weise weisen Sie Ansprechpartnern für einen B2C Debitor oder Kreditor zu. Sie können dann einen Kontakt als primären Kontakt auswählen. Wenn Sie die Seite **Schnell erstellen** verwenden, können Sie nur eine Kontaktperson auswählen.
+ Auf der Seite **Kontakt** können Sie, wenn es sich bei der Zeile um einen Ansprechpartner (einen nicht zusammengefassten Kontakt) handelt, die Registerkarte **Zugehörige Organisationen** verwenden, um einen oder mehrere Debitor(en) oder Kreditor(en) zuzuordnen. Auf diese Weise ordnen Sie Kunden oder Kreditoren dem zugrunde liegenden Ansprechpartner zu. Der Kunde oder Lieferant kann eine Organisation, eine Person oder beides sein. Sie können jeweils nur in einem der vier Felder einen Wert auswählen:

    + Wenn Sie einen Wert im Feld **Partei-ID** wählen, wird der zugrundeliegende Kontakt allen Rollen der gewählten Partei zugewiesen.
    + Wenn Sie einen Wert im Feld **Zugehöriger Kontakt** auswählen, wählen Sie den zusammengefassten Kontakt vom Typ **Person**.
    + Wenn Sie einen Wert im Feld **Verbundenes Konto** oder **Verbundener Kreditor** auswählen, wählen Sie eine Organisation aus.

    ![Registerkarte „Zugeordnete Organisationen“ auf der Seite „Kontakt“](media/party-gab-image3.png)

    Unabhängig von Ihrer Auswahl wird die Zuordnung auf der Ebene der Partei erstellt, sie gilt für alle Rollen der Partei und wird in der Entität **Kontakt für Partei** gespeichert.

> [!NOTE]
> Der Anzeigename für die Tabelle **Kontakt für Partei** in Customer-Engagement-Apps ist **Kontakt für Kunde/Lieferant**.

Wenn Sie eine **Kontakt**-Zeile öffnen, in der sowohl das Feld **Ist Debitor** als auch das Feld **Ist Kreditor** auf **Nein** festgelegt sind, wird die Registerkarte **Zugehörige Organisationen** angezeigt. Verwenden Sie diese Registerkarte, um eine oder mehrere Debitor- oder Kreditor-Organisationen mit dem Kontakt zu verknüpfen.

Wenn Sie eine Zeile **Kontakt** öffnen, in der entweder das Feld **Ist Debitor** oder das Feld **Ist Kreditor** auf **Ja** festgelegt ist, wird die Registerkarte **Verbundene Kontakte** angezeigt. Verwenden Sie diese Registerkarte, um einen oder mehrere Kontakte zuzuordnen.

## <a name="postal-addresses"></a>Postalische Adressen

Eine neue Registerkarte **Adressen** wurde auf den Seiten **Konto**, **Kontakt** und **Lieferant** eingeführt. Diese Registerkarte unterstützt mehrere postalische Adressen, indem sie ein Raster verwendet, wie in der folgenden Abbildung gezeigt.

![Raster für postalische Adressen](media/party-gab-image4.png)

Das Raster enthält die folgenden Spalten:

+ **Postadressen-Rollen** – Der Zweck der Postadresse.
+ **Ist primär** – Ein Wert, der angibt, ob die Adresse die primäre Adresse ist.
+ **Adressnummer** – Die Reihenfolge der Adressen.

Sie können die Schaltfläche **Neue Adresse** oberhalb des Rasters verwenden, um so viele Postadressen wie gewünscht zu erstellen.

Die Felder **Adresse 1** und **Adresse 2** auf der Registerkarte **Zusammenfassung** der Seite **Konto** entsprechen den Adressen **Lieferung** bzw. **Rechnung**.

![Registerkarte Zusammenfassung für Postadressen](media/party-gab-image5.png)

Die Felder **Adresse 1**, **Adresse 2** und **Adresse 3** auf der Registerkarte **Zusammenfassung** der Seite **Kontakt** entsprechen den Adressen **Geschäft**, **Lieferung** bzw. **Rechnung**.

## <a name="electronic-addresses"></a>Elektronische Adressen

Eine neue Registerkarte **Elektronische Adressen** wurde auf den Seiten **Konto**, **Kontakt** und **Lieferant** eingeführt. Diese Registerkarte unterstützt mehrere elektronische Adressen, indem sie ein Raster verwendet, wie in der folgenden Abbildung gezeigt.

![Raster für elektronische Adressen](media/party-gab-image6.png)

Das Raster enthält die folgenden Spalten:

+ **Typ** – Der Typ der elektronischen Adresse.
+ **Ist primär** – Ein Wert, der angibt, ob es sich bei der Adresse um die primäre Adresse handelt.
+ **Zweck** – Der Zweck der elektronischen Adresse.

Mit der Schaltfläche **Neue elektronische Adresse** über dem Raster können Sie so viele Adressen erstellen, wie Sie möchten.

Elektronische Adressen sind nur in diesem Raster verfügbar. In zukünftigen Versionen werden alle Felder für die Postanschrift und die elektronische Adresse aus anderen Registerkarten entfernt (z.B. aus den Registerkarten **Zusammenfassung** und **Details**).

## <a name="setup"></a>Einstellung

1. Öffnen Sie Ihre Kundenbindungs-App-Umgebung.

2. Installieren Sie die neueste Version (2.2.2.60 oder höher) von [Dual-write application orchestration solution](https://aka.ms/dual-write-app).

3. Installieren Sie [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab).

4. Öffnen Sie die Finance and Operations-App. Navigieren Sie zum Modul Datenverwaltung und wählen Sie die Registerkarte Duales Schreiben. Die Duales Schreiben-Verwaltungsseite wird geöffnet.

5. Wenden Sie beide in den Schritten 2 und 3 installierten Lösungen an, indem Sie die Funktion [Lösung anwenden](link-your-environment.md) verwenden.

6. Stoppen Sie die folgenden Zuordnungen, da sie nicht mehr benötigt werden. Führen Sie stattdessen die `Contacts V2 (msdyn_contactforparties)`-Zuordnung aus.

    + CDS-Kontakte V2 und Kontakte (bezieht sich auf Kundenkontakte)
    + CDS-Kontakte V2 und Kontakte (bezieht sich auf Lieferantenkontakte)

7. Die folgenden Entitätszuordnungen werden für die Partei-Funktionalität aktualisiert, daher muss die neueste Version auf diese Zuordnungen angewendet werden.

    Zuordnen | Update auf diese Version | Änderungen
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.5 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Customers V3 (accounts)` | 1.0.0.5 |Entfernte `PartyNumber` und andere parteibezogene Felder wie Name, persönliche Daten, postalische Adressfelder und elektronische Kontaktadresse.
    `Customer V3 (contacts)` | 1.0.0.5 | Entfernte `PartyNumber` und andere parteibezogene Felder wie Name, persönliche Daten, postalische Adressfelder und elektronische Kontaktadresse.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Entfernte `PartyNumber` und andere parteibezogene Felder wie Name, persönliche Daten, postalische Adressfelder und elektronische Kontaktadresse.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Ersetzen Sie die Kontaktperson durch die Referenz `ContactforParty`.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Ersetzen Sie die Kontaktperson durch die Referenz `ContactforParty`.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Ersetzen Sie die Kontaktperson durch die Referenz `ContactforParty`.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.1 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Complimentary Closings ( msdyn_compliemntaryclosings)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.

8. Bevor Sie die oben genannten Zuordnungen ausführen, müssen Sie die Integrationsschlüssel manuell aktualisieren, wie in den folgenden Schritten beschrieben. Wählen Sie dann **Speichern** aus.

    | Zuordnen | Schlüssel |
    |-----|------|
    | Konto |  accountnumber [Kontonummer]<br>msdyn_company.cdm_companycode [Firma (Firmencode)] |
    | Kontakt | msdyn_contactpersonid [Kontonummer/Ansprechpartner-ID]<br>msdyn_company.cdm_companycode [Firma (Firmencode)] |
    | Kontakt für Debitor/Lieferant | msdyn_contactforpartynumber [Kontakt für Partei-Nummer]<br>msdyn_associatedcompanyid.cdm_companycode [Zugehörige Firma (Buchungskreis)] |
    | Lieferant | msdyn_vendoraccountnumber [Kontonummer des Kreditors]<br>msdyn_company.cdm_companycode [Firma (Firmencode)]|

9. In Dataverse haben sich die Zeichengrenzen für die Regeln zur Erkennung von Duplikaten von 450 auf 700 Zeichen erhöht. Mit dieser Begrenzung können Sie einen oder mehrere Schlüssel zu den Regeln für die Duplikaterkennung hinzufügen. Erweitern Sie die Regel zur Erkennung von Duplikaten für die Tabelle **Konten**, indem Sie die folgenden Felder festlegen.

    | Feld | Wert |
    |-------|-------|
    | Name | Konten mit demselben Kontonamen. |
    | Beschreibung | Erkennt Kontodatensätze, die den gleichen Wert im Attribut Kontoname haben. |
    | Basis-Datensatz-Typ | Konto |
    | Übereinstimmender Datensatz Typ | Konto |
    | Kontoname (Feld) | Genaue Übereinstimmung |
    | Firma (Feld) | Genaue Übereinstimmung |
    | Beziehungstyp (Feld) | Genaue Übereinstimmung |
    | Partei Id (Feld) | Genaue Übereinstimmung |
    | Auswählen (Feld) | (leer) |

    ![Doppelte Regel für Konten](media/duplicate-rule-1.PNG)

10. Erweitern Sie die Regel zur Erkennung von Duplikaten für die Tabelle **Kontakte**, indem Sie die folgenden Felder festlegen.

    | Feld | Wert |
    |-------|-------|
    | Name | Kontakte mit gleichem Vornamen und Nachnamen. |
    | Beschreibung | Erkennt Kontakt-Datensätze, die die gleichen Werte in den Feldern Vorname und Nachname haben. |
    | Basis-Datensatz-Typ | Kontakt |
    | Übereinstimmender Datensatz Typ | Kontakt |
    | Vorname (Feld) | Genaue Übereinstimmung |
    | Nachname (Feld) | Genaue Übereinstimmung |
    | Firma (Feld) | Genaue Übereinstimmung |
    | Partei Id (Feld) | Genaue Übereinstimmung |
    | Auswählen (Feld) | (leer) |

    ![Duplizieren Sie die Regel für Kontakte](media/duplicate-rule-2.PNG)

11. Wenn Sie ein bestehender Dual-Write-Benutzer sind, folgen Sie den Anweisungen unter [Upgrade auf das Modell Partei und globales Adressbuch](upgrade-party-gab.md) und aktualisieren Sie Ihre Daten.

12. Führen Sie die Zuordnungen in der folgenden Reihenfolge aus. Wenn Sie eine Fehlermeldung erhalten, die besagt „Projektvalidierung fehlgeschlagen“. „Fehlendes Zielfeld...“, öffnen Sie dann die Zuordnung und wählen Sie **Tabellen aktualisieren**. Führen Sie dann die Zuordnung aus.

    Finance and Operations-App | Customer Engagement-App  
    ----------------------------|------------------------
    [CDS-Parteien](mapping-reference.md#220) | msdyn_parties
    [CDS Postadressorte](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS-Verlauf der Postanschrift V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS Postadressorte der Partei](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Parteikontakte V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Debitoren V3](mapping-reference.md#101) | Konten
    [Debitoren V3](mapping-reference.md#116) | Kontakte
    [Kreditoren V2](mapping-reference.md#202) | msdyn_vendors
    [Titel von Kontaktpersonen](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Schlussformeln](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Anreden](mapping-reference.md#228) | msdyn_salutations
    [Entscheidungsfunktionen](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Stellenfunktionen](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Treueebenen](mapping-reference.md#226) | msdyn_loyaltylevels
    [Arten von Persönlichkeitsmerkmalen](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Kontakte V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS-Verkaufsangebotskopf](mapping-reference.md#215) | Angebote
    [Auftragskopfzeilen CDS](mapping-reference.md#217) | salesorders
    [Verkaufsrechnungskopfzeilen V2](mapping-reference.md#118) | Rechnungen

> [!Note]
> Die Zuordnung `CDS Contacts V2 (contacts)` ist die Zuordnung, die Sie in Schritt 1 angehalten haben. Wenn Sie versuchen, andere Zuordnungen auszuführen, können diese 2 Zuordnungen in der Liste der Abhängigen erscheinen. Führen Sie diese Zuordnungen nicht aus.

> [!Note]
> Wenn die Lösung für das Partei- und globale Adressbuch installiert ist, müssen Sie die Steckung mit der Bezeichnung `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead` deaktivieren. Wenn Sie die Lösung für das Partei- und globale Adressbuch deinstallieren, müssen Sie das Plugin wieder aktivieren.

> [!Note]
> Das Feld `msdyn_*partynumber` (ein einzeiliges Textfeld), das in den Tabellen **Konto**, **Kontakt** und **Kreditor** enthalten ist, sollte in Zukunft nicht mehr verwendet werden. Der Name des Labels hat aus Gründen der Übersichtlichkeit das Präfix **(Veraltet)**. Verwenden Sie stattdessen das Feld **msdyn_partyid**. Das Feld ist ein Nachschlagefeld in der Tabelle **msdyn_party**.

> Tabellenname | Altes Feld | Neues Feld
> --------|-------|--------
> Konto | `msdyn_partynumber` | `msdyn_partyid`
> Kontakt | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Vorlagen

Eine Sammlung von Tabellenzuordnungen arbeitet für die Interaktion von Partei und globalem Adressbuch zusammen, wie in der folgenden Tabelle dargestellt.

| Finance and Operations-App | Customer Engagement-App | Beschreibung |
|----------------------------|-------------------------|-------------|
| [Titel von Kontaktpersonen](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Debitoren V3](mapping-reference.md#101) | Konten |
| [Debitoren V3](mapping-reference.md#116) | Kontakte |
| [CDS-Parteien](mapping-reference.md#220) | msdyn\_parties |
| [CDS Postadressorte der Partei](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS-Verlauf der Postanschrift V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS Postadressorte](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS-Verkaufsangebotskopf](mapping-reference.md#215) | Angebote |
| [Auftragskopfzeilen CDS](mapping-reference.md#217) | salesorders |
| [Schlussformeln](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Kontakte V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Entscheidungsfunktionen](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Stellenfunktionen](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Treueebenen](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Parteikontakte V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Arten von Persönlichkeitsmerkmalen](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Verkaufsrechnungskopfzeilen V2](mapping-reference.md#118) | Rechnungen |
| [Anreden](mapping-reference.md#228) | msdyn\_salutations |
| [Kreditoren V2](mapping-reference.md#202) | msdyn\_vendors |

Weitere Informationen finden Sie unter [Referenz für die Zuordnung von dualem Schreiben](mapping-reference.md).

## <a name="known-issues-and-limitations"></a>Bekannte Probleme und Einschränkungen

+ Wenn Sie in Finance and Operations-Apps einen Debitor zusammen mit einer Adresse erstellen und speichern, wird die Adresse möglicherweise nicht mit der Tabelle **Adresse** synchronisiert. Der Grund dafür ist ein Problem mit der Sequenzierung der Dual-Write-Plattform. Als Workaround erstellen Sie den Kunden zuerst und speichern ihn. Fügen Sie dann die Adresse hinzu.
+ Wenn in Finance and Operations-Apps ein Datensatz eines Debitors eine primäre Adresse hat und Sie einen neuen Kontakt für diesen Debitor erstellen, erbt der Kontakt-Datensatz eine primäre Adresse vom zugehörigen Debitor-Datensatz. Dies gilt auch für den Kreditor-Kontakt. Dataverse unterstützt dieses Verhalten derzeit nicht. Wenn Dual-Write aktiviert ist, wird ein Debitor-Kontakt, der mit einer primären Adresse aus der App Finance and Operations geerbt wurde, zusammen mit seiner Adresse nach Dataverse synchronisiert.
+ Elektronische Adressen aus der Tabelle `msdyn_partyelectronicaddress` fließen nicht in die elektronischen Adressfelder in den Tabellen **Konto** und **Kontakt**. Wir planen, dieses Problem in einem inkrementellen Release zu beheben. Die vorhandenen Daten auf den elektronischen Adressfeldern in den Tabellen **Konto** und **Kontakt** werden nicht überschrieben.
+ Elektronische Adressen, die auf der Registerkarte „Elektronische Adresse“ der Formulare **Konto**, **Kontakt** und **Kreditor** festgelegt sind, stammen aus der Tabelle `msdyn_partyelectronicaddress`. Diese Informationen fließen nicht in die zugehörigen Transaktionen wie Verkaufsauftrag, Angebot und Einkaufsbestellung. Wir planen, dieses Problem in einem inkrementellen Release zu beheben. Die bestehenden Daten auf den elektronischen Adressfeldern auf den Konto- und Kontakt-Datensätzen werden weiterhin auf Transaktionen wie Verkaufsauftrag, Angebot und Einkaufsbestellung funktionieren.
+ In Finance and Operations-Apps können Sie einen Datensatz für einen Kontakt über das Formular **Kontakt hinzufügen** erstellen. Wenn Sie versuchen, einen neuen Kontakt über das Formular **Kontakt anzeigen** zu erstellen, schlägt die Aktion fehl. Dies ist ein bekanntes Problem.

    ![Bekanntes Problem mit Kontakt hinzufügen](media/party-gab-contact-issue.png)

+ **Initial Sync** unterstützt nicht die Zeitfelder **Verfügbar von** und **Verfügbar bis** auf **KontaktfürPartei**, da DIXF den Wert in einen String statt in eine ganze Zahl umwandelt. Die Konvertierung löst den Fehler `Cannot convert the literal '<say 08:00:00>’ to the expected type edm.int32` aus.
+ Wenn eine Postadresse für mehr als einen Grund verwendet wird, z.B. als geschäftliche Kommunikationsadresse und Rechnungsadresse, sollte sie als `Business;Invoice` erscheinen, wie im folgenden Bild gezeigt. Wenn Sie ein Leerzeichen zwischen den Werten einfügen, erhalten Sie einen Fehler.

    ![Bekanntes Problem mit Adresse](media/party-gab-address-issue.png)

+ Sie können keine in der Zukunft liegende Postadresse mit einer Finance and Operations-App mit Dual-Write eingeben, da Dataverse keine Datumswirksamkeit unterstützt. Wenn Sie eine in der Zukunft liegende Postadresse mit einer Finance and Operations-App eingeben, wird diese vollständig auf Dataverse synchronisiert und Sie sehen die Adresse sofort auf der Benutzeroberfläche. Finance and Operations 
