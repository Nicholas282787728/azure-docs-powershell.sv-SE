---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393152"
---
# <span data-ttu-id="49ce0-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="49ce0-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="49ce0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="49ce0-103">tar bort en resurs prenumeration</span><span class="sxs-lookup"><span data-stu-id="49ce0-103">removes a share subscription</span></span>

## <span data-ttu-id="49ce0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49ce0-104">SYNTAX</span></span>

### <span data-ttu-id="49ce0-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="49ce0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ce0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ce0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ce0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ce0-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ce0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49ce0-108">DESCRIPTION</span></span>
<span data-ttu-id="49ce0-109">Cmdleten **Remove-AzDataShareSubscription** tar bort en resurs prenumeration</span><span class="sxs-lookup"><span data-stu-id="49ce0-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="49ce0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49ce0-110">EXAMPLES</span></span>

### <span data-ttu-id="49ce0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="49ce0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="49ce0-112">Med det här kommandot tas en sharesubscription med namnet AdsShareSubscription bort från konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="49ce0-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="49ce0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49ce0-113">PARAMETERS</span></span>

### <span data-ttu-id="49ce0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49ce0-114">-AccountName</span></span>
<span data-ttu-id="49ce0-115">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="49ce0-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="49ce0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49ce0-116">-AsJob</span></span>
<span data-ttu-id="49ce0-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="49ce0-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="49ce0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ce0-118">-DefaultProfile</span></span>
<span data-ttu-id="49ce0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49ce0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ce0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49ce0-120">-InputObject</span></span>
<span data-ttu-id="49ce0-121">Abonnemang för Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="49ce0-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="49ce0-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="49ce0-122">-Name</span></span>
<span data-ttu-id="49ce0-123">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="49ce0-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="49ce0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49ce0-124">-PassThru</span></span>
<span data-ttu-id="49ce0-125">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="49ce0-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="49ce0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ce0-126">-ResourceGroupName</span></span>
<span data-ttu-id="49ce0-127">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="49ce0-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="49ce0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49ce0-128">-ResourceId</span></span>
<span data-ttu-id="49ce0-129">Resurs-ID för Azure Data Share-prenumerationen</span><span class="sxs-lookup"><span data-stu-id="49ce0-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="49ce0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49ce0-130">-Confirm</span></span>
<span data-ttu-id="49ce0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49ce0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ce0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ce0-132">-WhatIf</span></span>
<span data-ttu-id="49ce0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49ce0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ce0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49ce0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ce0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ce0-135">CommonParameters</span></span>
<span data-ttu-id="49ce0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ce0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ce0-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49ce0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ce0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49ce0-138">INPUTS</span></span>

### <span data-ttu-id="49ce0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="49ce0-139">System.String</span></span>

### <span data-ttu-id="49ce0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="49ce0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="49ce0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49ce0-141">OUTPUTS</span></span>

### <span data-ttu-id="49ce0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49ce0-142">System.Boolean</span></span>

## <span data-ttu-id="49ce0-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49ce0-143">NOTES</span></span>

## <span data-ttu-id="49ce0-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49ce0-144">RELATED LINKS</span></span>
