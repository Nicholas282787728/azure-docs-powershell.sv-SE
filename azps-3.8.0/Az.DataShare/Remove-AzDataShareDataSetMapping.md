---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 3e28b55a77ffb5f8d4ba95743e897628948d15f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090596"
---
# <span data-ttu-id="3f222-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3f222-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="3f222-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f222-102">SYNOPSIS</span></span>
<span data-ttu-id="3f222-103">Tar bort en data uppsättnings mappning</span><span class="sxs-lookup"><span data-stu-id="3f222-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="3f222-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f222-104">SYNTAX</span></span>

### <span data-ttu-id="3f222-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3f222-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f222-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f222-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f222-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f222-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f222-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f222-108">DESCRIPTION</span></span>
<span data-ttu-id="3f222-109">Cmdleten **Remove-AzDataShareDataSetMapping** tar bort en data uppsättnings mappningar.</span><span class="sxs-lookup"><span data-stu-id="3f222-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="3f222-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f222-110">EXAMPLES</span></span>

### <span data-ttu-id="3f222-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f222-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3f222-112">De här kommandona tar bort den dataset som heter DSM från sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="3f222-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="3f222-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f222-113">PARAMETERS</span></span>

### <span data-ttu-id="3f222-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f222-114">-AccountName</span></span>
<span data-ttu-id="3f222-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="3f222-115">Azure data share account name</span></span>

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

### <span data-ttu-id="3f222-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f222-116">-DefaultProfile</span></span>
<span data-ttu-id="3f222-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f222-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f222-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f222-118">-InputObject</span></span>
<span data-ttu-id="3f222-119">Mappnings objekt för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="3f222-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f222-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f222-120">-Name</span></span>
<span data-ttu-id="3f222-121">Mappnings namn för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="3f222-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="3f222-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f222-122">-PassThru</span></span>
<span data-ttu-id="3f222-123">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="3f222-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="3f222-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f222-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f222-125">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="3f222-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3f222-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f222-126">-ResourceId</span></span>
<span data-ttu-id="3f222-127">Resurs-ID för Azure Data uppsättnings mappning</span><span class="sxs-lookup"><span data-stu-id="3f222-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="3f222-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f222-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="3f222-129">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="3f222-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3f222-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f222-130">-Confirm</span></span>
<span data-ttu-id="3f222-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f222-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f222-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f222-132">-WhatIf</span></span>
<span data-ttu-id="3f222-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f222-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f222-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f222-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f222-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f222-135">CommonParameters</span></span>
<span data-ttu-id="3f222-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f222-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f222-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f222-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f222-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f222-138">INPUTS</span></span>

### <span data-ttu-id="3f222-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3f222-139">System.String</span></span>

### <span data-ttu-id="3f222-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3f222-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="3f222-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f222-141">OUTPUTS</span></span>

### <span data-ttu-id="3f222-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f222-142">System.Boolean</span></span>

## <span data-ttu-id="3f222-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f222-143">NOTES</span></span>

## <span data-ttu-id="3f222-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f222-144">RELATED LINKS</span></span>
