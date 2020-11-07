---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: a87a11b1e894864593d9558b123b19b6bda06e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745198"
---
# <span data-ttu-id="ee3ba-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="ee3ba-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="ee3ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3ba-103">Hämta eller Visa värdar.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-103">Get or list hosts.</span></span>

## <span data-ttu-id="ee3ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee3ba-104">SYNTAX</span></span>

### <span data-ttu-id="ee3ba-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="ee3ba-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee3ba-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ee3ba-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee3ba-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee3ba-107">DESCRIPTION</span></span>
<span data-ttu-id="ee3ba-108">Denna cmdlet får en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="ee3ba-109">Denna cmdlet visar även alla värd grupper i en resurs grupp om inget värd grupp namn anges.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="ee3ba-110">Denna cmdlet visar även alla värd grupper i ett abonnemang om varken värd grupp namn eller resurs grupp namn anges.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="ee3ba-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee3ba-111">EXAMPLES</span></span>

### <span data-ttu-id="ee3ba-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee3ba-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="ee3ba-113">Det här kommandot returnerar en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-113">This command returns a host group.</span></span>

### <span data-ttu-id="ee3ba-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ee3ba-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="ee3ba-115">Det här kommandot returnerar alla värd grupper i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="ee3ba-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ee3ba-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="ee3ba-117">Det här kommandot returnerar alla värd grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="ee3ba-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee3ba-118">PARAMETERS</span></span>

### <span data-ttu-id="ee3ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3ba-119">-DefaultProfile</span></span>
<span data-ttu-id="ee3ba-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee3ba-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee3ba-121">-Name</span></span>
<span data-ttu-id="ee3ba-122">Namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-122">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee3ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee3ba-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3ba-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee3ba-125">-ResourceId</span></span>
<span data-ttu-id="ee3ba-126">ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="ee3ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3ba-127">CommonParameters</span></span>
<span data-ttu-id="ee3ba-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3ba-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee3ba-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3ba-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee3ba-130">INPUTS</span></span>

### <span data-ttu-id="ee3ba-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ee3ba-131">System.String</span></span>

## <span data-ttu-id="ee3ba-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee3ba-132">OUTPUTS</span></span>

### <span data-ttu-id="ee3ba-133">Microsoft. Azure. commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="ee3ba-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="ee3ba-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee3ba-134">NOTES</span></span>

## <span data-ttu-id="ee3ba-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee3ba-135">RELATED LINKS</span></span>
