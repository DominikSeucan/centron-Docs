---
description: Validiert am 7. Juli 2023 • Zuletzt bearbeitet am 01. Dezember 2023
---

# CORS konfigurieren

Mit dieser Operation können Sie das Cross-Origin Resource Sharing (CORS) für bestimmte Buckets aktivieren.

CORS ist ein vom World Wide Web Consortium (W3C) vorgeschlagener Standardmechanismus, der herkunftsübergreifende Anfragen von Servern ermöglicht. Bei Standard-Webseitenanfragen können die Skripte und Inhalte einer Website nicht mit denen einer anderen Website interagieren, da sie dieselbe Ursprungsrichtlinie (SOP) haben.

centron S3 Object Storage ermöglicht die Speicherung statischer Webressourcen in Buckets. Die Buckets von centron S3 Object Storage können als Website-Ressourcen dienen, wenn die Buckets richtig verwendet werden. Einzelheiten finden Sie im Abschnitt PUT Bucket Website. Eine Website in centron S3 Object Storage kann nur dann auf Anfragen anderer Websites antworten, wenn CORS richtig konfiguriert ist.

**Typische Anwendungsszenarien sind:**

Mit der Unterstützung von CORS können Sie JavaScript und HTML 5 verwenden, um Webanwendungen zu erstellen und direkt auf die Ressourcen in centron S3 Object Storage zuzugreifen, ohne Proxy-Server für die Übertragung verwenden zu müssen.

Sie können die Dragging-Funktion von HTML 5 aktivieren, um Dateien direkt in centron S3 Object Storage hochzuladen (mit Anzeige des Upload-Fortschritts) oder centron S3 Object Storage-Inhalte mithilfe von Webanwendungen zu aktualisieren.

Sie können externe Webseiten, Stylesheets und HTML 5-Anwendungen in verschiedenen Domänen hosten. Webfonts oder Bilder auf centron S3 Object Storage können von mehreren Websites gemeinsam genutzt werden.

Nur Benutzer mit der Berechtigung s3:PutBucketCORS können diesen Vorgang durchführen. Standardmäßig kann nur der Bucket-Besitzer diesen Vorgang ausführen. Der Bucket-Besitzer kann anderen Benutzern die Durchführung dieses Vorgangs gestatten, indem er ihnen die entsprechende Berechtigung erteilt. Nachdem die CORS-Konfiguration für den Bucket festgelegt wurde, wird sie innerhalb von 2 Minuten wirksam.



## Request Syntax&#x20;

```
 PUT /?cors HTTP/1.1
 Host: bucketname.s3.example.com
 User-Agent: agent
 Accept: */*
 Date: date
 Authorization: authorization
 Content-MD5: MD5
 Content-Length: length
 Expect: expect

 <?xml version="1.0" encoding="UTF-8"?>
 <CORSConfiguration>
   <CORSRule>
     <ID>id</ID>
     <AllowedMethod>method</AllowedMethod>
     <AllowedOrigin>origin</AllowedOrigin>
     <AllowedHeader>header</AllowedHeader>
     <MaxAgeSeconds>seconds</MaxAgeSeconds>
     <ExposeHeader>header</ExposeHeader>
   </CORSRule>
 </CORSConfiguration>
```



## Request Parameters

Diese Anfrage enthält keine Parameter.



## Request Headers

| Header               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                        | Kommentare                                                                                               |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| Content-MD5          | <p>Die MD5-Digest-Zeichenkette des Nachrichtentextes wird nach dem Standard RFC 1864 berechnet. Das heißt, es wird zunächst das 128-Bit-Binärfeld (die mit MD5 verschlüsselten Kopfdaten der Nachricht) berechnet. Anschließend werden die Binärdaten mithilfe der Base-64-Kodierung in eine Zeichenkette umgewandelt.</p><p></p><p>Typ: String</p><p></p><p>Beispiel: n58IG6hfM7vqI4K0vnWpog==</p> | Obligatorisch                                                                                            |
| x-amz-security-token | <p>Header-Feld zur Identifizierung der Anfrage eines föderierten Benutzers. Wenn die föderale Authentifizierungsfunktion aktiviert ist, werden Benutzer, die solche Anfragen senden, als föderierte Benutzer identifiziert.</p><p></p><p>Type: string</p>                                                                                                                                           | Optional. Dieser Parameter muss in der von den Benutzern des Verbunds gesendeten Anfrage enthalten sein. |



## Request Elemente

In dieser Anfrage müssen Sie die CORS-Konfiguration von Buckets im Anfragekörper vornehmen. Die Konfigurationsinformationen werden im XML-Format hochgeladen. In der folgenden Tabelle finden Sie die CORS-Konfigurationselemente.

| Element           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                          | Kommentare    |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| CORSConfiguration | <p>Gibt den CORSRules-Stammknoten an. Die maximale Größe beträgt 64 KB.</p><p></p><p>Type: Container</p><p>Ancestor: None</p>                                                                                                                                                                                                                                                                                                                         | Verpflichtend |
| CORSRule          | <p>Bezeichnet eine CORS-Regel. CORSConfiguration kann bis zu 100 Regeln enthalten.</p><p></p><p>Type: Container</p><p>Ancestor: <strong>CORSConfiguration</strong></p>                                                                                                                                                                                                                                                                                | Verpflichtend |
| ID                | <p>Gibt den eindeutigen Bezeichner einer Regel an. Der Wert kann maximal 255 Zeichen enthalten.</p><p></p><p>Type: String</p><p>Ancestor: Rule</p>                                                                                                                                                                                                                                                                                                    | Optional      |
| AllowedMethod     | <p>Zeigt eine Methode an, die durch eine CORS-Regel erlaubt ist.</p><p></p><p>Type: String</p><p>Valid values: <strong>GET</strong>, <strong>PUT</strong>, <strong>HEAD</strong>, <strong>POST</strong>, und <strong>DELETE</strong></p><p>Ancestor: Rule</p>                                                                                                                                                                                         | Verpflichtend |
| AllowedOrigin     | <p>Gibt einen Ursprung an, der durch eine CORS-Regel zugelassen ist. Es handelt sich um eine Zeichenkette, die eine Wildcard (*) enthalten kann. Jeder <strong>AllowedOrigin</strong> kann nur einen Wildcard-Wert enthalten(<code>*</code>).</p><p></p><p>Type: String</p><p>Ancestor: Rule</p>                                                                                                                                                      | Verpflichtend |
| AllowedHeader     | <p>Gibt einen zulässigen Header (<strong>Access-Control-Request-Headers</strong>) in einer CORS-Anfrage an. Wenn eine Anfrage <strong>Access-Control-Request-Header</strong> enthält, wird nur eine CORS-Anfrage, die der Konfiguration von <strong>AllowedHeader</strong> entspricht, als gültige Anfrage betrachtet. Jeder <strong>AllowedHeader</strong> kann nur einen Wildcard (*) enthalten.</p><p></p><p>Type: String</p><p>Ancestor: Rule</p> | Optional      |
| MaxAgeSeconds     | <p>Gibt die Antwortzeit des CORS an, die von einem Server zwischengespeichert werden kann. Sie wird in Sekunden ausgedrückt. Jede <strong>CORSRule</strong> kann nur eine <strong>MaxAgeSeconds</strong> enthalten. Sie kann auf einen negativen Wert gesetzt werden.</p><p></p><p>Type: Integer</p><p>Ancestor: Rule</p>                                                                                                                             | Optional      |
| ExposeHeader      | <p>Kennzeichnet einen ergänzten Header in CORS-Antworten. Der Header liefert zusätzliche Informationen für Server. Er darf keine Leerzeichen enthalten.</p><p></p><p>Type: String</p><p>Ancestor: Rule</p>                                                                                                                                                                                                                                            | Optional      |



## Response Syntax

```
HTTP/1.1 status_code
 Server: Server Name
 x-amz-request-id: request id
 x-amz-id-2: id
 x-reserved: amazon, aws and amazon web services are trademarks or registered trademarks of Amazon Technologies, Inc
 Date: date
 Content-Length: 0
```



## Response Headers

Diese Response verwendet allgemeine Header.



## Response Elements

Diese Antwort enthält keine Elemente.



## Fehlermeldungen

Es werden keine speziellen Fehlermeldungen zurückgegeben.



## Beispiel Request

```
PUT /?cors HTTP/1.1
 User-Agent: curl/7.19.0 (x86_64-suse-linux-gnu) libcurl/7.19.0 OpenSSL/0.9.8{ zlib/1.2.3 libidn/1.10
 Host: bucketname.s3.example.com
 Accept: */*
 Date: Tue, 28 Apr 2015 08:56:07 +0000
 Authorization:  AWS D13E0C94E722DD69423C:QhHpU6Amg/2r6wIYdU3RXIx7Tlc=
 Content-MD5: x3R4DBZgOrwsI6DwztrQCg==
 Content-Length: 468
<CORSConfiguration>
   <CORSRule>
     <AllowedMethod>POST</AllowedMethod>
     <AllowedMethod>GET</AllowedMethod>
     <AllowedMethod>HEAD</AllowedMethod>
     <AllowedMethod>PUT</AllowedMethod>
     <AllowedMethod>DELETE</AllowedMethod>
     <AllowedOrigin>s3.example.com</AllowedOrigin>
     <AllowedOrigin>www.example.com</AllowedOrigin>
     <AllowedHeader>AllowedHeader_1</AllowedHeader>
     <AllowedHeader>AllowedHeader_2</AllowedHeader>
     <MaxAgeSeconds>100</MaxAgeSeconds>
     <ExposeHeader>ExposeHeader_1</ExposeHeader>
     <ExposeHeader>ExposeHeader_2</ExposeHeader>
   </CORSRule>
 </CORSConfiguration>
```



## Beispielantwort

```
HTTP/1.1 200 OK
 Server: S3
 x-amz-request-id: C2D2F581B3C5AF6C6698322AB56836F6
 x-amz-id-2: lDGZAj4h+A33eYauDCTsPvFSHzBXEtZon6Eg1idIZl18/2/odotyqJUJ/lTh80uA
 x-reserved: amazon, aws and amazon web services are trademarks or registered trademarks of Amazon Technologies, Inc
 Date: Tue, 28 Apr 2015 08:56:07 GMT
 Content-Length: 0
```
