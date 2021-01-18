---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524677"
---
# <span data-ttu-id="85887-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="85887-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="85887-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85887-102">SYNOPSIS</span></span>
<span data-ttu-id="85887-103">Visar API-nycklarna för en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="85887-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="85887-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85887-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85887-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85887-105">DESCRIPTION</span></span>
<span data-ttu-id="85887-106">Visar API-nycklarna för en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="85887-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="85887-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85887-107">EXAMPLES</span></span>

### <span data-ttu-id="85887-108">Exempel 1: lista med blockchain API-nycklar</span><span class="sxs-lookup"><span data-stu-id="85887-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="85887-109">Det här kommandot visar API-nycklar för en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="85887-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="85887-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85887-110">PARAMETERS</span></span>

### <span data-ttu-id="85887-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="85887-111">-BlockchainMemberName</span></span>
<span data-ttu-id="85887-112">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="85887-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="85887-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85887-113">-DefaultProfile</span></span>
<span data-ttu-id="85887-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85887-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85887-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85887-115">-ResourceGroupName</span></span>
<span data-ttu-id="85887-116">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="85887-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="85887-117">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="85887-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="85887-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85887-118">-SubscriptionId</span></span>
<span data-ttu-id="85887-119">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="85887-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="85887-120">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="85887-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85887-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85887-121">-Confirm</span></span>
<span data-ttu-id="85887-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85887-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85887-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85887-123">-WhatIf</span></span>
<span data-ttu-id="85887-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85887-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85887-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85887-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85887-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85887-126">CommonParameters</span></span>
<span data-ttu-id="85887-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85887-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85887-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85887-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85887-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85887-129">INPUTS</span></span>

## <span data-ttu-id="85887-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85887-130">OUTPUTS</span></span>

### <span data-ttu-id="85887-131">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="85887-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="85887-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85887-132">NOTES</span></span>

<span data-ttu-id="85887-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="85887-133">ALIASES</span></span>

## <span data-ttu-id="85887-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85887-134">RELATED LINKS</span></span>

