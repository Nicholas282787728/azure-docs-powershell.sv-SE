---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: f10aaca629519d40334aabdac604531b726edd69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744406"
---
# <span data-ttu-id="ddc7b-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="ddc7b-101">Set-AzDataShare</span></span>

## <span data-ttu-id="ddc7b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc7b-103">Uppdaterar en befintlig data resurs</span><span class="sxs-lookup"><span data-stu-id="ddc7b-103">Updates an existing data share</span></span>

## <span data-ttu-id="ddc7b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddc7b-104">SYNTAX</span></span>

### <span data-ttu-id="ddc7b-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ddc7b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc7b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc7b-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc7b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc7b-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc7b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddc7b-108">DESCRIPTION</span></span>
<span data-ttu-id="ddc7b-109">Cmdleten **set-AzDataShare** uppdaterar en data resurs som finns inom ett angivet Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="ddc7b-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="ddc7b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddc7b-110">EXAMPLES</span></span>

### <span data-ttu-id="ddc7b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddc7b-111">Example 1</span></span>
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

<span data-ttu-id="ddc7b-112">Det här kommandot uppdaterar en befintlig data resurs med namnet AdsShare</span><span class="sxs-lookup"><span data-stu-id="ddc7b-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="ddc7b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddc7b-113">PARAMETERS</span></span>

### <span data-ttu-id="ddc7b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ddc7b-114">-AccountName</span></span>
<span data-ttu-id="ddc7b-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="ddc7b-115">Azure data share account name</span></span>

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

### <span data-ttu-id="ddc7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc7b-116">-DefaultProfile</span></span>
<span data-ttu-id="ddc7b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc7b-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ddc7b-118">-Description</span></span>
<span data-ttu-id="ddc7b-119">Beskrivning av data resurs</span><span class="sxs-lookup"><span data-stu-id="ddc7b-119">Description of Data Share</span></span>

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

### <span data-ttu-id="ddc7b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc7b-120">-InputObject</span></span>
<span data-ttu-id="ddc7b-121">Azure Data Share-objekt</span><span class="sxs-lookup"><span data-stu-id="ddc7b-121">Azure data share object</span></span>


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

### <span data-ttu-id="ddc7b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddc7b-122">-Name</span></span>
<span data-ttu-id="ddc7b-123">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="ddc7b-123">Azure data share name</span></span>

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

### <span data-ttu-id="ddc7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ddc7b-125">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="ddc7b-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ddc7b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc7b-126">-ResourceId</span></span>
<span data-ttu-id="ddc7b-127">Resurs-ID för Azure Data-resursen</span><span class="sxs-lookup"><span data-stu-id="ddc7b-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="ddc7b-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="ddc7b-128">-TermsOfUse</span></span>
<span data-ttu-id="ddc7b-129">Användnings villkor för data resurs</span><span class="sxs-lookup"><span data-stu-id="ddc7b-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="ddc7b-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddc7b-130">-Confirm</span></span>
<span data-ttu-id="ddc7b-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddc7b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc7b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc7b-132">-WhatIf</span></span>
<span data-ttu-id="ddc7b-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddc7b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddc7b-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddc7b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc7b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc7b-135">CommonParameters</span></span>
<span data-ttu-id="ddc7b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc7b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc7b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc7b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc7b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddc7b-138">INPUTS</span></span>

### <span data-ttu-id="ddc7b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ddc7b-139">System.String</span></span>

### <span data-ttu-id="ddc7b-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ddc7b-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ddc7b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddc7b-141">OUTPUTS</span></span>

### <span data-ttu-id="ddc7b-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ddc7b-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ddc7b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddc7b-143">NOTES</span></span>

## <span data-ttu-id="ddc7b-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddc7b-144">RELATED LINKS</span></span>