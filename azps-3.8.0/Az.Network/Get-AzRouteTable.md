---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091015"
---
# <span data-ttu-id="cc03e-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cc03e-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="cc03e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc03e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc03e-103">Hämtar routningstabeller.</span><span class="sxs-lookup"><span data-stu-id="cc03e-103">Gets route tables.</span></span>

## <span data-ttu-id="cc03e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc03e-104">SYNTAX</span></span>

### <span data-ttu-id="cc03e-105">Noexpandering (standard)</span><span class="sxs-lookup"><span data-stu-id="cc03e-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc03e-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="cc03e-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc03e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc03e-107">DESCRIPTION</span></span>
<span data-ttu-id="cc03e-108">Cmdleten **Get-AzRouteTable** får Azure Route-tabeller.</span><span class="sxs-lookup"><span data-stu-id="cc03e-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="cc03e-109">Du kan hämta en enda routningstabell eller hämta alla väg tabeller i en resurs grupp eller i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="cc03e-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="cc03e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc03e-110">EXAMPLES</span></span>

### <span data-ttu-id="cc03e-111">Exempel 1: Hämta en routningstabell</span><span class="sxs-lookup"><span data-stu-id="cc03e-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="cc03e-112">Det här kommandot hämtar routningstabellen med namnet RouteTable01 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cc03e-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="cc03e-113">Exempel 2: lista väg tabeller med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="cc03e-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="cc03e-114">Det här kommandot får alla väg tabeller vars namn börjar med "RouteTable"</span><span class="sxs-lookup"><span data-stu-id="cc03e-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="cc03e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc03e-115">PARAMETERS</span></span>

### <span data-ttu-id="cc03e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc03e-116">-DefaultProfile</span></span>
<span data-ttu-id="cc03e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc03e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc03e-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cc03e-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc03e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc03e-119">-Name</span></span>
<span data-ttu-id="cc03e-120">Anger namnet på den routningstabell som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="cc03e-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cc03e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc03e-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc03e-122">Anger namnet på den resurs grupp som innehåller de väg tabeller som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="cc03e-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cc03e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc03e-123">CommonParameters</span></span>
<span data-ttu-id="cc03e-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc03e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc03e-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc03e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc03e-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc03e-126">INPUTS</span></span>

### <span data-ttu-id="cc03e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cc03e-127">System.String</span></span>

## <span data-ttu-id="cc03e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc03e-128">OUTPUTS</span></span>

### <span data-ttu-id="cc03e-129">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="cc03e-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="cc03e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc03e-130">NOTES</span></span>

## <span data-ttu-id="cc03e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc03e-131">RELATED LINKS</span></span>

[<span data-ttu-id="cc03e-132">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cc03e-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="cc03e-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cc03e-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="cc03e-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cc03e-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)

