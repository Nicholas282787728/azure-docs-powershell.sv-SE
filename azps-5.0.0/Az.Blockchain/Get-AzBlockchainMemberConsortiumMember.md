---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272786"
---
# <span data-ttu-id="41a6a-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="41a6a-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="41a6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="41a6a-103">Visar en lista över konsortiet medlemmar för en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="41a6a-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="41a6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41a6a-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="41a6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="41a6a-106">Visar en lista över konsortiet medlemmar för en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="41a6a-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="41a6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41a6a-107">EXAMPLES</span></span>

### <span data-ttu-id="41a6a-108">Exempel 1: visar konsortiet medlemmar för en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="41a6a-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="41a6a-109">Det här kommandot visar konsortiet medlemmar för en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="41a6a-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="41a6a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41a6a-110">PARAMETERS</span></span>

### <span data-ttu-id="41a6a-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="41a6a-111">-BlockchainMemberName</span></span>
<span data-ttu-id="41a6a-112">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="41a6a-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="41a6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a6a-113">-DefaultProfile</span></span>
<span data-ttu-id="41a6a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41a6a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41a6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="41a6a-116">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="41a6a-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="41a6a-117">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="41a6a-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="41a6a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41a6a-118">-SubscriptionId</span></span>
<span data-ttu-id="41a6a-119">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="41a6a-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="41a6a-120">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="41a6a-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41a6a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a6a-121">CommonParameters</span></span>
<span data-ttu-id="41a6a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a6a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a6a-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41a6a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a6a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41a6a-124">INPUTS</span></span>

## <span data-ttu-id="41a6a-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41a6a-125">OUTPUTS</span></span>

### <span data-ttu-id="41a6a-126">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="41a6a-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="41a6a-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41a6a-127">NOTES</span></span>

<span data-ttu-id="41a6a-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="41a6a-128">ALIASES</span></span>

## <span data-ttu-id="41a6a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41a6a-129">RELATED LINKS</span></span>

