---
username: VYU2635
password: KintoCore2021!
qa: https://kinto-qa.taf.co.id/
uat: https://kinto-uat.taf.co.id/lms/Pages/Login
---

Bug
Agreement asset view
- [ ] agreement asset card tab
- [ ] financial data tab
Agreement application view
- [ ] asset tab

#### log
05/27 start analyse database for print customer
done print customer pull requested at 15.58
done found out it prod at 16.33

#### Print agreement card
```
Error Generating ReportAGR_AST_CARD: Exception has been thrown by the target of an invocation. => Invalid object name 'FOUNDATION_OPL_SIT_CAMUNDA.dbo.REF_OFFICE'.
```
#### Analyse print customer
API generate PDF https://kinto-uat.taf.co.id/api/fou/v1/Report/GenerateReportR3
```
Error Generating ReportCUST_CARD: Exception has been thrown by the target of an invocation. => Failed to enable constraints. One or more rows contain values violating non-null, unique, or foreign-key constraints.
```

#### tafo 520
https://kinto-qa.taf.co.id/api/fou/v1/RefMaster/GetListKeyValueActiveByCode


#### Agrmnt view
##### agrmnt asset card tab
`IncreaseMileageX/CalculateOldDataByAgrmntAssetId`
`IncreaseMillageXController.cs`
a200716d58062155da13fd8f8d0f0ce0d8d25569
Christian Then
title: make new api submit request increase mileage

`v1/ReplacementCarX/GetAgrmntAssetOplByAgrmntAssetId`
`ReplacementCarXController.cs`
d09967d2fafb5d1d1b5b796c37aade1034a513bc
Raphael
title: TAFO_520 Raphael BugLog 178

##### agrmnt asset/financial tab

`AgrmntAsset/GetAgrmntAssetFinOplByAgrmntAssetId`
Core
d0eabc876cdfdd6bfdcdba3562d93e038413bd12
AgrmntAssetViewController.cs
Samsudin
title : Branched from $/LMS/ADINS_LMS


`AgrmntAsset/GetListAgrmntAssetFeeByAgrmntAssetId`
6a132ac62364a40de3462ae76b6b2a957dbd9b65
AgrmntAssetViewController.cs
Raphael
title : TAFO-520. Raphael AgrmntAssetFee Controller Function

`AgrmntAsset/GetAgrmntAssetOthExpenseOplByAgrmntAssetId`
d09967d2fafb5d1d1b5b796c37aade1034a513bc
AgrmntAssetViewController.cs
Raphael
title : TAFO_520 Raphael BugLog 178

#### Exploring inside of code
##### CalculateOldDataByAgrmntAssetId
```cs
AMENDMENT_TYPE_INCREASE_MILEAGE
AMENDMENT_TYPE_REPLACEMENT_CAR

public async Task<JsonResult> CalculateOldDataByAgrmntAssetId(ReqByListId req){
    List<ResIncreaseMileageObj> data = await iIncreaseMileageTrObService.CalculateOldDataByAgrmntAssetId(req.ListId);
    AmendmenFeeRuleObj amdFee = await iAmendmentTrObService.GetAmendmentFeeRuleObjByAmendmentTypeAndCurrCode(LMSXCommonConstant.AMENDMENT_TYPE_REPLACEMENT_CAR, "IDR");
    ResListIncreaseMileageObj res = new ResListIncreaseMileageObj();
    res.IncreaseMileageObjs = data;
    res.AdminFee = amdFee.AdminFeeAmt;
    return new JsonResult(res);
}

//AdIns.LMS.BusinessService.X\TransactionObjectService\IncreaseMillageTrObService.cs
public virtual async Task<List<ResIncreaseMileageObj>> CalculateOldDataByAgrmntAssetId(List<long> agrmntAssetId)
```
