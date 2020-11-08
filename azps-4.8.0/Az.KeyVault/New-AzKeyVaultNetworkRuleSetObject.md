---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259455"
---
# <span data-ttu-id="5b492-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="5b492-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="5b492-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b492-102">SYNOPSIS</span></span>
<span data-ttu-id="5b492-103">Skapa ett objekt som representerar inställningar för nätverks regler.</span><span class="sxs-lookup"><span data-stu-id="5b492-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="5b492-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b492-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b492-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b492-105">DESCRIPTION</span></span>
<span data-ttu-id="5b492-106">Skapa ett objekt som representerar de nätverks regel inställningar som kan användas när du skapar ett valv.</span><span class="sxs-lookup"><span data-stu-id="5b492-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="5b492-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b492-107">EXAMPLES</span></span>

### <span data-ttu-id="5b492-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5b492-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="5b492-109">Skapa ett nytt valv och ange nätverks regler för att tillåta åtkomst till angiven IP-adress från det virtuella nätverk som identifieras av $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="5b492-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="5b492-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b492-110">PARAMETERS</span></span>

### <span data-ttu-id="5b492-111">-Kringgå</span><span class="sxs-lookup"><span data-stu-id="5b492-111">-Bypass</span></span>
<span data-ttu-id="5b492-112">Anger kringgående av nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="5b492-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b492-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="5b492-113">-DefaultAction</span></span>
<span data-ttu-id="5b492-114">Anger standard åtgärd för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="5b492-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b492-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b492-115">-DefaultProfile</span></span>
<span data-ttu-id="5b492-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5b492-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b492-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="5b492-117">-IpAddressRange</span></span>
<span data-ttu-id="5b492-118">Anger tillåtet nätverks-IP-adressintervall för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="5b492-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b492-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5b492-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5b492-120">Anger tillåtet virtuellt nätverks-ID för nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="5b492-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b492-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b492-121">CommonParameters</span></span>
<span data-ttu-id="5b492-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b492-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b492-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b492-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b492-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b492-124">INPUTS</span></span>

### <span data-ttu-id="5b492-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="5b492-125">None</span></span>

## <span data-ttu-id="5b492-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b492-126">OUTPUTS</span></span>

### <span data-ttu-id="5b492-127">Microsoft. Azure. commands. valv. Models. PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b492-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="5b492-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b492-128">NOTES</span></span>

## <span data-ttu-id="5b492-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b492-129">RELATED LINKS</span></span>
