---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527216"
---
# <span data-ttu-id="f5c71-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f5c71-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="f5c71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5c71-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c71-103">För att kontrol lera om det finns ett resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f5c71-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="f5c71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5c71-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5c71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5c71-105">DESCRIPTION</span></span>
<span data-ttu-id="f5c71-106">För att kontrol lera om det finns ett resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f5c71-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="f5c71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5c71-107">EXAMPLES</span></span>

### <span data-ttu-id="f5c71-108">Exempel 1: kontrol lera om det finns ett resurs namn</span><span class="sxs-lookup"><span data-stu-id="f5c71-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="f5c71-109">Kommandot kontrollerar om det finns ett resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f5c71-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="f5c71-110">Exempel 2: kontrol lera om ett resurs namn är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="f5c71-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="f5c71-111">Kommandot kontrollerar om det finns ett resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f5c71-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="f5c71-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5c71-112">PARAMETERS</span></span>

### <span data-ttu-id="f5c71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c71-113">-DefaultProfile</span></span>
<span data-ttu-id="f5c71-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c71-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="f5c71-115">-Location</span></span>
<span data-ttu-id="f5c71-116">Plats namn.</span><span class="sxs-lookup"><span data-stu-id="f5c71-116">Location Name.</span></span>

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

### <span data-ttu-id="f5c71-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5c71-117">-Name</span></span>
<span data-ttu-id="f5c71-118">Hämtar eller anger namnet som ska kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="f5c71-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="f5c71-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5c71-119">-SubscriptionId</span></span>
<span data-ttu-id="f5c71-120">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f5c71-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f5c71-121">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f5c71-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c71-122">– Skriv</span><span class="sxs-lookup"><span data-stu-id="f5c71-122">-Type</span></span>
<span data-ttu-id="f5c71-123">Hämtar eller anger typen av resurs som ska kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="f5c71-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="f5c71-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5c71-124">-Confirm</span></span>
<span data-ttu-id="f5c71-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5c71-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5c71-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c71-126">-WhatIf</span></span>
<span data-ttu-id="f5c71-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5c71-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c71-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5c71-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5c71-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c71-129">CommonParameters</span></span>
<span data-ttu-id="f5c71-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c71-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c71-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5c71-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c71-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5c71-132">INPUTS</span></span>

## <span data-ttu-id="f5c71-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5c71-133">OUTPUTS</span></span>

### <span data-ttu-id="f5c71-134">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="f5c71-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="f5c71-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5c71-135">NOTES</span></span>

<span data-ttu-id="f5c71-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f5c71-136">ALIASES</span></span>

## <span data-ttu-id="f5c71-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5c71-137">RELATED LINKS</span></span>

