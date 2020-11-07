---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: c0b2b8eb249e466c0e57127e0df9ee9b0afad048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744437"
---
# <span data-ttu-id="93185-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="93185-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="93185-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93185-102">SYNOPSIS</span></span>
<span data-ttu-id="93185-103">Skapar ett nytt data delnings konto</span><span class="sxs-lookup"><span data-stu-id="93185-103">Creates new data share account</span></span>

## <span data-ttu-id="93185-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93185-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93185-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93185-105">DESCRIPTION</span></span>
<span data-ttu-id="93185-106">**New-AzDataShareAccount** cmdlet skapar ett datashare-konto i den angivna Azure resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="93185-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="93185-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93185-107">EXAMPLES</span></span>

### <span data-ttu-id="93185-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93185-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="93185-109">Skapar ett konto med namnet "WikiADS" i resurs gruppen "annonser"</span><span class="sxs-lookup"><span data-stu-id="93185-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="93185-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93185-110">PARAMETERS</span></span>

### <span data-ttu-id="93185-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93185-111">-AsJob</span></span>
<span data-ttu-id="93185-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="93185-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="93185-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93185-113">-DefaultProfile</span></span>
<span data-ttu-id="93185-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93185-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93185-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="93185-115">-Location</span></span>
<span data-ttu-id="93185-116">Den plats där du vill skapa data delnings kontot.</span><span class="sxs-lookup"><span data-stu-id="93185-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="93185-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="93185-117">-Name</span></span>
<span data-ttu-id="93185-118">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="93185-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="93185-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93185-119">-ResourceGroupName</span></span>
<span data-ttu-id="93185-120">Resurs grupp namnet för Azure Data Share-kontot skapas i.</span><span class="sxs-lookup"><span data-stu-id="93185-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="93185-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="93185-121">-Tag</span></span>
<span data-ttu-id="93185-122">De taggar som ska kopplas till Azure Data Share-kontot.</span><span class="sxs-lookup"><span data-stu-id="93185-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93185-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93185-123">-Confirm</span></span>
<span data-ttu-id="93185-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93185-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93185-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93185-125">-WhatIf</span></span>
<span data-ttu-id="93185-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93185-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93185-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93185-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93185-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93185-128">CommonParameters</span></span>
<span data-ttu-id="93185-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93185-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93185-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93185-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93185-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93185-131">INPUTS</span></span>

### <span data-ttu-id="93185-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="93185-132">None</span></span>

## <span data-ttu-id="93185-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93185-133">OUTPUTS</span></span>

### <span data-ttu-id="93185-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="93185-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="93185-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93185-135">NOTES</span></span>

## <span data-ttu-id="93185-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93185-136">RELATED LINKS</span></span>
