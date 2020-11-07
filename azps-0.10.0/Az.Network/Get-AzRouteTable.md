---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922218"
---
# <span data-ttu-id="61bbf-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="61bbf-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="61bbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="61bbf-103">Hämtar routningstabeller.</span><span class="sxs-lookup"><span data-stu-id="61bbf-103">Gets route tables.</span></span>

## <span data-ttu-id="61bbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61bbf-104">SYNTAX</span></span>

### <span data-ttu-id="61bbf-105">Byggnad</span><span class="sxs-lookup"><span data-stu-id="61bbf-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61bbf-106">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="61bbf-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61bbf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61bbf-107">DESCRIPTION</span></span>
<span data-ttu-id="61bbf-108">Cmdleten **Get-AzRouteTable** får Azure Route-tabeller.</span><span class="sxs-lookup"><span data-stu-id="61bbf-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="61bbf-109">Du kan hämta en enda routningstabell eller hämta alla väg tabeller i en resurs grupp eller i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="61bbf-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="61bbf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61bbf-110">EXAMPLES</span></span>

### <span data-ttu-id="61bbf-111">Exempel 1: Hämta en routningstabell</span><span class="sxs-lookup"><span data-stu-id="61bbf-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="61bbf-112">Det här kommandot hämtar routningstabellen med namnet RouteTable01 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="61bbf-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="61bbf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61bbf-113">PARAMETERS</span></span>

### <span data-ttu-id="61bbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bbf-114">-DefaultProfile</span></span>
<span data-ttu-id="61bbf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61bbf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bbf-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="61bbf-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bbf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="61bbf-117">-Name</span></span>
<span data-ttu-id="61bbf-118">Anger namnet på den routningstabell som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="61bbf-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bbf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bbf-119">-ResourceGroupName</span></span>
<span data-ttu-id="61bbf-120">Anger namnet på den resurs grupp som innehåller de väg tabeller som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="61bbf-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bbf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bbf-121">CommonParameters</span></span>
<span data-ttu-id="61bbf-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61bbf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bbf-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bbf-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bbf-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61bbf-124">INPUTS</span></span>

## <span data-ttu-id="61bbf-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61bbf-125">OUTPUTS</span></span>

### <span data-ttu-id="61bbf-126">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="61bbf-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="61bbf-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61bbf-127">NOTES</span></span>

## <span data-ttu-id="61bbf-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61bbf-128">RELATED LINKS</span></span>

[<span data-ttu-id="61bbf-129">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="61bbf-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="61bbf-130">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="61bbf-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="61bbf-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="61bbf-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


