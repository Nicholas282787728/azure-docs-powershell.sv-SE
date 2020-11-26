---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273237"
---
# <span data-ttu-id="effe3-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="effe3-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="effe3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="effe3-102">SYNOPSIS</span></span>
<span data-ttu-id="effe3-103">Hämtar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="effe3-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="effe3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="effe3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="effe3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="effe3-105">DESCRIPTION</span></span>
<span data-ttu-id="effe3-106">Cmdleten **Get-AzApplicationGatewayFirewallPolicy** hämtar en brand Väggs princip för Application Gateway..</span><span class="sxs-lookup"><span data-stu-id="effe3-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="effe3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="effe3-107">EXAMPLES</span></span>

### <span data-ttu-id="effe3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="effe3-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="effe3-109">Det här kommandot hämtar brand Väggs principen för Application Gateway med namnet FirewallPolicy1 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGwFirewallPolicy variabel.</span><span class="sxs-lookup"><span data-stu-id="effe3-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="effe3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="effe3-110">PARAMETERS</span></span>

### <span data-ttu-id="effe3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="effe3-111">-DefaultProfile</span></span>
<span data-ttu-id="effe3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="effe3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="effe3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="effe3-113">-Name</span></span>
<span data-ttu-id="effe3-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="effe3-114">The resource name.</span></span>

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

### <span data-ttu-id="effe3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="effe3-115">-ResourceGroupName</span></span>
<span data-ttu-id="effe3-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="effe3-116">The resource group name.</span></span>

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

### <span data-ttu-id="effe3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="effe3-117">CommonParameters</span></span>
<span data-ttu-id="effe3-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="effe3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="effe3-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="effe3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="effe3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="effe3-120">INPUTS</span></span>

### <span data-ttu-id="effe3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="effe3-121">System.String</span></span>

## <span data-ttu-id="effe3-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="effe3-122">OUTPUTS</span></span>

### <span data-ttu-id="effe3-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="effe3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="effe3-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="effe3-124">NOTES</span></span>

## <span data-ttu-id="effe3-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="effe3-125">RELATED LINKS</span></span>