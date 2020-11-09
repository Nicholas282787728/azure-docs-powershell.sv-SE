---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320271"
---
# <span data-ttu-id="ec983-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ec983-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="ec983-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec983-102">SYNOPSIS</span></span>
<span data-ttu-id="ec983-103">Tar bort en data uppsättnings mappning</span><span class="sxs-lookup"><span data-stu-id="ec983-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="ec983-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec983-104">SYNTAX</span></span>

### <span data-ttu-id="ec983-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ec983-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec983-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec983-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec983-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec983-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec983-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec983-108">DESCRIPTION</span></span>
<span data-ttu-id="ec983-109">Cmdleten **Remove-AzDataShareDataSetMapping** tar bort en data uppsättnings mappningar.</span><span class="sxs-lookup"><span data-stu-id="ec983-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="ec983-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec983-110">EXAMPLES</span></span>

### <span data-ttu-id="ec983-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec983-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="ec983-112">De här kommandona tar bort den dataset som heter DSM från sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="ec983-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="ec983-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec983-113">PARAMETERS</span></span>

### <span data-ttu-id="ec983-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec983-114">-AccountName</span></span>
<span data-ttu-id="ec983-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="ec983-115">Azure data share account name</span></span>

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

### <span data-ttu-id="ec983-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec983-116">-DefaultProfile</span></span>
<span data-ttu-id="ec983-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec983-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec983-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec983-118">-InputObject</span></span>
<span data-ttu-id="ec983-119">Mappnings objekt för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="ec983-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="ec983-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec983-120">-Name</span></span>
<span data-ttu-id="ec983-121">Mappnings namn för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="ec983-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="ec983-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec983-122">-PassThru</span></span>
<span data-ttu-id="ec983-123">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="ec983-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="ec983-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec983-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec983-125">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="ec983-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ec983-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec983-126">-ResourceId</span></span>
<span data-ttu-id="ec983-127">Resurs-ID för Azure Data uppsättnings mappning</span><span class="sxs-lookup"><span data-stu-id="ec983-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="ec983-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ec983-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="ec983-129">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="ec983-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ec983-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec983-130">-Confirm</span></span>
<span data-ttu-id="ec983-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec983-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec983-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec983-132">-WhatIf</span></span>
<span data-ttu-id="ec983-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec983-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec983-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec983-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec983-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec983-135">CommonParameters</span></span>
<span data-ttu-id="ec983-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec983-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec983-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec983-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec983-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec983-138">INPUTS</span></span>

### <span data-ttu-id="ec983-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ec983-139">System.String</span></span>

### <span data-ttu-id="ec983-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ec983-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="ec983-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec983-141">OUTPUTS</span></span>

### <span data-ttu-id="ec983-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec983-142">System.Boolean</span></span>

## <span data-ttu-id="ec983-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec983-143">NOTES</span></span>

## <span data-ttu-id="ec983-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec983-144">RELATED LINKS</span></span>
