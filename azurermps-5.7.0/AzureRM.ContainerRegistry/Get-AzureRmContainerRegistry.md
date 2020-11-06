---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: dc1b35831de68ad31877be05610d1b075b27452f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584388"
---
# <span data-ttu-id="f29af-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f29af-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="f29af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f29af-102">SYNOPSIS</span></span>
<span data-ttu-id="f29af-103">Hämtar en container-registrering.</span><span class="sxs-lookup"><span data-stu-id="f29af-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f29af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f29af-104">SYNTAX</span></span>

### <span data-ttu-id="f29af-105">ListRegistriesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f29af-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f29af-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f29af-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f29af-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f29af-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f29af-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f29af-108">DESCRIPTION</span></span>
<span data-ttu-id="f29af-109">Get-AzureRmContainerRegistry cmdlet får ett angivet behållar-register eller alla behållar-registren i en resurs grupp eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f29af-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="f29af-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f29af-110">EXAMPLES</span></span>

### <span data-ttu-id="f29af-111">Exempel 1: Hämta ett angivet behållar register</span><span class="sxs-lookup"><span data-stu-id="f29af-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f29af-112">Det här kommandot hämtar den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="f29af-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="f29af-113">Exempel 2: Hämta alla behållar register i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="f29af-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="f29af-114">Det här kommandot får alla behållar register i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f29af-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="f29af-115">Exempel 3: Hämta alla undersöknings register i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="f29af-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

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

<span data-ttu-id="f29af-116">Det här kommandot får alla behållar-registren i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f29af-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="f29af-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f29af-117">PARAMETERS</span></span>

### <span data-ttu-id="f29af-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f29af-118">-Name</span></span>
<span data-ttu-id="f29af-119">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="f29af-119">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f29af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f29af-120">-ResourceGroupName</span></span>
<span data-ttu-id="f29af-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f29af-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListRegistriesParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f29af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29af-122">-DefaultProfile</span></span>
<span data-ttu-id="f29af-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f29af-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f29af-124">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="f29af-124">-IncludeDetail</span></span>
<span data-ttu-id="f29af-125">Visa mer information om behållar registret.</span><span class="sxs-lookup"><span data-stu-id="f29af-125">Show more details about the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29af-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f29af-126">-ResourceId</span></span>
<span data-ttu-id="f29af-127">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="f29af-127">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f29af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29af-128">CommonParameters</span></span>
<span data-ttu-id="f29af-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29af-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f29af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29af-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f29af-131">INPUTS</span></span>

### <span data-ttu-id="f29af-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="f29af-132">None</span></span>
<span data-ttu-id="f29af-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f29af-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f29af-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f29af-134">OUTPUTS</span></span>

### <span data-ttu-id="f29af-135">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f29af-135">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="f29af-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f29af-136">NOTES</span></span>

## <span data-ttu-id="f29af-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f29af-137">RELATED LINKS</span></span>

[<span data-ttu-id="f29af-138">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f29af-138">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="f29af-139">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f29af-139">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="f29af-140">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f29af-140">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

