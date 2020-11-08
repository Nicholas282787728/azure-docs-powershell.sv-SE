---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103281"
---
# <span data-ttu-id="e1854-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="e1854-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="e1854-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1854-102">SYNOPSIS</span></span>
<span data-ttu-id="e1854-103">Visar resurs typens SKU: er.</span><span class="sxs-lookup"><span data-stu-id="e1854-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="e1854-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1854-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e1854-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1854-105">DESCRIPTION</span></span>
<span data-ttu-id="e1854-106">Visar resurs typens SKU: er.</span><span class="sxs-lookup"><span data-stu-id="e1854-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="e1854-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1854-107">EXAMPLES</span></span>

### <span data-ttu-id="e1854-108">Exempel 1: lista SKU för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="e1854-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="e1854-109">Det här kommandot visar SKU för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e1854-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="e1854-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1854-110">PARAMETERS</span></span>

### <span data-ttu-id="e1854-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1854-111">-DefaultProfile</span></span>
<span data-ttu-id="e1854-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1854-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1854-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1854-113">-SubscriptionId</span></span>
<span data-ttu-id="e1854-114">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e1854-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e1854-115">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e1854-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e1854-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1854-116">CommonParameters</span></span>
<span data-ttu-id="e1854-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1854-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1854-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1854-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1854-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1854-119">INPUTS</span></span>

## <span data-ttu-id="e1854-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1854-120">OUTPUTS</span></span>

### <span data-ttu-id="e1854-121">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="e1854-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="e1854-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1854-122">NOTES</span></span>

<span data-ttu-id="e1854-123">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e1854-123">ALIASES</span></span>

## <span data-ttu-id="e1854-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1854-124">RELATED LINKS</span></span>

