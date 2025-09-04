# Imput message

<?xml version="1.0" encoding="UTF-8"?>

<OBBISOFT>

<MESSAGE>

<STANDARD\_MESSAGE>

<CUSTOMER\_MESSAGE><![CDATA[001179~RECE2GEF~BERGESLC~GEFCO~20250218123818--5~2025-02-18T12:38:18+01:00~START~NLHFMA1GAPZ418998~~VN~048530000.001~2T~243018~2025-02-18T00:00:00+01:00~~S~~~~012TI20ES..A3...~GQS6K5615~GQ~0~048530000.362~TAR~BAL TARRAGONA (CEVA FVL SPAIN)~H.E.D.A., S.A. (VN)~MUELLE DE ANDALUCIA~~43004~43~TARRAGONA~ES~~~~N]]></CUSTOMER\_MESSAGE>

<EV\_ENTREE>XXPART</EV\_ENTREE>

<FILENAME>BERGE\_RECE2GEF\_20240417.txt</FILENAME>

<SYNCHRO\_NO>001179</SYNCHRO\_NO>

<DATEVEN>2025-02-18T12:38:18+01:00</DATEVEN>

</STANDARD\_MESSAGE>

</MESSAGE>

<CRITERES>

<METIER>EDI</METIER>

<CONTEXTE>XXPART\_EVENT</CONTEXTE>

<EVENT\_ID>RECE2GEF</EVENT\_ID>

<EVENT\_SUB\_ID>RECE2GEF-START</EVENT\_SUB\_ID>

<MVT\_NO>001179</MVT\_NO>

<MVT\_TYPE>RECE</MVT\_TYPE>

<DEP\_POINT\_ID>243018</DEP\_POINT\_ID>

<ARR\_POINT\_ID>243018</ARR\_POINT\_ID>

<VEH\_VIN>NLHFMA1GAPZ418998</VEH\_VIN>

<COMMODITY\_ID>VN</COMMODITY\_ID>

<VEH\_MAKE\_ID>2T</VEH\_MAKE\_ID>

<REF1>NLHFMA1GAPZ418998</REF1>

<REF2>RECE2GEF|243018|BERGE\_RECE2GEF\_20240417.txt</REF2>

</CRITERES>

</OBBISOFT>

|  |  |
| --- | --- |
| EQ\_NO | 1179 |
| FILE\_NO | RECE2GEF |
| SENDER\_ID | BERGESLC |
| RECEIVER\_ID | GEFCO |
| TIMESTAMP | 20250218123818--5 |
| FILE\_DATE | 2025-02-18T12:38:18+01:00 |
| CONTEXT | START |
| VEH\_VIN | NLHFMA1GAPZ418998 |
| VEH\_LICENSE\_NUMBER |  |
| COMMODITY\_ID | VN |
| VEH\_CUSTOMER\_ID | 048530000.001 |
| VEH\_MAKE\_ID | 2T |
| ARR\_PLATFORM\_ID | 243018 |
| END\_TRANSP\_DATE | 2025-02-18T00:00:00+01:00 |
| CARRIER\_ID |  |
| TRANSPORT\_MODE | S |
| MEANS\_ID |  |
| TRANS\_DOC\_NO |  |
| DEP\_PLATFORM\_ID |  |
| VEH\_MODEL\_ID | 012TI20ES..A3... |
| VEH\_EXTMODEL\_ID | GQS6K5615 |
| VEH\_MODEL\_MEANING | GQ |
| KM | 0 |
| CONSIGNEE\_ID | 048530000.362 |
| CONSIGNEE\_EXTID | TAR |
| CONSIGNEE\_NAME | BAL TARRAGONA (CEVA FVL SPAIN) |
| CONSIGNEE\_NAME2 | H.E.D.A., S.A. (VN) |
| CONSIGNEE\_ADDRESS | MUELLE DE ANDALUCIA |
| CONSIGNEE\_ADDRESS2 |  |
| CONSIGNEE\_ZIP | 43004 |
| CONSIGNEE\_STATE | 43 |
| CONSIGNEE\_CITY | TARRAGONA |
| CONSIGNEE\_ISO\_COUNTRY\_ID | ES |
| PARK\_STORING\_AREA\_ID |  |
| PARK\_STORING\_WALK\_ID |  |
| PARK\_STORING\_SPACE\_NO |  |
| STORAGE\_CHECK | N |

### RECE2GEF Treatment

Make [primary calculation](#_primary_calculation)

|  |  |  |
| --- | --- | --- |
| Variable name | Value |  |
| £BesRef | get the Reference Number of the transmission provide by DXC/or FileName |  |
| £OrderDate | OBBISOFT.MESSAGE/STANDARD\_MESSAGE.DATEVEN (Input format YYYY-MM-DDTHH:MI:SS , Output format YYYY-MM-DDTHH:MI:SS ) | 2025-02-18T12:38:18+01:00🡺**2025-02-18T12:38:18** |
| £Contexte | OBBISOFT.MESSAGE.CRITERES.CONTEXTE | XXPART\_EVENT |
| £EventID | OBBISOFT.MESSAGE.CRITERES.EVENT\_ID | RECE2GEF |
| £Param1 | OBBISOFT.PIVOTS.ABONNE.PARAM1 |  |
| £Param2 | OBBISOFT.PIVOTS.ABONNE.PARAM2 | BERGE,SIPCO |
| £listIssuer | OBBISOFT.PIVOTS.ABONNE.PARAM3 |  |
| £Param4 | OBBISOFT.PIVOTS.ABONNE.PARAM4 | BERGE,SIPCO |
| £PropCodifRes | "PCOD SI2G\_CE " | "PCOD SI2G\_CE " |
| £SynchroMode | "NO\_ONE" | "NO\_ONE" |
| £ SynchroNum | "" |  |
| £DateEven | OBBISOFT.MESSAGE.STANDARD\_MESSAGE.DATEVEN | 2025-02-18T12:38:18+01:00 |
| £Codifevent = | “GEFCO” | “GEFCO” |
| £issuer | SENDER\_ID | BERGESLC |
| £OriginSoftware | If £issuer in £listIssuer then £OriginSoftware = concatenate(£issuer;"+")  Else  £OriginSoftware = £issuer | BERGESLC |
| £DeliveryKind | DELIVERY | DELIVERY |
| £CheckCallOff | False | False |
| £MsgMasterNo | “” |  |
| £MsgMasterSequence | “” |  |
| £MsgMasterNumber | “” |  |

Make [Record data calculation](#_Record_data_calculation)

|  |  |  |
| --- | --- | --- |
| Variable | value |  |
| £Vin | VEH\_VIN | NLHFMA1GAPZ418998 |
| £License | VEH\_LICENSE\_NUMBER |  |
| £PropCodifRes | "PCOD SI2G\_CE" | PCOD SI2G\_CE |
| £DEP\_POINT\_ID | DEP\_PLATFORM\_ID |  |
| £ARR\_POINT\_ID | ARR\_PLATFORM\_ID | 243018 |
| £Nature | COMMODITY\_ID if avail else « VN » | VN |
| £DOO | Concat (“DO.” ; SENDER\_ID) | DO.BERGESLC |
| £Mvt\_type = | Concat (FILE\_NO ; "-" ; CONTEXT) | RECE2GEF-START |
| £Mvt | FILE\_NO | RECE2GEF |
| £Issuer | SENDER\_ID | BERGESLCF |

£MsgMasterNumber =”0”

£MsgMasterSequence =”000”

£MsgMasterNo=””

If £PARAM4 is filled and SENDER\_ID = “BERGESLC”

|  |  |  |
| --- | --- | --- |
| Variable |  | Value |
| $CodifLoadADep | GEFCO |  |
| $CodifLoadArr | GEFCO |  |
| £LoadMovement | If RECE2GEF.CONTEXT= “START" then **£LoadMovement = « EXP »**  If RECE2GEF.CONTEXT= “CANCEL" then **£LoadMovement = « UNEXP »** | EXP |
| £Ext\_LoadNo | Concatenate VIN ; « \_ » ; **£LoadDep;** ; « \_AUTO» ; | NLHFMA1GAPZ418998\_243012\_AUTO |
| £LoadNo | “” |  |
| £LOAdStatus |  |  |
| £LoadDep | If RECE2GEF.ARR\_PLATFORM\_ID = £PARAM4 element1Then  £CodifLoadDep =”GEFCO”  **£LoadDep** = £PARAM4 element2 | RECE2GEF.ARR\_PLATFORM\_ID =243018  RECE2GEF.ARR\_PLATFORM\_ID = 243018  £CodifLoadDep =”GEFCO”  £LoadDep = 243012 |
| £TripNo | Concatenate VIN ; « \_ » ; **£LoadDep;** ; « \_AUTO» ; | NLHFMA1GAPZ418998\_243012\_AUTO |
| £TranspMode | ‘R’ | R |
| £Codifcarrier | PCOD SI2G\_CE | PCOD SI2G\_CE |
| £Codifcharter | PCOD SI2G\_CE | PCOD SI2G\_CE |
| £Carrier | concact (“TRSP\_” ; RECE2GEF.SENDER\_ID” ;“\_R” ) | TRSP\_BERGESLC\_R |
| £Charter | £Charter= £Carrier | TRSP\_BERGESLC\_R |
| £means | ”JOKEY” | “JOKEY” |
| £ARR\_POINT\_ID | if **£ARR\_POINT\_ID** = RECE2GEF.ARR\_PLATFORM\_ID  £CodifLoadArr =”GEFCO”  **£LoadArr** =£ARR\_POINT\_ID | £ARR\_POINT\_ID =243018  RECE2GEF.ARR\_PLATFORM\_ID = 243018  £CodifLoadArr =”GEFCO”  £LoadArr = 243018 |
| £PTF | RECE2GEF.DEP\_PLATFORM\_ID | “” |
| £ManifestNo | £ManifestNo = «  » | “” |
| £Receiver | £Receiver = concat (£Issuer; “.” ; £TranspMode)  (as the Load dis made by the partner, dont need to transfert that load to GEFCO tools ) | BERGESLC.R |
| £CodifReceiver | £CodifReceiver =£Codifcarrier | PCOD SI2G\_CE |
| £Nb\_veh\_trip | 1 | 1 |
| £TruckPlateNo | ”” |  |
| £DriverName | ”” |  |
| £WagonNo | ”” |  |
| £VesselNo | ”” |  |
| £VesselName | ”” |  |
| £DeliveryKind | ”” |  |
| £RealDateTime | **£RealDateTime** = RECE2GEF.END\_TRANSP\_DATE if avail else SYSTEM\_DATE  Subtract 1 hour from **£RealDateTime**  Format YYYY-MM-DDTHH:MI:SS  Example  If END\_TRANSPORT-DATE =  2025-03-06T00:00:00+01:00 then 2025-03-05-23:00:00  2025-03-30T02:45:35+01:00 then 2025-03-30T01:45:35 | RECE2GEF.END\_TRANSP\_DATE = 2025-02-18T00:00:00+01:00 🡺 2025-02-17T23 :00 :00 |
| £SynchroMode | “MASTER\_MESSAGE” |  |
| £MsgMasterNo | concatenate (£VIN,£MVT, sysdate (format yyyymmddhh24miss)) | NLHFMA1GAPZ418998RECE2GEF20250423140347 |
| £MsgMasterSequence | ”001” | “001” |
| £MsgMasterNumber | If RECE2GEF.KM is filled  ”3”  Else “2” | 2 |

make an [**INCOMMING\_LOAD**](#_INCOMING_LOAD_Mapping) mapping

<?xml version="1.0" encoding="UTF-8"?>

<IncomingLoad>

<Header>

<MessageNo>RECE2GEF\_23020484509802.xml</MessageNo>

<MessageDate>2025-02-18T13:38:18</MessageDate>

<Issuer>

<Codification>PCOD SI2G\_CE</Codification>

<XCode>BERGESLC</XCode>

</Issuer>

<Receiver>

<Codification>PCOD SI2G\_CE</Codification>

<XCode>BERGESLC.R</XCode>

</Receiver>

<OriginSoftware>BERGESLC</OriginSoftware>

<MvtType>EXP</MvtType>

<MsgSynchroMode>MASTER\_MESSAGE</MsgSynchroMode>

<MsgMasterNo>NLHFMA1GAPZ418998RECE2GEF20250423140347</MsgMasterNo>

<MsgMasterSequence>001</MsgMasterSequence>

<MsgMasterNumber>3</MsgMasterNumber> **should be 2**

</Header>

<Trip>

**<TripXNo >NLHFMA1GAPZ418998\_243012\_AUTO</TripXNo >**

<TotalVehiclesNumber>1</TotalVehiclesNumber>

<Supplier>

<Codification>PCOD SI2G\_CE</Codification>

<XCode>TRSP\_BERGESLC\_R</XCode>

</Supplier>

<ExecSupplier>

<Codification>PCOD SI2G\_CE</Codification>

<XCode>TRSP\_BERGESLC\_R</XCode>

</ExecSupplier>

</Trip>

<Load>

**<LoadXNo> NLHFMA1GAPZ418998\_243012\_AUTO </LoadXNo>**

<TransportMode>R</TransportMode>

<LoadDeparture>

**<Codification> GEFCO </Codification>**

<XCode>243012</XCode>

<RealDateTime>2025-02-17T23:00:00</RealDateTime>

</LoadDeparture>

<LoadArrival>

<Codification>GEFCO</Codification>

<XCode>243018</XCode>

</LoadArrival>

<Vehicle>

<VehIdentification>

<Vin>NLHFMA1GAPZ418998</Vin>

</VehIdentification>

<Movement>EXP</Movement>

</Vehicle>

</Load>

</IncomingLoad>

Send output

£Token1 = Concat(“XXPART:”; £Issuer ; “-“;£Mvt\_Type)

£Token2 = concat (£VIN ; “/” ; £DEP\_POINT\_ID; “/” ; £ARR\_POINT\_ID)

£Token3 = “OK IN\_LOAD”

Make successful Tracking

*Mapping of in coming order update\_veh to update the mileage of the vehicle*

If RECE2GEF.KM is filled

£Mileage = RECE2GEF.KM

£OrderKind = « **UPDATE\_VEH**»

£RealDateTime = SYSTEM\_DATE

£SynchroMode = “MASTER\_MESSAGE”

If £MsgMasterNo is not filled then £MsgMasterNo = concatenate (£VIN,£MVT, sysdate (format yyyymmddhh24miss))

£MsgMasterSequence =£MsgMasterSequence +1 ( format 3 characters example if 1 the 001)

If £MsgMasterNumber =”0” then £MsgMasterNumber =”2”.

make an  [**INCOMMING\_ORDER** mapping](#_INCOMING_EVENT_Mapping)

Send output

£Token1 = Concat(“XXPART:”; £Issuer ; “-“;£Mvt\_Type)

£Token2 = concat (£VIN ; “/” ; £DEP\_POINT\_ID; “/” ; £ARR\_POINT\_ID)

£Token3 = “OK IN ORDER VEH\_UPDATE”

Make successful Tracking

£MsgMasterSequence =~~”002”~~ £MsgMasterSequence +1 ( format 3 characteres exemple if 1 the 001)

£MsgMasterSequence =£MsgMasterSequence +1 ( format 3 characteres exemple if 1 the 001)

Make [RECE2GEF calculation](#_RECE2GEF_calculation)

|  |  |  |
| --- | --- | --- |
| Variable | value |  |
| £EventLoc | ARR\_PLATFORM\_ID | 243018 |
| £RealDateTime | END\_TRANSP\_DATE the | 2025-02-18T00:00:00+01:00 |
| £PTF | ARR\_PLATFORM\_ID | 243018 |
| £EventKind | If £Mvt\_Type= "RECE2GEF-START"  £EventKind = “EXECUTION”  If £Mvt\_Type= "RECE2GEF-CANCEL"  £EventKind = “EXECUTION” | EXECUTION |
| £EventXcode | “RECEPT” | “RECEPT” |
| £EventXSubCode | £Mvt\_Type |  |
| £EventActionDescription | If £Mvt\_Type= "RECE2GEF-START"  £EventActionDescription = concat(“recept in :” ; £EventLoc ;” by “;£issuer)  If £Mvt\_Type= "RECE2GEF-CANCEL"  £EventActionDescription = concat(“cancel rece in :” ; £EventLoc ;” by “;£issuer) |  |
| £PLACE | Concatenate (PARK\_STORING\_AREA\_ID; ”-“; PARK\_STORING\_WALK\_ID;”-“; PARK\_STORING\_SPACE\_NO )  Put “-“ only if the data defore or after is fileld |  |

**£RealDateTime** = RECE2GEF.END\_TRANSP\_DATE if avail else SYSTEM\_DATE

Make an [**INCOMMING\_EVENT** mapping](#_INCOMING_EVENT_Mapping)

Send output

£Token1 = Concat(“XXPART:”; £Issuer ; “-“;£Mvt\_Type)

£Token2 = concat (£VIN ; “/” ; £DEP\_POINT\_ID; “/” ; £ARR\_POINT\_ID)

£Token3 = “OK IN\_EVENT”

Make successful Tracking