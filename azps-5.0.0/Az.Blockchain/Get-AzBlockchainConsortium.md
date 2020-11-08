---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272791"
---
# <span data-ttu-id="770b1-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="770b1-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="770b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="770b1-102">SYNOPSIS</span></span>
<span data-ttu-id="770b1-103">Visar en lista över tillgängliga konsortier för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="770b1-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="770b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="770b1-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="770b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="770b1-105">DESCRIPTION</span></span>
<span data-ttu-id="770b1-106">Visar en lista över tillgängliga konsortier för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="770b1-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="770b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="770b1-107">EXAMPLES</span></span>

### <span data-ttu-id="770b1-108">Exempel 1: skaffa blockchain Consortium.</span><span class="sxs-lookup"><span data-stu-id="770b1-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="770b1-109">Det här kommandot visar konsortiet under ett abonnemang för en viss plats.</span><span class="sxs-lookup"><span data-stu-id="770b1-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="770b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="770b1-110">PARAMETERS</span></span>

### <span data-ttu-id="770b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770b1-111">-DefaultProfile</span></span>
<span data-ttu-id="770b1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="770b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770b1-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="770b1-113">-Location</span></span>
<span data-ttu-id="770b1-114">Plats namn.</span><span class="sxs-lookup"><span data-stu-id="770b1-114">Location Name.</span></span>

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

### <span data-ttu-id="770b1-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="770b1-115">-SubscriptionId</span></span>
<span data-ttu-id="770b1-116">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="770b1-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="770b1-117">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="770b1-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="770b1-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="770b1-118">-Confirm</span></span>
<span data-ttu-id="770b1-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="770b1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770b1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770b1-120">-WhatIf</span></span>
<span data-ttu-id="770b1-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="770b1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770b1-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="770b1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770b1-123">CommonParameters</span></span>
<span data-ttu-id="770b1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770b1-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="770b1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770b1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="770b1-126">INPUTS</span></span>

## <span data-ttu-id="770b1-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="770b1-127">OUTPUTS</span></span>

### <span data-ttu-id="770b1-128">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="770b1-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="770b1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="770b1-129">NOTES</span></span>

<span data-ttu-id="770b1-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="770b1-130">ALIASES</span></span>

## <span data-ttu-id="770b1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="770b1-131">RELATED LINKS</span></span>

