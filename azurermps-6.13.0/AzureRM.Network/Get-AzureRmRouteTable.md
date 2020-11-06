---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 04e50033a304918eb37d28c2ef5ea5328d5744c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576899"
---
# <span data-ttu-id="41821-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="41821-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="41821-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41821-102">SYNOPSIS</span></span>
<span data-ttu-id="41821-103">Hämtar routningstabeller.</span><span class="sxs-lookup"><span data-stu-id="41821-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41821-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41821-104">SYNTAX</span></span>

### <span data-ttu-id="41821-105">Noexpandering (standard)</span><span class="sxs-lookup"><span data-stu-id="41821-105">NoExpand (Default)</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41821-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="41821-106">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41821-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41821-107">DESCRIPTION</span></span>
<span data-ttu-id="41821-108">Cmdleten **Get-AzureRmRouteTable** får Azure Route-tabeller.</span><span class="sxs-lookup"><span data-stu-id="41821-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="41821-109">Du kan hämta en enda routningstabell eller hämta alla väg tabeller i en resurs grupp eller i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="41821-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="41821-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41821-110">EXAMPLES</span></span>

### <span data-ttu-id="41821-111">Exempel 1: Hämta en routningstabell</span><span class="sxs-lookup"><span data-stu-id="41821-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="41821-112">Det här kommandot hämtar routningstabellen med namnet RouteTable01 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="41821-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="41821-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41821-113">PARAMETERS</span></span>

### <span data-ttu-id="41821-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41821-114">-DefaultProfile</span></span>
<span data-ttu-id="41821-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41821-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41821-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="41821-116">-ExpandResource</span></span>
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

### <span data-ttu-id="41821-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="41821-117">-Name</span></span>
<span data-ttu-id="41821-118">Anger namnet på den routningstabell som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="41821-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41821-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41821-119">-ResourceGroupName</span></span>
<span data-ttu-id="41821-120">Anger namnet på den resurs grupp som innehåller de väg tabeller som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="41821-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="41821-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41821-121">CommonParameters</span></span>
<span data-ttu-id="41821-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41821-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41821-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41821-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41821-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41821-124">INPUTS</span></span>

### <span data-ttu-id="41821-125">System. String</span><span class="sxs-lookup"><span data-stu-id="41821-125">System.String</span></span>

## <span data-ttu-id="41821-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41821-126">OUTPUTS</span></span>

### <span data-ttu-id="41821-127">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="41821-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="41821-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41821-128">NOTES</span></span>

## <span data-ttu-id="41821-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41821-129">RELATED LINKS</span></span>

[<span data-ttu-id="41821-130">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="41821-130">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="41821-131">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="41821-131">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="41821-132">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="41821-132">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


