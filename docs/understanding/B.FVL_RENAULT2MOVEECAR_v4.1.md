|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| **ESB Specification** | | | | |
| **Business :** *Business for ESB perspective*  NOSTRA,INES, EDI,GEOLOG,ISYGO, … | | ***MOVEECAR*** | | |
| **Flow description :** | | **RENAULT ORDER TO MOVEECAR** | | |
| **Inbound server** *(to setup the flow parameters)* | |  | | |
| **Inbound Queue : I…. or B….** | | **B.FVL\_RENAULT2MOVEECAR** | | |
| **Outbound server and Qmanager** | |  | | |
| **Outbound Queue  : B…. or O….** | | O.MOVEECAR\_GEFCO2MOVEECAR | | |
| **Mapping : (yes/no)** | | **YES/NO** | | |
| **Outbound to be send to EDI**  **(DXC -BES) : (yes/no)** | | **NO** | | |
| DXC -BES setup (\*\*\*\*Header definition): | | | | |
| Type | | | *(8 characters max)* | |
| Sender | | | *(14 characters max)* | |
| Consignee | | | *(14 characters max)* | |
|  |  | | | |
| ESB setup (How outbound queue(s) is managed):  *Information to be provided by ESB team* | | | | |
| EAI\_DISPATCH : *the name of the field or the name of the incoming flow tag or other external variable or list of values ​​that can fill the key of this table* | | |  | |
| TDMQ<InboundQueueName>\_QU | | |  | |
| FIC\_GENERIQUE\_QU : *Flow id* | | |  | |
| PARAM : *yes/no does this table allow the determination of the output queue?* | | |  | |
| **OBSERVATIONS** | | | |
|  | | | |

|  |
| --- |
| **Document history** |

|  |  |  |  |
| --- | --- | --- | --- |
| **Version** | **Date** | **Requestor** | **Description** |
| 1.0 | 01/07/2020 | Bhagyada Modali | Initial Document |
| 1.2 | 11/09/2020 | Fabiola Maillot | [FLXALP-2676](http://jira.inetgefco.net/jiraprod/browse/FLXALP-2676) Evolution  Mapping of incoming\_order for VA00  Modification of model code for TR01 |
| V1.0-b | 13/10/2020 | F Maillot | [FLXALP-2767](http://jira.inetgefco.net/jiraprod/browse/FLXALP-2767) : add product tag and other evolution need by the outbound flow  Rename this version V1.0-b as this mapper was not delivered to production so the version still be 1.0 |
| V1.0-c | 20/10/2020 | F Maillot | Evolution following the test with MOVEECAR |
| V1.0-d | 28/10/2020 | F Maillot | Evolution following the test with MOVEECAR |
| V1.0-e | 29/10/2020 | F Maillot | Put False in the <CheckCallOff> for announce |
| V1.1 | 22/01/2021 | F Maillot | [FLXALP-2926](http://jira.inetgefco.net/jiraprod/browse/FLXALP-2926) Modification for locking\_order  Suppress the LOCK\_ORDER or UNLOCK\_ORDER in the TR01 treatment and replace by a new tag **CheckPickupUnavailable** |
| V1.1-a | 22/01/2021 | F Maillot | Evolution and CANCELLATION |
| V1.1-b | 17/03/2021 | F Maillot | Modification on CheckPickupUnavailable put it as the same level as PickupDate |
| V1.1-c | 25/03/2021 | Fabiola Maillot | [FLXALP-3068](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3068) Modification country of delivery and consignee in the incoming\_order |
| V1.2 | 29/04/2021 | Fabiola maillot | [FLXALP-3145](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3145) : Add an Incomming\_order VEH Update in the VA00 treatment |
| V1.3 | 01/07/2021 | Vincent Santerre | Update of Delivery in incoming order |
| V1.4 | 19/07/2021 | Vincent Santerre | Update of the incoming order LockingOrderno into LockingOrderNo |
| V1.5 | 26/08/2021 | Vincent Santerre | Update of MsgsynchroNumber |
| V1.6 | 31/08/2021 | Vincent Santerre | Update of MsgSynchroNumber |
| V1.7 | 01/09/2021 | Vincent Santerre | Update of MsgSynchroNumber + insert of £SEQ |
| V1.8 | 06/09/2021 | Vincent Santerre | [FLXALP-3455](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3455) Update of MsgSynchroNumber to replace by NO\_ONE |
| V1.9 | 16/09/2021 | Hicham TAHRI | [FLXALP-3481](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3481) Update |
| V2.0 | 23/09/2021 | Vincent Santerre | Update of country |
| V2.1 | 13/09/2021 | Fabiola Maillot | [FLXALP-3533](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3533) Modification for VE01 : change ServiceOrder**n**o by ServiceOrder**No**  Populate a customer\_reference to store the LOGISTICS-PARTNER-CD |
| V2.2 | 15/11/2021 | Hicham TAHRI | [FLXALP-3576](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3576) Add a customer reference DELETED after the integration of TD01 |
| V2.3 | 08/12/2021 | Vincent Santerre | Update of £Model\_Ext in VA01 and TR01 |
| V2.4 | 16/02/2022 | Hicham TAHRI | [FLXALP-3714](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3714) Add a height and length of the VA00 in the incoming order announce |
| V2.5 | 22/02/2022 | Hicham TAHRI | [FLXALP-3722](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3722) Add a value  “DELETED” in CustomerReference at the integration of the TR01 if we deliver the vehicle to external compound |
| V2.6 | 02/03/2022 | Vincent Santerre | [FLXALP-3730](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3730)  Update of MvtType in the case of VIN change |
| V2.6a | 03/03/2022 | Vincent Santerre | [FLXALP-3730](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3730)  Correction of MvtType in the case of VIN change |
| V2.7 | 15/03/2022 | TAHRI Hicham | [FLXALP-3754](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3754) A little update |
| V3.0 | 05/04/2022 | TAHRI HICHAM | [FLXALP-3788](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3788) An update in order to create two compounds GEFCO with the same code STEFI. We need to create an internatl code even if we are not release agent. we have to send messages to AS400 |
| V3.1 | 02/05/2022 | Vincent Santerre | [FXLALP-3828](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3828)  Update of Pickup in the case of UPDATE\_VEH |
| V3.2 | 16/05/2022 | TAHRI Hicham | [FLXALP-3842](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3842) Add an incoming event in order to make the transport available for the compound Sandouville at the integration of transport order available for Italy |
| V3.3 | 07/06/2022 | TAHRI Hicham | [FLXALP-3876](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3876). A little update concerning VA00 in order to update the vehicles for the uses case update of the VINs |
| V3.4 | 10/06/2022 | TAHRI.Hicham | [FLXALP-3885](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3885) An update of date event |
| V3.5 | 17/06/2022 | TAHRi HIcham | [FLXALP-3897](http://jira.inetgefco.net/jiraprod/browse/FLXALP-3897) An update concerning a first VA00 with two VINs (new and old) and to ta3.5 b ke into account a new need the used vehicles.  3.5b Some update concerning the VA02 update |
| V3.6 | 24/03/2023 | TAHRI Hicham | An update concerning the information of the previous transport done by another carrier |
| V3.7 | 09/05/2023 | TAHRI Hicham | [FLXALP-4202](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4202) A little update concerning the **£Pickup\_Start** at the integration of the TR01 |
| V3.8 | 23/10/2023 | Vincent Santerre | [FLXALP-4335](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4335)  Update on VA00 Vehicle update |
| V3.8a | 30/10/2023 | Vincent Santerre | [FLXALP-4335](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4335)  Update on VA00 Vehicle update (ModelDeterminationMode) |
| V3.9 | 21/03/2024 | Hicham TAHRI | [FLXALP-4420](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4420) Update on VA00 new field “registration” and engine type |
| V4.0 | 23/05/2024 | Hicham TAHRI | [FLXALP-4452](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4452)  New use case transport done by another carrier from CEVA’s compound |
| 4.0a | 30/05/2024 | Hicham TAHRI | [FLXALP-4452](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4452)  A little update |
| 4.0b | 03/06/2024 | Hicham TAHRI | [FLXALP-4452](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4452) update of the LD01 |
| 4.0C | 06/06/2024 | Hicham TAHRI | [FLXALP-4452](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4452) take into account information in the VA00 : DeliveryCutomerxcode |
| 4.0d | 10/06/2024 | Hicham TAHRI | [FLXALP-4452](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4452) a new update |
| 4.1 | 14/04/23 | Hicham TAHRI | [FLXALP-4535](http://jira.inetgefco.net/jiraprod/browse/FLXALP-4535) A new update |

|  |
| --- |
| **S O M M A I R E** |

[1 Interfaces 6](#_Toc168910768)

[1.1. Inbound interface 6](#_Toc168910769)

[1.2. Outbound interface 6](#_Toc168910770)

[1.2.1. dispatch type 6](#_Toc168910771)

[1.2.2. Static method (\*\*) 6](#_Toc168910772)

[1.2.3. Dynamic method (\*\*) 7](#_Toc168910773)

[1.2.3.1 DISPATCH TABLE : TDMQ\_FIC\_GENERIQUE\_QU 7](#_Toc168910774)

[1.2.3.2 DISPATCH TABLE : EAI\_DISPATCH 7](#_Toc168910775)

[1.2.3.3 DISPATCH TABLE : EAI\_DISPATCH\_DETAIL 7](#_Toc168910776)

[1.2.3.4 DISPATCH TABLE : TDMQ\_PARAM 7](#_Toc168910777)

[1.2.3.5 DISPATCH TABLE : TDMQ<FlowName> 7](#_Toc168910778)

[1.2.4. OUTBOUND INTERFACE 7](#_Toc168910779)

[2 TRACKING 8](#_Toc168910780)

[2.1. Success tracking 8](#_Toc168910781)

[2.2. Announce tracking: ANN01 8](#_Toc168910782)

[2.3. Error tracking 8](#_Toc168910783)

[2.3.1. Erreurs techniques 9](#_Toc168910784)

[2.3.2. Erreurs fonctionnelles 9](#_Toc168910785)

[3 Consignes d’exploitation 10](#_Toc168910786)

[4 Stored Procedure 10](#_Toc168910787)

[5 Paramètres du flow 10](#_Toc168910788)

[5.1. Les 2 paramètres du flow : $PARAM1 et $PARAM2 10](#_Toc168910789)

[5.2. Queue suite 11](#_Toc168910790)

[5.3. routing to a GENERIC QUEUE 11](#_Toc168910791)

[5.1. Accumulation des flow entrants 11](#_Toc168910792)

[6 Structure de l’Information 12](#_Toc168910793)

[6.1. Input STRUCTURE 12](#_Toc168910794)

[6.2. DEFINTION OF OBBISOFT.PIVOTS.ABONNE.PARAMx 13](#_Toc168910795)

[6.3. Records Format 13](#_Toc168910796)

[6.3.1. HEADER : ALL Record Type (except LD01) 13](#_Toc168910797)

[6.3.2. VA00 :Vehicle Identification 15](#_Toc168910798)

[6.3.3. VA01 : Ordre for transit 16](#_Toc168910799)

[6.3.4. VA02 : Announce Vehicle on a SHIP 18](#_Toc168910800)

[6.3.5. TR01 : TRANSPORT Order 19](#_Toc168910801)

[6.3.6. RD01 : CANCEL Order transit/Lock/Service 21](#_Toc168910802)

[6.3.7. VE01 : Service Ordre 22](#_Toc168910803)

[6.3.8. TD01 : Cancel Transport Order 23](#_Toc168910804)

[6.3.9. HR01 : LOCK/UNLOCK Order 24](#_Toc168910805)

[6.3.10. LD01 : LOAD/UNLOAD Order 25](#_Toc168910806)

[6.4. OUTBOUND STRUCTURE 26](#_Toc168910807)

[6.4.1. Preliminary Information 26](#_Toc168910808)

[6.4.2. treatment 29](#_Toc168910809)

[6.4.3. Outbound Structure Details 30](#_Toc168910810)

[6.4.3.1 INCOMMING\_ORDER Mapping 30](#_Toc168910811)

[6.4.3.2 INCOMING LOAD Mapping 35](#_Toc168910812)

[6.4.3.3 INCOMING EVENT mapping 37](#_Toc168910813)

[6.5. Traitements de mapping 38](#_Toc168910814)

[6.6. Traitements specifiques 39](#_Toc168910815)

[6.7. Traitements post-accumulation 39](#_Toc168910816)

# Interfaces

## Inbound interface

Inbound queue **B.FVL\_RENAULT2MOVEECAR**

Inbound format **: XML**

This table concerns EAI flow: I. \* and not B. \*, except for volumetry

*(\*) If this CU is used to treat the flow of 2 starting applications, then fill in this column 2.*

*(\*\*) = to be specified after consulting EAI team*

*(\*\*\*) = to specify if for derivatives (B. \*)*

|  |  |
| --- | --- |
| **Application 1** | |
| Which app. Generate the message | EDI |
| Test server | gerdcwflowdqm01 |
| Preproduction server | gexdcwflowjqm03 |
| Production server | gexdcwflowmqmv3 |
| **File interface specificity** | |
| Incoming folder |  |
| Filename format |  |
| Grouped reading (Y/N) ? (\*\*) |  |
| Type (scheduled or pushed) |  |
| Frequency for scheduling |  |
| Archive folder (if not standard ) |  |
| Archive duration |  |
| **Message interface specificity** | |
| Specificity |  |
| Archive on file system (Y/N) ? |  |
| Archive folder |  |
| Archive duration |  |
| **Common** | |
| Frequency of the exchange (daily, weekly, monthly) (\*\*\*) |  |
| Volume (\*\*\*) |  |

## Outbound interface

|  |  |  |
| --- | --- | --- |
| **No** | dispatch type | **Choix**(\*)  *(cocher une seule ligne)* |
| 1 | 1 to 1 (pas de choix possible) |  |
| 2 | n to 1 static method. |  |
| 3 | n to 1 dynamic method. |  |
| 4 | 1 to n static method. |  |
| 5 | 1 to n dynamic method. | X |

*(\*) For an inbound flow, the EAI can generate 1 or more outbound flows.*

*The output flow can be obvious, we have no choice (check line 1),*

*or*

*the outbound flow depends on a solution programmed in hard mode (ex: algorithm modulo) (one speaks of static method) (tick line 2 or 4 as the case),*

*or*

*the outbound flow depends on a solution using the external tables (we speak of dynamic method). This case also includes the case of 1 flow entering without choosing the outgoing flow, because one passes by the external tables. (check line 3 or 5 as appropriate).*

### Static method (\*\*)

Specify the list of codes, associated output queues, structures and fields for programming the dispatch rule.

Ex: modulo

Ex: Explain here how we go from 1 incoming flow to n outgoing flows.

*(\*\*) = to be specified after consulting EAI team*

### Dynamic method (\*\*)

Dispatch tables are used to transmit the flow to the partner's queue (s).

The EAI team will set up the necessary parameters: see Settings on page 1

|  |  |
| --- | --- |
| DISPATCH TABLE : TDMQ\_FIC\_GENERIQUE\_QU *Information to be provided by EAI Team* | |
| INBOUND | OUTBOUND |
|  |  |
| DISPATCH TABLE : EAI\_DISPATCH *Information to be provided by EAI Team* | |
| MAPPEUR | |
|  | |
| DISPATCH TABLE : EAI\_DISPATCH\_DETAIL *Information to be provided by EAI Team* | |
| INBOUND | OUTBOUND |
| **If DXC-BES : inbound queue name** | **B.FIC\_GENERIQUE\_HEADER** |
| **If DXC-BES : inbound queue name** | **O.EAI\_GEF2BES\_TMP\_FIC** |
| DISPATCH TABLE : TDMQ\_PARAM *Information to be provided by EAI Team* | |
| INBOUND | Outbound Queue |
|  |  |
| DISPATCH TABLE : TDMQ<FlowName> *Information to be provided by EAI Team* | |
| INBOUND | OUTBOUND |
|  |  |

### OUTBOUND INTERFACE

Outbound Queue **: O.MOVEECAR\_GEFCO2MOVEECAR**

Outbound Format : (*JMS-XML,FILE-XML,FLATFILE,CVS…)* **XML**

Only for outbound flow EAI : O.\*

|  |  |
| --- | --- |
| Which application read the message  (\*\*) ?  (EDI or Business application) | MOVEECAR |
| Test server | gerdcwflowdqm01 |
| Pre-production server | gexdcwflowjqm01 |
| Production server | gexdcwflowpqmv1 |
| **File interface specificity** | | |
| Reception folder |  |
| Filename |  |
| File creation |  |
| Post function |  |
| Folder consumer |  |
| **Message interface specificity** | | |
| **Specificity** |  |

*(\*\*) = this table is to be completed by the flow team for if it is a flow towards the EDI*

# TRACKING

The intranet application ‘Suivi EAI’ allows you to manually track and replay archived flows.

**Tracking (**Yes/no**) :** yes (by default)

**Archiving duration (in hours) (\*):**168 hours (by default)

**(\*)** Values ​​must be filled in if there is at least one normal follow-up, announcement or follow-up error.

## Success tracking

Info: No trace of tracking in normal situation in case of error with dynamic archiving.

Inbound queue : B.FVL\_RENAULT2MOVEECAR.

If the follow-up is occasional specify the conditions here : to be precise

|  |  |
| --- | --- |
| **Value for token 1**(max 128 c) | £Token1 |
| **Value for token 2**(max 128 c) | £Token2 |
| **Value for token 3**(max 128 c) | £Token3 |

In special cases, the follow-up can be done for each flow of arrival, or for each flow discarded, or ... consult the EAI team to leave the standard.

These are occasional follow-up sessions to express exceptional situations. The "follow up announcement" will not be interpreted as an error. He goes back to the tracking database as a normal follow-up (in green).

Inbound queue: Inbound queue

Le « suivi annonce » est toujours de type conditionnel (Yes/no) : to be precise

Dans quelles conditions ? : to be precise

|  |  |
| --- | --- |
| Announce tracking: ANN01 | |
| Context description: | This announce is made when… |
| Reference used in the treatment (maximum 10c) : | ANN01 |
| Token 1 (maximum 128c) meaning | **« Flow not taken into account … »** |
| Token 2 (maximum 128c) meaning | **tag1,« | »,tag2,« | »,tagA/tagB/tagC, « | » ,tag3, « | »,tag4…** |
| Token 3 (maximum 128c) meaning | **« flow stopped » or « flow continues » or «… »** |
| Action (continue flow, stop flow, other): |  |
| Dynamic archiving (Yes/no) | N |

## Error tracking

Note: Errors of the "unavailable resources" type (BDD, MQ, etc.) should not be treated in this chapter because they will be subject to automatic processing implemented by the tool.

**The service life in the error tracking database will be:**

**- Without dynamic archiving: the same as that of normal monitoring.**

**- With dynamic archiving: dynamically aligned to at least the value of the archiving duration of database type.**

### Erreurs techniques

|  |  |  |  |
| --- | --- | --- | --- |
| Erreur longueur *(traitement standard EAI)* | | **NON-TESTEE** | **TESTEE** |
| Meaning of the error : | Il s’agit des erreurs (ou non) provoquées par des longueurs hors normes du inbound flow. | | |
| Référence utilisée dans le traitement  (maximum 10c) | SF.CtlLG | | |
| Consignes | **CONSF01** | | |

|  |  |  |  |
| --- | --- | --- | --- |
| Erreur structure XML systématique pour un message XML *(traitement standard EAI)* | | **NON-TESTEE** | **TESTEE** |
| Meaning of the error : | La structure du message XML n’est pas conforme | | |
| Référence utilisée dans le traitement (maximum 10c) | SF.MES\_XML | | |
| Meaning Jeton 1 (maximum 128c) | structure XML non conforme | | |
| Action (continuation, arrêt flow, autre ) : | Arrêt du flow sans traiter les autres erreurs | | |
| Consignes | **CONSF01** | | |

### Erreurs fonctionnelles

Il s’agit des erreurs fonctionnelles qui sont référencées dans les traitements et les interfaces de départ et d’arrivée.

|  |  |
| --- | --- |
| Applicative Error i : | |
| Meaning of the error: | ? |
| Reference used in the treatment  (maximum 10c) | *ER ?* |
| Token 1 meaning (maximum 128c) | *To be specified* |
| Token 2 meaning (maximum 128c) | *To be specified* |
| Token 3 meaning (maximum 128c) (\*) | *? Error text ?* |
| Action (continue flow, stop flow, other): | “Flow is stopped without dealing with the other errors”  Or  “Flow is stopped after dealing with the other errors” |
| Instruction code | ???  See §Operating Instructions |
| Dynamic archiving (Yes/No) (\*\*\*) |  |

(\*) Jeton dédié au libellé long of the error (si nécessaire)

(\*\*) Code court of the error

(\*\*\*) Valable pour ARCHIVAGE (statique)=NON

# Consignes d’exploitation

Il s’agit du détail des consignes :

* Suivi (CONSSnnn)
* Alerte (CONSAnnn)
* Queue saturé (CONSQnnn)
* Base de donnée applicative indisponible (CONSDnnn)
* Autres (CONSXnnn)

Lorsque pendant le traitement on détecte une erreur codifiée ER…0n, la CONS…0n doit être appliquée

|  |  |  |  |
| --- | --- | --- | --- |
| **Code consigne** | **Erreur** | **Description** | **Qui appeler** |
| **CONSF01** | **SF.MES\_XML**  **Ou**  **SF.CtlLG** | Enregistrer l’incident en relevant le nom du flow, le nom du fichier, le code erreur et les jetons.  Acquittement immédiat | Equipe de maintenance/exploit des études(*email*) |
|  |  |  |  |
|  |  |  |  |

# Stored Procedure

The stored function is the methodological means for accessing the databases. The realization of the stored functions remains the domain of the Business domain.

The stored functions are validated in the test environment by the EAI cell. The modification of the stored function must be synchronous and in agreement with the EAI cell.

|  |  |
| --- | --- |
| **Fonctions stockées** | |
| **Nom** | **Description** |
|  |  |
|  |  |
|  |  |

# Paramètres du flow

## Les 2 paramètres du flow : $PARAM1 et $PARAM2

Each EAI flow has two external parameters from 1 to maximum 64 characters that can be modified "on line" by the EAI team.

The flow parameters can appear in the mapper algorithms (example: in the arrival structure).

They will be referenced by the mnemonics $ PARAM1 and $ PARAM2 and will be used in the construction of tokens, or in mapping processes. The meaning of two parameters remains the responsibility of the CU Editor. These parameters can allow the outsourcing of values ​​that change quite often.

|  |  |  |
| --- | --- | --- |
| **Paramètre** | **Utilisé (**Yes/no**)** | **Valeur** |
| $PARAM1 | Oui | Version flow |
| $PARAM2 | Non |  |

Exemple : dans le §Suivi on peut préciser que le $PARAM1 sera toujours ajouté dans le jeton2 quelque soit la situation (normale, erreur, annonce, doublon)

## Queue suite

The concept of "queue suite" allows the respect of the chronological order of the messages within the framework of an architecture: Flow father and several flow son and in certain circumstances.

In this case, the tail queue will have to point to the tail of the mapper immediately less important in the order of priorities.

**Gestion de la queue suite (**Yes/no**) :** à préciser

**Nom de la queue suite :** QueueArrivée

**Condition pour le traitement local (expression booléenne) :**

## routing to a GENERIC QUEUE

The messages may be routed to one or more generic tails each consisting of a set of "n" tails numbered from: nomqueue01 to n in a manner:

A) Pseudo-random according to the date, or

B) Compared to a calculated and bounded variable "v" provided by the mapper. The bounds of the variable must be between 0 and a maximum "m-1" value. We say that the variable "v" is computed with respect to a functional criterion, modulo "m".

Observation: It is necessary that m >> n. The value n depends on a circumstantial choice. For example: universe (test, pre-production, production). The value m is fixed and is set to the scheduler of the mapper.

Generic routing management (Yes / no): to be specified

(if yes, define the values ​​of variables nomqueue, m, formula, and n by environment)

|  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| cas | Nom de la queue  (**nomqueue**) | **m** | Formule de calcul de v avant modulo | **n** | | |
| Intégr. | pré-prod | prod |
| A |  |  |  |  |  |  |
| B | exemple :  O.NOS\_MIG\_MODULOVIN | ex : 100 | exemple :  additionner la valeur entière de la représentation binaire pour la chaîne xxxxx (donnée en entrée du flow) | ex :  10 | ex :  10 | ex :  10 |

## Accumulation des flow entrants

Dans le cas où le flow sortant résulte d’un ‘append’ de plusieurs flow entrant, on doit paramétrer un traitement d’accumulation

|  |  |  |
| --- | --- | --- |
| **Paramètre** | **Meaning** | **Valeur** |
| $QUANTITE | Nombre de flow entrant à cumuler | ? |
| $FREQUENCE | Fréquence de traitement du flow résultat | ? |

Un traitement post-accumulation est décrit dans le §‎7.1Traitements post-accumulation

# Structure de l’Information

## Input STRUCTURE

INPUT Flow: **I.PIVOTS**

Format (XML, fixe format, variable format, others ) : **Flat Fix Format**

**Description**

|  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| <?xml version="1.0" encoding="UTF-8"?> | | | | |  |  |
| <OBBISOFT> | | |  | |  |  |
|  | <MESSAGE> | | |  |  |  |
|  |  | <STANDARD\_MESSAGE> | | |  |  |
|  |  |  | <CUSTOMER\_MESSAGE> | |  |  |
|  |  |  |  | **<![CDATA[** | £Cdata | ]]> |
|  |  |  | </CUSTOMER\_MESSAGE> | |  |  |
|  |  |  | <EV\_ENTREE> | | « RENAULT » | </EV\_ENTREE> |
|  |  |  | <FILENAME> | | Filename | </FILENAME> |
|  |  |  | <FILE\_LINE\_NO> | |  | </FILE\_LINE\_NO> |
|  |  |  | <SYNCHRO\_NO> | |  | </SYNCHRO\_NO> |
|  |  |  | < DATEVEN > | | £DATEVEN | </DATEVEN> |
|  |  | </STANDARD\_MESSAGE> | | |  |  |
|  | </MESSAGE> | | | |  |  |
|  | <CRITERES> | | |  |  |  |
|  |  | **<METIER>** | | | "EDI" | </METIER> |
|  |  | **<CONTEXTE>** | | | RENAULT\_ORDER | </CONTEXTE> |
|  |  | **<EVENT\_ID>** | | | £MVT\_TYPE | </EVENT\_ID> |
|  |  | **<EVENT\_SUB\_ID>** | | |  | </EVENT\_SUB\_ID> |
|  |  | **<MVT\_NO>** | | | £ORDER | </MVT\_NO > |
|  |  | <MVT\_TYPE**>** | | | £MVT\_TYPE | </MVT\_TYPE > |
|  |  | <CONTEXTE\_MVT**>** | | |  | </CONTEXTE\_MVT > |
|  |  | <MESSAGE\_CODE**>** | | |  | </MESSAGE\_CODE> |
|  |  |  |  |  | <!--\*\*\*\*\*\*\*\*DEPARTURE\*\*\*\*\*\*\*\*\*\*\*\*\*--> |  |
|  |  | **<DEP\_POINT\_ID>** | | | £DEP\_POINT\_ID | </DEP\_POINT\_ID > |
|  |  | <DEP\_POINT> | | |  | </INT\_DEP\_POINT > |
|  |  | <INT\_DEP\_POINT> | | |  | </INT\_DEP\_POINT > |
|  |  | **<DEP\_COUNTRY>** | | |  | </DEP\_COUNTRY> |
|  |  |  |  |  | <!--\*\*\*\*\*\*\*\*ARRIVAL\*\*\*\*\*\*\*\*\*\*\*\*\*--> |  |
|  |  | **<ARR\_POINT\_ID>** | | | £ARR\_POINT\_ID | </ARR\_POINT\_ID > |
|  |  | <ARR\_POINT> | | |  | </INT\_ARR\_POINT\_ID > |
|  |  | <INT\_ARR\_POINT\_ID> | | |  | </INT\_ARR\_POINT\_ID > |
|  |  | **<ARR\_COUNTRY>** | | | £ARR\_POINT\_ID -Ctry | </ARR\_COUNTRY> |
|  |  | <DELIVERY\_XCODE**>** | | |  | </DELIVERY\_XCODE > |
|  |  | <DELIVERY\_TYPE**>** | | |  | </DELIVERY\_XCODE > |
|  |  | <MESSAGE\_CODE**>** | | |  | </MESSAGE\_CODE > |
|  |  | <DELIVERY\_AREA\_XCODE**>** | | |  | </DELIVERY\_XCODE > |
|  |  | <CONSIGNEE\_XCODE**>** | | |  | </CONSIGNEE\_XCODE > |
|  |  | <PICKUP\_DATE**>** | | |  | </PICKUP\_DATE > |
|  |  |  |  |  | <!--\*\*\*\*\*\*\*\*VEHICLE\*\*\*\*\*\*\*\*\*\*\*\*\*--> |  |
|  |  | <VEH\_VIN> | | | VEHICLE-ID | </VEH\_VIN> |
|  |  | <VEH\_IMMAT> | | |  | </VEH\_IMMAT> |
|  |  | <NUMOF> | | |  | </VEH\_IMMAT> |
|  |  | <COMMODITY\_ID> | | | "VN" | </COMMODITY\_ID> |
|  |  | <VEH\_MAKE\_ID> | | |  | </VEH\_MAKE\_ID> |
|  |  |  |  |  | <!--\*\*\*\*\*\*\*\*LOCKING\*\*\*\*\*\*\*\*\*\*\*\*\*--> |  |
|  |  | <LOCKING\_KIND> | | | £Lock | </LOCKING\_KIND> |
|  |  | <LOCKING\_ID> | | |  | </LOCKING\_ID> |
|  |  |  |  |  | <!--\*\*\*\*\*\*\*\*SERVICES\*\*\*\*\*\*\*\*\*\*\*\*\*--> |  |
|  |  | <SERV\_ORDER\_INT> | | |  | </SERV\_ORDER\_INT> |
|  |  | <SERV\_ORDER\_EXT> | | | £Services | </SERV\_ORDER\_EXT> |
|  |  | <CHECK\_CUSTOMS> | | |  | </CHECK\_CUSTOMST> |
|  |  | <ORDER\_STATUS> | | |  | </ORDER\_STATUS> |
|  |  | <SERV\_PLATFORM\_ID> | | | If FILE\_NO= VE01 VE01.NODE else no tag | </SERV\_PLATFORM\_ID> |
|  |  |  |  |  | <!--\*\*\*\*\*\*\*\*TRSP ORDER\*\*\*\*\*\*\*\*\*\*\*\*\*--> |  |
|  |  | <SHIP\_STATUS> | | |  | </SHIP\_STATUS> |
|  |  | <TRANSPORT\_MODE> | | |  | </TRANSPORT\_MODE> |
|  |  | <CARRIER\_ID> | | | £Carrier | </CARRIER\_ID> |
|  |  | <CHARTER\_ID> | | |  | </CHARTER\_ID> |
|  |  | <LOAD\_NUM\_EXT> | | |  | </LOAD\_NUM\_EXT> |
|  |  | <LOAD\_NUM\_INT> | | |  | </LOAD\_NUM\_INT> |
|  |  | <VOY\_NUM\_EXT> | | |  | </VOY\_NUM\_EXT> |
|  |  | <VOY\_NUM\_INT> | | |  | </VOY\_NUM\_INT> |
|  |  | **<REF1>** | |  | Concatenate ([VEHICLE-ID] ;”|”;[UNIQUE-VEHICLE-CD] | </REF1> |
|  |  | **<REF2>** | |  | £REF2 | </REF2> |
|  | </CRITERES> | | |  |  |  |
| </OBBISOFT> | | |  | |  |  |

## DEFINTION OF OBBISOFT.PIVOTS.ABONNE.PARAMx

|  |  |
| --- | --- |
| **Parameter** | **Value** |
| $PARAM1 | *list of departure point ( separate by a “|”) for which we have to create a specific £Codification* |
| $PARAM2 | *list of carrier ( separate by a “|”) for which we have to transport the vehicles example GEF|CEV|BRG* |
| $PARAM3 |  |
| $PARAM4 |  |

## Records Format

### HEADER : ALL Record Type (except LD01)

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length |
| SENDER | Sender Part name | A | 1 | 5 |
| RECEIVER | Receiver Part name | A | 6 | 5 |
| TIMESTAMP | When the messages has been sent YYYYMMDDHHMMSS | A | 11 | 14 |
| TRANSMISSION-WAY | Link between the supplier and Renault | A | 25 | 5 |
| BATCH-CODE | Batch identifier (not needed by Renault) | A | 30 | 5 |
| UNIQUE-VEHICLE-CD | Unique vehicle or consignment ID | A | 35 | 15 |
| FILLER |  | A | 50 | 51 |

### VA00 :Vehicle Identification

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the exchanged message | Char | 101 | 4 | VA00 |
| SENDER-CD | RNLT Code identifying the technical sender partner of the message | Char | 105 | 3 | REN |
| RECEIVER-CD | RNLT Code identifying the technical receiver partner of the message | Char | 108 | 3 | CA1, AT1,Etc… |
| VEHICLE-ID | VIN Number (Vehicle Identification Number) | Char | 111 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Constant indicating the fact the distribution is managed by Renault company | Char | 131 | 2 | RN |
| DESTINATION-NODE | RNLT Code of the final destination of the complete transport scheme (MADP position on the OL) | Char | 133 | 12 | P AU MEL, ZGDZ |
| LOGISTICS-DESTINATION-CD | Country ISO Standard code of the final destination of the complete transport scheme | Char | 145 | 6 | 033 |
| LOGISTICS-DESTINATION-DESC | RNLT Administrative identifier of the final consignee of the complete transport scheme (adressee argument) | Char | 151 | 30 | 366N17846 |
| JOURNEY-CD | Not used by RENAULT | Char | 181 | 4 | Blank |
| VESSEL-NAME | Not used by RENAULT | Char | 185 | 30 | Blank |
| LOGISTICS-PARTNER-CD | RNLT supplier Code carrying out the OT or the primary OP | Char | 215 | 3 | RS1 |
| LOGISTICS-PARTNER-NAME | Wording of the RNLT supplier code carrying out the OT or the primary OP | Char | 218 | 30 | AUTOTRANS |
| LOAD-NO | Not used by RENAULT | Char | 248 | 10 | Blank |
| ACTUAL-DEPARTURE-DATE | Pilot Date of departure from the plant (Pilot MADT into YYYYMMDD format) | Char | 258 | 8 | 20060725 |
| SCHEDULED-ARRIVAL-DATE | Arrival Pilot date to the final destination of the transport scheme (Pilot MADP into YYYYMMDD format) | Char | 266 | 8 | 20060920 |
| LOADING-NODE | Not used by RENAULT | Char | 274 | 12 | Blank |
| UNLOADING-NODE | Not used by RENAULT | Char | 286 | 12 | Blank |
| NET-WEIGHT | Net vehicle weight (in kg) | Char | 298 | 8 | 1670 |
| LENGTH | Not used by RENAULT | Char | 306 | 6 | Blank |
| WIDTH | Not used by RENAULT | Char | 312 | 6 | Blank |
| HEIGHT | Not used by RENAULT | Char | 318 | 6 | Blank |
| COLOR-CD | Not used by RENAULT | Char | 324 | 3 | Blank |
| COLOUR | RNLT Code identifying the vehicle"s COLOUR | Char | 327 | 30 | Orange |
| MODEL-GROUP | RNLT Code identifying the transport model the vehicle belongs to | Char | 357 | 4 | MT04 |
| MODEL-GROUP-DESC | RNLT language identifying the transport model the vehicle belongs to | Char | 361 | 30 | Gamme 1 (clio, twingo) |
| MODEL-SPEC | RNLT Code identifying the commercial model the vehicle belongs to | Char | 391 | 18 | H45, CL2 |
| MODEL-SPEC-DESC | RNLT Code identifying the commercial version the vehicle belongs to | Char | 409 | 35 | 5 LXD 15F E4 |
| TRANSMISSION-DATE | Date of the message transmission (into YYYYMMDD format) | Char | 444 | 8 | 20060723 |
| TRANSMISSION-TIME | Hour of the message transmission (into HHMMSS format) | Char | 452 | 6 | 115522 |
| WRAP-GUARD-CD | RNLT Code identifying the packaging type (protection) applied by the plant | Char | 458 | 1 | 4 |
| OLD-VEHICLE-CD | Previous value of the VIN number before its change (temporary VIN) | Char | 459 | 20 | VF1BBA01721322145 |
| BUILT-TO-ORDER-CD | Indicator of final customer allocation | Char | 479 | 1 | 0=>No , 1=>Yes |
| ORDER-CD | Not used by RENAULT | Char | 480 | 15 | Blank |
| DPTMO | RNLT Code identifying the manufacturing plant of the vehicle | Char | 495 | 3 | 101 |
| PRIORISATION | Indicating if the vehicle is priority | Char | 498 | 1 | 0 => non, 1 => oui |
| ARA-PRONOS | ARA-PRONOS Date YYYYMMDD | Char | 499 | 8 | 20060920 |
| DAD-DATE | DAD Date YYYYMMDD | Char | 507 | 8 | 20060920 |
| OWNER-DC | Owner DC | Char | 515 | 1 | 3 |
| OWNER-DCZ | Owner DCZ | Char | 516 | 2 | 34 |
| OWNER-ACCOUNT | Owner Account | Char | 518 | 6 | 000978 |
| MADT-DATE | The MADT date (Vehicle available for transportation) (FORMAT YYYYMMDD) | Char | 524 | 8 | 20090217 |
| COLOUR-CODE | The RNLT code of the COLOUR | Char | 532 | 6 | TEBV9 |
| ENGINE-SIZE | Blank | Char | 538 | 6 |  |
| FUEL-TYPE | The RNLT code indicating the fuel type | Char | 544 | 6 | DIESEL,ESSSPB,ELEC,GPL |
| ENGINE-NUMBER | The unique engine number | Char | 550 | 7 |  |
| GEARBOX-NUMBER | The unique gearbox number | Char | 557 | 7 |  |
| RADIO-CODE | The radio code | Char | 564 | 4 | 4362 |
| ENGINE-TYPE | Type of engine | Char | 568 | 6 | K9K |
| MAKE | Make of the vehicle | Char | 574 | 5 | APL12 |
| EXPECTED-CLIENT-DELIVERY-DATE | Expected client delivery date(YYYYMMDD) | Char | 579 | 8 | 20090220 |
| DR-TYPE | Type of DR | Char | 587 | 2 | 05 |
| TVV | Type Version Variant | Char | 589 | 18 | LH2A46 |
| LENGTH-MAXI | Vehicle length note received from COC | Char | 607 | 4 | 1950 |
| WIDTH-MAXI | Vehicle width note received from COC | Char | 611 | 4 | 1550 |
| HEIGHT-MAXI | Vehicle height note received from COC | Char | 615 | 4 | 1450 |
| TCM-DATE | Tombee de chaine mecanique Date | Char | 619 | 8 | 20090220 |
| INDICECONTREMARQUE | Countercheck Mark Index | Char | 627 | 1 | 3 |
| QUALITY-STATUS | Quality Status | Char | 628 | 2 | RB,RC,RD,VN |
| D\_LIV\_SOU | Delivery Due Date | Char | 630 | 8 |  |
| NUMCDE | Order Number | Char | 638 | 6 |  |
| NUM\_IMMAT | Numéro d’immatricuation | Char | 644 | 12 |  |
| FILLER | Blank | Char | 579 | 1922 | Blank |

### VA01 : Ordre for transit

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the message. | Char | 101 | 4 | VA01 |
| SENDER-CD | Code identifying the technical sender of the message. | Char | 105 | 3 | REN |
| RECEIVER-CD | Code identifying the technical receiver of the message. | Char | 108 | 3 | CA1 |
| VEHICLE-ID | VIN (Vehicle Identification Number) | Char | 111 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Always RN. Not used by receivers. | Char | 131 | 2 | RN |
| DESTINATION-NODE | Not used. | Char | 133 | 12 | Blank |
| LOGISTICS-DESTINATION-CD | Not used. | Char | 145 | 6 | Blank |
| LOGISTICS-DESTINATION-DESC | Not used. | Char | 151 | 30 | Blank |
| JOURNEY-CD | Not used. | Char | 181 | 4 | Blank |
| VESSEL-NAME | Not used. | Char | 185 | 30 | Blank |
| LOGISTICS-PARTNER-CD | Code of the supplier responsible for this transit request. | Char | 215 | 3 | CAT |
| LOGISTICS-PARTNER-NAME | Name of the supplier responsible for this transit request. | Char | 218 | 30 | CAT |
| LOAD-NO | Not used. | Char | 248 | 10 | Blank |
| ACTUAL-DEPARTURE-DATE | Commitment date for the end of transit. | Char | 258 | 8 | 20060925 |
| SCHEDULED-ARRIVAL-DATE | Commitment date for the start of transit. | Char | 266 | 8 | 20060924 |
| LOADING-NODE | Code identifying the compound. | Char | 274 | 12 | P ES BCN CA1 |
| UNLOADING-NODE | Code identifying the compound. | Char | 286 | 12 | P ES BCN CA1 |
| NET-WEIGHT | Not used. | Char | 298 | 8 | Blank |
| LENGTH | Not used. | Char | 306 | 6 | Blank |
| WIDTH | Not used. | Char | 312 | 6 | Blank |
| HEIGHT | Not used. | Char | 318 | 6 | Blank |
| COLOUR-CD | Not used. | Char | 324 | 3 | Blank |
| COLOUR | Not used. | Char | 327 | 30 | Blank |
| MODEL-GROUP | Not used. | Char | 357 | 4 | Blank |
| MODEL-GROUP-DESC | Not used. | Char | 361 | 30 | Blank |
| MODEL-SPEC | Not used. | Char | 391 | 18 | Blank |
| MODEL-SPEC-DESC | Not used. | Char | 409 | 35 | Blank |
| TRANSMISSION-DATE | Date of the message transmission. | Char | 444 | 8 | 20060723 |
| TRANSMISSION-TIME | Hour of the message transmission. | Char | 452 | 6 | 115522 |
| WRA-PGUARD-CD | Not used. | Char | 458 | 1 | Blank |
| OLD-VEHICLE-CD | Not used. | Char | 459 | 20 | Blank |
| BUILT-TO-ORDER-CD | Not used. | Char | 479 | 1 | Blank |
| ORDER-CD | Unique identifier of the transit request. | Char | 480 | 15 | 000000000011234 |
| DPTMO | Not used. | Char | 495 | 3 | Blank |
| HANDOVER-TYPE | Code indicating the position of the compound on the transport scheme : E = Next transport is planned. T = End of transport plan. W = Temporary end of transport plan. | Char | 498 | 1 | E, T or W |
| NEXT-LOGISTICS-PARTNER | Code of the supplier responsible for the next OT. | Char | 499 | 20 | FRI |
| RANK | Rank of the transit request in the transport plan. | Char | 519 | 2 | 01 |
| FILLER | Empty for future needs. | Char | 521 | 1980 | Blank |

### VA02 : Announce Vehicle on a SHIP

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the exchanged message | Char | 101 | 4 | VA02 |
| SENDER-CD | RNLT Code identifying the technical sender partner of the message | Char | 105 | 3 | REN |
| RECEIVER-CD | RNLT Code identifying the technical receiver partner of the message | Char | 108 | 3 | To be defined |
| VEHICLE-ID | VIN Number (Vehicle Identification Number) | Char | 111 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Constant indicating the fact the distribution is managed by Renault company | Char | 131 | 2 | RN |
| TRANSPORT-METHOD-CD | Code of the transport Mode | Char | 133 | 2 | =M for maritim =R for road =F for rail =B for flotation boat |
| TRANSPORT-MEAN-NAME | Name / Reference of the of the transport mean | Char | 135 | 30 |  |
| LOGISTICS-PARTNER-CD | RNLT supplier Code carrying out the OT or the primary OP | Char | 165 | 3 | RSM |
| LOAD-NO | Lot/Load number | Char | 168 | 13 | CAT4682451975 |
| ACTUAL-DATE-DATE | Actual MADo date of the OT | Char | 181 | 8 | 20080708 |
| ACTUAL-DATE-TIME | Actual MADo hour of the OT | Char | 189 | 6 | 142556 |
| SCHEDULED-ARRIVAL-DATE | Provisional date of arrival at UNLOADING-NODE | Char | 195 | 8 | 20080709 |
| LOADING-NODE | Code of the center of loading | Char | 203 | 12 |  |
| UNLOADING-NODE | Code of the center of unloading | Char | 215 | 12 |  |
| TRANSMISSION-DATE | Date of the message transmission | Char | 227 | 8 | 20080708 |
| TRANSMISSION-TIME | Hour of the message transmission | Char | 235 | 6 | 162506 |
| VEHICLE-CD | Not used by RENAULT for this message | Char | 241 | 15 | Blank |
| ORDER-CD | Digital identifier. Guarantees that the Order sent is unique | Char | 256 | 15 | Blank |
| USER-CD | Not used by RENAULT for this message | Char | 271 | 7 | Blank |
| RETURN-NODE | Not used by RENAULT for this message | Char | 278 | 12 | Blank |
| FILLER | Blank | Char | 290 | 2211 | Blank |

### TR01 : TRANSPORT Order

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the message. | Char | 101 | 4 | TR01 |
| SENDER-CD | Renaul code identifying the technical sender partner of the message | Char | 105 | 3 | REN |
| RECEIVER-CD | Renault code identifying the technical receiver partner of the message | Char | 108 | 3 | CA1 |
| VEHICLE-ID | VIN (Vehicle Identification Number) | Char | 111 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Renault code indicating that the distribution is managed by Renault. | Char | 131 | 2 | RN |
| LOGISTICS-PARTNER-CD | Renault code identifying the carrier | Char | 133 | 3 | CAT |
| REQUESTED-START-DATE | Transport should start before this date (Pilot MADo). | Char | 136 | 8 | 20060812 |
| REQUESTED-START-TIME | Not used by RENAULT | Char | 144 | 6 | Blank |
| REQUESTED-ARRIVAL-DATE | Transport should end before this date (Pilot MADd). | Char | 150 | 8 | 20060920 |
| START-NODE | Renault code identifying the departure compound | Char | 158 | 12 | P FR LEH ATT |
| START-NAME | Renault label identifying the departure compound | Char | 170 | 35 | LE HAVRE (PORT) FRA ATT |
| START-ZIP-CODE | Zip code of the departure compound | Char | 205 | 7 | 76600 |
| START-ADDRESS-LINE1 | Address of the departure compound (1st part) | Char | 212 | 35 | WALON c/o AUTOTRANS-Centre Roulier |
| START-ADDRESS-LINE2 | Address of the departure compound (2nd part) | Char | 247 | 35 | Port Sud, Quai Bougainville |
| START-CITY | City of the departure compound | Char | 282 | 25 | LE HAVRE |
| START-COUNTRY | Country of the departure compound | Char | 307 | 15 | FRANCE |
| DESTINATION-NODE | Renault code identifying the arrival compound | Char | 322 | 12 | P SI KOPECA1 |
| DESTINATION-NAME | Renault label identifying the arrival compound | Char | 334 | 35 | KOPER (PORT) |
| DESTINATION-ZIP-CODE | Zip code of the arrival compound | Char | 369 | 7 | 76600 |
| DESTINATION-ADDRESS-LINE1 | Address of the arrival compound (1st part) | Char | 376 | 35 | WALON c/o AUTOTRANS-Centre Roulier |
| DESTINATION-ADDRESS-LINE2 | Address of the arrival compound (2nd part) | Char | 411 | 35 | Port Sud, Quai Bougainville |
| DESTINATION-CITY | City of the arrival compound | Char | 446 | 25 | KOPER |
| DESTINATION-COUNTRY | Country of the arrival compound | Char | 471 | 15 | SLOVENIE |
| DEALER-ORDER-NO | Not used by RENAULT | Char | 486 | 10 | Blank |
| TRANSPORT-ZONE-NODE | Renault code identifying the geographical area | Char | 496 | 12 | ZG\_SL |
| ONWARD-DESTINATION-NODE | Not used by RENAULT | Char | 508 | 12 | Blank |
| ONWARD-DESTINATION-NAME | Not used by RENAULT | Char | 520 | 35 | Blank |
| ONWARD-DESTINATION-ZIP-CODE | Not used by RENAULT | Char | 555 | 7 | Blank |
| ONWARD-DESTINATION-ADDRESS-LINE1 | Not used by RENAULT | Char | 562 | 35 | Blank |
| ONWARD-DESTINATION-ADDRESS-LINE2 | Not used by RENAULT | Char | 597 | 35 | Blank |
| ONWARD-DESTINATION-CITY | Not used by RENAULT | Char | 632 | 25 | Blank |
| ONWARD-DESTINATION-COUNTRY | Not used by RENAULT | Char | 657 | 15 | Blank |
| ONWARD-DESTINATION-ZONE-NODE | Not used by RENAULT | Char | 672 | 12 | Blank |
| EDAT-REQUIRED | Not used by RENAULT | Char | 684 | 1 | Blank |
| DEALER-HOLIDAY-START-DATE1 | Not used by RENAULT | Char | 685 | 8 | Blank |
| DEALER-HOLIDAY-END-DATE1 | Not used by RENAULT | Char | 693 | 8 | Blank |
| DEALER-HOLIDAY-START-DATE2 | Not used by RENAULT | Char | 701 | 8 | Blank |
| DEALER-HOLIDAY-END-DATE2 | Not used by RENAULT | Char | 709 | 8 | Blank |
| NET-WEIGHT | Not used by RENAULT | Char | 717 | 8 | Blank |
| LENGTH | Not used by RENAULT | Char | 725 | 6 | Blank |
| WIDTH | Not used by RENAULT | Char | 731 | 6 | Blank |
| HEIGHT | Not used by RENAULT | Char | 737 | 6 | Blank |
| COLOUR-CD | Not used by RENAULT | Char | 743 | 3 | Blank |
| COLOUR | Not used by RENAULT | Char | 746 | 30 | Blank |
| MODEL-GROUP | Not used by RENAULT | Char | 776 | 4 | Blank |
| MODEL-GROUP-DESC | Not used by RENAULT | Char | 780 | 30 | Blank |
| MODEL-SPEC | Not used by RENAULT | Char | 810 | 18 | Blank |
| MODEL-SPEC-DESC | Not used by RENAULT | Char | 828 | 35 | Blank |
| PARKING-POSITION | Not used by RENAULT | Char | 863 | 9 | Blank |
| TRANSMISSION-DATE | Date of the message transmission. | Char | 872 | 8 | 20060723 |
| TRANSMISSION-TIME | Hour of the message transmission. | Char | 880 | 6 | 115522 |
| PLACEMENT-DEALER-NODE | Renault code identifying the account where the vehicle distribution ends (Adressee argument) | Char | 886 | 12 | 922N11111 |
| PLACEMENT-DEALER-NAME | Name of the dealership where the vehicle distribution ends. | Char | 898 | 35 | MARTINIQUE |
| PLACEMENT-DEALER-ZIP-CODE | Zip code of the dealership where the vehicle distribution ends. | Char | 933 | 7 | 97825 |
| PLACEMENT-DEALER-ADDRESS-LINE1 | Address of the dealership where the vehicle distribution ends (1st part) | Char | 940 | 35 | RTE NATIONALE LE CHA |
| PLACEMENT-DEALER-ADDRESS-LINE2 | Address of the dealership where the vehicle distribution ends (2nd part) | Char | 975 | 35 | BP 6 |
| PLACEMENT-DEALER-CITY | City of the dealership where the vehicle distribution ends | Char | 1010 | 25 | LAMENTIN |
| PLACEMENT-DEALER-COUNTRY | Country of the dealership where the vehicle distribution ends | Char | 1035 | 15 | MARTINIQUE |
| PAYMENT-METHOD | Not used by RENAULT | Char | 1050 | 2 | Blank |
| PAYMENT-METHOD-DESCRIPTION | Not used by RENAULT | Char | 1052 | 30 | Blank |
| DUTY-FREE-INDICATOR | Not used by RENAULT | Char | 1082 | 1 | Blank |
| DEALER-LANGUAGE-CODE | Not used by RENAULT | Char | 1083 | 3 | Blank |
| TRANSPORTATION-CD | Renault code identifying the transport mode. | Char | 1086 | 1 | R |
| ORDER-CD | Technical identifier of this transport request | Char | 1087 | 15 | 000000000011211 |
| AVAILABILITY-TYPE | Indicates if the vehicle is available for transport activities. | Char | 1102 | 1 | A or U or blank |
| RANK | Rank of the transport request in the transport scheme. | Char | 1103 | 2 | "01" |
| FILLER | May be used for future needs. | Char | 1105 | 1396 | Blank |

### RD01 : CANCEL Order transit/Lock/Service

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the exchanged message | Char | 101 | 4 | RD01 |
| SENDER-CD | RNLT Code identifying the technical sender partner of the message | Char | 105 | 3 | REN |
| RECEIVER-CD | RNLT Code identifying the technical receiver partner of the message | Char | 108 | 3 | To be defined |
| VEHICLE-ID | VIN Number(Vehicle Identification Number) | Char | 111 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Constant indicating the fact the distribution is managed by Renault company | Char | 131 | 2 | RN |
| LOGISTICS-PARTNER-CD | RNLT supplier Code carrying out the OT or the primary OP | Char | 133 | 3 | RS1 |
| LOGISTICS-PARTNER-NAME | Wording of the RNLT supplier code carrying out the OT or the primary OP | Char | 136 | 30 | AUTOTRANS |
| LOAD-NO | Not used by RENAULT | Char | 166 | 10 | Blank |
| TRANSMISSION-DATE | Date of the message transmission (into YYYYMMDD format) | Char | 176 | 8 | 20060723 |
| TRANSMISSION-TIME | Hour of the message transmission (into HHMMSS format) | Char | 184 | 6 | 115522 |
| ORDER-CD | digital identifier (guarantees the order sent is unique) | Char | 190 | 15 | "000000000011234" |
| NODE | RNLT center code where the OP is carried out | Char | 205 | 12 | "P AU MEL", "ZG DZ" |
| FILLER | Blank | Char | 217 | 1982 | Blank |

### VE01 : Service Ordre

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the exchanged message | Char | 101 | 4 | VE01 |
| SENDER-CD | RNLT Code identifying the technical sender partner of the message | Char | 105 | 3 | REN |
| RECEIVER-CD | RNLT Code identifying the technical receiver partner of the message | Char | 108 | 3 | To be defined |
| VEHICLE-ID | VIN Number(Vehicle Identification Number) | Char | 111 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Constant indicating the fact the distribution is managed by Renault company | Char | 131 | 2 | RN |
| LOGISTICS-PARTNER-CD | RNLT supplier Code carrying out the OT or the primary OP | Char | 133 | 3 | GEO |
| NODE | RNLT center code where the OP is carried out | Char | 136 | 12 | P UA ILL |
| VEHICLE-ENHANCEMENT | RNLT Code of the technical (ex : washing) or administrative (custom clearance) service"s type of the OP (LA01 DP) | Char | 148 | 5 | LAV |
| VEHICLE-ENHANCEMENT-DESCRIPTION | Wording of the RNLT Code of the technical or administrative service"s type of the OP | Char | 153 | 30 | Washing |
| OPERATION-1 | Not used by RENAULT | Char | 183 | 3 | Blank |
| OPERATION-DESCRIPTION-1 | Not used by RENAULT | Char | 186 | 30 | Blank |
| BLANK | Not used by RENAULT | Char | 216 | 594 | Blank |
| OPERATION-20 | Not used by RENAULT | Char | 810 | 3 | Blank |
| OPERATION-DESCRIPTION-20 | Not used by RENAULT | Char | 813 | 30 | Blank |
| PART-1 | Not used by RENAULT | Char | 843 | 15 | Blank |
| PART-DESCRIPTION-1 | Not used by RENAULT | Char | 858 | 30 | Blank |
| PART-QUANTITY-1 | Not used by RENAULT | Char | 888 | 7 | Blank |
| PART-UNIT-OF-MEASURE-1 | Not used by RENAULT | Char | 895 | 3 | Blank |
| BLANK2 | Not used by RENAULT | Char | 898 | 1008 | Blank |
| PART-20 | Not used by RENAULT | Char | 1906 | 15 | Blank |
| PART-DESCRIPTION-20 | Not used by RENAULT | Char | 1921 | 30 | Blank |
| PART-QUANTITY-20 | Not used by RENAULT | Char | 1951 | 7 | Blank |
| PART-UNIT-OF-MEASURE-20 | Not used by RENAULT | Char | 1958 | 3 | Blank |
| SCHEDULED-VE-COMPLETION-DATE | Commitment date for the end of the service | Char | 1961 | 8 | 20061106 |
| TRANSMISSION-DATE | Date of the message transmission (into YYYYMMDD format) | Char | 1969 | 8 | 20060723 |
| TRANSMISSION-TIME | Hour of the message transmission (into HHMMSS format) | Char | 1977 | 6 | 115522 |
| SCHEDULED-ARRIVAL-DATE | Commitment date for the beginning of the service | Char | 1983 | 8 | 20061101 |
| ORDER-CD | digital identifier (guarantees the order sent is unique) | Char | 1991 | 15 | 000000000011211 |
| PRIMARY-RANK | Primary rank of the service order | Char | 2006 | 2 | "01" |
| SECONDARY-RANK | Secondary rank of the service order | Char | 2008 | 2 | "01" |
| SERVICE-INFO | Complementary information related to service | Char | 2010 | 5 | T225S  For MLD service : Ex G270S  Char 1 = LTSM type code  Char 2 to 4 = LTSM period of interval (045, 090, 270, 225 …)  Char 5 = LTSM invoicing code = A ou S  Si A facturation de l'Alliance  Si S facturation de la filiale commerciale (Subsidiary)  Remarque Renault :  Recevoir un A sera une anomalie, donc à facturer comme si c’était un S |
| FILLER | blank | Char | 2015 | 486 | Blank |

### TD01 : Cancel Transport Order

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the exchanged message | Char | 101 | 4 | TD01 |
| SENDER-CD | RNLT Code identifying the technical sender partner of the message | Char | 105 | 3 | REN |
| RECEIVER-CD | RNLT Code identifying the technical receiver partner of the message | Char | 108 | 3 | To be defined |
| VEHICLE-ID | VIN Number(Vehicle Identification Number) | Char | 111 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Constant indicating the fact the distribution is managed by Renault company | Char | 131 | 2 | RN |
| LOGISTICS-PARTNER-CD | RNLT supplier Code carrying out the OT or the primary OP | Char | 133 | 3 | RS1 |
| SCHEDULED-DESTINATION-ARRIVAL-DATE | Commitment date for the end of the transport (=MADd into YYYYMMDD format) | Char | 136 | 8 | 20061001 |
| DESTINATION-NODE | RNLT code of the arrival center of the OT | Char | 144 | 12 | P SI KOPECA1 |
| DESTINATION-NAME | RNLT code"s wording of the arrival center of the OT | Char | 156 | 35 | KOPER (PORT) |
| DESTINATION-ZIP-CODE | RNLT Zip Code of the arrival center of the OT | Char | 191 | 7 | 76600 |
| DESTINATION-ADDRESS-LINE1 | RNLT Address of the arrival center of the OT (1st part) | Char | 198 | 35 | WALON c/o AUTOTRANS-Centre Roulier |
| DESTINATION-ADDRESS-LINE2 | RNLT Address of the arrival center of the OT (2nd part) | Char | 233 | 35 | Port Sud, Quai Bougainville |
| DESTINATION-CITY | RNLT City of the arrival center of the OT | Char | 268 | 25 | KOPER |
| DESTINATION-COUNTRY | RNLT Country of the arrival center of the OT | Char | 293 | 15 | SLOVENIE |
| DEALER-ORDER-NO | Not used by RENAULT | Char | 308 | 10 | Blank |
| START-NODE | Code of the distribution center for the beginning of the transport order cancelled | Char | 318 | 12 | P SI KO CA1 |
| DESTINATION-ZONE-NODE | RNLT code of the geographical area if OT to GA | Char | 330 | 12 | ZG\_UK |
| TRANSMISSION-DATE | Date of the message transmission (into YYYYMMDD format) | Char | 342 | 8 | 20060723 |
| TRANSMISSION-TIME | Hour of the message transmission (into HHMMSS format) | Char | 350 | 6 | 115522 |
| ORDER-CD | digital identifier (guarantees the order sent is unique) | Char | 356 | 15 | 000000000011211 |
| FILLER | Blank | Char | 371 | 2130 | Blank |

### HR01 : LOCK/UNLOCK Order

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Field name | Description | Format | Start | Length | Example |
| INTERFACE-ID | Code identifying the exchanged message | Char | 101 | 4 | HR01 |
| SENDER-CD | RNLT Code identifying the technical sender partner of the message | Char | 105 | 3 | REN |
| RECEIVER-CD | RNLT Code identifying the technical receiver partner of the message | Char | 108 | 3 | To be defined |
| ACTION | ACTION code of the hold message | Char | 111 | 1 | A: add the demand M : modify the demand R: release the demand |
| VEHICLE-ID | VIN Number(Vehicle Identification Number) | Char | 112 | 20 | VF1BBA01721345676 |
| BUSINESS-TYPE | Constant indicating the fact the distribution is managed by Renault company | Char | 132 | 2 | RN |
| HOLD-CD | RNLT Code identifying the holding type of the OP LA01 DP | Char | 134 | 4 | BLQ (Quality), BLC (Commercial),  BLF (financial), BLL (Logistic), BLR (Reform Holding), PAR (storage), RPF (freeze Financial), RAQ (Freeze Quality), MUT (MUTualization) |
| HOLD-DESCRIPTION | Wording of the RNLT Code identifying the holding type of the OP | Char | 138 | 30 | wiring broken |
| HOLD-START-DATE | Commitment Date for the beginning of the service | Char | 168 | 8 | 20060902 |
| ESTIMATED-RELEASE-DATE | Forecasted Date estimate by RNLT of the end of a hold service | Char | 176 | 8 |  |
| ACTUAL-RELEASE-DATE | End of hold service date asked by RNLT (if ACTION = R) | Char | 184 | 8 | 20060910 or blank |
| TRANSMISSION-DATE | Date of the message transmission (into YYYYMMDD format) | Char | 192 | 8 | 20060723 |
| TRANSMISSION-TIME | Hour of the message transmission (into HHMMSS format) | Char | 200 | 6 | 115522 |
| HOLD-NUMBER | RNLT number of the holding related to the OP | Char | 206 | 6 | SBF036 |
| HOLD-NODE-CD | RNLT center code where the OP is carried out. | Char | 212 | 12 | "P AU MEL" |
| LOGISTICS-PARTNER-CD | RNLT supplier Code carrying out the OT or the primary OP | Char | 224 | 3 | RS1 |
| ORDER-CD | digital identifier (guarantees the order sent is unique) | Char | 227 | 15 | 000000020092006 |
| PRIMARY-RANK | Primary rank of the service order | Char | 242 | 2 | "01" |
| SECONDARY-RANK | Secondary rank of the service order | Char | 244 | 2 | "01" |
| FILLER | Blank | Char | 246 | 2255 | Blank |

### LD01 : LOAD/UNLOAD Order

ATTENTION : LD01 est le seul mouvement sans entête technique

ACHTUNG : LD01 ist das einzige Werk ohne technische Überschrift

TAKE CARE : LD01 is the only movement without a technical header

ध्यान : LD01 तकनीकी हेडर के बिना एकमात्र आंदोलन है

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| **Field Name** | **Description** | Format | Start | length |
| INTERFACE-ID | Interface ID | A-4 | 1 | 4 |
| SENDER-CD | STEFI code that identifies the Logistics Partner sending the transmission | A-3 | 5 | 3 |
| RECEIVER-CD | Transmission receiver – in this case STEFI | A-3 | 8 | 3 |
| VEHICLE-ID | Unique ID of the vehicle | A-20 | 11 | 20 |
| BUSINESS-TYPE | Business Type | A-2 | 31 | 2 |
| LOAD-NO | Unique reference number of the Load (excluding Logistics Partner code) | A-10 | 33 | 10 |
| START-NODE | Node from which the vehicle will be transported | A-12 | 43 | 12 |
| DESTINATION-NODE | Node to which the vehicle will be transported | A-12 | 55 | 12 |
| ESTIMATED-COLLECTION-DATE | Estimated Load Collection Date (YYYYMMDD) from Start Node | A-8 | 67 | 8 |
| ESTIMATED-COLLECTION-TIME | Estimated Load Collection Time (HHMMSS) from Start Node | A-6 | 75 | 6 |
| ESTIMATED-DEALER-ARRIVAL-DATE | Estimated Arrival Date of vehicle (YYYYMMDD) at Dealer (Required for dealer delivery | A-8 | 81 | 8 |
| ESTIMATED-DEALER-ARRIVAL-TIME | Estimated Arrival Time of vehicle (HHMMSS) at Dealer Required for dealer delivery | A-6 | 89 | 6 |
| TRANSMISSION-DATE | Transmission Date (YYYYMMDD) | A-8 | 95 | 8 |
| TRANSMISSION-TIME | Transmission Time (HHMMSS) | A-6 | 103 | 6 |
| CARRIER-COMPANY | Name of the company physically transporting the vehicle | A-30 | 109 | 30 |
| TRUCK-REG-NO | Registration No. of the truck transporting the vehicle | A-12 | 139 | 12 |
| TRAILER-REG-NO | Registration No. of the trailer transporting the vehicle | A-12 | 151 | 12 |
| CARNET-TIR-NO | Carnet TIR No. | A-15 | 163 | 15 |
| DRIVER-NAME | Name of truck driver | A-30 | 178 | 30 |
| LICENSE-PLATE-NO | License Plate No. of the truck transporting the vehicle | A-10 | 208 | 10 |
| Quantity-of-units |  | A-4 | 218 | 4 |
| Sequence number |  | A-4 | 222 | 4 |
| VAT Number |  | A-12 | 226 | 12 |
| FILLER | Filler | A-5 | 238 | 5 |

## OUTBOUND STRUCTURE

### Preliminary Information

The following variables are mentioned in the Outbound Structure chapter.

This table shows in which flows they are used.

|  |  |
| --- | --- |
| **Variable name** | **Value** |
| **£Filename** | OBBISOFT.MESSAGE.STANDARD\_MESSAGE.FILENAME |
| **£OrderDate** | ~~OBBISOFT.MESSAGESTANDARD\_MESSAGE.DATEVEN (Input format YYYY-MM-DDTHH:MI:SS , Output~~  sysdate format YYYY-MM-DDTHH:MI:SS ) |
| **£VIN** | £VIN = Left([VEHICLE\_ID];17) it is the string from 111 characters for all messages except LD01. For LD01 the position of the field is “11” |

*£PARAM1 is a list of departure point ( separate by a “|”) for which VA01 make the eXIT of the vehicle*

**£PARAM1**=OBBISOFT.PIVOTS.ABONNE.PARAM1

*£PARAM2 is a list of carrier ( separate by a “|”) in the VA01 where we are responsible for the next transport*

**£PARAM2=** OBBISOFT.PIVOTS.ABONNE.PARAM2

|  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | [INTERFACE-ID]= "VA00" | [INTERFACE-ID]= "VA01" | [INTERFACE-ID]= "VA02" | [INTERFACE-ID]= "TR01" | [INTERFACE-ID]= "TD01" | [INTERFACE-ID]= "VE01" | [INTERFACE-ID]= "RD01" | [INTERFACE-ID]= "HR01" |
| FILE\_NO | VA00 | VA01 | VA02 | TR01 | TD01 | VE01 | RD01 | HR01 |
| **£DEP\_POINT\_ID** | “” | LOADING-NODE | LOADING-NODE | START-NODE] | START-NODE] | NODE | NODE | HOLD-NODE-CD |
| £LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD |
| £SEQ | “” | 20 | 20 | 20 | 10 | 20 | 10 | 20 |
| **£INT\_DEP\_POINT\_ID** | “” | “” | “” | “” | “” | “” | “” | “” |
| **£Sender** |  | LOADING-NODE | LOADING-NODE | [START-NODE] |  |  |  |  |
| **£Sender\_Roma** |  | Concatenate ("EXP." ; £DEP\_POINT\_ID ) | Concatenate ("EXP." ; £DEP\_POINT\_ID ) | Concatenate ("EXP." ; £DEP\_POINT\_ID ) |  |  |  |  |
| **£ARR\_POINT\_ID** | LOGISTICS-DESTINATION-CD | UNLOADING-NODE | UNLOADING-NODE | DESTINATION-NODE | DESTINATION-NODE | “” | “” | “” |
| **£ARR\_POINT\_ID\_CTRY** | LOGISTICS-DESTINATION-DESC |  |  |  |  |  |  |  |
| **£INT\_ARR\_POINT\_ID** | “” | “” | “” | “” | “” | “” | “” | “” |
| **£Delivery** |  | If HANDOVER-TYPE = « E »  Then concatenate (LOADING-NODE; “\_E”)  Else LOADING-NODE |  | IF TRANSPORT-ZONE-NODE is filled  If the two first digit = “ZG”  then PLACEMENT-DEALER-NODE  else “TRANSPORT-ZONE-NODE”  else DESTINATION-NODE |  |  |  |  |
| **£Consignee** | ~~LOGISTICS-DESTINATION-DESC~~  Conccatenate(OWNER-DC, OWNER-DCZ, OWNER-ACCOUNT) |  |  |  |  |  | “” |  |
| **£Delivery\_Roma** |  | concatener( "STO."; LOADING-NODE) |  | IF TRANSPORT-ZONE-NODE is filled  then PLACEMENT-DEALER-NODE  else concatenate("STO." ; DESTINATION-NODE) |  |  |  |  |
| **£Consignee\_Roma** |  |  |  | ~~)~~ |  |  |  |  |
| **£ORDER** | Concatenate (“VA00\_”, Header.[UNIQUE-VEHICLE-CD]) | ORDER-CD | ORDER-CD | ORDER-CD | ORDER-CD | ORDER-CD | ORDER-CD | ORDER-CD |
| **£MVT\_NO** | INTERFACE-ID | INTERFACE-ID | INTERFACE-ID] | INTERFACE-ID | INTERFACE-ID | INTERFACE-ID | INTERFACE-ID | Concatenate ( “HR01”; ACTION ) |
| **£Pickup\_Start** | If ACTUAL-DEPARTURE-DATE]avail else SystemDate | If ACTUAL-DEPARTURE-DATE]avail else SystemDate | If SCHEDULED-ARRIVAL-DATE avail else SystemDate | SystemDate |  |  |  |  |
| **£DelivDate** | SCHEDULED-ARRIVAL-DATE if avail else null | SCHEDULED-ARRIVAL-DATE if avail else null |  | REQUESTED-ARRIVAL-DATE if avail else null |  |  |  |  |
| **Divers** | “” |  | “” | **£Carrier=** TR01.LOGISTICS-PARTNER-CD | **“”** | **£Srv**= VEHICLE-ENHANCEMENT |  | **£Lock =** HR01.HOLD-CD+ HR01.ACTION |
| **£Old\_Vin** | [OLD\_VEHICLE\_CD] take only the first 17 characters if filleld  Else “”it is the string from 459 characters |  |  |  |  |  |  |  |
| **£Colour** | COLOUR suppress the blank and take only the 17 first characters |  |  |  |  |  |  |  |
| **£factory** | DPTMO |  |  |  |  |  |  |  |
| **£Lock\_level** |  |  |  | If AVAILABILITY-TYPE NOT null then "TR01" |  |  |  | HOLD-CD |
| **£Lock\_oper** |  |  |  | AVAILABILITY-TYPE] = "U"  £Lock\_oper = "Lock"  AVAILABILITY-TYPE] = "A"  £Lock\_oper = "UNlock" else null |  |  |  |  |
| **£Lock\_Order** |  |  |  |  |  |  |  | HOLD-NUMBER |
| **£Lock\_site** |  |  |  | you |  |  |  | HOLD-NODE-CD |
| £Model\_Ext | £Model\_Ext = concatener (SUPPRESPACE(VA00.MODEL\_GROUP) ; SUPPRESPACE(VA00.MODEL\_SPEC)) |  |  |  |  |  |  |  |
| £Length | VA00.LENGTH if available |  |  |  |  |  |  |  |
| £Height | VA00.HEIGHT if available |  |  |  |  |  |  |  |
| $ProductionDate | MADT-DATE | “” | “” | “” | “” | “” | “” | “” |
| £CheckOrdered | If BUILT-TO-ORDER-CD= 1  then TRUE else FALSE |  |  |  |  |  |  |  |
| £Country | LOGISTICS-DESTINATION-CD | “” |  |  |  |  |  |  |
| £PriorityLevel | PRIORISATION |  |  |  |  |  |  |  |
| **£Delivery\_Zone** |  |  |  | [TRANSPORT-ZONE-NODE] if filled else “DELETED” |  |  |  |  |
| **£CustomerOfferXCode** |  | If NEXT-LOGISTICS-PARTNER is not in the list **£PARAM2** then « RENAULT\_EP » |  | Concatenate (« RENAULT\_ » ; [TRANSPORTATION-CD) |  |  |  |  |
| **£Codification** |  |  |  | **If £DEP\_POINT\_ID** is in the list of £PARAM1 and (TR01. DESTINATION-COUNTRY = “ITALIE” or the six first digit of TR01. TRANSPORT-ZONE-NODE = “ZG\_ITA” ) then « PCOD RESRENAULT1 » else « PCOD RESRENAULT » |  |  |  |  |
| £Kind | £Kind= « VO » if VA00.BUSINESS-TYPE =”VO” else £Kind = « VN » |  |  | £Kind= « VO » if TR01.BUSINESS-TYPE =”VO” else £Kind = « VN » |  |  |  |  |
| £Issuer | £Issuer= DO.RENAULTVO if VA00.BUSINESS-TYPE =”VO” else "DO.RENAULT" |  |  | £Issuer= DO.RENAULTVO if TR01.BUSINESS-TYPE =”VO” else "DO.RENAULT" |  |  |  |  |
| £CheckPickupSite | £CheckPickupSite= “False” if VA00.BUSINESS-TYPE =”VO” else “TRUE” |  |  | £CheckPickupSite= “False” if TR01.BUSINESS-TYPE =”VO” else “TRUE” |  |  |  |  |
| **£Product** | **£Product=”**VORENAULT » if VA00.BUSINESS-TYPE =”VO” else « DEFAUT » |  |  | **£Product=”**VORENAULT » if TR01.BUSINESS-TYPE =”VO” else « DEFAUT » |  |  |  |  |
| **£ProductDeterminationMode** | **£ProductDeterminationMode=**blank if VA00.BUSINESS-TYPE =”VO” else “CRITERIA” |  |  | **£ProductDeterminationMode=**blank if TR01.BUSINESS-TYPE =”VO” else “CRITERIA” |  |  |  |  |
| £Principal | £Principal= DO.RENAULTVO if VA00.BUSINESS-TYPE =”VO” else "DO.RENAULT" |  |  | £Principal= DO.RENAULTVO if TR01.BUSINESS-TYPE =”VO” else "DO.RENAULT" |  |  |  |  |
| £REGISTRATION | NUM\_IMMAT |  |  |  |  |  |  |  |
| £FUEL-TYPE | FUEL-TYPE |  |  |  |  |  |  |  |
| £DeliveryKind |  | If NEXT-LOGISTICS-PARTNER is not in the list **£PARAM2** then ~~‘ON\_SITE’~~ blank  else ‘DELIVERY’ |  |  |  |  |  |  |
| £EXTERNAL\_CARRIER |  | If NEXT-LOGISTICS-PARTNER is not in the list **£PARAM2** then NEXT-LOGISTICS-PARTNER |  |  |  |  |  |  |
| £DeliveryCustomer | Concatenate(OWNER-DC; OWNER-DCZ; OWNER-ACCOUNT) if available |  |  |  |  |  |  |  |

|  |  |
| --- | --- |
| £Token1 | Concatenate (**£DEP\_POINT\_ID, ‘-‘ ; £ARR\_POINT\_D) ,** |
| £Token2 | **£VIN** |
| £Token3 | =[SENDER-CD] “ |” [INTERFACE-ID] “|” [ORDER-CD ] “|” [HEADER. TIMESTAMP ( off the message treat) |

### treatment

|  |  |
| --- | --- |
| Movement | mapping |
| TR01 | If TR01.BUSINESS-TYPE =”VO” then  If TR01.[AVAILABILITY-TYPE] =”A”  £MVT\_NO=TR01\_A\_VO  make an INCOMMING\_ORDER Announce  else  £MVT\_NO=TR01\_U\_VO  make an INCOMMING\_ORDER VEH\_UPDATE  else  If TR01.[AVAILABILITY-TYPE] =”A”  **£CheckPickupUnavailable = “FALSE” and** £FlagTR01 = RECEPT  else  **£CheckPickupUnavailable = “TRUE” and** £FlagTR01 = UNRECEP  make an INCOMMING\_ORDER Announce  if **£Codification =** PCOD RESRENAULT1  make an INCOMING EVENT  **Then**  **If** TR01.[AVAILABILITY-TYPE] =”A” and **£Codification =** PCOD RESRENAULT1  £FlagTR01 = PICKUP\_AVAILABLE  make an INCOMING EVENT |
| VA01 | make an INCOMMING\_ORDER ANNOUNCE |
| RD01 | make an INCOMMING\_ORDER CANCELLATION |
| TD01 | make an INCOMMING\_ORDER CANCELLATION |
| HR01 | If HR01.[ ACTION ] = “R”  make an INCOMMING\_ORDER UNLOCK  else  make an INCOMMING\_ORDER LOCK |
| VE01 | make an INCOMMING\_ORDER SERVICES |
| VA02 | make an INCOMMING\_ORDER VEH\_UPDATE |
| VA00 | If £Old\_Vin is filled then  £PreviousVin= £Old\_Vin and £NewVin = blank  make an INCOMMING\_ORDER Announce  £PreviousVin= £Old\_Vin and £NewVin = £VIN  make an INCOMMING\_ORDER Announce  make an INCOMMING\_ORDER VEH\_UPDATE  else  £PreviousVin= £VIN and £NewVin = blank  make an INCOMMING\_ORDER Announce  make an INCOMMING\_ORDER VEH\_UPDATE |
| LD01 | Make an INCOMMING\_LOAD |

### Outbound Structure Details

Output Flow: **O.MOVEECAR\_GEFCO2MOVEECAR**

Format (XML, fixe format, variable format, others ) : **XML**

Tag are created only if the data to put into the value is filled.

Parent tags are created only if a child tag is filled at least

* **Note : Date & Time fields formats in the output structure**

**"REAL\_DATETIME": YYYY-MM-DDTHH:MI:SS**

**"PLANNED\_DATE": YYYY-MM-DD**

**"PLANNED\_TIME": DDTHH:MI:SS**

#### INCOMMING\_ORDER Mapping

**Make the output message below**

| **Node Level** | | | | |  |  | | **VALUE** |  | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **1** | **2** | **3** | **4** | **5** | **ANNOUNCE** | | **CANCELLATION** | | | **LOCK** | **UNLOCK** | **SERVICE** | **UPDATE\_VEH** | |
| Order/ | | | | |  | |  | | |  |  |  |  | |
|  | OrderXno | | | | £ORDER | | £ORDER | | | £ORDER | £ORDER | £ORDER | £ORDER | |
|  | OrderDate | | | | £OrderDate | | £OrderDate | | | £OrderDate | £OrderDate | £OrderDate | £OrderDate | |
|  | Issuer/ | | | |  | |  | | |  |  |  |  | |
|  |  | Code | | |  | |  | | |  |  |  |  | |
|  |  | Codification | | | PCOD RESRENAULT | | PCOD RESRENAULT | | | PCOD RESRENAULT | PCOD RESRENAULT | PCOD RESRENAULT | PCOD RESRENAULT | |
|  |  | XCode | | | ~~"DO.RENAULT"~~ £Issuer if filled else "DO.RENAULT" | | "DO.RENAULT" | | | "DO.RENAULT" | "DO.RENAULT" | "DO.RENAULT" | "DO.RENAULT" | |
|  | Receiver/ | | | |  | |  | | |  |  |  |  | |
|  |  | Codification | | | GEFCO | | GEFCO | | | GEFCO | GEFCO | GEFCO | GEFCO | |
|  |  | XCode | | | LOGISTICS-PARTNER-CD | | LOGISTICS-PARTNER-CD | | | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | LOGISTICS-PARTNER-CD | If If £MVT\_NO ="VA02" then “GEF”  Else LOGISTICS-PARTNER-CD | |
|  | SpecialRules | | | |  | |  | | |  |  |  |  | |
|  |  | ReceiverDeterminationMode | | | CONTRACT | |  | | | CONTRACT | CONTRACT | CONTRACT | CONTRACT | |
|  | OriginSoftware | | | | STEFI | | STEFI | | | STEFI | STEFI | STEFI | STEFI | |
|  | OrderLine/ | | | |  | |  | | |  |  |  |  | |
|  |  | RecordNo | | |  | |  | | |  |  |  |  | |
|  |  | MsgSynchroMode | | | NO\_ONE | | NO\_ONE | | |  |  |  |  | |
|  |  | MsgSynchroNumber | | |  | |  | | |  |  |  |  | |
|  |  | Kind | | | ANNOUNCE | | CANCELLATION | | | LOCKING | UNLOCKING | SERVICE | UPDATE\_VEH | |
|  |  | MvtType | | | £MVT\_NO | | £MVT\_NO | | | £MVT\_NO | £MVT\_NO | £MVT\_NO | If £Old\_Vin not null,  Concatenate(£MVT\_NO ; «\_New\_VIN »)  Else £MVT\_NO | |
|  |  | Mvtno | | | £ORDER | | £ORDER | | | £ORDER | £ORDER | £ORDER | £ORDER | |
|  |  | AnnounceSpecialRules | | |  | |  | | |  |  |  |  | |
|  |  |  | CheckAllocation | | True | |  | | |  |  |  |  | |
|  |  |  | VehModelDeterminationMode | | RENAULT | |  | | |  |  |  | RENAULT | |
|  |  |  | CheckPreannounce | | If £MVT\_NO ="VA00"  then TRUE else FALSE | |  | | |  |  |  |  | |
|  |  |  | CheckPickupSite | | £CheckPickupSite if filled else TRUE | |  | | |  |  |  |  | |
|  |  |  | **PrincipalDeterminationMode** | | “CRITERIA” | |  | | |  |  |  |  | |
|  |  |  | **ProductDeterminationMode** | | **£ProductDeterminationMode** if filled else“CRITERIA” | |  | | |  |  |  |  | |
|  |  | AllocationSpecialRules | | |  | |  | | |  |  |  |  | |
|  |  |  | CheckCallOff | | FALSE | |  | | |  |  |  |  | |
|  |  |  | CheckChangeAddressOnly | | False | |  | | |  |  |  |  | |
|  |  |  | CheckLastAllocationSite | | True | |  | | |  |  |  |  | |
|  |  |  | CheckIfExistsUpdateOperation | | True | |  | | |  |  |  |  | |
|  |  | CancellationSpecialRules | | |  | |  | | |  |  |  |  | |
|  |  |  | CheckCancelAllocationOnly | |  | | TRUE | | |  |  |  |  | |
|  |  |  | IfAlreadyInProcess | |  | | PREVIOUS\_STOCK | | |  |  |  |  | |
|  |  |  | **CheckFindMvtNoToCancel** | |  | | TRUE | | |  |  |  |  | |
|  |  | VehIdentification | | |  | |  | | |  |  |  |  | |
|  |  |  | Vin | | £PreviousVin if filled else £VIN | | £VIN | | | £VIN | £VIN | £VIN |  | |
|  |  |  | ~~Plateno~~ PlateNo | | £REGISTRATION | |  | | |  |  |  | £REGISTRATION | |
|  |  |  | OF | |  | |  | | |  |  |  |  | |
|  |  |  | CAF | | UNIQUE-VEHICLE-CD if avail | | UNIQUE-VEHICLE-CD if avail | | | UNIQUE-VEHICLE-CD if avail | UNIQUE-VEHICLE-CD if avail | UNIQUE-VEHICLE-CD if avail | UNIQUE-VEHICLE-CD if avail | |
|  |  |  | CustomerIdentification | | UNIQUE-VEHICLE-CD] if avail | | UNIQUE-VEHICLE-CD if avail | | | UNIQUE-VEHICLE-CD if avail | UNIQUE-VEHICLE-CD if avail | UNIQUE-VEHICLE-CD if avail | UNIQUE-VEHICLE-CD if avail | |
|  |  |  | NewVin | | £NewVin | |  | | |  |  |  |  | |
|  |  | VehDescription | | |  | |  | | |  |  |  |  | |
|  |  |  | Kind | | £Kind if filled else VN | |  | | |  |  |  |  | |
|  |  |  | Make | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification |  | |  | | |  |  |  |  | |
|  |  |  |  | XCode |  | |  | | |  |  |  |  | |
|  |  |  | Model | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification | PCODIF VEHRENAULT | |  | | |  |  |  | PCODIF VEHRENAULT | |
|  |  |  |  | XCode | £Model\_Ext if avail | |  | | |  |  |  | £Model\_Ext if avail | |
|  |  |  | **Engine** | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification | PCODIF VEHRENAULT | |  | | |  |  |  | PCODIF VEHRENAULT | |
|  |  |  |  | XCode | £FUEL-TYPE if avail | |  | | |  |  |  | £FUEL-TYPE if avail | |
|  |  |  | Length | | £Length | |  | | |  |  |  | £Length | |
|  |  |  | Height | | £Height | |  | | |  |  |  | £Height | |
|  |  |  |  | |  | |  | | |  |  |  |  | |
|  |  |  |  | |  | |  | | |  |  |  |  | |
|  |  |  | Color | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification | PCODIF VEHRENAULT if needed | |  | | |  |  |  | PCODIF VEHRENAULT if needed | |
|  |  |  |  | XCode | £Colour if avail | |  | | |  |  |  | £Colour if avail | |
|  |  |  | ProductionSite | |  | |  | | |  |  |  |  | |
|  |  |  |  | Code |  | |  | | |  |  |  |  | |
|  |  |  |  | Meaning |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification | PCOD RESRENAULT | |  | | |  |  |  | PCOD RESRENAULT if needed | |
|  |  |  |  | XCode | £factory if avail | |  | | |  |  |  | £factory if avail | |
|  |  |  | ProductionDate | | £ProductionDate | |  | | |  |  |  | VA00.[MADT-DATE] if avail (format YYYYMMDD) | |
|  |  |  | CheckOrdered | | £CheckOrdered | |  | | |  |  |  | £CheckOrdered | |
|  |  |  | CheckMoving | |  | |  | | |  |  |  |  | |
|  |  | Principal | | |  | |  | | |  |  |  |  | |
|  |  |  | Codification | | PCOD RESRENAULT | | PCOD RESRENAULT | | |  |  |  |  | |
|  |  |  | XCode | | ~~"DO.RENAULT"~~ £Principal if filled else "DO.RENAULT" | | "DO.RENAULT" | | |  |  |  |  | |
|  |  | Pickup | | |  | |  | | |  |  |  |  | |
|  |  |  | Codification | | **£Codification** if filled else PCOD RESRENAULT | |  | | |  |  |  | ~~PCOD RESRENAULT~~ | |
|  |  |  | XCode | | £Sender if avail | |  | | |  |  |  | ~~£Sender if avail~~ | |
|  |  |  | RomaCodification | | PCOD RESRENAULT | |  | | |  |  |  | ~~PCOD RESRENAULT~~ | |
|  |  |  | RomaXCode | | £Sender\_Roma if avail | |  | | |  |  |  | ~~£Sender\_Roma if avail~~ | |
|  |  |  |  | |  | |  | | |  |  |  |  | |
|  |  | **CheckPickupUnavailable** | | | **£CheckPickupUnavailable** | |  | | |  |  |  |  | |
|  |  | PickupDate | | | £Pickup\_Start if avail | |  | | |  |  |  | £Pickup\_Start if avail | |
|  |  | CustomerLoadno | | |  | |  | | |  |  |  |  | |
|  |  | Delivery | | |  | |  | | |  |  |  |  | |
|  |  |  | Codification | | If VA01.NEXT-LOGISTICS-PARTNER is not in the list **£PARAM2** then « PCOD RESRENAULT \_EP » else PCOD RESRENAULT | |  | | |  |  |  | PCOD RESRENAULT | |
|  |  |  | XCode | | £Delivery if avail | |  | | |  |  |  |  | |
|  |  |  | Name | | TR01.DESTINATION-NAME if available else TR01. PLACEMENT-DEALER-NAME | |  | | |  |  |  |  | |
|  |  |  | Name2 | |  | |  | | |  |  |  |  | |
|  |  |  | Address | | TR01.DESTINATION-ADDRESS-LINE1 NAME if available else TR01. PLACEMENT-DEALER-ADDRESS-LINE1 | |  | | |  |  |  |  | |
|  |  |  | Adress2 | | TR01.DESTINATION-ADDRESS-LINE2 if available else TR01. PLACEMENT-DEALER-ADDRESS-LINE2 | |  | | |  |  |  |  | |
|  |  |  | Zip | | TR01.DESTINATION-ZIP-CODE if available else TR01. PLACEMENT-DEALER-ZIP-CODE | |  | | |  |  |  |  | |
|  |  |  | City | | TR01.DESTINATION-CITY if available else TR01. PLACEMENT-DEALER-CITY | |  | | |  |  |  |  | |
|  |  |  | State | |  | |  | | |  |  |  |  | |
|  |  |  | Country | |  | |  | | |  |  |  |  | |
|  |  |  | **CountryCodification** | | PCOD RESRENAULT | |  | | |  |  |  |  | |
|  |  |  | **CountryXCode** | | TR01.DESTINATION-COUNTRY if available  else TR01.PLACEMENT-DEALER-COUNTRY | |  | | |  |  |  |  | |
|  |  |  | **CustomerAreaXCode** | | **£Delivery\_Zone** | |  | | |  |  |  |  | |
|  |  |  | RomaCodification | | PCOD RESRENAULT | |  | | |  |  |  |  | |
|  |  |  | RomaXCode | | £Delivery\_Roma | |  | | |  |  |  |  | |
|  |  |  | **DeliveryCustomerXCode** | |  | |  | | |  |  |  | £DeliveryCustomer | |
|  |  | DeliveryKind | | | No tag if £DeliveryKind is blank else £DeliveryKind if available else DELIVERY | | DELIVERY | | |  |  |  |  | |
|  |  | DeliveryDate | | |  | |  | | |  |  |  | ~~£DeliveryCustomer~~ | |
|  |  | DeliveryTimeStart | | |  | |  | | |  |  |  |  | |
|  |  | DeliveryTimeEnd | | |  | |  | | |  |  |  |  | |
|  |  | Consignee | | |  | |  | | |  |  |  |  | |
|  |  |  | Codification | | PCOD RESRENAULT | |  | | |  |  |  | PCOD RESRENAULT | |
|  |  |  | XCode | | £Consignee if avail | |  | | |  |  |  | £Consignee if avail | |
|  |  |  | **CountryCodification** | | PCOD RESRENAULT | |  | | |  |  |  |  | |
|  |  |  | **CountryXCode** | | £Country | |  | | |  |  |  |  | |
|  |  |  | RomaCodification | | PCOD RESRENAULT | |  | | |  |  |  |  | |
|  |  |  | RomaXCode | | £Consignee\_Roma if avail | |  | | |  |  |  |  | |
|  |  | SalesTerms | | |  | |  | | |  |  |  |  | |
|  |  |  | **Codification** | | PCOD RESRENAULT | |  | | |  |  |  |  | |
|  |  |  | **CustomerOfferXCode** | | **£CustomerOfferXCode** | |  | | |  |  |  |  | |
|  |  |  | PriorityLevel | | £PriorityLevel | |  | | |  |  |  | £PriorityLevel | |
|  |  | **Product** | | |  | |  | | |  |  |  |  | |
|  |  |  | **Code** | | **£Product** if filled else « DEFAUT » | |  | | |  |  |  |  | |
|  |  | LockingDescription | | |  | |  | | |  |  |  |  | |
|  |  |  | Type | |  | |  | | | "BUS" | "BUS" |  |  | |
|  |  |  | Level | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification |  | |  | | | PCODIF VEHRENAULT | PCODIF VEHRENAULT |  |  | |
|  |  |  |  | XCode |  | |  | | | £Lock\_level | £Lock\_level |  |  | |
|  |  |  | LockingOrderNo | |  | |  | | | £Lock\_Order | £Lock\_Order |  |  | |
|  |  |  | UnlockingRequestDate | |  | |  | | | HR01.[ESTIMATED-RELEASE-DATE] if avail |  |  |  | |
|  |  |  | CheckAutomaticUnlocking | |  | |  | | | FALSE |  |  |  | |
|  |  |  | LockingSite | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification |  | |  | | | PCOD RESRENAULT |  |  |  | |
|  |  |  |  | XCode |  | |  | | | £Lock\_site |  |  |  | |
|  |  | ServiceOrder | | |  | |  | | |  |  |  |  | |
|  |  |  | ServiceDescription | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification |  | |  | | |  |  | PCODIF VEHRENAULT |  | |
|  |  |  |  | XCode |  | |  | | |  |  | If VEHICLE-ENHANCEMENT = 'MLD '  Then SERVICE\_INFO  Else VEHICLE-ENHANCEMENT |  | |
|  |  |  |  | Meaning |  | |  | | |  |  | VEHICLE-ENHANCEMENT-DESCRIPTION if avail |  | |
|  |  |  | ServiceOrderNo | |  | |  | | |  |  | ORDER-CD |  | |
|  |  |  | ServiceStatus | |  | |  | | |  |  | START |  | |
|  |  |  | ServiceSite | |  | |  | | |  |  |  |  | |
|  |  |  |  | Codification |  | |  | | |  |  | PCOD RESRENAULT |  | |
|  |  |  |  | XCode |  | |  | | |  |  | NODE]if av |  | |
|  |  |  | StartRequestedDate | |  | |  | | |  |  | SCHEDULED-ARRIVAL-DATE if avail |  | |
|  |  |  | EndRequestedDate | |  | |  | | |  |  | VE01.[SCHEDULED-VE-COMPLETION-DATE] if avail |  | |
|  |  | CustomerReference/ | | |  | |  | | |  |  |  | *Map this tag and sub tag Only if £MVT\_NO= “VA02”* | |
|  |  |  | ReferenceKind | | DIV | |  | | |  |  |  | DIV | |
|  |  |  | ReferenceType | | « DEMANDEUR » | |  | | |  |  |  | « ORIGINE\_JOURNEY » (if needed) | |
|  |  |  | ReferenceXType | | « DEMANDEUR » | |  | | |  |  |  | « ORIGINE\_JOURNEY » (if needed) | |
|  |  |  | Reference | | VA00.[LOGISTICS-DESTINATION-DESC] if avail | |  | | |  |  |  | VA02.[LOGISTICS-PARTNER-CD] if avail | |
|  |  | CustomerReference/ | | |  | |  | | |  |  |  | *Map this tag and sub tag Only if £MVT\_NO= “VA02”* | |
|  |  |  | ReferenceKind | | DIV if £Delivry\_Zone filled | | DIV | | |  |  |  | DIV | |
|  |  |  | ReferenceType | | « DELIVERY\_ZONE » if £Delivry\_Zone fileld | | « DELIVERY\_ZONE » | | |  |  |  | “ORIGINE\_NM\_TRSP” (if needed) | |
|  |  |  | ReferenceXType | | « DELIVERY\_ZONE » if £Delivry\_Zone filled | | « DELIVERY\_ZONE » | | |  |  |  | “ORIGINE\_NM\_TRSP” (if needed) | |
|  |  |  | Reference | | **£Delivery\_Zone** | | DELETED | | |  |  |  | TRANSPORT-MEAN-NAME if avail | |
|  |  | CustomerReference/ | | |  | |  | | |  |  |  | *Map this tag and sub tag Only if £MVT\_NO= “VA02”* | |
|  |  |  | ReferenceKind | | VEH\_DESC | |  | | |  |  |  | DIV | |
|  |  |  | ReferenceType | | « RADIO » | |  | | |  |  |  | « ORIGINE\_NODE » (if needed) | |
|  |  |  | ReferenceXType | | « RADIO » | |  | | |  |  |  | « ORIGINE\_NODE » (if needed) | |
|  |  |  | Reference | | VA00.[RADIO-CODE] if avail | |  | | |  |  |  | LOADING-NODE if avail | |
|  |  | CustomerReference/ | | | map this tag only if £EXTERNAL\_CARRIER is available | |  | | |  |  |  | *Map this tag and sub tag Only if £MVT\_NO= “VA02”* | |
|  |  |  | ReferenceKind | | "DIV" | |  | | |  |  |  | DIV | |
|  |  |  | ReferenceType | | “EXTERNAL\_ATTRIBUTE” | |  | | |  |  |  | “ORIGINE\_DEP\_DATE” (if needed) | |
|  |  |  | ReferenceXType | | « CARRIER » | |  | | |  |  |  | “ORIGINE\_DEP\_DATE” (if needed) | |
|  |  |  | Reference | | **Concatenate (« CAR| » ;** £EXTERNAL\_CARRIER) | |  | | |  |  |  | ACTUAL-DATE-DATE if avail | |
|  |  | CustomerReference/ | | |  | |  | | |  |  |  |  | |
|  |  |  | ReferenceKind | | DIV | | DIV | | | DIV | DIV | DIV | DIV | |
|  |  |  | ReferenceType | | « LOGISTICS-PARTNER-CD » | | « LOGISTICS-PARTNER-CD » | | | « LOGISTICS-PARTNER-CD » | « LOGISTICS-PARTNER-CD » | « LOGISTICS-PARTNER-CD » | « LOGISTICS-PARTNER-CD » | |
|  |  |  | ReferenceXType | | « LOGISTICS-PARTNER-CD » | | « LOGISTICS-PARTNER-CD » | | | « LOGISTICS-PARTNER-CD » | « LOGISTICS-PARTNER-CD » | « LOGISTICS-PARTNER-CD » | « LOGISTICS-PARTNER-CD » | |
|  |  |  | Reference | | £LOGISTICS-PARTNER-CD | | £LOGISTICS-PARTNER-CD | | | £LOGISTICS-PARTNER-CD | £LOGISTICS-PARTNER-CD | £LOGISTICS-PARTNER-CD | £LOGISTICS-PARTNER-CD | |

#### INCOMING LOAD Mapping

| **Node Level** | | | | | | **Value** | **Comments** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **IncomingLoad/** | | | | | 1-1 |  |  |
|  | Header/ | | | | 1-1 |  |  |
|  |  | MessageNo | | | 1-1 | ~~£FILE\_NAME~~ concatenate(**£Filename ; »-« ;** £VIN;”-“; £DATEVEN) | Put the original full filename |
|  |  | RecordNo | | | 0-1 |  | Raw number in received file |
|  |  | MessageDate | | | 1-1 | £DATEVEN | This is the date of the receiving of the file in the EAI. |
|  |  | **Issuer/** | | | 1-1 |  |  |
|  |  |  | Code | | 1-1 |  |  |
|  |  |  | Codification | | 0-1 | PCOD RESRENAULT |  |
|  |  |  | XCode | | 0-1 | ~~START-NODE~~ “STEFI” |  |
|  |  |  | Name | | 0-1 |  |  |
|  |  |  | Contact | | 0-1 |  |  |
|  |  |  | Phone | | 0-1 |  |  |
|  |  |  | Mail | | 0-1 |  |  |
|  |  |  | Language | | 0-1 |  |  |
|  |  | **Receiver/** | | | 1-1 |  |  |
|  |  |  | Code | | 1-1 |  |  |
|  |  |  | Name | | 0-1 |  |  |
|  |  |  | Codification | | 0-1 | PCOD RESRENAULT |  |
|  |  |  | XCode | | 0-1 | LD01.RECEIVER-CD |  |
|  |  | **OriginSoftware** | | | 0-1 | “STEFI” | In any case, the OriginSoftware tag must be created and with a value |
|  |  | **MvtType** | | | 0-1 | **Concanate(**“LD01-”, LD01.LOAD-NO) |  |
|  |  | **MvtNo** | | | 0-1 | “LD01” |  |
|  |  | **MsgSynchroMode** | | | 0-1 | NO\_ONE |  |
|  |  | **MsgSynchroNumber** | | |  |  |  |
|  |  | **MsgMasterNo** | | |  |  |  |
|  |  | **MsgMasterSequence** | | |  |  |  |
|  |  | **MsgMasterNumber** | | |  |  |  |
|  | Trip/ | | | | 0-1 |  |  |
|  |  | TripNo | | | 0-1 |  | Trip number in Moveecar |
|  |  | TripXNo | | | 1-1 | LD01.LOAD-NO if available | Trip number in external system |
|  |  | TotalVehiclesNumber | | | 1-1 | LD01.Quantity-of-units if available | Total number of vehicles in the trip  *(position 110 to 112, in the record line)* |
|  |  | Supplier | | | 0-1 |  |  |
|  |  |  | Code | | 0-1 |  |  |
|  |  |  | Codification | | 0-1 | PCOD RESRENAULT |  |
|  |  |  | XCode | | 0-1 | ~~CARRIER-COMPANY~~ LD01.RECEIVER-CD |  |
|  |  |  | Name | | 0-1 |  |  |
|  |  | ExecSupplier | | | 0-1 |  |  |
|  |  |  | Code | | 0-1 |  |  |
|  |  |  | Codification | | 0-1 | PCOD RESRENAULT |  |
|  |  |  | XCode | | 0-1 | LD01.RECEIVER-CD |  |
|  |  |  | Name | | 1-1 |  |  |
|  |  |  | Name2 | | 0-1 |  |  |
|  |  |  | Address | | 0-1 |  |  |
|  |  |  | Address2 | | 0-1 |  |  |
|  |  |  | Zip | | 0-1 |  |  |
|  |  |  | City | | 0-1 |  |  |
|  |  |  | State | | 0-1 |  |  |
|  |  |  | Country2 | | 0-1 |  |  |
|  |  |  | Country3 | | 0-1 |  |  |
|  |  |  | ContactName | | 0-1 |  |  |
|  |  |  | Phone | | 0-1 |  |  |
|  |  |  | Email | | 0-1 |  |  |
|  |  | RoadMeans/ | | | 0-1 |  |  |
|  |  |  | TruckPlateNo | | 0-1 | LD01.LICENSE-PLATE-NO if available |  |
|  |  |  | TrailerPlateNo | | 0-1 | LD01.TRAILER-REG-NO if available |  |
|  |  |  | DriverName | | 0-1 | LD01.DRIVER-NAME if available |  |
|  | Load/ | | | | 1-N |  |  |
|  |  | LoadNo | | | 0-1 |  | Load Number in Moveecar |
|  |  | LoadXNo | | | 1-1 | LD01.LOAD-NO if available | External Load Number (in Origin system) |
|  |  | TransportMode | | | 1-1 | "R" |  |
|  |  | DeliveryKind | | | 0-1 | ~~"DELIVERY"~~  ON\_SITE | ‘delivery on site’ (ON\_SITE) or ‘to be delivered’ (DELIVERY) |
|  |  | LoadStatus | | | 1-1 |  |  |
|  |  | RawNo | | | 0-1 |  |  |
|  |  | LoadDeparture/ | | | 1-1 |  |  |
|  |  |  | Code | | 0-1 |  |  |
|  |  |  | Codification | | 0-1 | PCOD RESRENAULT |  |
|  |  |  | XCode | | 0-1 | LD01.START-NODE |  |
|  |  |  | Name | | 1-1 |  |  |
|  |  |  | Name2 | | 0-1 |  |  |
|  |  |  | Address | | 0-1 |  |  |
|  |  |  | Address2 | | 0-1 |  |  |
|  |  |  | Zip | | 0-1 |  |  |
|  |  |  | City | | 1-1 |  |  |
|  |  |  | State | | 0-1 |  |  |
|  |  |  | Country2 | | 1-1 |  |  |
|  |  |  | Country3 | | 1-1 |  |  |
|  |  |  | PlannedDate | | 0-1 | LD01.ESTIMATED-COLLECTION-DATE if available format YYYY-MM-DD |  |
|  |  |  | PlannedTime | | 0-1 | LD01.ESTIMATED-COLLECTION-TIME if available format HH:MM::SS |  |
|  |  |  | RealDateTime | | 0-1 |  |  |
|  |  | LoadArrival | | | 1-1 |  |  |
|  |  |  | Code | | 0-1 |  |  |
|  |  |  | Codification | | 0-1 | ~~PCOD RESRENAULT~~ |  |
|  |  |  | XCode | | 0-1 | ~~DESTINATION-NODE~~ |  |
|  |  |  | Name | | 0-1 |  |  |
|  |  |  | Name2 | | 0-1 |  |  |
|  |  |  | Address | | 0-1 |  |  |
|  |  |  | Address2 | | 0-1 |  |  |
|  |  |  | Zip | | 0-1 |  |  |
|  |  |  | City | | 1-1 |  |  |
|  |  |  | State | | 0-1 |  |  |
|  |  |  | Country2 | | 1-1 |  |  |
|  |  |  | Country3 | | 1-1 |  |  |
|  |  |  | PlannedDate | | 0-1 |  |  |
|  |  |  | PlannedTime | | 0-1 |  |  |
|  |  | VehiclesNumber | | | 1-1 |  |  |
|  |  | Vehicle | | | 1-N |  |  |
|  |  |  | VehIdentification | | 1-1 |  |  |
|  |  |  |  | Vin | 0-1 | £VIN |  |
|  |  |  |  | PlateNo | 0-1 |  |  |
|  |  |  | OperationNo | | 0-1 |  |  |
|  |  |  | Movement | | 0-1 | If ~~LICENSE-PLATE-NO~~ LD01.LOAD-NO is not available “OUT” else “IN” |  |
|  |  |  | ManifestNo | | 0-1 |  |  |
|  |  |  | FloorPosition | | 0-1 |  |  |

#### INCOMING EVENT mapping

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| IncomingEvent | | | |  |  |
| Header/ | | | | |  |
|  | MessageNo | | | | CONCAT(“TR01-” + **£VIN** + “-“ + current date format YYYYMMDD-HHMISS)  Example : TR01-VF1K381EGMU067173-20210708-152301 |
|  | RecordNo | | | |  |
|  | MessageDate | | | |  |
|  | Issuer/ | | | |  |
|  |  | Code | | |  |
|  |  | Codification | | | ‘PCOD RESRENAULT’ |
|  |  | XCode | | | "DO.RENAULT" |
|  |  | Name | | |  |
|  |  | Contact | | |  |
|  |  | Phone | | |  |
|  |  | Mail | | |  |
|  |  | Language | | |  |
|  | Receiver/ | | | |  |
|  |  | Code | | |  |
|  |  | Name | | |  |
|  |  | Codification | | | ‘GEFCO’ |
|  |  | XCode | | | ‘160’ |
|  | OriginSoftware | | | | ‘STEFI’ |
|  | MvtType | | | | ‘TR01’ |
|  | MvtNo | | | |  |
|  | MsgSynchroMode | | | |  |
|  | MsgSynchroNumber | | | |  |
|  | MsgMasterNo | | | |  |
|  | MsgMasterSequence | | | |  |
|  | MsgMasterNumber | | | |  |
| Event/ | | | | |  |
|  | ~~XId~~ | | | |  |
|  | ~~EventType~~ | | | |  |
|  |  | ~~ActionKind~~ ActionKind | | | ‘EXECUTION’ |
|  |  | ~~Code~~ | | |  |
|  |  | SubCode | | |  |
|  |  | Codification | | | ‘GEFCO’ |
|  |  | XCode | | | £FlagTR01 |
|  |  | XSubCode | | |  |
|  | Meaning | | | |  |
|  | Comments | | | |  |
|  | Location | | | |  |
|  |  | ThirdParty | | |  |
|  |  |  | Code | |  |
|  |  |  | Codification | | PCOD RESRENAULT1 |
|  |  |  | XCode | | **£DEP\_POINT\_ID** |
|  |  | Name | | |  |
|  |  | Name2 | | |  |
|  |  | Address | | |  |
|  |  | Address2 | | |  |
|  |  | Zip | | |  |
|  |  | City | | |  |
|  |  | Country | | |  |
|  |  | Longitude | | |  |
|  |  | Latitude | | |  |
|  | Origin | | | | ‘STEFI’ |
|  | RealDateTime | | | | **£Pickup\_Start** *(format YYYY-MM-DDThh:mm:ss) if* **£Pickup\_Start is in format YYYYMMDD add hh:mm:ss =00:00:00 for example if £Pickup\_Start 20220415 the result is 2022-04-15T00:00:00** |
|  | RealDateTimeUtc | | | |  |
|  | PlannedDateTime | | | |  |
|  | PlannedDateTimeUtc | | | |  |
|  | VehIdentification | | | |  |
|  |  | Vin | | | **£VIN** |
|  |  | PlateNo | | |  |
|  |  | OF | | |  |
|  |  | CAF | | |  |
|  |  | CustomerIdentification | | |  |

**Description du formalisme XML :** Paragraphe valable uniquement pour le format XML

**En-tête JAVA MQSeries JMS :** l’entête jms est obligatoire lorsque le flow doit être consommé dans un environnement jms.

En-tête JMS (Yes/no) : à préciser en collaboration avec l’équipe EAI

|  |  |
| --- | --- |
| **Attribut de la déclaration** | **Valeur de l’attribut** |
| MSG\_TYPE |  |
| MSG\_VERSION |  |

**Description de l’enregistrement :** Insérer ici tous les fichiers externes pouvant décrire la structure de départ (.xsd, xls, …) ou décrire l’enregistrement dans un tableau word.

Et aussi les instructions du genre :

* Si un tag n’a pas de valeur, ne pas le renseigner dans la structure de sortie.
* Toutes les dates sont au format ssaa/mm/jj hh :mn ss
* Le ‘.’ est utilisé pour les données numériques avec décimales

**Déclarations de début XML**

Exemple : <?xml version="**1.0**" encoding="**utf-8**"?>

Déclarations de début XML (Yes/no) : à préciser en collaboration avec l’équipe EAI

|  |  |
| --- | --- |
| **Attribut de la déclaration** | **Valeur de l’attribut** |
| version | 1.0 |
| encoding | UTF-8 |

## Traitements de mapping

Si besoin insérer ici le fichier .xls décrivant le mapping ou insérer ici un tableau avec la description du mapping

Le traitement peut faire référence aux paramètres $PARAM1 et $PARAM2, aux codes d’erreur ou d’annonce.

## Traitements specifiques

Si besoin préciser les traitements spécifiques à effectuer.

Ex : Passage du mode DOS des CR en mode UNIX CRLF

Faire du NON CONVERT

## Traitements post-accumulation

On spécifie ici le traitement à effectuer sur les données lorsque le traitement d’accumulation est terminé.

Exemple :

*Le traitement d’accumulation des flow entrants est terminé.*

*Donc on trouvera des flow entrants pour différents abonnés.*

*Il s’agit de les regrouper par abonné (utiliser la valeur du tag OBBISOFT/PIVOTS/ABONNE/ID\_ABONNE de chaque flow entrant),*

*Puis de déposer un flow d’arrivée par abonné après y avoir ajouter le tag .*