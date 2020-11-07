---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: f97f7ca82ae17c61994a84fbc4b1405b41fdb566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586191"
---
# <span data-ttu-id="ecc53-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ecc53-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="ecc53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecc53-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc53-103">Hämtar behållar grupper.</span><span class="sxs-lookup"><span data-stu-id="ecc53-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecc53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecc53-104">SYNTAX</span></span>

### <span data-ttu-id="ecc53-105">ListContainerGroupParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ecc53-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecc53-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ecc53-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecc53-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="ecc53-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc53-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecc53-108">DESCRIPTION</span></span>
<span data-ttu-id="ecc53-109">Cmdleten **Get-AzureRmContainerGroup** hämtar en angiven behållar grupp eller alla behållar grupper i en resurs grupp eller abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ecc53-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="ecc53-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecc53-110">EXAMPLES</span></span>

### <span data-ttu-id="ecc53-111">Exempel 1: hämtar en angiven behållar grupp</span><span class="sxs-lookup"><span data-stu-id="ecc53-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

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
```

<span data-ttu-id="ecc53-112">Kommandot hämtar den angivna behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="ecc53-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="ecc53-113">Exempel 2: hämtar behållar grupper i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ecc53-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="ecc53-114">Kommandot hämtar behållar grupperna i resurs gruppen `demo` .</span><span class="sxs-lookup"><span data-stu-id="ecc53-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="ecc53-115">Exempel 3: hämtar behållar grupper i den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="ecc53-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="ecc53-116">Kommandot hämtar behållar grupperna i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ecc53-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="ecc53-117">Exempel 4: hämtar behållar grupper med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ecc53-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

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
```

<span data-ttu-id="ecc53-118">Kommandot hämtar behållar gruppen med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ecc53-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="ecc53-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecc53-119">PARAMETERS</span></span>

### <span data-ttu-id="ecc53-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecc53-120">-Name</span></span>
<span data-ttu-id="ecc53-121">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="ecc53-121">The container group Name.</span></span>

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

### <span data-ttu-id="ecc53-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc53-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecc53-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ecc53-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="ecc53-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc53-124">-ResourceId</span></span>
<span data-ttu-id="ecc53-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ecc53-125">The resource id.</span></span>

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

### <span data-ttu-id="ecc53-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc53-126">-DefaultProfile</span></span>
<span data-ttu-id="ecc53-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc53-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc53-128">CommonParameters</span></span>
<span data-ttu-id="ecc53-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc53-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecc53-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc53-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecc53-131">INPUTS</span></span>

### <span data-ttu-id="ecc53-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ecc53-132">System.String</span></span>

## <span data-ttu-id="ecc53-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecc53-133">OUTPUTS</span></span>

### <span data-ttu-id="ecc53-134">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ecc53-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="ecc53-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecc53-135">NOTES</span></span>

## <span data-ttu-id="ecc53-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecc53-136">RELATED LINKS</span></span>
