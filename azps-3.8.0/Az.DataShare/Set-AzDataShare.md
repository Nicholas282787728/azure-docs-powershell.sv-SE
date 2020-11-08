---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: c92348e32247bfed0b3aa7ce59b4772f7d3ef4af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092143"
---
# <span data-ttu-id="93747-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="93747-101">Set-AzDataShare</span></span>

## <span data-ttu-id="93747-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93747-102">SYNOPSIS</span></span>
<span data-ttu-id="93747-103">Uppdaterar en befintlig data resurs</span><span class="sxs-lookup"><span data-stu-id="93747-103">Updates an existing data share</span></span>

## <span data-ttu-id="93747-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93747-104">SYNTAX</span></span>

### <span data-ttu-id="93747-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="93747-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93747-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93747-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93747-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93747-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93747-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93747-108">DESCRIPTION</span></span>
<span data-ttu-id="93747-109">Cmdleten **set-AzDataShare** uppdaterar en data resurs som finns inom ett angivet Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="93747-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="93747-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93747-110">EXAMPLES</span></span>

### <span data-ttu-id="93747-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93747-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="93747-112">Det här kommandot uppdaterar en befintlig data resurs med namnet AdsShare</span><span class="sxs-lookup"><span data-stu-id="93747-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="93747-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93747-113">PARAMETERS</span></span>

### <span data-ttu-id="93747-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93747-114">-AccountName</span></span>
<span data-ttu-id="93747-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="93747-115">Azure data share account name</span></span>

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

### <span data-ttu-id="93747-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93747-116">-DefaultProfile</span></span>
<span data-ttu-id="93747-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93747-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93747-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="93747-118">-Description</span></span>
<span data-ttu-id="93747-119">Beskrivning av data resurs</span><span class="sxs-lookup"><span data-stu-id="93747-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93747-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93747-120">-InputObject</span></span>
<span data-ttu-id="93747-121">Azure Data Share-objekt</span><span class="sxs-lookup"><span data-stu-id="93747-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93747-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="93747-122">-Name</span></span>
<span data-ttu-id="93747-123">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="93747-123">Azure data share name</span></span>

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

### <span data-ttu-id="93747-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93747-124">-ResourceGroupName</span></span>
<span data-ttu-id="93747-125">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="93747-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="93747-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93747-126">-ResourceId</span></span>
<span data-ttu-id="93747-127">Resurs-ID för Azure Data-resursen</span><span class="sxs-lookup"><span data-stu-id="93747-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="93747-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="93747-128">-TermsOfUse</span></span>
<span data-ttu-id="93747-129">Användnings villkor för data resurs</span><span class="sxs-lookup"><span data-stu-id="93747-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93747-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93747-130">-Confirm</span></span>
<span data-ttu-id="93747-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93747-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93747-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93747-132">-WhatIf</span></span>
<span data-ttu-id="93747-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93747-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93747-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93747-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93747-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93747-135">CommonParameters</span></span>
<span data-ttu-id="93747-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93747-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93747-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93747-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93747-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93747-138">INPUTS</span></span>

### <span data-ttu-id="93747-139">System. String</span><span class="sxs-lookup"><span data-stu-id="93747-139">System.String</span></span>

### <span data-ttu-id="93747-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="93747-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="93747-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93747-141">OUTPUTS</span></span>

### <span data-ttu-id="93747-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="93747-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="93747-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93747-143">NOTES</span></span>

## <span data-ttu-id="93747-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93747-144">RELATED LINKS</span></span>
