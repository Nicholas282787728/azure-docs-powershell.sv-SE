---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320268"
---
# <span data-ttu-id="18dc8-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="18dc8-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="18dc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="18dc8-103">tar bort en inbjudan</span><span class="sxs-lookup"><span data-stu-id="18dc8-103">removes an invitation</span></span>

## <span data-ttu-id="18dc8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18dc8-104">SYNTAX</span></span>

### <span data-ttu-id="18dc8-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="18dc8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18dc8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18dc8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18dc8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18dc8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18dc8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18dc8-108">DESCRIPTION</span></span>
<span data-ttu-id="18dc8-109">Cmdleten **Remove-AzDataShareInvitation** tar bort en datashare-inbjudan.</span><span class="sxs-lookup"><span data-stu-id="18dc8-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="18dc8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18dc8-110">EXAMPLES</span></span>

### <span data-ttu-id="18dc8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="18dc8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="18dc8-112">De här kommandona tar bort en inbjudan som heter ADSInvite från Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="18dc8-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="18dc8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18dc8-113">PARAMETERS</span></span>

### <span data-ttu-id="18dc8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18dc8-114">-AccountName</span></span>
<span data-ttu-id="18dc8-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="18dc8-115">Azure data share account name</span></span>

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

### <span data-ttu-id="18dc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dc8-116">-DefaultProfile</span></span>
<span data-ttu-id="18dc8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18dc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18dc8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18dc8-118">-InputObject</span></span>
<span data-ttu-id="18dc8-119">Objekt i Azure Data-delningsinbjudan</span><span class="sxs-lookup"><span data-stu-id="18dc8-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18dc8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="18dc8-120">-Name</span></span>
<span data-ttu-id="18dc8-121">Namn på Azure Data-delningsinbjudan</span><span class="sxs-lookup"><span data-stu-id="18dc8-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="18dc8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18dc8-122">-PassThru</span></span>
<span data-ttu-id="18dc8-123">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="18dc8-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="18dc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="18dc8-125">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="18dc8-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="18dc8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18dc8-126">-ResourceId</span></span>
<span data-ttu-id="18dc8-127">Resurs-ID för Azure Data Share-inbjudan</span><span class="sxs-lookup"><span data-stu-id="18dc8-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="18dc8-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="18dc8-128">-ShareName</span></span>
<span data-ttu-id="18dc8-129">Azure Data Share-namn.</span><span class="sxs-lookup"><span data-stu-id="18dc8-129">Azure data share name.</span></span>

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

### <span data-ttu-id="18dc8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18dc8-130">-Confirm</span></span>
<span data-ttu-id="18dc8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18dc8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18dc8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18dc8-132">-WhatIf</span></span>
<span data-ttu-id="18dc8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18dc8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18dc8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18dc8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18dc8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dc8-135">CommonParameters</span></span>
<span data-ttu-id="18dc8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dc8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dc8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18dc8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dc8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18dc8-138">INPUTS</span></span>

### <span data-ttu-id="18dc8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="18dc8-139">System.String</span></span>

### <span data-ttu-id="18dc8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="18dc8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="18dc8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18dc8-141">OUTPUTS</span></span>

### <span data-ttu-id="18dc8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18dc8-142">System.Boolean</span></span>

## <span data-ttu-id="18dc8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18dc8-143">NOTES</span></span>

## <span data-ttu-id="18dc8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18dc8-144">RELATED LINKS</span></span>
