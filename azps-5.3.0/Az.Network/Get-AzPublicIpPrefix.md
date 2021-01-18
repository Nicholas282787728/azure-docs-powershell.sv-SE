---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 567fdda7c4f95a1bcdecab172223608ec78ef1f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522438"
---
# <span data-ttu-id="13304-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13304-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="13304-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13304-102">SYNOPSIS</span></span>
<span data-ttu-id="13304-103">Hämtar ett offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="13304-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="13304-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13304-104">SYNTAX</span></span>

### <span data-ttu-id="13304-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="13304-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13304-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13304-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13304-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13304-107">DESCRIPTION</span></span>
<span data-ttu-id="13304-108">Cmdleten **Get-AzPublicIpPrefix** får ett eller flera offentliga IP-prefix i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="13304-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="13304-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13304-109">EXAMPLES</span></span>

### <span data-ttu-id="13304-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13304-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="13304-111">Det här kommandot får en offentlig IP-prefixlängd med myPublicIpPrefix1 i resurs gruppen myRg</span><span class="sxs-lookup"><span data-stu-id="13304-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="13304-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="13304-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="13304-113">Det här kommandot får alla allmänna IP-adressprefix som börjar med myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="13304-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="13304-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13304-114">PARAMETERS</span></span>

### <span data-ttu-id="13304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13304-115">-DefaultProfile</span></span>
<span data-ttu-id="13304-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13304-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13304-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="13304-117">-Name</span></span>
<span data-ttu-id="13304-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="13304-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="13304-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13304-119">-ResourceGroupName</span></span>
<span data-ttu-id="13304-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="13304-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="13304-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13304-121">-ResourceId</span></span>
<span data-ttu-id="13304-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="13304-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13304-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13304-123">CommonParameters</span></span>
<span data-ttu-id="13304-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13304-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13304-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13304-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13304-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13304-126">INPUTS</span></span>

### <span data-ttu-id="13304-127">System. String</span><span class="sxs-lookup"><span data-stu-id="13304-127">System.String</span></span>

## <span data-ttu-id="13304-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13304-128">OUTPUTS</span></span>

### <span data-ttu-id="13304-129">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13304-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="13304-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13304-130">NOTES</span></span>

## <span data-ttu-id="13304-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13304-131">RELATED LINKS</span></span>

[<span data-ttu-id="13304-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13304-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="13304-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13304-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="13304-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13304-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
