---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584619"
---
# <span data-ttu-id="e4ce7-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e4ce7-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="e4ce7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ce7-103">Tar bort en väg från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4ce7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4ce7-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4ce7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ce7-106">Cmdleten **Remove-AzureRmRouteConfig** tar bort en väg från en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="e4ce7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="e4ce7-108">Exempel 1: ta bort en väg</span><span class="sxs-lookup"><span data-stu-id="e4ce7-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="e4ce7-109">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av cmdleten **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="e4ce7-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="e4ce7-110">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e4ce7-111">Den aktuella cmdleten tar bort vägen med namnet Route02 och skickar resultatet till cmdleten **set-AzureRmRouteTable** , som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="e4ce7-112">Tabellen innehåller inte längre vägen med namnet Route02.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="e4ce7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4ce7-113">PARAMETERS</span></span>

### <span data-ttu-id="e4ce7-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4ce7-114">-Name</span></span>
<span data-ttu-id="e4ce7-115">Anger namnet på den väg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-115">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4ce7-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e4ce7-116">-RouteTable</span></span>
<span data-ttu-id="e4ce7-117">Anger den routningstabell som innehåller vägen som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ce7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ce7-118">-DefaultProfile</span></span>
<span data-ttu-id="e4ce7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4ce7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ce7-120">CommonParameters</span></span>
<span data-ttu-id="e4ce7-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ce7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ce7-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ce7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ce7-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4ce7-123">INPUTS</span></span>

### <span data-ttu-id="e4ce7-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4ce7-124">PSRouteTable</span></span>
<span data-ttu-id="e4ce7-125">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e4ce7-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="e4ce7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4ce7-126">OUTPUTS</span></span>

### <span data-ttu-id="e4ce7-127">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4ce7-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e4ce7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4ce7-128">NOTES</span></span>

## <span data-ttu-id="e4ce7-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4ce7-129">RELATED LINKS</span></span>

[<span data-ttu-id="e4ce7-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e4ce7-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="e4ce7-131">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e4ce7-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="e4ce7-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e4ce7-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="e4ce7-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e4ce7-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


