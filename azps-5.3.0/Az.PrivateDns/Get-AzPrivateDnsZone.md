---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523098"
---
# <span data-ttu-id="a3177-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3177-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="a3177-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3177-102">SYNOPSIS</span></span>
<span data-ttu-id="a3177-103">Hämtar en privat DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="a3177-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="a3177-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3177-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3177-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3177-105">DESCRIPTION</span></span>
<span data-ttu-id="a3177-106">Cmdleten **Get-AzPrivateDnsZone** har en privat DNS-zon (Domain Name System) från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a3177-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="a3177-107">Om du anger parametern *Name* returneras ett enskilt **PrivateDnsZone** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a3177-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="a3177-108">Om du inte anger parametern *Name* returneras en matris med alla zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a3177-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="a3177-109">Du kan använda **PrivateDnsZone** -objektet för att uppdatera zonen, till exempel att du kan lägga till **Recordset** -objekt i den.</span><span class="sxs-lookup"><span data-stu-id="a3177-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="a3177-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3177-110">EXAMPLES</span></span>

### <span data-ttu-id="a3177-111">Exempel 1: Hämta en zon</span><span class="sxs-lookup"><span data-stu-id="a3177-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="a3177-112">Exempel 2: Hämta alla zoner i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a3177-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="a3177-113">Det här exemplet får alla de privata DNS-zonerna i den angivna resurs gruppen och lagrar dem sedan i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="a3177-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="a3177-114">Exempel 3: Hämta alla zoner i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="a3177-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="a3177-115">Det här exemplet får alla de privata DNS-zonerna i det aktuella Azure-abonnemanget och lagrar dem i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="a3177-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="a3177-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3177-116">PARAMETERS</span></span>

### <span data-ttu-id="a3177-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3177-117">-DefaultProfile</span></span>
<span data-ttu-id="a3177-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a3177-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3177-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3177-119">-Name</span></span>
<span data-ttu-id="a3177-120">Anger namnet på den privata DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a3177-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="a3177-121">Om du inte anger ett värde för parametern *Name* får denna cmdlet alla privata DNS-zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a3177-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="a3177-122">Om du också utelämnar parametern *ResourceGroupName* blir denna cmdlet alla privata DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a3177-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3177-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3177-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3177-124">Anger namnet på den resurs grupp som innehåller den privata DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a3177-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="a3177-125">Om du inte anger *ResourceGroupName* måste du också utelämna parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="a3177-125">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="a3177-126">I det här fallet hämtar denna cmdlet alla privata DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a3177-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3177-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3177-127">CommonParameters</span></span>
<span data-ttu-id="a3177-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3177-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3177-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3177-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3177-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3177-130">INPUTS</span></span>

### <span data-ttu-id="a3177-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3177-131">None</span></span>

## <span data-ttu-id="a3177-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3177-132">OUTPUTS</span></span>

### <span data-ttu-id="a3177-133">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3177-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="a3177-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3177-134">NOTES</span></span>

## <span data-ttu-id="a3177-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3177-135">RELATED LINKS</span></span>

[<span data-ttu-id="a3177-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3177-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="a3177-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3177-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="a3177-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3177-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
