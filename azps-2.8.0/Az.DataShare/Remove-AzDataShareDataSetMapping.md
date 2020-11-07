---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 249f166bcf4dd61d9b8da7cf4d67a2ac20f705ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744418"
---
# <span data-ttu-id="4c848-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="4c848-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="4c848-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c848-102">SYNOPSIS</span></span>
<span data-ttu-id="4c848-103">Tar bort en data uppsättnings mappning</span><span class="sxs-lookup"><span data-stu-id="4c848-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="4c848-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c848-104">SYNTAX</span></span>

### <span data-ttu-id="4c848-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4c848-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c848-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c848-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c848-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c848-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c848-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c848-108">DESCRIPTION</span></span>
<span data-ttu-id="4c848-109">Cmdleten **Remove-AzDataShareDataSetMapping** tar bort en data uppsättnings mappningar.</span><span class="sxs-lookup"><span data-stu-id="4c848-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="4c848-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c848-110">EXAMPLES</span></span>

### <span data-ttu-id="4c848-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4c848-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4c848-112">De här kommandona tar bort den dataset som heter DSM från sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="4c848-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="4c848-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c848-113">PARAMETERS</span></span>

### <span data-ttu-id="4c848-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4c848-114">-AccountName</span></span>
<span data-ttu-id="4c848-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="4c848-115">Azure data share account name</span></span>

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

### <span data-ttu-id="4c848-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c848-116">-DefaultProfile</span></span>
<span data-ttu-id="4c848-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c848-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c848-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c848-118">-InputObject</span></span>
<span data-ttu-id="4c848-119">Mappnings objekt för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="4c848-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="4c848-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c848-120">-Name</span></span>
<span data-ttu-id="4c848-121">Mappnings namn för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="4c848-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="4c848-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c848-122">-PassThru</span></span>
<span data-ttu-id="4c848-123">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="4c848-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="4c848-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c848-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c848-125">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="4c848-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4c848-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c848-126">-ResourceId</span></span>
<span data-ttu-id="4c848-127">Resurs-ID för Azure Data uppsättnings mappning</span><span class="sxs-lookup"><span data-stu-id="4c848-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="4c848-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4c848-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="4c848-129">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="4c848-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4c848-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c848-130">-Confirm</span></span>
<span data-ttu-id="4c848-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c848-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c848-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c848-132">-WhatIf</span></span>
<span data-ttu-id="4c848-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c848-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c848-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c848-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c848-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c848-135">CommonParameters</span></span>
<span data-ttu-id="4c848-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c848-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c848-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c848-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c848-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c848-138">INPUTS</span></span>

### <span data-ttu-id="4c848-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4c848-139">System.String</span></span>

### <span data-ttu-id="4c848-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="4c848-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="4c848-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c848-141">OUTPUTS</span></span>

### <span data-ttu-id="4c848-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c848-142">System.Boolean</span></span>

## <span data-ttu-id="4c848-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c848-143">NOTES</span></span>

## <span data-ttu-id="4c848-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c848-144">RELATED LINKS</span></span>
