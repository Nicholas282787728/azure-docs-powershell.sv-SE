---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325284"
---
# <span data-ttu-id="1d84e-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1d84e-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="1d84e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d84e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d84e-103">Hämtar en Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="1d84e-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="1d84e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d84e-104">SYNTAX</span></span>

### <span data-ttu-id="1d84e-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1d84e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d84e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d84e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d84e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d84e-107">DESCRIPTION</span></span>
<span data-ttu-id="1d84e-108">Cmdleten **Get-AzFirewallPolicy** hämtar en eller flera brand väggar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="1d84e-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="1d84e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d84e-109">EXAMPLES</span></span>

### <span data-ttu-id="1d84e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1d84e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="1d84e-111">I det här exemplet får du en brand Väggs princip med namnet "firewallPolicy" i resurs gruppen "TestRg"</span><span class="sxs-lookup"><span data-stu-id="1d84e-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="1d84e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d84e-112">PARAMETERS</span></span>

### <span data-ttu-id="1d84e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d84e-113">-DefaultProfile</span></span>
<span data-ttu-id="1d84e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d84e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d84e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d84e-115">-Name</span></span>
<span data-ttu-id="1d84e-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="1d84e-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d84e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d84e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d84e-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1d84e-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d84e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d84e-119">-ResourceId</span></span>
<span data-ttu-id="1d84e-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1d84e-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d84e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d84e-121">CommonParameters</span></span>
<span data-ttu-id="1d84e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d84e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d84e-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d84e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d84e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d84e-124">INPUTS</span></span>

### <span data-ttu-id="1d84e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1d84e-125">System.String</span></span>

## <span data-ttu-id="1d84e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d84e-126">OUTPUTS</span></span>

### <span data-ttu-id="1d84e-127">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1d84e-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="1d84e-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdletar. Network, version = 1.12.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1d84e-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1d84e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d84e-129">NOTES</span></span>

## <span data-ttu-id="1d84e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d84e-130">RELATED LINKS</span></span>
