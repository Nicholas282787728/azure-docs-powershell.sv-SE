---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272776"
---
# <span data-ttu-id="e3fa7-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="e3fa7-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="e3fa7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fa7-103">Visa API-nycklarna för Transaction-noden.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="e3fa7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3fa7-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e3fa7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3fa7-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fa7-106">Visa API-nycklarna för Transaction-noden.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="e3fa7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3fa7-107">EXAMPLES</span></span>

### <span data-ttu-id="e3fa7-108">Exempel 1: lista API-nycklar för en transaktionskö</span><span class="sxs-lookup"><span data-stu-id="e3fa7-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="e3fa7-109">Det här kommandot visar API-nycklar för en Transaction-nod.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="e3fa7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3fa7-110">PARAMETERS</span></span>

### <span data-ttu-id="e3fa7-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="e3fa7-111">-BlockchainMemberName</span></span>
<span data-ttu-id="e3fa7-112">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="e3fa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fa7-113">-DefaultProfile</span></span>
<span data-ttu-id="e3fa7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3fa7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fa7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3fa7-116">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e3fa7-117">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e3fa7-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3fa7-118">-SubscriptionId</span></span>
<span data-ttu-id="e3fa7-119">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3fa7-120">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3fa7-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="e3fa7-121">-TransactionNodeName</span></span>
<span data-ttu-id="e3fa7-122">Nodnamn för transaktion.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-122">Transaction node name.</span></span>

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

### <span data-ttu-id="e3fa7-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3fa7-123">-Confirm</span></span>
<span data-ttu-id="e3fa7-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3fa7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3fa7-125">-WhatIf</span></span>
<span data-ttu-id="e3fa7-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3fa7-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3fa7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fa7-128">CommonParameters</span></span>
<span data-ttu-id="e3fa7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fa7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fa7-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3fa7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fa7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3fa7-131">INPUTS</span></span>

## <span data-ttu-id="e3fa7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3fa7-132">OUTPUTS</span></span>

### <span data-ttu-id="e3fa7-133">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="e3fa7-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="e3fa7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3fa7-134">NOTES</span></span>

<span data-ttu-id="e3fa7-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e3fa7-135">ALIASES</span></span>

## <span data-ttu-id="e3fa7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3fa7-136">RELATED LINKS</span></span>
