---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: dc80b30e02901aaa56185270cb775d7b9ea1f106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092148"
---
# <span data-ttu-id="34451-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="34451-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="34451-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34451-102">SYNOPSIS</span></span>
<span data-ttu-id="34451-103">tar bort en utlösare</span><span class="sxs-lookup"><span data-stu-id="34451-103">removes a trigger</span></span>

## <span data-ttu-id="34451-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34451-104">SYNTAX</span></span>

### <span data-ttu-id="34451-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="34451-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34451-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34451-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34451-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34451-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34451-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34451-108">DESCRIPTION</span></span>
<span data-ttu-id="34451-109">Cmdleten **Remove-AzDataShareTrigger** tar bort en datashare-utlösare</span><span class="sxs-lookup"><span data-stu-id="34451-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="34451-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34451-110">EXAMPLES</span></span>

### <span data-ttu-id="34451-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34451-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="34451-112">De här kommandona tar bort en trigger som heter AdsTrigger från AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="34451-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="34451-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34451-113">PARAMETERS</span></span>

### <span data-ttu-id="34451-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34451-114">-AccountName</span></span>
<span data-ttu-id="34451-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="34451-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34451-116">-AsJob</span></span>
<span data-ttu-id="34451-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="34451-117">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34451-118">-DefaultProfile</span></span>
<span data-ttu-id="34451-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34451-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34451-120">-InputObject</span></span>
<span data-ttu-id="34451-121">Azure Data Share trigger-objekt</span><span class="sxs-lookup"><span data-stu-id="34451-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34451-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="34451-122">-Name</span></span>
<span data-ttu-id="34451-123">Namn på Azure Data Share-avtryckare</span><span class="sxs-lookup"><span data-stu-id="34451-123">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34451-124">-PassThru</span></span>
<span data-ttu-id="34451-125">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="34451-125">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34451-126">-ResourceGroupName</span></span>
<span data-ttu-id="34451-127">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="34451-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34451-128">-ResourceId</span></span>
<span data-ttu-id="34451-129">Resurs-ID för Azure Data Share trigger</span><span class="sxs-lookup"><span data-stu-id="34451-129">The resource id of azure data share trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34451-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="34451-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="34451-131">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="34451-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34451-132">-Confirm</span></span>
<span data-ttu-id="34451-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34451-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34451-134">-WhatIf</span></span>
<span data-ttu-id="34451-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34451-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34451-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34451-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34451-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34451-137">CommonParameters</span></span>
<span data-ttu-id="34451-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34451-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34451-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34451-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34451-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34451-140">INPUTS</span></span>

### <span data-ttu-id="34451-141">System. String</span><span class="sxs-lookup"><span data-stu-id="34451-141">System.String</span></span>

### <span data-ttu-id="34451-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="34451-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="34451-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34451-143">OUTPUTS</span></span>

### <span data-ttu-id="34451-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34451-144">System.Boolean</span></span>

## <span data-ttu-id="34451-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34451-145">NOTES</span></span>

## <span data-ttu-id="34451-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34451-146">RELATED LINKS</span></span>
