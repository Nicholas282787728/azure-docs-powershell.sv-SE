---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: 692a32372718ee3100bd0ad0038d7ff89d483654
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101370"
---
# <span data-ttu-id="d97ee-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="d97ee-101">Get-AzHost</span></span>

## <span data-ttu-id="d97ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d97ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d97ee-103">Hämta eller Visa värdar.</span><span class="sxs-lookup"><span data-stu-id="d97ee-103">Get or list hosts.</span></span>

## <span data-ttu-id="d97ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d97ee-104">SYNTAX</span></span>

### <span data-ttu-id="d97ee-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="d97ee-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d97ee-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d97ee-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d97ee-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d97ee-107">DESCRIPTION</span></span>
<span data-ttu-id="d97ee-108">Denna cmdlet får en värd i en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="d97ee-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="d97ee-109">Denna cmdlet listar också alla värdar i en värd grupp om ett värdnamn inte anges.</span><span class="sxs-lookup"><span data-stu-id="d97ee-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="d97ee-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d97ee-110">EXAMPLES</span></span>

### <span data-ttu-id="d97ee-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d97ee-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="d97ee-112">Det här kommandot returnerar en värd.</span><span class="sxs-lookup"><span data-stu-id="d97ee-112">This command returns a host.</span></span>

### <span data-ttu-id="d97ee-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d97ee-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="d97ee-114">Det här kommandot returnerar instans vyn för en värd.</span><span class="sxs-lookup"><span data-stu-id="d97ee-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="d97ee-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d97ee-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="d97ee-116">Det här kommandot returnerar alla värdar i den angivna värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="d97ee-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="d97ee-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d97ee-117">PARAMETERS</span></span>

### <span data-ttu-id="d97ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97ee-118">-DefaultProfile</span></span>
<span data-ttu-id="d97ee-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d97ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d97ee-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="d97ee-120">-HostGroupName</span></span>
<span data-ttu-id="d97ee-121">Namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="d97ee-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97ee-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="d97ee-122">-InstanceView</span></span>
<span data-ttu-id="d97ee-123">Anger att den här cmdleten bara får instans av värden.</span><span class="sxs-lookup"><span data-stu-id="d97ee-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97ee-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="d97ee-124">-Name</span></span>
<span data-ttu-id="d97ee-125">Namnet på värden.</span><span class="sxs-lookup"><span data-stu-id="d97ee-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="d97ee-127">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d97ee-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97ee-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d97ee-128">-ResourceId</span></span>
<span data-ttu-id="d97ee-129">ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="d97ee-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97ee-130">CommonParameters</span></span>
<span data-ttu-id="d97ee-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97ee-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d97ee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97ee-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d97ee-133">INPUTS</span></span>

### <span data-ttu-id="d97ee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d97ee-134">System.String</span></span>

## <span data-ttu-id="d97ee-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d97ee-135">OUTPUTS</span></span>

### <span data-ttu-id="d97ee-136">Microsoft. Azure. commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="d97ee-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="d97ee-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d97ee-137">NOTES</span></span>

## <span data-ttu-id="d97ee-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d97ee-138">RELATED LINKS</span></span>
