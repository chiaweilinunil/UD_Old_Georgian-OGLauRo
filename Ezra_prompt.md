# Prompt: Parse Old Georgian Verses into CoNLL-U Format

## Task

Parse the following Old Georgian verses into `.conllu` format, following the Universal Dependencies (UD) conventions and matching the annotation style of the reference examples provided below.

## Input

```
# sent_id = 3_1
# text = მოვიდა და მოიწია ერთიღა იგი შჳდეული, და იყვნეს ძენი იგი ისრაელისანი თითოეულად თჳსსა ქალაქსა, და შეკრბა ყოველი იგი ერი ერთბამად, ვითარცა ერთი კაცი, იერუსალემდ.
# sent_id = 3_2
# text = და აღდგა ისუ იოსედეკეანი და ძმანი მისნი, მღდელნი იგი, და ზორობაბელ, ძჱ სალათიელისი, და ძმანი მისნი, და აღაშჱნეს საკურთხეველი საკუერთხთაჲ უფლისა ღმრთისა ისრაელისაჲ შეწირვად მას ზედა საკუერთხი, ვითარცა წერილ არს შჯულსა მოსესსა, კაცისა მის ღმრთისა.
# sent_id = 3_3_1
# text = და განჰმზადნეს საზორველნი და განმზადებულებისა მისებრ თჳსისაჲსა, რამეთუ ეშინოდა ნათესავთაგან მის ქუეყანისათა.
# sent_id = 3_3_2
# text = და შეწირეს მას ზედა საკუერთხი მეყსეულად უფლისა ღმრთისა თჳსისა _ ერთი ცისკარს და ერთი მწუხრი.
```

## Lemma

Extract lemmas using the National Parliamentary Library of Georgia's Old Georgian dictionary:
<http://www.nplg.gov.ge/gwdict/index.php?a=term&d=57&t=31272>


## XPOS

For UPOS=VERB, XPOS should have this format V_[voice]_[mood]_[tense]_[preverb]_[version]_[S:3Sg]_[O:3Sg]_[IO:3Sg]

## Example 
```
# sentence_id = 1_1
# text = პირველსა მას წელსა კჳროს მეფისა სპარსთაჲსა, აღსრულებასა სიტყჳსა უფლისაჲსა პირითა იერემია წინაწარმეტყუელისაჲთა განაღჳძა უფალმან სული კჳროსისი, მეფისა სპარსთაჲსაჲ, და მისცა ბრძანებაჲ მცნებისაჲ ყოველსა საშარავანდედოსა თჳსსა და მიწერა ყოველთა მიმართ სახე ესე:
1	პირველსა	პირველი	ADJ	A_Ord_Dat_Sg	Case=Dat|Number=Sing|NumType=Ord	3	amod	3:amod	LMSeg:პირველ[ი]|Translit=pirvelsa
2	მას	იგი	PRON	Pron_Dem_Dat_Sg	Case=Dat|Number=Sing|PronType=Dem	3	det	3:det	LMSeg:იგი|Translit=mas
3	წელსა	წელი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	14	obl	14:obl	LMSeg:წელ[ი]|Translit=c̣elsa
4	კჳროს	კჳროს	PROPN	N_Prop	NameType=Giv	5	nmod	5:nmod	LMSeg:კჳროს|Translit=k̇wiros
5	მეფისა	მეფე	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	3	nmod	3:nmod	LMSeg:მეფე|Translit=mepisa
6	სპარსთაჲსა	სპარსი	PROPN	N_Prop_Obl_Pl_Gen_Sg	Case=Gen|Case[sauf]=Gen|Number=Plur|Number[sauf]=Sing|NameType=Nat	5	nmod	5:nmod	LMSeg:სპარს[ი]|Translit=sparstayisa
7	,	,	PUNCT	Punct_Comma	_	8	punct	8:punct	LMSeg:,
8	აღსრულებასა	აღსრულება	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	14	obl	14:obl	LMSeg:აღ·სრულება|Translit=agsrulebasa
9	სიტყჳსა	სიტყუა	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	8	nmod	8:nmod	LMSeg:სიტყუა|Translit=sitq̇visa
10	უფლისაჲსა	უფალი	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	9	nmod	9:nmod	LMSeg:უფალ[ი]|Translit=uplisaysa
11	პირითა	პირი	NOUN	N_Ins_Sg	Case=Ins|Number=Sing	8	nmod	8:nmod	LMSeg:პირ[ი]|Translit=pirita
12	იერემია	იერემია	PROPN	N_Prop_Gen_Sg	Case=Gen|Number=Sing|NameType=Giv	13	nmod	13:nmod	LMSeg:იერემია|Translit=ieremia
13	წინაწარმეტყუელისაჲთა	წინაწარმეტყუელი	NOUN	N_Gen_Sg_Ins_Sg	Case=Gen|Case[sauf]=Ins|Number=Sing|Number[sauf]=Sing	11	nmod	11:nmod	LMSeg:წინაწარ·მეტყუელ[ი]|Translit=c̣inac̣armetq̇uelisayta
14	განაღჳძა	განღჳძება	VERB	V_Act_Aor_Pv_AV_S:3Sg	Mood=Ind|Number[subj]=Sing|Person[subj]=3|Tense=Aor|VerbForm=Fin	0	root	0:root	LMSeg:გან·ღჳძება|Translit=ganagwiʒa
15	უფალმან	უფალი	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	14	nsubj	14:nsubj	LMSeg:უფალ[ი]|Translit=upalman
16	სული	სული	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	14	obj	14:obj	LMSeg:სულ[ი]|Translit=suli
17	კჳროსისი	კჳროსი	PROPN	N_Prop_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing|NameType=Giv	16	nmod	16:nmod	LMSeg:კჳროს[ი]|Translit=k̇wirosisi
18	,	,	PUNCT	Punct_Comma	_	19	punct	19:punct	LMSeg:,
19	მეფისა	მეფე	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	17	appos	17:appos	LMSeg:მეფე|Translit=mepisa
20	სპარსთაჲსაჲ	სპარსი	PROPN	N_Prop_Obl_Pl_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Gen|Case[sauf2]=Nom|Number=Plur|Number[sauf]=Sing|Number[sauf2]=Sing|NameType=Nat	19	nmod	19:nmod	LMSeg:სპარს[ი]|Translit=sparstayisay
21	,	,	PUNCT	Punct_Comma	_	23	punct	23:punct	LMSeg:,
22	და	და	CCONJ	Cj_Coord	_	23	cc	23:cc	LMSeg:და|Translit=da
23	მისცა	მიცემა	VERB	V_Act_Aor_Pv_S:3Sg_IO:3Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=3|Person[subj]=3|Tense=Aor|VerbForm=Fin	14	conj	14:conj	LMSeg:მი·ცემა|Translit=misca
24	ბრძანებაჲ	ბრძანებაჲ	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	23	obj	23:obj	LMSeg:ბრძანებაჲ|Translit=brʒanebay
25	მცნებისაჲ	მცნებაჲ	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	24	nmod	24:nmod	LMSeg:მცნებაჲ|Translit=mc̣nebisay
26	ყოველსა	ყოველი	PRON	Pron_Tot_Dat_Sg	Case=Dat|Number=Sing|PronType=Tot	27	det	27:det	LMSeg:ყოველი|Translit=qovelsa
27	საშარავანდედოსა	საშარავანდედო	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	23	iobj	23:iobj	LMSeg:საშარავანდედო|Translit=sašaravandedosa
28	თჳსსა	თჳსი	PRON	Pron_Poss_Dat_Sg	Case=Dat|Number=Sing|Poss=Yes|PronType=Prs	27	nmod	27:nmod	LMSeg:თჳსი|Translit=tvissa
29	და	და	CCONJ	Cj_Coord	_	30	cc	30:cc	LMSeg:და|Translit=da
30	მიწერა	წერა	VERB	V_Act_Aor_Pv_S:3Sg_O:3Pl	Mood=Ind|Number[obj]=Plur|Number[subj]=Sing|Person[obj]=3|Person[subj]=3|Tense=Aor|VerbForm=Fin	23	conj	23:conj	LMSeg:წერა|Translit=mic̣era
31	ყოველთა	ყოველი	PRON	Pron_Tot_Obl_Pl	Case=Dat|Number=Plur|PronType=Tot	30	obl	30:obl	LMSeg:ყოველი|Translit=qovelta
32	მიმართ	მიმართ	ADP	Post	AdpType=Post|Case=Dat	31	case	31:case	LMSeg:მიმართ|Translit=mimart
33	სახე	სახე	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	30	obj	30:obj	LMSeg:სახე|Translit=saḵe
34	ესე	ესე	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	33	det	33:det	LMSeg:ესე|Translit=ese|SpaceAfter=No
35	:	:	PUNCT	Punct_Colon	_	24	punct	24:punct	LMSeg::

# sentence_id = 1_2
# text = ესრე იტყჳს კჳროს, მეფჱ სპარსთაჲ: ყოველი შარავანდედებაჲ ქუეყანისაჲ მომცა მე უფალმან, ღმერთმან ზეცისამან, და მან მიბრძანა მე მოძიებად, რაჲთა უშჱნო მას ტაძარი იერუსალემს ჰურიასტანისასა.
1	ესრე	ესრე	ADV	Adv	_	2	advmod	2:advmod	LMSeg:ესრე|Translit=esre
2	იტყჳს	თქუმა	VERB	V_Act_Pres_IV_S:3Sg	Mood=Ind|Number[subj]=Sing|Person[subj]=3|Tense=Pres|VerbForm=Fin	0	root	0:root	LMSeg:თქუმა|Translit=iṭq̇wis
3	კჳროს	კჳროსი	PROPN	N_Prop	NameType=Giv	2	nsubj	2:nsubj	LMSeg:კჳროს[ი]|Translit=k'iros
4	,	,	PUNCT	Punct_Comma	_	5	punct	5:punct	LMSeg:,
5	მეფჱ	მეფე	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	3	appos	3:appos	LMSeg:მეფე|Translit=mepē
6	სპარსთაჲ	სპარსი	PROPN	N_Prop_Obl_Pl_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Plur|Number[sauf]=Sing|NameType=Nat	5	nmod	5:nmod	LMSeg:სპარს[ი]|Translit=sparstay
7	:	:	PUNCT	Punct_Colon	_	2	punct	2:punct	LMSeg::
8	ყოველი	ყოველი	ADJ	A_Nom_Sg	Case=Nom|Number=Sing	9	amod	9:amod	LMSeg:ყოველ[ი]|Translit=q̇oveli
9	შარავანდედებაჲ	შარავანდედება	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	11	obj	11:obj	LMSeg:შარავანდედება|Translit=sharavandedebay
10	ქუეყანისაჲ	ქუეყანა	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	9	nmod	9:nmod	LMSeg:ქუეყანა|Translit=kueq̇anisay
11	მომცა	მოცემა	VERB	V_Act_Aor_Pv_S:3Sg_IO:1Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=1|Person[subj]=3|Tense=Aor|VerbForm=Fin	2	parataxis	2:parataxis	LMSeg:მო·ცემა|Translit=momca
12	მე	მე	PRON	Pron_Pers_1Sg	Number=Sing|Person=1|PronType=Prs	11	iobj	11:iobj	LMSeg:მე|Translit=me
13	უფალმან	უფალი	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	11	nsubj	11:nsubj	LMSeg:უფალ[ი]|Translit=upalman
14	,	,	PUNCT	Punct_Comma	_	15	punct	15:punct	LMSeg:,
15	ღმერთმან	ღმერთი	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	13	appos	13:appos	LMSeg:ღმერთ[ი]|Translit=gmertman
16	ზეცისამან	ზეცა	NOUN	N_Gen_Sg_Erg_Sg	Case=Gen|Case[sauf]=Erg|Number=Sing|Number[sauf]=Sing	15	nmod	15:nmod	LMSeg:ზეცა|Translit=zecisaman
17	,	,	PUNCT	Punct_Comma	_	20	punct	20:punct	LMSeg:,
18	და	და	CCONJ	Cj_Coord	_	20	cc	20:cc	LMSeg:და|Translit=da
19	მან	იგი	PRON	Pron_Dem_Erg_Sg	Case=Erg|Number=Sing|PronType=Dem	20	nsubj	20:nsubj	LMSeg:იგი|Translit=man
20	მიბრძანა	მიბრძანება	VERB	V_Act_Aor_Pv_S:3Sg_IO:1Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=1|Person[subj]=3|Tense=Aor|VerbForm=Fin	11	conj	11:conj	LMSeg:მი·ბრძანება|Translit=mibrzana
21	მე	მე	PRON	Pron_Pers_1Sg	Number=Sing|Person=1|PronType=Prs	20	iobj	20:iobj	LMSeg:მე|Translit=me
22	მოძიებად	მოძიება	NOUN	N_Adv	Case=Adv	20	xcomp	20:xcomp	LMSeg:მო·ძიება|Translit=moziebad
23	,	,	PUNCT	Punct_Comma	_	25	punct	25:punct	LMSeg:,
24	რაჲთა	რაჲთა	SCONJ	Cj_Sub	_	25	mark	25:mark	LMSeg:რაჲთა|Translit=rayta
25	უშჱნო	შჱნება	VERB	V_Act_Subj_Pv_UV_S:1Sg_IO:3Sg	Mood=Sub|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=3|Person[subj]=1|Tense=Aor|VerbForm=Fin	20	advcl	20:advcl	LMSeg:შჱნება|Translit=ushēno
26	მას	იგი	PRON	Pron_Dem_Dat_Sg	Case=Dat|Number=Sing|PronType=Dem	25	iobj	25:iobj	LMSeg:იგი|Translit=mas
27	ტაძარი	ტაძარი	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	25	obj	25:obj	LMSeg:ტაძარ[ი]|Translit=ṭazari
28	იერუსალემს	იერუსალემი	PROPN	N_Prop_Dat_Sg	Case=Dat|Number=Sing|NameType=Geo	25	obl	25:obl	LMSeg:იერუსალემ[ი]|Translit=ierusalems
29	ჰურიასტანისასა	ჰურიასტანი	PROPN	N_Prop_Gen_Sg_Dat_Sg	Case=Gen|Case[sauf]=Dat|Number=Sing|Number[sauf]=Sing|NameType=Geo	28	nmod	28:nmod	LMSeg:ჰურიასტან[ი]|Translit=huriastanisasa
30	.	.	PUNCT	Punct_FullStop	_	2	punct	2:punct	LMSeg:.

# sentence_id = 1_3
# text = თუ ვინმე იყოს თქუენგანი, ყოველსა მაგას ერსა უფლისასა, რომელსა თანა იყოს ღმერთი მისი, მის თანა აღვედინ იერუსალემს ჰურიასტანისასა და აღაშჱნენ სახლი იგი უფლისა ღმრთისა ისრაელისაჲ.
1	თუ	თუ	SCONJ	Cj_Sub	_	3	mark	3:mark	LMSeg:თუ|Translit=tu
2	ვინმე	ვინმე	PRON	Pron_Ind_Nom_Sg	Case=Nom|Number=Sing|PronType=Ind	3	nsubj	3:nsubj	LMSeg:ვინმე|Translit=vinme
3	იყოს	ყოფა	VERB	V_Act_Subj_IV_S:3Sg	Mood=Sub|Number[subj]=Sing|Person[subj]=3|Tense=Aor|VerbForm=Fin	19	advcl	19:advcl	LMSeg:ყოფა|Translit=iqos
4-5	თქუენგანი	_	_	_	_	_	_	_	Translit=tkuengani
4	თქუენ	თქუენი	PRON	Pron_Pers_2Pl	Number=Plur|Person=2|PronType=Prs	2	nmod	2:nmod	LMSeg:თქუენი|Translit=tkuen
5	განი	გან	ADP	Post	AdpType=Post|Case[sauf]=Nom	4	case	4:case	LMSeg:გან|Translit=gani
6	ყოველსა	ყოველი	ADJ	A_Dat_Sg	Case=Dat|Number=Sing	8	amod	8:amod	LMSeg:ყოველ[ი]|Translit=qovelsa
7	მაგას	ეგე	PRON	Pron_Dem_Dat_Sg	Case=Dat|Number=Sing|PronType=Dem	8	det	8:det	LMSeg:იგი|Translit=magas
8	ერსა	ერი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	3	obl	3:obl	LMSeg:ერ[ი]|Translit=ersa
9	უფლისასა	უფალი	NOUN	N_Gen_Sg_Dat_Sg	Case=Gen|Case[sauf]=Dat|Number=Sing|Number[sauf]=Sing	8	nmod	8:nmod	LMSeg:უფალ[ი]|Translit=uplisasa
10	,	,	PUNCT	Punct_Comma	_	13	punct	13:punct	LMSeg:,
11	რომელსა	რომელი	PRON	Pron_Rel_Dat_Sg	Case=Dat|Number=Sing|PronType=Rel	13	obl	13:obl	LMSeg:რომელ[ი]|Translit=romelsa
12	თანა	თანა	ADP	Post	AdpType=Post|Case=Dat	11	case	11:case	LMSeg:თანა|Translit=tana
13	იყოს	ყოფა	VERB	V_Act_Subj_IV_S:3Sg	Mood=Sub|Number[subj]=Sing|Person[subj]=3|Tense=Aor|VerbForm=Fin	8	acl:relcl	8:acl:relcl	LMSeg:ყოფა|Translit=iqos
14	ღმერთი	ღმერთი	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	13	nsubj	13:nsubj	LMSeg:ღმერთ[ი]|Translit=gmrti
15	მისი	მისი	PRON	Pron_Poss_3Sg_Nom_Sg	Case=Nom|Number=Sing|Person=3|Poss=Yes|PronType=Prs	14	nmod	14:nmod	LMSeg:მისი|Translit=misi
16	,	,	PUNCT	Punct_Comma	_	19	punct	19:punct	LMSeg:,
17	მის	იგი	PRON	Pron_Dem_Dat_Sg	Case=Dat|Number=Sing|PronType=Dem	19	obl	19:obl	LMSeg:იგი|Translit=mis
18	თანა	თანა	ADP	Post	AdpType=Post|Case=Dat	17	case	17:case	LMSeg:თანა|Translit=tana
19	აღვედინ	აღსვლა	VERB	V_Act_Imp_Pv_S:3Sg	Mood=Imp|Number[subj]=Sing|Person[subj]=3|Tense=Aor|VerbForm=Fin	0	root	0:root	LMSeg:აღ·სვლა|Translit=agvedin
20	იერუსალემს	იერუსალემი	PROPN	N_Prop_Dat_Sg	Case=Dat|Number=Sing|NameType=Geo	19	obl	19:obl	LMSeg:იერუსალემ[ი]|Translit=ierusalems
21	ჰურიასტანისასა	ჰურიასტანი	PROPN	N_Prop_Gen_Sg_Dat_Sg	Case=Gen|Case[sauf]=Dat|Number=Sing|Number[sauf]=Sing|NameType=Geo	20	nmod	20:nmod	LMSeg:ჰურიასტან[ი]|Translit=huriastanisasa
22	და	და	CCONJ	Cj_Coord	_	23	cc	23:cc	LMSeg:და|Translit=da
23	აღაშჱნენ	აღშენება	VERB	V_Act_Imp_Pv_AV_S:3Sg	Mood=Imp|Number[subj]=Sing|Person[subj]=3|Tense=Aor|VerbForm=Fin	19	conj	19:conj	LMSeg:აღ·შენება|Translit=agashenen
24	სახლი	სახლი	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	23	obj	23:obj	LMSeg:სახლ[ი]|Translit=saxli
25	იგი	იგი	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	24	det	24:det	LMSeg:იგი|Translit=igi
26	უფლისა	უფალი	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	24	nmod	24:nmod	LMSeg:უფალ[ი]|Translit=uplisa
27	ღმრთისა	ღმერთი	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	26	appos	26:appos	LMSeg:ღმერთ[ი]|Translit=gmrtisa
28	ისრაელისაჲ	ისრაელი	PROPN	N_Prop_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing|NameType=Geo	27	nmod	27:nmod	LMSeg:ისრაელ[ი]|Translit=israelisay|SpaceAfter=No
29	.	.	PUNCT	Punct_FullStop	_	19	punct	19:punct	LMSeg:.

# sentence_id = 1_4
# text = და თავადი ღმერთი, რომელი-იგი დამკჳდრებულ არს იერუსალემს, იყავნ მის თანა; და ყოველი განმზადებულებაჲ მის თანა წარიღენ ადგილსა მას, სადა-იგი თჳთ დამკჳდრებულ არს. და თანა-წარიღენ ყოველივე აღსაგებელი თჳსი, რომელ-რაჲ იყოს ოქროჲსაჲ და ვეცხლისაჲ. სხუაჲ ჭურჭერი და საცხოვარი მოყუასთა თჳსთა თანა წარიღენ განსაგებელად ტაძრისა მის ღმრთისა იერუსალემდ.
1	და	და	CCONJ	Cj_Coord	_	10	cc	10:cc	LMSeg:და|Translit=da
2	თავადი	თავადი	ADJ	A_Nom_Sg	Case=Nom|Number=Sing	3	amod	3:amod	LMSeg:თავადი|Translit=tavadi
3	ღმერთი	ღმერთი	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	10	nsubj	10:nsubj	LMSeg:ღმერთ[ი]|Translit=gmerti
4	,	,	PUNCT	Punct_Comma	_	6	punct	6:punct	LMSeg:,
5	რომელი-იგი	რომელი-იგი	PRON	Pron_Rel_Nom_Sg	Case=Nom|Number=Sing|PronType=Rel	6	nsubj	6:nsubj	LMSeg:რომელი+იგი|Translit=romel-igi
6	დამკჳდრებულ	დამკჳდრება	VERB	V_Part_Pv_Abs	Case=Abs|Tense=Past|VerbForm=Part	3	acl:relcl	3:acl:relcl	LMSeg:და·მკჳდრება|Translit=damkwidrebul
7	არს	ყოფა	AUX	V_Act_Pres_S:3Sg	Mood=Ind|Number[subj]=Sing|Person[subj]=3|Tense=Pres|VerbForm=Fin	6	aux	6:aux	LMSeg:ყოფა|Translit=ars
8	იერუსალემს	იერუსალემი	PROPN	N_Prop_Dat_Sg	Case=Dat|Number=Sing|NameType=Geo	6	obl	6:obl	LMSeg:იერუსალემ[ი]|Translit=ierusalems
9	,	,	PUNCT	Punct_Comma	_	6	punct	6:punct	LMSeg:,
10	იყავნ	ყოფა	VERB	V_Act_Imp_IV_S:3Sg	Mood=Imp|Number[subj]=Sing|Person[subj]=3|Tense=Pres|VerbForm=Fin	0	root	0:root	LMSeg:ყოფა|Translit=iqavn
11	მის	იგი	PRON	Pron_Dem_Gen_Sg	Case=Gen|Number=Sing|PronType=Dem	10	obl	10:obl	LMSeg:იგი|Translit=mis
12	თანა	თანა	ADP	Post	AdpType=Post|Case=Gen	11	case	11:case	LMSeg:თანა|Translit=tana
13	;	;	PUNCT	Punct_SemiColon	_	19	punct	19:punct	LMSeg:;
14	და	და	CCONJ	Cj_Coord	_	19	cc	19:cc	LMSeg:და|Translit=da
15	ყოველი	ყოველი	ADJ	A_Nom_Sg	Case=Nom|Number=Sing	16	amod	16:amod	LMSeg:ყოველი|Translit=qoveli
16	განმზადებულებაჲ	განმზადებულება	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	19	obj	19:obj	LMSeg:განმზადებულება|Translit=ganmzadebulebay
17	მის	იგი	PRON	Pron_Dem_Gen_Sg	Case=Gen|Number=Sing|PronType=Dem	19	obl	19:obl	LMSeg:იგი|Translit=mis
18	თანა	თანა	ADP	Post	AdpType=Post|Case=Gen	17	case	17:case	LMSeg:თანა|Translit=tana
19	წარიღენ	წარღება	VERB	V_Act_Imp_SV_S:3Sg	Mood=Imp|Number[subj]=Sing|Person[subj]=3|Tense=Pres|VerbForm=Fin	10	conj	10:conj	LMSeg:წარ·ღება|Translit=carigen
20	ადგილსა	ადგილი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	19	obl	19:obl	LMSeg:ადგილ[ი]|Translit=adgilsa
21	მას	იგი	PRON	Pron_Dem_Dat_Sg	Case=Dat|Number=Sing|PronType=Dem	20	det	20:det	LMSeg:იგი|Translit=mas
22	,	,	PUNCT	Punct_Comma	_	26	punct	26:punct	LMSeg:,
23	სადა-იგი	სადა-იგი	ADV	Adv_Rel	PronType=Rel	26	advmod	26:advmod	LMSeg:სადა+იგი|Translit=sada-igi
24	თჳთ	თჳთ	ADV	Adv	_	26	advmod	26:advmod	LMSeg:თჳთ|Translit=twit
25	დამკჳდრებულ	დამკჳდრება	VERB	V_Part_Pv_Abs	Case=Abs|Tense=Past|VerbForm=Part	20	acl:relcl	20:acl:relcl	LMSeg:და·მკჳდრება|Translit=damkwidrebul
26	არს	ყოფა	AUX	V_Act_Pres_S:3Sg	Mood=Ind|Number[subj]=Sing|Person[subj]=3|Tense=Pres|VerbForm=Fin	25	aux	25:aux	LMSeg:ყოფა|Translit=ars
27	.	.	PUNCT	Punct_FullStop	_	19	punct	19:punct	LMSeg:.
28	და	და	CCONJ	Cj_Coord	_	29	cc	29:cc	LMSeg:და|Translit=da
29	თანა-წარიღენ	თანაწარღება	VERB	V_Act_Imp_Pv_IV_S:3Pl	Mood=Imp|Number[subj]=Plur|Person[subj]=3|Tense=Pres|VerbForm=Fin	19	conj	19:conj	LMSeg:თანა·წარ·ღება|Translit=tana-carigen
30	ყოველივე	ყოველივე	PRON	Pron_Ind_Nom_Sg	Case=Nom|Number=Sing|PronType=Ind	31	det	31:det	LMSeg:ყოველივე|Translit=qovelive
31	აღსაგებელი	აღსაგებელი	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	29	obj	29:obj	LMSeg:აღსაგებელი|Translit=agsagebeli
32	თჳსი	თჳსი	PRON	Pron_Poss_3Sg_Nom_Sg	Case=Nom|Number=Sing|Person=3|Poss=Yes|PronType=Prs	31	nmod	31:nmod	LMSeg:თჳსი|Translit=twisi
33	,	,	PUNCT	Punct_Comma	_	35	punct	35:punct	LMSeg:,
34	რომელ-რაჲ	რომელ-რაჲ	PRON	Pron_Rel_Nom_Sg	Case=Nom|Number=Sing|PronType=Rel	35	nsubj	35:nsubj	LMSeg:რომელი+რაჲ|Translit=romel-ray
35	იყოს	ყოფა	VERB	V_Act_Subj_IV_S:3Sg	Mood=Sub|Number[subj]=Sing|Person[subj]=3|Tense=Pres|VerbForm=Fin	31	acl:relcl	31:acl:relcl	LMSeg:ყოფა|Translit=iqos
36	ოქროჲსაჲ	ოქრო	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	35	xcomp	35:xcomp	LMSeg:ოქრო|Translit=okroysay
37	და	და	CCONJ	Cj_Coord	_	38	cc	38:cc	LMSeg:და|Translit=da
38	ვეცხლისაჲ	ვეცხლი	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	36	conj	36:conj	LMSeg:ვეცხლ[ი]|Translit=veclisay
39	.	.	PUNCT	Punct_FullStop	_	35	punct	35:punct	LMSeg:.

# sentence_id = 1_5
# text = და აღდგეს მფლობელნი იგი მამათმთავართაჲ მათ იუდაჲსთაჲ და ბენიამენისთაჲ და მღდელნი იგი და ლევიტელნი და ყოველნივე, რომელთაჲ განაღჳძა უფალმან ღმერთმან სული მათი აღსლვად და აღშჱნებად ტაძრისა მის უფლისა იერუსალემდ.
1	და	და	CCONJ	Cj_Coord	_	2	cc	2:cc	LMSeg:და|Translit=da
2	აღდგეს	აღდგომა	VERB	V_Act_Aor_Pv_S:3Pl	Mood=Ind|Number[subj]=Plur|Person[subj]=3|Tense=Aor|VerbForm=Fin	0	root	0:root	LMSeg:აღ·დგომა|Translit=agdges
3	მფლობელნი	მფლობელი	NOUN	N_Nom_Pl	Case=Nom|Number=Plur	2	nsubj	2:nsubj	LMSeg:მფლობელ[ი]|Translit=mplobelni
4	იგი	იგი	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	3	det	3:det	LMSeg:იგი|Translit=igi
5	მამათმთავართაჲ	მამათმთავარი	NOUN	N_Obl_Pl_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Plur|Number[sauf]=Sing	3	nmod	3:nmod	LMSeg:მამათმთავარ[ი]|Translit=mamatmtavartay
6	მათ	იგი	PRON	Pron_Dem_Obl_Pl	Case=Gen|Number=Plur|PronType=Dem	5	det	5:det	LMSeg:იგი|Translit=mat
7	იუდაჲსთაჲ	იუდა	PROPN	N_Prop_Gen_Sg_Obl_Pl_Nom_Sg	Case=Gen|Case[sauf2]=Nom|Case[sauf]=Gen|Number=Sing|Number[sauf2]=Sing|Number[sauf]=Pl|NameType=Giv	5	nmod	5:nmod	LMSeg:იუდა|Translit=iudaystay
8	და	და	CCONJ	Cj_Coord	_	9	cc	9:cc	LMSeg:და|Translit=da
9	ბენიამენისთაჲ	ბენიამენი	PROPN	N_Prop_Gen_Sg_Obl_Pl_Nom_Sg	Case=Gen|Case[sauf2]=Nom|Case[sauf]=Gen|Number=Sing|Number[sauf2]=Sing|NameType=Giv	7	conj	7:conj	LMSeg:ბენიამენ[ი]|Translit=beniamenistay
10	და	და	CCONJ	Cj_Coord	_	11	cc	11:cc	LMSeg:და|Translit=da
11	მღდელნი	მღდელი	NOUN	N_Nom_Pl	Case=Nom|Number=Plur	3	conj	3:conj	LMSeg:მღდელ[ი]|Translit=mgdelni
12	იგი	იგი	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	11	det	11:det	LMSeg:იგი|Translit=igi
13	და	და	CCONJ	Cj_Coord	_	14	cc	14:cc	LMSeg:და|Translit=da
14	ლევიტელნი	ლევიტელი	NOUN	N_Nom_Pl	Case=Nom|Number=Plur	3	conj	3:conj	LMSeg:ლევიტელ[ი]|Translit=leviṭelni
15	და	და	CCONJ	Cj_Coord	_	16	cc	16:cc	LMSeg:და|Translit=da
16	ყოველნივე	ყოველი	PRON	Pron_Tot_Nom_Pl	Case=Nom|Number=Plur|PronType=Tot	3	conj	3:conj	LMSeg:ყოველი+ვე|Translit=qovelnive
17	,	,	PUNCT	Punct_Comma	_	19	punct	19:punct	LMSeg:,
18	რომელთაჲ	რომელი	PRON	Pron_Rel_Obl_Pl_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Plur|Number[sauf]=Sing|PronType=Rel	22	nmod	22:nmod	LMSeg:რომელ[ი]|Translit=romeltay
19	განაღჳძა	განღჳძება	VERB	V_Act_Aor_Pv_AV_S:3Sg	Mood=Ind|Number[subj]=Sing|Person[subj]=3|Tense=Aor|VerbForm=Fin	16	acl:relcl	16:acl:relcl	LMSeg:გან·ღჳძება|Translit=ganagwiʒa
20	უფალმან	უფალი	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	19	nsubj	19:nsubj	LMSeg:უფალ[ი]|Translit=upalman
21	ღმერთმან	ღმერთი	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	20	appos	20:appos	LMSeg:ღმერთ[ი]|Translit=gmertman
22	სული	სული	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	19	obj	19:obj	LMSeg:სულ[ი]|Translit=suli
23	მათი	მათი	PRON	Pron_Poss_Obl_Pl	Case=Gen|Number=Plur|Poss=Yes|PronType=Prs	22	nmod	22:nmod	LMSeg:მათი|Translit=mati
24	აღსლვად	აღსლვა	NOUN	N_Adv	Case=Adv	19	advcl	19:advcl	LMSeg:აღ·სლვა|Translit=agslvad
25	და	და	CCONJ	Cj_Coord	_	26	cc	26:cc	LMSeg:და|Translit=da
26	აღშჱნებად	აღშჱნება	NOUN	N_Adv	Case=Adv	24	conj	24:conj	LMSeg:აღ·შჱნება|Translit=agšēnebad
27	ტაძრისა	ტაძარი	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	26	obj	26:obj	LMSeg:ტაძარ[ი]|Translit=ṭaʒrisa
28	მის	იგი	PRON	Pron_Dem_Gen_Sg	Case=Gen|Number=Sing|PronType=Dem	27	det	27:det	LMSeg:იგი|Translit=mis
29	უფლისა	უფალი	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	27	nmod	27:nmod	LMSeg:უფალ[ი]|Translit=uplisa
30	იერუსალემდ	იერუსალემი	PROPN	N_Prop_Adv_Sg	Case=All|Number=Sing|NameType=Geo	26	obl	26:obl	LMSeg:იერუსალემ[ი]|Translit=ierusalemd
31	.	.	PUNCT	Punct_FullStop	_	2	punct	2:punct	LMSeg:.ù

# sentence_id = 1_6
# text = და ყოველნი იგი, რომელნი იყვნეს გარემოჲს მათსა, შემწე ეყოფოდეს და განაძლიერებდეს,   ჴელთა მათთა მისცემდეს ოქროსა და ვეცხლსა და ჭურჭერსა და საცხოვარსა და ძღუნითა და შესაწირავითა აღავსებდეს.
1	და	და	CCONJ	Cj_Coord	_	11	cc	11:cc	LMSeg:და|Translit=da
2	ყოველნი	ყოველი	PRON	Pron_Tot_Nom_Pl	Case=Nom|Number=Plur|PronType=Tot	11	nsubj	11:nsubj	LMSeg:ყოველი|Translit=qovelni
3	იგი	იგი	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	2	det	2:det	LMSeg:იგი|Translit=igi
4	,	,	PUNCT	Punct_Comma	_	6	punct	6:punct	LMSeg:,
5	რომელნი	რომელი	PRON	Pron_Rel_Nom_Pl	Case=Nom|Number=Plur|PronType=Rel	6	nsubj	6:nsubj	LMSeg:რომელ[ი]|Translit=romelni
6	იყვნეს	ყოფა	VERB	V_Act_Aor_IV_S:3Pl	Mood=Ind|Number[subj]=Plur|Person[subj]=3|Tense=Aor|VerbForm=Fin	2	acl:relcl	2:acl:relcl	LMSeg:ყოფა|Translit=iqvnes
7	გარემოჲს	გარემო	ADV	Adv	_	6	advmod	6:advmod	LMSeg:გარემო|Translit=garemoys
8	მათსა	მათი	PRON	Pron_Poss_Dat_Sg	Case=Dat|Number=Sing|Poss=Yes|PronType=Prs	7	nmod	7:nmod	LMSeg:მათი|Translit=matsa
9	,	,	PUNCT	Punct_Comma	_	11	punct	11:punct	LMSeg:,
10	შემწე	შემწე	NOUN	N_Abs_Sg	Case=Abs|Number=Sing	11	xcomp	11:xcomp	LMSeg:შემწე|Translit=šemc̣e
11	ეყოფოდეს	ყოფა	VERB	V_Act_Imp_EV_IO:3_S:3Pl	Mood=Ind|Number[subj]=Plur|Person[iobj]=3|Person[subj]=3|Tense=Imp|VerbForm=Fin	0	root	0:root	LMSeg:ყოფა|Translit=eqopodes
12	და	და	CCONJ	Cj_Coord	_	13	cc	13:cc	LMSeg:და|Translit=da
13	განაძლიერებდეს	განძლიერება	VERB	V_Act_Imp_AV_S:3Pl	Mood=Ind|Number[subj]=Plur|Person[subj]=3|Tense=Imp|VerbForm=Fin	11	conj	11:conj	LMSeg:გან·ძლიერება|Translit=ganaʒlierebdes
14	,	,	PUNCT	Punct_Comma	_	17	punct	17:punct	LMSeg:,
15	ჴელთა	ჴელი	NOUN	N_Obl_Pl	Case=Dat|Number=Plur	17	obl	17:obl	LMSeg:ჴელ[ი]|Translit=qelta
16	მათთა	მათი	PRON	Pron_Poss_Obl_Pl	Case=Dat|Number=Plur|Poss=Yes|PronType=Prs	15	nmod	15:nmod	LMSeg:მათი|Translit=matta
17	მისცემდეს	მიცემა	VERB	V_Act_Imp_S:3Pl	Mood=Ind|Number[subj]=Plur|Person[subj]=3|Tense=Imp|VerbForm=Fin	11	conj	11:conj	LMSeg:მი·ცემა|Translit=miscemdes
18	ოქროსა	ოქრო	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	17	obj	17:obj	LMSeg:ოქრო|Translit=okrosa
19	და	და	CCONJ	Cj_Coord	_	20	cc	20:cc	LMSeg:და|Translit=da
20	ვეცხლსა	ვეცხლი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	18	conj	18:conj	LMSeg:ვეცხლ[ი]|Translit=vecxlsa
21	და	და	CCONJ	Cj_Coord	_	22	cc	22:cc	LMSeg:და|Translit=da
22	ჭურჭერსა	ჭურჭერი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	18	conj	18:conj	LMSeg:ჭურჭერ[ი]|Translit=č̣urč̣ersa
23	და	და	CCONJ	Cj_Coord	_	24	cc	24:cc	LMSeg:და|Translit=da
24	საცხოვარსა	საცხოვარი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	18	conj	18:conj	LMSeg:საცხოვარ[ი]|Translit=sacxovarsa
25	და	და	CCONJ	Cj_Coord	_	29	cc	29:cc	LMSeg:და|Translit=da
26	ძღუნითა	ძღუენი	NOUN	N_Ins_Sg	Case=Ins|Number=Sing	29	obl	29:obl	LMSeg:ძღუენ[ი]|Translit=ʒgunita
27	და	და	CCONJ	Cj_Coord	_	28	cc	28:cc	LMSeg:და|Translit=da
28	შესაწირავითა	შესაწირავი	NOUN	N_Ins_Sg	Case=Ins|Number=Sing	26	conj	26:conj	LMSeg:შესაწირავ[ი]|Translit=šesac̣iravita
29	აღავსებდეს	აღვსება	VERB	V_Act_Imp_AV_S:3Pl	Mood=Ind|Number[subj]=Plur|Person[subj]=3|Tense=Imp|VerbForm=Fin	11	conj	11:conj	LMSeg:აღ·ვსება|Translit=agavsebdes|SpaceAfter=No
30	.	.	PUNCT	Punct_FullStop	_	11	punct	11:punct	LMSeg:.

# sentence_id = 1_7
# text = და მეფემან კჳროს მღებად სცა ყოველი იგი სამსახურებელი სახლისა მის უფლისაჲ, რომელ გამოიღო ნაბუქოდონოსორ მეფემან იერუსალემით და მისცა დამარხვად სახლსა ღმრთისა თჳსისასა.
1	და	და	CCONJ	Cj_Coord	_	5	cc	5:cc	LMSeg:და|Translit=da
2	მეფემან	მეფე	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	5	nsubj	5:nsubj	LMSeg:მეფე|Translit=mepeman
3	კჳროს	კჳროს	PROPN	N_Prop	NameType=Giv	2	appos	2:appos	LMSeg:კჳროს|Translit=k̇wiros
4	მღებად	ღება	NOUN	N_Adv	Case=Adv	5	xcomp	5:xcomp	LMSeg:ღება|Translit=mgebad
5	სცა	ცემა	VERB	V_Act_Aor_S:3Sg_IO:3Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=3|Person[subj]=3|Tense=Aor|VerbForm=Fin	0	root	0:root	LMSeg:ცემა|Translit=sca
6	ყოველი	ყოველი	PRON	Pron_Tot_Nom_Sg	Case=Nom|Number=Sing|PronType=Tot	8	det	8:det	LMSeg:ყოველი|Translit=qoveli
7	იგი	იგი	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	8	det	8:det	LMSeg:იგი|Translit=igi
8	სამსახურებელი	სამსახურებელი	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	5	obj	5:obj	LMSeg:სამსახურებელ[ი]|Translit=samsaxurebeli
9	სახლისა	სახლი	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	8	nmod	8:nmod	LMSeg:სახლ[ი]|Translit=saxlisa
10	მის	იგი	PRON	Pron_Dem_Gen_Sg	Case=Gen|Number=Sing|PronType=Dem	9	det	9:det	LMSeg:იგი|Translit=mis
11	უფლისაჲ	უფალი	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	9	nmod	9:nmod	LMSeg:უფალ[ი]|Translit=uplisay
12	რომელ	რომელი	PRON	Pron_Rel_Abs_Sg	Case=Abs|Number=Sing|PronType=Rel	13	obj	13:obj	LMSeg:რომელ[ი]|Translit=romel
13	გამოიღო	გამოღება	VERB	V_Act_Aor_Pv_IV_S:3Sg	Mood=Ind|Number[subj]=Sing|Person[subj]=3|Tense=Aor|VerbForm=Fin	8	acl:relcl	8:acl:relcl	LMSeg:გამო·ღება|Translit=gamoigo
14	ნაბუქოდონოსორ	ნაბუქოდონოსორ	PROPN	N_Prop	NameType=Giv	15	appos	15:appos	LMSeg:ნაბუქოდონოსორ|Translit=nabukodonosor
15	მეფემან	მეფე	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	13	nsubj	13:nsubj	LMSeg:მეფე|Translit=mepeman
16	იერუსალემით	იერუსალემი	PROPN	N_Prop_Ins_Sg	Case=Ins|Number=Sing|NameType=Geo	13	obl	13:obl	LMSeg:იერუსალემ[ი]|Translit=ierusalemit
17	და	და	CCONJ	Cj_Coord	_	18	cc	18:cc	LMSeg:და|Translit=da
18	მისცა	მიცემა	VERB	V_Act_Aor_Pv_S:3Sg_IO:3Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=3|Person[subj]=3|Tense=Aor|VerbForm=Fin	5	conj	5:conj	LMSeg:მი·ცემა|Translit=misca
19	დამარხვად	დამარხვა	NOUN	N_Adv	Case=Adv	18	xcomp	18:xcomp	LMSeg:და·მარხვა|Translit=damarxvad
20	სახლსა	სახლი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	18	obl	18:obl	LMSeg:სახლ[ი]|Translit=saxlsa
21	ღმრთისა	ღმერთი	NOUN	N_Gen_Sg	Case=Gen|Number=Sing	20	nmod	20:nmod	LMSeg:ღმერთ[ი]|Translit=gmrtisa
22	თჳსისასა	თჳსი	PRON	Pron_Poss_Gen_Sg_Dat_Sg	Case=Gen|Case[sauf]=Dat|Number=Sing|Number[sauf]=Sing|Poss=Yes|PronType=Prs	21	nmod	21:nmod	LMSeg:თჳსი|Translit=twisisasa|SpaceAfter=No
23	.	.	PUNCT	Punct_FullStop	_	5	punct	5:punct	LMSeg:.

# sentence_id = 1_8
# text = მოღებად სცა ყოველი იგი კჳროს, მეფემან სპარსთამან, ჴელითა მითრდატ მეფასისაჲთა და მიუთუალა და მისცა სამნასარს, მთავარსა იუდაჲსსა.
1	მოღებად	მოღება	NOUN	N_Adv	Case=Adv	2	xcomp	2:xcomp	LMSeg:მო·ღება|Translit=mogebad
2	სცა	ცემა	VERB	V_Act_Aor_S:3Sg_IO:3Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=3|Person[subj]=3|Tense=Aor|VerbForm=Fin	0	root	0:root	LMSeg:ცემა|Translit=sca
3	ყოველი	ყოველი	PRON	Pron_Tot_Nom_Sg	Case=Nom|Number=Sing|PronType=Tot	4	det	4:det	LMSeg:ყოველი|Translit=qoveli
4	იგი	იგი	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	2	obj	2:obj	LMSeg:იგი|Translit=igi
5	კჳროს	კჳროს	PROPN	N_Prop	NameType=Giv	2	nsubj	2:nsubj	LMSeg:კჳროს|Translit=k̇wiros
6	,	,	PUNCT	Punct_Comma	_	7	punct	7:punct	LMSeg:,
7	მეფემან	მეფე	NOUN	N_Erg_Sg	Case=Erg|Number=Sing	5	appos	5:appos	LMSeg:მეფე|Translit=mepeman
8	სპარსთამან	სპარსი	PROPN	N_Prop_Obl_Pl_Erg_Sg	Case=Gen|Case[sauf]=Erg|Number=Plur|Number[sauf]=Sing|NameType=Nat	7	nmod	7:nmod	LMSeg:სპარს[ი]|Translit=sparstaman
9	,	,	PUNCT	Punct_Comma	_	10	punct	10:punct	LMSeg:,
10	ჴელითა	ჴელი	NOUN	N_Ins_Sg	Case=Ins|Number=Sing	2	obl	2:obl	LMSeg:ჴელ[ი]|Translit=qelita
11	მითრდატ	მითრდატ	PROPN	N_Prop	NameType=Giv	10	nmod	10:nmod	LMSeg:მითრდატ|Translit=mitrdat
12	მეფასისაჲთა	მეფასი	NOUN	N_Gen_Sg_Ins_Sg	Case=Gen|Case[sauf]=Ins|Number=Sing|Number[sauf]=Sing	11	appos	11:appos	LMSeg:მეფასი|Translit=mepasisayta
13	და	და	CCONJ	Cj_Coord	_	14	cc	14:cc	LMSeg:და|Translit=da
14	მიუთუალა	მითუალვა	VERB	V_Act_Aor_Pv_UV_S:3Sg_IO:3Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=3|Person[subj]=3|Tense=Aor|VerbForm=Fin	2	conj	2:conj	LMSeg:მი·თუალვა|Translit=miutuala
15	და	და	CCONJ	Cj_Coord	_	16	cc	16:cc	LMSeg:და|Translit=da
16	მისცა	მიცემა	VERB	V_Act_Aor_Pv_S:3Sg_IO:3Sg	Mood=Ind|Number[iobj]=Sing|Number[subj]=Sing|Person[iobj]=3|Person[subj]=3|Tense=Aor|VerbForm=Fin	2	conj	2:conj	LMSeg:მი·ცემა|Translit=misca
17	სამნასარს	სამნასარ	PROPN	N_Prop_Dat_Sg	Case=Dat|Number=Sing|NameType=Giv	16	iobj	16:iobj	LMSeg:სამნასარ|Translit=samnasars
18	,	,	PUNCT	Punct_Comma	_	19	punct	19:punct	LMSeg:,
19	მთავარსა	მთავარი	NOUN	N_Dat_Sg	Case=Dat|Number=Sing	17	appos	17:appos	LMSeg:მთავარ[ი]|Translit=mtavarsa
20	იუდაჲსსა	იუდა	PROPN	N_Prop_Gen_Sg_Dat_Sg	Case=Gen|Case[sauf]=Dat|Number=Sing|Number[sauf]=Sing|NameType=Giv	19	nmod	19:nmod	LMSeg:იუდა|Translit=iudayssa|SpaceAfter=No
21	.	.	PUNCT	Punct_FullStop	_	2	punct	2:punct	LMSeg:.

# sentence_id = 1_9
# text = და ესე არს რიცხჳ აღთუალვისაჲ მის: საზორველნი იგი ოქროჲსანი ოცდაათ და საზორველნი სამსახურებელთა მათ ვეცხლისათანი ათას ოცდაცხრა
1	და	და	CCONJ	Cj_Coord	_	3	cc	3:cc	LMSeg:და|Translit=da
2	ესე	ესე	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	3	nsubj	3:nsubj	LMSeg:ესე|Translit=ese
3	არს	ყოფა	VERB	V_Act_Pres_S:3Sg	Mood=Ind|Number[subj]=Sing|Person[subj]=3|Tense=Pres|VerbForm=Fin	0	root	0:root	LMSeg:ყოფა|Translit=ars
4	რიცხჳ	რიცხჳ	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	3	xcomp	3:xcomp	LMSeg:რიცხჳ|Translit=ricxwi
5	აღთუალვისაჲ	აღთუალვა	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	4	nmod	4:nmod	LMSeg:აღ·თუალვა|Translit=agtualvisay
6	მის	იგი	PRON	Pron_Dem_Gen_Sg	Case=Gen|Number=Sing|PronType=Dem	5	det	5:det	LMSeg:იგი|Translit=mis
7	:	:	PUNCT	Punct_Colon	_	8	punct	8:punct	LMSeg::
8	საზორველნი	საზორველი	NOUN	N_Nom_Pl	Case=Nom|Number=Plur	4	appos	4:appos	LMSeg:საზორველ[ი]|Translit=sazorvelni
9	იგი	იგი	PRON	Pron_Dem_Nom_Sg	Case=Nom|Number=Sing|PronType=Dem	8	det	8:det	LMSeg:იგი|Translit=igi
10	ოქროჲსანი	ოქრო	NOUN	N_Gen_Sg_Nom_Pl	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Plur	8	nmod	8:nmod	LMSeg:ოქრო|Translit=okroysani
11	ოცდაათ	ოცდაათი	NUM	Num_Nom	Case=Nom|NumType=Card	8	nummod	8:nummod	LMSeg:ოცდაათ[ი]|Translit=ocdaat
12	და	და	CCONJ	Cj_Coord	_	13	cc	13:cc	LMSeg:და|Translit=da
13	საზორველნი	საზორველი	NOUN	N_Nom_Pl	Case=Nom|Number=Plur	8	conj	8:conj	LMSeg:საზორველ[ი]|Translit=sazorvelni
14	სამსახურებელთა	სამსახურებელი	NOUN	N_Obl_Pl	Case=Gen|Number=Plur	13	nmod	13:nmod	LMSeg:სამსახურებელ[ი]|Translit=samsaxurebelta
15	მათ	იგი	PRON	Pron_Dem_Obl_Pl	Case=Gen|Number=Plur|PronType=Dem	14	det	14:det	LMSeg:იგი|Translit=mat
16	ვეცხლისათანი	ვეცხლი	NOUN	N_Gen_Sg_Nom_Pl	Case=Gen|Case[sauf]=Gen|Case[sauf2]=Nom|Number=Sing|Number[sauf]=Plur|Number[sauf2]=Plur	13	nmod	13:nmod	LMSeg:ვეცხლ[ი]|Translit=vecxlisatani
17	ათას	ათასი	NUM	Num_Abs	Case=Abs|NumType=Card	13	nummod	13:nummod	LMSeg:ათას[ი]|Translit=atas
18	ოცდაცხრა	ოცდაცხრა	NUM	Num_Abs	Case=Abs|NumType=Card	17	compound	17:compound	LMSeg:ოცდაცხრა|Translit=ocdacxra


# sentence_id = 1_10
# text = და პინაკები ოქროჲსაჲ ოცდაათ და ვეცხლისანი მერმე ათას.
1	და	და	CCONJ	Cj_Coord	_	2	cc	2:cc	LMSeg:და|Translit=da
2	პინაკები	პინაკი	NOUN	N_Nom_Pl	Case=Nom|Number=Plur	0	root	0:root	LMSeg:პინაკ[ი]|Translit=pinak̇ebi
3	ოქროჲსაჲ	ოქრო	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	2	nmod	2:nmod	LMSeg:ოქრო|Translit=okroysay
4	ოცდაათ	ოცდაათი	NUM	Num_Abs	Case=Abs|NumType=Card	2	nummod	2:nummod	LMSeg:ოცდაათ[ი]|Translit=ocdaat
5	და	და	CCONJ	Cj_Coord	_	6	cc	6:cc	LMSeg:და|Translit=da
6	ვეცხლისანი	ვეცხლი	NOUN	N_Gen_Sg_Nom_Pl	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Plur	2	conj	2:conj	LMSeg:ვეცხლ[ი]|Translit=vecxlisani
7	მერმე	მერმე	ADV	Adv	_	6	advmod	6:advmod	LMSeg:მერმე|Translit=merme
8	ათას	ათასი	NUM	Num_Abs	Case=Abs|NumType=Card	6	nummod	6:nummod	LMSeg:ათას[ი]|Translit=atas|SpaceAfter=No
9	.	.	PUNCT	Punct_FullStop	_	2	punct	2:punct	LMSeg:.


# sentence_id = 1_11
# text = და ყოველი ჭურჭერი ოქროჲსაჲ და ვეცხლსაჲ ხუთ ათას ოთხას ყოვლითურთ, რომელნი გამოვიდოდეს სამნასარის თანა ბაბილონით იერუსალემდ.
1	და	და	CCONJ	Cj_Coord	_	3	cc	3:cc	LMSeg:და|Translit=da
2	ყოველი	ყოველი	PRON	Pron_Tot_Nom_Sg	Case=Nom|Number=Sing|PronType=Tot	3	det	3:det	LMSeg:ყოველი|Translit=qoveli
3	ჭურჭერი	ჭურჭერი	NOUN	N_Nom_Sg	Case=Nom|Number=Sing	0	root	0:root	LMSeg:ჭურჭერ[ი]|Translit=č̣urč̣eri
4	ოქროჲსაჲ	ოქრო	NOUN	N_Gen_Sg_Nom_Sg	Case=Gen|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	3	nmod	3:nmod	LMSeg:ოქრო|Translit=okroysay
5	და	და	CCONJ	Cj_Coord	_	6	cc	6:cc	LMSeg:და|Translit=da
6	ვეცხლსაჲ	ვეცხლი	NOUN	N_Dat_Sg_Nom_Sg	Case=Dat|Case[sauf]=Nom|Number=Sing|Number[sauf]=Sing	4	conj	4:conj	LMSeg:ვეცხლ[ი]|Translit=vecxlsay
7	ხუთ	ხუთი	NUM	Num_Nom	Case=Nom|NumType=Card	8	nummod	8:nummod	LMSeg:ხუთ[ი]|Translit=xut
8	ათას	ათასი	NUM	Num_Nom	Case=Nom|NumType=Card	3	nummod	3:nummod	LMSeg:ათას[ი]|Translit=atas
9	ოთხას	ოთხასი	NUM	Num_Nom	Case=Nom|NumType=Card	8	compound	8:compound	LMSeg:ოთხას[ი]|Translit=otxas
10	ყოვლითურთ	ყოვლითურთ	ADV	Adv	_	3	advmod	3:advmod	LMSeg:ყოვლითურთ|Translit=qovliturt
11	,	,	PUNCT	Punct_Comma	_	13	punct	13:punct	LMSeg:,
12	რომელნი	რომელი	PRON	Pron_Rel_Nom_Pl	Case=Nom|Number=Plur|PronType=Rel	13	nsubj	13:nsubj	LMSeg:რომელ[ი]|Translit=romelni
13	გამოვიდოდეს	გამოსლვა	VERB	V_Act_Imp_Pv_S:3Pl	Mood=Ind|Number[subj]=Plur|Person[subj]=3|Tense=Imp|VerbForm=Fin	3	acl:relcl	3:acl:relcl	LMSeg:გამო·სლვა|Translit=gamovidodes
14	სამნასარის	სამნასარ	PROPN	N_Prop_Gen_Sg	Case=Gen|Number=Sing|NameType=Giv	13	obl	13:obl	LMSeg:სამნასარ[ი]|Translit=samnasaris
15	თანა	თანა	ADP	Post	AdpType=Post|Case=Gen	14	case	14:case	LMSeg:თანა|Translit=tana
16	ბაბილონით	ბაბილონი	PROPN	N_Prop_Ins_Sg	Case=Ins|Number=Sing|NameType=Geo	13	obl	13:obl	LMSeg:ბაბილონ[ი]|Translit=babilonit
17	იერუსალემდ	იერუსალემი	PROPN	N_Prop_Adv_Sg	Case=All|Number=Sing|NameType=Geo	13	obl	13:obl	LMSeg:იერუსალემ[ი]|Translit=ierusalemd
18	.	.	PUNCT	Punct_FullStop	_	3	punct	3:punct	LMSeg:.
```
