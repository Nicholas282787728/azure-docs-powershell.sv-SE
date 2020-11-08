---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260846"
---
# <span data-ttu-id="f963b-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f963b-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="f963b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f963b-102">SYNOPSIS</span></span>
<span data-ttu-id="f963b-103">Hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f963b-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="f963b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f963b-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f963b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f963b-105">DESCRIPTION</span></span>
<span data-ttu-id="f963b-106">Cmdleten **Get-AzAvailabilitySet** hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f963b-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="f963b-107">Du kan ange namnet på en specifik tillgänglighets uppsättning som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="f963b-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="f963b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f963b-108">EXAMPLES</span></span>

### <span data-ttu-id="f963b-109">Exempel 1: skaffa en specifik tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="f963b-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f963b-110">Det här kommandot får tillgänglighets uppsättningen som heter AvailabilitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f963b-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f963b-111">Exempel 2: Hämta alla tillgänglighets uppsättningar</span><span class="sxs-lookup"><span data-stu-id="f963b-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f963b-112">Det här kommandot får alla tillgänglighets uppsättningar i resurs gruppen "ResourceGroup11".</span><span class="sxs-lookup"><span data-stu-id="f963b-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f963b-113">Exempel 3: Hämta alla tillgänglighets uppsättningar med filtrering</span><span class="sxs-lookup"><span data-stu-id="f963b-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f963b-114">Det här kommandot får alla tillgänglighets uppsättningar i resurs gruppen "ResourceGroup11" som börjar med "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="f963b-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="f963b-115">Exempel 4: Hämta alla tillgänglighets uppsättningar med namn som börjar på AvailabilitySet0</span><span class="sxs-lookup"><span data-stu-id="f963b-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f963b-116">Det här kommandot får alla tillgänglighets uppsättningar som börjar med "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="f963b-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="f963b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f963b-117">PARAMETERS</span></span>

### <span data-ttu-id="f963b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f963b-118">-DefaultProfile</span></span>
<span data-ttu-id="f963b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f963b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f963b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f963b-120">-Name</span></span>
<span data-ttu-id="f963b-121">Anger namnet på en tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="f963b-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f963b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f963b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f963b-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f963b-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f963b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f963b-124">CommonParameters</span></span>
<span data-ttu-id="f963b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f963b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f963b-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f963b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f963b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f963b-127">INPUTS</span></span>

### <span data-ttu-id="f963b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f963b-128">System.String</span></span>

## <span data-ttu-id="f963b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f963b-129">OUTPUTS</span></span>

### <span data-ttu-id="f963b-130">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f963b-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f963b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f963b-131">NOTES</span></span>

## <span data-ttu-id="f963b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f963b-132">RELATED LINKS</span></span>

[<span data-ttu-id="f963b-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f963b-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="f963b-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f963b-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


