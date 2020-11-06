---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583824"
---
# <span data-ttu-id="59ee2-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59ee2-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="59ee2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="59ee2-103">Uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="59ee2-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59ee2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59ee2-104">SYNTAX</span></span>

### <span data-ttu-id="59ee2-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="59ee2-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59ee2-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="59ee2-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59ee2-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="59ee2-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59ee2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59ee2-108">DESCRIPTION</span></span>
<span data-ttu-id="59ee2-109">Cmdleten **Update-AzureRmContainerRegistry** uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="59ee2-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="59ee2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59ee2-110">EXAMPLES</span></span>

### <span data-ttu-id="59ee2-111">Exempel 1: Aktivera administratörs användare för ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="59ee2-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

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

<span data-ttu-id="59ee2-112">Det här kommandot aktiverar administratörs användaren för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="59ee2-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="59ee2-113">Exempel 2: Ange det lagrings konto som används av ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="59ee2-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="59ee2-114">Det här kommandot anger det angivna testregistret för att använda ett befintligt lagrings konto `mystorageaccount` i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="59ee2-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="59ee2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59ee2-115">PARAMETERS</span></span>

### <span data-ttu-id="59ee2-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="59ee2-116">-DisableAdminUser</span></span>
<span data-ttu-id="59ee2-117">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="59ee2-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ee2-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="59ee2-118">-EnableAdminUser</span></span>
<span data-ttu-id="59ee2-119">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="59ee2-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ee2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="59ee2-120">-Name</span></span>
<span data-ttu-id="59ee2-121">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="59ee2-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="59ee2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ee2-122">-ResourceGroupName</span></span>
<span data-ttu-id="59ee2-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="59ee2-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="59ee2-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="59ee2-124">-StorageAccountName</span></span>
<span data-ttu-id="59ee2-125">Namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="59ee2-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="59ee2-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="59ee2-126">-Tag</span></span>
<span data-ttu-id="59ee2-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="59ee2-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59ee2-128">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="59ee2-128">For example:</span></span>

<span data-ttu-id="59ee2-129">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="59ee2-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59ee2-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59ee2-130">-Confirm</span></span>
<span data-ttu-id="59ee2-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59ee2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59ee2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59ee2-132">-WhatIf</span></span>
<span data-ttu-id="59ee2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59ee2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59ee2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59ee2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59ee2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ee2-135">-DefaultProfile</span></span>
<span data-ttu-id="59ee2-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59ee2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59ee2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ee2-137">CommonParameters</span></span>
<span data-ttu-id="59ee2-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ee2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ee2-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ee2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ee2-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59ee2-140">INPUTS</span></span>

## <span data-ttu-id="59ee2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59ee2-141">OUTPUTS</span></span>

### <span data-ttu-id="59ee2-142">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59ee2-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="59ee2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59ee2-143">NOTES</span></span>

## <span data-ttu-id="59ee2-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59ee2-144">RELATED LINKS</span></span>

[<span data-ttu-id="59ee2-145">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59ee2-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="59ee2-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59ee2-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="59ee2-147">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59ee2-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
