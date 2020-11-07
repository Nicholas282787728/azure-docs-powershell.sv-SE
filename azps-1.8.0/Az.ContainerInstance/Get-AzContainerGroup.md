---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 79f71c31f1a04b350733465338e9edcbd281af5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754422"
---
# <span data-ttu-id="90e15-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="90e15-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="90e15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90e15-102">SYNOPSIS</span></span>
<span data-ttu-id="90e15-103">Hämtar behållar grupper.</span><span class="sxs-lookup"><span data-stu-id="90e15-103">Gets container groups.</span></span>

## <span data-ttu-id="90e15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90e15-104">SYNTAX</span></span>

### <span data-ttu-id="90e15-105">ListContainerGroupParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="90e15-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90e15-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="90e15-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90e15-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="90e15-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90e15-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90e15-108">DESCRIPTION</span></span>
<span data-ttu-id="90e15-109">Cmdleten **Get-AzContainerGroup** hämtar en angiven behållar grupp eller alla behållar grupper i en resurs grupp eller abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="90e15-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="90e15-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90e15-110">EXAMPLES</span></span>

### <span data-ttu-id="90e15-111">Exempel 1: hämtar en angiven behållar grupp</span><span class="sxs-lookup"><span data-stu-id="90e15-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="90e15-112">Kommandot hämtar den angivna behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="90e15-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="90e15-113">Exempel 2: hämtar behållar grupper i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="90e15-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="90e15-114">Kommandot hämtar behållar grupperna i resurs gruppen `demo` .</span><span class="sxs-lookup"><span data-stu-id="90e15-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="90e15-115">Exempel 3: hämtar behållar grupper i den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="90e15-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="90e15-116">Kommandot hämtar behållar grupperna i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="90e15-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="90e15-117">Exempel 4: hämtar behållar grupper med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="90e15-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="90e15-118">Kommandot hämtar behållar gruppen med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="90e15-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="90e15-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90e15-119">PARAMETERS</span></span>

### <span data-ttu-id="90e15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e15-120">-DefaultProfile</span></span>
<span data-ttu-id="90e15-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90e15-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90e15-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="90e15-122">-Name</span></span>
<span data-ttu-id="90e15-123">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="90e15-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e15-124">-ResourceGroupName</span></span>
<span data-ttu-id="90e15-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="90e15-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e15-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90e15-126">-ResourceId</span></span>
<span data-ttu-id="90e15-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="90e15-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e15-128">CommonParameters</span></span>
<span data-ttu-id="90e15-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e15-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e15-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e15-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90e15-131">INPUTS</span></span>

### <span data-ttu-id="90e15-132">System. String</span><span class="sxs-lookup"><span data-stu-id="90e15-132">System.String</span></span>

## <span data-ttu-id="90e15-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90e15-133">OUTPUTS</span></span>

### <span data-ttu-id="90e15-134">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="90e15-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="90e15-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90e15-135">NOTES</span></span>

## <span data-ttu-id="90e15-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90e15-136">RELATED LINKS</span></span>
