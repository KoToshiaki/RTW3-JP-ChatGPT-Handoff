# 98_unsafe_items — UNSAFE判定Items（翻訳禁止）

項目数: 22

文字列そのものがステータステーブル・役割テーブル・セーブキー名として1.00.59平文CODEに独立リテラルで実在。翻訳禁止。

---

## TDLGFILTER/cbStatusFilter/Text

- Stable ID: TDLGFILTER/cbStatusFilter/Text
- Component: cbStatusFilter
- Property: Text
- English: All
- Group: FILTER
- Dispatch: TComboBox Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル5件（文脈: [ansistring] ...try...........Ignore..........||.........NoToAll.........YesToAl）
- Reason: 独立ANSISTRING5件（艦種/汎用パーサクラスタ 'CVL'/'Any'/'Warning! Illegal ship type:' 等で比較利用の実在を確認済み）（Textは同コンボItemsと一括判定） / cbStatusFilterはStyle未指定（既定=編集可能）かつ旧新DFM不一致のため旧CODE証拠の転用も不完全

## TDLGFILTER/cbStatusFilter/Items.Strings[0]

- Stable ID: TDLGFILTER/cbStatusFilter/Items.Strings[0]
- Component: cbStatusFilter
- Property: Items.Strings[0]
- English: All
- Group: FILTER
- Dispatch: TComboBox Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル5件（文脈: [ansistring] ...try...........Ignore..........||.........NoToAll.........YesToAl）
- Reason: 独立ANSISTRING5件（艦種/汎用パーサクラスタ 'CVL'/'Any'/'Warning! Illegal ship type:' 等で比較利用の実在を確認済み） / cbStatusFilterはStyle未指定（既定=編集可能）かつ旧新DFM不一致のため旧CODE証拠の転用も不完全

## TDLGFILTER/cbStatusFilter/Items.Strings[1]

- Stable ID: TDLGFILTER/cbStatusFilter/Items.Strings[1]
- Component: cbStatusFilter
- Property: Items.Strings[1]
- English: Active
- Group: FILTER
- Dispatch: TComboBox Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル7件（文脈: [short] ...TabIndex.Integer..Rect.TRect..||.Boolean..x.F...TTabGetImageEvent....）
- Reason: 独立ANSISTRING5件 — 'Fate'/'Training'/'Deployed' と並ぶ艦ステータス文字列クラスタ / cbStatusFilterはStyle未指定（既定=編集可能）かつ旧新DFM不一致のため旧CODE証拠の転用も不完全

## TDLGFILTER/cbStatusFilter/Items.Strings[2]

- Stable ID: TDLGFILTER/cbStatusFilter/Items.Strings[2]
- Component: cbStatusFilter
- Property: Items.Strings[2]
- English: Reserve
- Group: FILTER
- Dispatch: TComboBox Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル1件（文脈: [ansistring] ......... *........../...........||......... (..........)...SV.....）
- Reason: 独立ANSISTRING1件 + ステータス表示テーブル 'Reserve fleet' と同族 / cbStatusFilterはStyle未指定（既定=編集可能）かつ旧新DFM不一致のため旧CODE証拠の転用も不完全

## TDLGFILTER/cbStatusFilter/Items.Strings[3]

- Stable ID: TDLGFILTER/cbStatusFilter/Items.Strings[3]
- Component: cbStatusFilter
- Property: Items.Strings[3]
- English: Mothballed
- Group: FILTER
- Dispatch: TComboBox Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル1件（文脈: [ansistring] .........Reserve fleet...........||..........Trade protection......）
- Reason: 独立ANSISTRING1件 — 'Reserve fleet'/'Trade protection'/'On foreign station' と連続する艦ステータステーブルの一員 / cbStatusFilterはStyle未指定（既定=編集可能）かつ旧新DFM不一致のため旧CODE証拠の転用も不完全

## TDLGFILTER/cbStatusFilter/Items.Strings[4]

- Stable ID: TDLGFILTER/cbStatusFilter/Items.Strings[4]
- Component: cbStatusFilter
- Property: Items.Strings[4]
- English: Trade protection
- Group: FILTER
- Dispatch: TComboBox Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル1件（文脈: [ansistring] .............Mothballed..........||............On foreign station..）
- Reason: 独立ANSISTRING1件 — 同上ステータステーブルの一員 / cbStatusFilterはStyle未指定（既定=編集可能）かつ旧新DFM不一致のため旧CODE証拠の転用も不完全

## TDLGCAMPDIVROLE/cbRole/Items.Strings[0]

- Stable ID: TDLGCAMPDIVROLE/cbRole/Items.Strings[0]
- Component: cbRole
- Property: Items.Strings[0]
- English: Screen
- Group: CAMPDIVROLE
- Dispatch: TComboBox Style=csDropDownList ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル5件（文脈: [ansistring] ...ndent.........Scout...........||..........Support.........Core..）
- Reason: 独立ANSISTRING5件 — 'Independent'/'Scout'/'Support'/'Core'/'Patrol'/'Fleet Flag' の戦隊役割名テーブル。DR調査で確認済みの役割シリアライズキー群（'Role'/'LeadDiv'）と整合し、役割は文字列として保存・比較される蓋然性が高い

## TDLGCAMPDIVROLE/cbRole/Items.Strings[1]

- Stable ID: TDLGCAMPDIVROLE/cbRole/Items.Strings[1]
- Component: cbRole
- Property: Items.Strings[1]
- English: Support
- Group: CAMPDIVROLE
- Dispatch: TComboBox Style=csDropDownList ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル4件（文脈: [ansistring] ...l.........Support ............||.........Invasion ...........Inv）
- Reason: 同上（独立ANSISTRING4件）

## TDLGCAMPDIVROLE/cbRole/Items.Strings[2]

- Stable ID: TDLGCAMPDIVROLE/cbRole/Items.Strings[2]
- Component: cbRole
- Property: Items.Strings[2]
- English: Core
- Group: CAMPDIVROLE
- Dispatch: TComboBox Style=csDropDownList ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル3件（文脈: [ansistring] ...reen..........Support.........||............Fleet Flag..........）
- Reason: 同上（独立ANSISTRING3件）

## TDLGPICKFORCE/rgDayNight/Items.Strings[0]

- Stable ID: TDLGPICKFORCE/rgDayNight/Items.Strings[0]
- Component: rgDayNight
- Property: Items.Strings[0]
- English: Day
- Group: PICKFORCE
- Dispatch: TRadioGroup Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル6件（文脈: [ansistring] ..... ...........%d%m%E..........||.........Night...........Twiligh）
- Reason: 独立ANSISTRING6件 — 'SeaState'/'Year'/'Month'/'Hour' と並ぶシナリオ/セーブのキー名として実在

## TDLGPICKFORCE/rgDayNight/Items.Strings[1]

- Stable ID: TDLGPICKFORCE/rgDayNight/Items.Strings[1]
- Component: rgDayNight
- Property: Items.Strings[1]
- English: Night
- Group: PICKFORCE
- Dispatch: TRadioGroup Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル1件（文脈: [ansistring] .....%d%m%E..........Day.........||...........Twilight............L）
- Reason: 独立ANSISTRING1件 — 'Day'/'Twilight' の時間帯表示テーブル

## TDLGPICKFORCE/rgWeather/Items.Strings[0]

- Stable ID: TDLGPICKFORCE/rgWeather/Items.Strings[0]
- Component: rgWeather
- Property: Items.Strings[0]
- English: Good
- Group: PICKFORCE
- Dispatch: TRadioGroup Style=(default) ItemIndex=0 events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル3件（文脈: [ansistring] ...or............Fair............||............Elite...U.....SVW3..）
- Reason: 独立ANSISTRING3件 — 'Poor'/'Fair'/'Average'/'Veteran' 等の品質テーブルと同名

## TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[0]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[0]
- Component: rgPriority1
- Property: Items.Strings[0]
- English: Speed
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル14件（文脈: [ansistring] ...ame...........Course..........||...........Side............Forma）
- Reason: 独立ANSISTRING14件 — 'Course'/'Side'/'Formation' と並ぶ艦シリアライズキー名と完全一致

## TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[2]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[2]
- Component: rgPriority1
- Property: Items.Strings[2]
- English: Range
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル6件（文脈: [short] ...ionT.@.....8.D.L.D............||..@........................SmoothT.@.）
- Reason: 独立ANSISTRING5件+Short1件 — セーブキー名クラスタと一致

## TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[4]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[4]
- Component: rgPriority1
- Property: Items.Strings[4]
- English: Firepower
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル2件（文脈: [ansistring] .........HvyEndurance............||...........Maneuver............T）
- Reason: 独立ANSISTRING2件 — 'Maneuver'/'Toughness' と並ぶ機体ステータスキー名と一致

## TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[5]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[5]
- Component: rgPriority1
- Property: Items.Strings[5]
- English: Toughness
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル2件（文脈: [ansistring] .............Maneuver............||...........Reliability.........L）
- Reason: 独立ANSISTRING2件 — 同上キー名と一致

## TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[6]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority1/Items.Strings[6]
- Component: rgPriority1
- Property: Items.Strings[6]
- English: Reliability
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル3件（文脈: [ansistring] ...._^[..]...........-...........||.........Location............Sta）
- Reason: 独立ANSISTRING3件 — 同上キー名と一致

## TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[0]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[0]
- Component: rgPriority2
- Property: Items.Strings[0]
- English: Speed
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル14件（文脈: [ansistring] ...ame...........Course..........||...........Side............Forma）
- Reason: 独立ANSISTRING14件 — 'Course'/'Side'/'Formation' と並ぶ艦シリアライズキー名と完全一致

## TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[2]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[2]
- Component: rgPriority2
- Property: Items.Strings[2]
- English: Range
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル6件（文脈: [short] ...ionT.@.....8.D.L.D............||..@........................SmoothT.@.）
- Reason: 独立ANSISTRING5件+Short1件 — セーブキー名クラスタと一致

## TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[4]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[4]
- Component: rgPriority2
- Property: Items.Strings[4]
- English: Firepower
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル2件（文脈: [ansistring] .........HvyEndurance............||...........Maneuver............T）
- Reason: 独立ANSISTRING2件 — 'Maneuver'/'Toughness' と並ぶ機体ステータスキー名と一致

## TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[5]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[5]
- Component: rgPriority2
- Property: Items.Strings[5]
- English: Toughness
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル2件（文脈: [ansistring] .............Maneuver............||...........Reliability.........L）
- Reason: 独立ANSISTRING2件 — 同上キー名と一致

## TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[6]

- Stable ID: TDLGAIRCRAFTREQUEST/rgPriority2/Items.Strings[6]
- Component: rgPriority2
- Property: Items.Strings[6]
- English: Reliability
- Group: AIRCRAFTREQUEST
- Dispatch: TRadioGroup Style=(default) ItemIndex=None events=なし
- Classification: UNSAFE_STRING_SEMANTICS
- Evidence: 独立リテラル3件（文脈: [ansistring] ...._^[..]...........-...........||.........Location............Sta）
- Reason: 独立ANSISTRING3件 — 同上キー名と一致

