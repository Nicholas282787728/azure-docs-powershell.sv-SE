---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: a2bcfa4232c7e69bdb17a5d56ff7b79373593b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744412"
---
# <span data-ttu-id="486a5-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="486a5-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="486a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="486a5-102">SYNOPSIS</span></span>
<span data-ttu-id="486a5-103">tar bort en resurs prenumeration</span><span class="sxs-lookup"><span data-stu-id="486a5-103">removes a share subscription</span></span>

## <span data-ttu-id="486a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="486a5-104">SYNTAX</span></span>

### <span data-ttu-id="486a5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="486a5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="486a5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="486a5-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="486a5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="486a5-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="486a5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="486a5-108">DESCRIPTION</span></span>
<span data-ttu-id="486a5-109">Cmdleten **Remove-AzDataShareSubscription** tar bort en resurs prenumeration</span><span class="sxs-lookup"><span data-stu-id="486a5-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="486a5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="486a5-110">EXAMPLES</span></span>

### <span data-ttu-id="486a5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="486a5-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="486a5-112">Med det här kommandot tas en sharesubscription med namnet AdsShareSubscription bort från konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="486a5-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="486a5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="486a5-113">PARAMETERS</span></span>

### <span data-ttu-id="486a5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="486a5-114">-AccountName</span></span>
<span data-ttu-id="486a5-115">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="486a5-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="486a5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="486a5-116">-AsJob</span></span>
<span data-ttu-id="486a5-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="486a5-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="486a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486a5-118">-DefaultProfile</span></span>
<span data-ttu-id="486a5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="486a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="486a5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="486a5-120">-InputObject</span></span>
<span data-ttu-id="486a5-121">Abonnemang för Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="486a5-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486a5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="486a5-122">-Name</span></span>
<span data-ttu-id="486a5-123">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="486a5-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="486a5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="486a5-124">-PassThru</span></span>
<span data-ttu-id="486a5-125">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="486a5-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="486a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="486a5-127">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="486a5-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="486a5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="486a5-128">-ResourceId</span></span>
<span data-ttu-id="486a5-129">Resurs-ID för Azure Data Share-prenumerationen</span><span class="sxs-lookup"><span data-stu-id="486a5-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="486a5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="486a5-130">-Confirm</span></span>
<span data-ttu-id="486a5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="486a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="486a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="486a5-132">-WhatIf</span></span>
<span data-ttu-id="486a5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="486a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="486a5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="486a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="486a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486a5-135">CommonParameters</span></span>
<span data-ttu-id="486a5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486a5-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="486a5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486a5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="486a5-138">INPUTS</span></span>

### <span data-ttu-id="486a5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="486a5-139">System.String</span></span>

### <span data-ttu-id="486a5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="486a5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="486a5-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="486a5-141">OUTPUTS</span></span>

### <span data-ttu-id="486a5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="486a5-142">System.Boolean</span></span>

## <span data-ttu-id="486a5-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="486a5-143">NOTES</span></span>

## <span data-ttu-id="486a5-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="486a5-144">RELATED LINKS</span></span>
