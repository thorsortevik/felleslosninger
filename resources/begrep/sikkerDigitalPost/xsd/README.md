-----

layout: default  
title: Skjema (XSD) filer  
headtitle: Sikker digital post

id: Oversikt/XSDfiler

next: Eksempler

-----

## {{page.title}}

Dokumentasjon av kilder og ev. endringer i XSD-skjemaer for [Sikker
digital post](../)

Grunnen til at vi lagrer disse lokalt er for å sikre at verktøy ikke
trenger å være online for å kunne jobbe med XSD-ene.  
For at dette skal fungere må også referanser til URLer endres til å peke
på lokale filer.  
For de filene vi har endret på er det inkludert en bash-kommando for å
vise hvilke endringer som er gjort.  
Disse kommandoene kan pastes rett inn i en terminal, og kan kjøres fra
katalogen \`SikkerDigitalPost/xsd\`.  
Kommandoene piper til vim for å vise diff med farger.  
For å avslutte vim, skriv \`:q\` og trykk Enter.  
Eventuelt kan du droppe den siste pipen til vim for å vise diff rett i
terminalen (uten farger).

#### Sikker digital post XSD filer:

  - [sdp.xsd](sdp.xsd)
  - [sdp-feil.xsd](sdp-feil.xsd)
  - [sdp-felles.xsd](sdp-felles.xsd)
  - [sdp-kvittering.xsd](sdp-kvittering.xsd)
  - [sdp-manifest.xsd](sdp-manifest.xsd)
  - [sdp-melding.xsd](sdp-melding.xsd)

Beskrivelse: [http://begrep.difi.no/SikkerDigitalPost/](../)

#### [ASiC XSD fil](asic-e/)

  - Skjema for META-INF/signatures.xml i en [Dokumentpakke (ASiC-E
    bundle)](../forretningslag/Dokumentpakke/)
  - [ts\_102918v010201.xsd](asic-e/ts_102918v010201.xsd)
      - Original:
        <http://www.etsi.org/deliver/etsi_ts/102900_102999/102918/01.02.01_60/ts_102918v010201p0.zip>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -Ls http://www.etsi.org/deliver/etsi_ts/102900_102999/102918/01.02.01_60/ts_102918v010201p0.zip \
        | funzip | diff -uw --strip-trailing-cr - asic-e/ts_102918v010201.xsd | vim -R -
        ```

#### [Ebxml XSD filer](ebxml/)

  - Skjemaer som hører til ebXML-standarden.
  - [ebbp-signals-2.0.xsd](ebxml/ebbp-signals-2.0.xsd)
      - Original:
        <http://docs.oasis-open.org/ebxml-bp/2.0.4/ebbp-signals-2.0.4.xsd>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -Ls http://docs.oasis-open.org/ebxml-bp/2.0.4/ebbp-signals-2.0.4.xsd \
        | diff -uw --strip-trailing-cr - ebxml/ebbp-signals-2.0.xsd | vim -R -
        ```

<!-- end list -->

  - [ebms-header-3\_0-200704.xsd](ebxml/ebms-header-3_0-200704.xsd)
      - Original:
        <http://docs.oasis-open.org/ebxml-msg/ebms/v3.0/core/os/ebms-header-3_0-200704.xsd>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -Ls http://docs.oasis-open.org/ebxml-msg/ebms/v3.0/core/os/ebms-header-3_0-200704.xsd \
        | diff -uw --strip-trailing-cr - ebxml/ebms-header-3_0-200704.xsd | vim -R -
        ```
      - Referanse:
        <http://docs.oasis-open.org/ebxml-bp/2.0.4/OS/signalSchema/documentation/ebxmlbp-v2.0.4-Document-os-SignalSchema-en.html>

#### [ETSI XSD fil](etsi/)

  - [XAdES.xsd](etsi/XAdES.xsd)
      - Original: http://uri.etsi.org/01903/v1.3.2/XAdES.xsd
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -Ls http://uri.etsi.org/01903/v1.3.2/XAdES.xsd \
        | diff -uw --strip-trailing-cr - etsi/XAdES.xsd | vim -R -
        ```

#### [Difi sin oppslagstjeneste XSD](oppslag/)

  - [oppslagstjeneste-metadata-14-05.xsd](oppslag/oppslagstjeneste-metadata-14-05.xsd)
      - Original:
        http://begrep.difi.no/Oppslagstjenesten/xsd/oppslagstjeneste-metadata-14-05.xsd
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -Ls http://begrep.difi.no/Oppslagstjenesten/xsd/oppslagstjeneste-metadata-14-05.xsd \
        | diff -uw --strip-trailing-cr - oppslag/oppslagstjeneste-metadata-14-05.xsd | vim -R -
        ```

#### [Standard business document (SBD) XSD filer](SBDH20040506-02/)

  - [SBDH20040506-02/](SBDH20040506-02/)
  - Original:
    <https://joinup.ec.europa.eu/catalogue/distribution/sbdh-xml-schema-files>
  - Ingen endringer.

#### [Universal Business Language XSD fil](ubl/)

  - [ubl](ubl/)
  - Originaler:
    <http://docs.oasis-open.org/ubl/prd4-UBL-2.1/xsd/common/>
  - Ingen endringer.

#### [World Wide Web Consortium XSD filer](w3/)

  - [exc-c14n.xsd](w3/exc-c14n.xsd)
      - Original:
        <http://www.w3.org/TR/2002/REC-xml-exc-c14n-20020718/exc-c14n.xsd>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -sL http://www.w3.org/TR/2002/REC-xml-exc-c14n-20020718/exc-c14n.xsd \
        | diff -uw --strip-trailing-cr - w3/exc-c14n.xsd | vim -R -
        ```

<!-- end list -->

  - [soap-envelope.xsd](w3/soap-envelope.xsd)
      - Original: <http://www.w3.org/2003/05/soap-envelope/>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -sL http://www.w3.org/2003/05/soap-envelope/ \
        | diff -uw --strip-trailing-cr - w3/soap-envelope.xsd | vim -R -
        ```

<!-- end list -->

  - [xenc-schema.xsd](w3/xenc-schema.xsd)
      - Original:
        <http://www.w3.org/TR/2002/REC-xmlenc-core-20021210/xenc-schema.xsd>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -sL http://www.w3.org/TR/2002/REC-xmlenc-core-20021210/xenc-schema.xsd \
        | diff -uw --strip-trailing-cr - w3/xenc-schema.xsd | vim -R -
        ```

<!-- end list -->

  - [xlink.xsd](w3/xlink.xsd)
      - Original: <http://www.w3.org/1999/xlink.xsd>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -sL http://www.w3.org/1999/xlink.xsd \
        | diff -uw --strip-trailing-cr - w3/xlink.xsd | vim -R -
        ```

<!-- end list -->

  - [xml.xsd](w3/xml.xsd)
      - Original: <http://www.w3.org/2001/xml.xsd>
      - Ingen endringer.
  - [xmldsig-core-schema.xsd](w3/xmldsig-core-schema.xsd)
      - Original:
        <http://www.w3.org/TR/xmldsig-core/xmldsig-core-schema.xsd>
      - Endringer:
        ``` brush: bash; toolbar: false
        curl -sL http://www.w3.org/TR/xmldsig-core/xmldsig-core-schema.xsd \
        | diff -uw --strip-trailing-cr - w3/xmldsig-core-schema.xsd | vim -R -
        ```

#### [SOAP/1.1 envelope XSD fil](xmlsoap/)

  - [envelope.xsd](xmlsoap/envelope.xsd)
      - Original: <http://schemas.xmlsoap.org/soap/envelope/>
      - Ingen endringer.

#### [xs3p/](xs3p/)