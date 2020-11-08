---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091288"
---
# <span data-ttu-id="60416-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="60416-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="60416-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60416-102">SYNOPSIS</span></span>
<span data-ttu-id="60416-103">Hämtar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="60416-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="60416-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60416-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60416-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60416-105">DESCRIPTION</span></span>
<span data-ttu-id="60416-106">Cmdleten **Get-AzApplicationGatewayFirewallPolicy** hämtar en brand Väggs princip för Application Gateway..</span><span class="sxs-lookup"><span data-stu-id="60416-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="60416-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60416-107">EXAMPLES</span></span>

### <span data-ttu-id="60416-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="60416-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60416-109">Det här kommandot hämtar brand Väggs principen för Application Gateway med namnet FirewallPolicy1 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGwFirewallPolicy variabel.</span><span class="sxs-lookup"><span data-stu-id="60416-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="60416-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60416-110">PARAMETERS</span></span>

### <span data-ttu-id="60416-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60416-111">-DefaultProfile</span></span>
<span data-ttu-id="60416-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60416-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60416-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="60416-113">-Name</span></span>
<span data-ttu-id="60416-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="60416-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60416-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60416-115">-ResourceGroupName</span></span>
<span data-ttu-id="60416-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="60416-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60416-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60416-117">CommonParameters</span></span>
<span data-ttu-id="60416-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60416-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60416-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60416-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60416-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60416-120">INPUTS</span></span>

### <span data-ttu-id="60416-121">System. String</span><span class="sxs-lookup"><span data-stu-id="60416-121">System.String</span></span>

## <span data-ttu-id="60416-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60416-122">OUTPUTS</span></span>

### <span data-ttu-id="60416-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="60416-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="60416-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60416-124">NOTES</span></span>

## <span data-ttu-id="60416-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60416-125">RELATED LINKS</span></span>