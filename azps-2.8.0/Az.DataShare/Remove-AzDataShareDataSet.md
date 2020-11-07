---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 122d5118761e3a4b7a400b4bc73daa29d218c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744422"
---
# <span data-ttu-id="1f8fb-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="1f8fb-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="1f8fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8fb-103">Tar bort en data uppsättnings mappning</span><span class="sxs-lookup"><span data-stu-id="1f8fb-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="1f8fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f8fb-104">SYNTAX</span></span>

### <span data-ttu-id="1f8fb-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1f8fb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f8fb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f8fb-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f8fb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f8fb-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f8fb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f8fb-108">DESCRIPTION</span></span>
<span data-ttu-id="1f8fb-109">Cmdleten **Remove-AzDataShareDataSet** tar bort en data mängd.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="1f8fb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f8fb-110">EXAMPLES</span></span>

### <span data-ttu-id="1f8fb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f8fb-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="1f8fb-112">De här kommandona tar bort den dataset som heter DS från Share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="1f8fb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f8fb-113">PARAMETERS</span></span>

### <span data-ttu-id="1f8fb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1f8fb-114">-AccountName</span></span>
<span data-ttu-id="1f8fb-115">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="1f8fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8fb-116">-DefaultProfile</span></span>
<span data-ttu-id="1f8fb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f8fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f8fb-118">-InputObject</span></span>
<span data-ttu-id="1f8fb-119">Ett Azure Data Set-objekt.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8fb-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f8fb-120">-Name</span></span>
<span data-ttu-id="1f8fb-121">Namn på Azure Data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8fb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f8fb-122">-PassThru</span></span>
<span data-ttu-id="1f8fb-123">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="1f8fb-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="1f8fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f8fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f8fb-125">Resurs grupp namnet för Azure Data Share-kontot.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="1f8fb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f8fb-126">-ResourceId</span></span>
<span data-ttu-id="1f8fb-127">Resurs-ID för Azure-datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="1f8fb-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1f8fb-128">-ShareName</span></span>
<span data-ttu-id="1f8fb-129">Azure Data Share-namn.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-129">Azure data share name.</span></span>

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

### <span data-ttu-id="1f8fb-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f8fb-130">-Confirm</span></span>
<span data-ttu-id="1f8fb-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f8fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f8fb-132">-WhatIf</span></span>
<span data-ttu-id="1f8fb-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f8fb-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f8fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8fb-135">CommonParameters</span></span>
<span data-ttu-id="1f8fb-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8fb-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f8fb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8fb-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f8fb-138">INPUTS</span></span>

### <span data-ttu-id="1f8fb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1f8fb-139">System.String</span></span>

### <span data-ttu-id="1f8fb-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="1f8fb-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="1f8fb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f8fb-141">OUTPUTS</span></span>

### <span data-ttu-id="1f8fb-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f8fb-142">System.Boolean</span></span>

## <span data-ttu-id="1f8fb-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f8fb-143">NOTES</span></span>

## <span data-ttu-id="1f8fb-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f8fb-144">RELATED LINKS</span></span>
