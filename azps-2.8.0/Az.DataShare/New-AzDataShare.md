---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: ccb40de9ef5e9e68cf62b7b05edeaac9ae10efbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744442"
---
# <span data-ttu-id="96064-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="96064-101">New-AzDataShare</span></span>

## <span data-ttu-id="96064-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96064-102">SYNOPSIS</span></span>
<span data-ttu-id="96064-103">Skapar en Azure Data-resurs.</span><span class="sxs-lookup"><span data-stu-id="96064-103">Creates a azure data share.</span></span>

## <span data-ttu-id="96064-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96064-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96064-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96064-105">DESCRIPTION</span></span>
<span data-ttu-id="96064-106">Cmdleten **New-AzDataShare** skapar en data resurs i ett angivet Azure Data Share-konto genom att ange resurs grupp namn, konto namn, resurs namn och delnings typ.</span><span class="sxs-lookup"><span data-stu-id="96064-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="96064-107">Beskrivning och användnings villkor är valfria parametrar som kan anges när data resursen skapas.</span><span class="sxs-lookup"><span data-stu-id="96064-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="96064-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96064-108">EXAMPLES</span></span>

### <span data-ttu-id="96064-109">Exempel 1: skapa en data resurs</span><span class="sxs-lookup"><span data-stu-id="96064-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="96064-110">Det här kommandot skapar en data resurs med namnet AdsShare of Natura CopyBased i data Share-kontot WikiAdsAccount under resurs gruppens annonser med beskrivning och användnings villkor.</span><span class="sxs-lookup"><span data-stu-id="96064-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="96064-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96064-111">PARAMETERS</span></span>

### <span data-ttu-id="96064-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96064-112">-AccountName</span></span>
<span data-ttu-id="96064-113">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="96064-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96064-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96064-114">-DefaultProfile</span></span>
<span data-ttu-id="96064-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96064-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96064-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="96064-116">-Description</span></span>
<span data-ttu-id="96064-117">Beskrivning av Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="96064-117">Description of azure data share</span></span>

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

### <span data-ttu-id="96064-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="96064-118">-Name</span></span>
<span data-ttu-id="96064-119">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="96064-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96064-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96064-120">-ResourceGroupName</span></span>
<span data-ttu-id="96064-121">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="96064-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96064-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="96064-122">-TermsOfUse</span></span>
<span data-ttu-id="96064-123">Användnings villkor för Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="96064-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="96064-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96064-124">-Confirm</span></span>
<span data-ttu-id="96064-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96064-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96064-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96064-126">-WhatIf</span></span>
<span data-ttu-id="96064-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96064-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96064-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96064-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96064-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96064-129">CommonParameters</span></span>
<span data-ttu-id="96064-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96064-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96064-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96064-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96064-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96064-132">INPUTS</span></span>

### <span data-ttu-id="96064-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="96064-133">None</span></span>

## <span data-ttu-id="96064-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96064-134">OUTPUTS</span></span>

### <span data-ttu-id="96064-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="96064-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="96064-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96064-136">NOTES</span></span>

## <span data-ttu-id="96064-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96064-137">RELATED LINKS</span></span>