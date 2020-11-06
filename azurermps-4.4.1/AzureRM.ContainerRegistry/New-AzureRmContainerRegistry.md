---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574990"
---
# <span data-ttu-id="c56d2-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c56d2-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="c56d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c56d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c56d2-103">Skapar ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="c56d2-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c56d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c56d2-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c56d2-105">DESCRIPTION</span></span>
<span data-ttu-id="c56d2-106">Cmdleten **New-AzureRmContainerRegistry** skapar en container-registrering.</span><span class="sxs-lookup"><span data-stu-id="c56d2-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="c56d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c56d2-107">EXAMPLES</span></span>

### <span data-ttu-id="c56d2-108">Exempel 1: skapa ett behållar register med ett nytt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c56d2-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="c56d2-109">Det här kommandot skapar ett behållar register med ett nytt lagrings konto i resurs gruppen `MyResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="c56d2-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="c56d2-110">Exempel 2: skapa en behållare med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="c56d2-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="c56d2-111">Det här kommandot skapar ett behållar register med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="c56d2-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="c56d2-112">Exempel 3: skapa ett behållar register med ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c56d2-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : mystorageaccount
```

<span data-ttu-id="c56d2-113">Det här kommandot skapar ett behållar register med ett befintligt lagrings konto `mystorageaccount` i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c56d2-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="c56d2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c56d2-114">PARAMETERS</span></span>

### <span data-ttu-id="c56d2-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="c56d2-115">-EnableAdminUser</span></span>
<span data-ttu-id="c56d2-116">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="c56d2-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56d2-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="c56d2-117">-Location</span></span>
<span data-ttu-id="c56d2-118">Behållarens register plats.</span><span class="sxs-lookup"><span data-stu-id="c56d2-118">Container Registry Location.</span></span>
<span data-ttu-id="c56d2-119">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c56d2-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c56d2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c56d2-120">-Name</span></span>
<span data-ttu-id="c56d2-121">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="c56d2-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="c56d2-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c56d2-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56d2-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="c56d2-124">-Sku</span></span>
<span data-ttu-id="c56d2-125">SKU för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="c56d2-125">Container Registry SKU.</span></span>
<span data-ttu-id="c56d2-126">Tillåtna värden: grundläggande.</span><span class="sxs-lookup"><span data-stu-id="c56d2-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56d2-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c56d2-127">-StorageAccountName</span></span>
<span data-ttu-id="c56d2-128">Namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c56d2-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="c56d2-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c56d2-129">-Tag</span></span>
<span data-ttu-id="c56d2-130">Register märken för behållare. nyckel värde par i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c56d2-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c56d2-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c56d2-131">For example:</span></span>

<span data-ttu-id="c56d2-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c56d2-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56d2-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c56d2-133">-Confirm</span></span>
<span data-ttu-id="c56d2-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c56d2-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56d2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56d2-135">-WhatIf</span></span>
<span data-ttu-id="c56d2-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c56d2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56d2-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c56d2-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56d2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56d2-138">-DefaultProfile</span></span>
<span data-ttu-id="c56d2-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c56d2-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c56d2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56d2-140">CommonParameters</span></span>
<span data-ttu-id="c56d2-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56d2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56d2-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56d2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56d2-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c56d2-143">INPUTS</span></span>

## <span data-ttu-id="c56d2-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c56d2-144">OUTPUTS</span></span>

### <span data-ttu-id="c56d2-145">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c56d2-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c56d2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c56d2-146">NOTES</span></span>

## <span data-ttu-id="c56d2-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c56d2-147">RELATED LINKS</span></span>

[<span data-ttu-id="c56d2-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c56d2-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="c56d2-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c56d2-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c56d2-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c56d2-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
