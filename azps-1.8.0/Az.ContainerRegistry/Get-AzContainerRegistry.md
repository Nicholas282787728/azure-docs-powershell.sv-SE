---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: d0ba9315efd61657359bb45883b83cb2bae0095a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754416"
---
# <span data-ttu-id="d3976-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d3976-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="d3976-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3976-102">SYNOPSIS</span></span>
<span data-ttu-id="d3976-103">Hämtar en container-registrering.</span><span class="sxs-lookup"><span data-stu-id="d3976-103">Gets a container registry.</span></span>

## <span data-ttu-id="d3976-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3976-104">SYNTAX</span></span>

### <span data-ttu-id="d3976-105">ListRegistriesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d3976-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3976-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3976-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3976-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3976-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3976-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3976-108">DESCRIPTION</span></span>
<span data-ttu-id="d3976-109">Get-AzContainerRegistry cmdlet får ett angivet behållar-register eller alla behållar-registren i en resurs grupp eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d3976-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="d3976-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3976-110">EXAMPLES</span></span>

### <span data-ttu-id="d3976-111">Exempel 1: Hämta ett angivet behållar register</span><span class="sxs-lookup"><span data-stu-id="d3976-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d3976-112">Det här kommandot hämtar den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d3976-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="d3976-113">Exempel 2: Hämta alla behållar register i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d3976-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="d3976-114">Det här kommandot får alla behållar register i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d3976-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="d3976-115">Exempel 3: Hämta alla undersöknings register i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="d3976-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="d3976-116">Det här kommandot får alla behållar-registren i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d3976-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="d3976-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3976-117">PARAMETERS</span></span>

### <span data-ttu-id="d3976-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3976-118">-DefaultProfile</span></span>
<span data-ttu-id="d3976-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d3976-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3976-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="d3976-120">-IncludeDetail</span></span>
<span data-ttu-id="d3976-121">Visa mer information om behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d3976-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="d3976-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3976-122">-Name</span></span>
<span data-ttu-id="d3976-123">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="d3976-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3976-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3976-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3976-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d3976-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3976-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3976-126">-ResourceId</span></span>
<span data-ttu-id="d3976-127">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="d3976-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3976-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3976-128">CommonParameters</span></span>
<span data-ttu-id="d3976-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3976-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3976-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3976-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3976-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3976-131">INPUTS</span></span>

### <span data-ttu-id="d3976-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d3976-132">System.String</span></span>

## <span data-ttu-id="d3976-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3976-133">OUTPUTS</span></span>

### <span data-ttu-id="d3976-134">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d3976-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d3976-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3976-135">NOTES</span></span>

## <span data-ttu-id="d3976-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3976-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3976-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d3976-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="d3976-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d3976-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="d3976-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d3976-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

