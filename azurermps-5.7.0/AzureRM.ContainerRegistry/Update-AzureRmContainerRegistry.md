---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578271"
---
# <span data-ttu-id="a558a-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a558a-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="a558a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a558a-102">SYNOPSIS</span></span>
<span data-ttu-id="a558a-103">Uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="a558a-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a558a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a558a-104">SYNTAX</span></span>

### <span data-ttu-id="a558a-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a558a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a558a-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a558a-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a558a-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a558a-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a558a-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a558a-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a558a-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a558a-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a558a-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a558a-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a558a-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a558a-111">DESCRIPTION</span></span>
<span data-ttu-id="a558a-112">Update-AzureRmContainerRegistry cmdlet uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="a558a-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="a558a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a558a-113">EXAMPLES</span></span>

### <span data-ttu-id="a558a-114">Exempel 1: Aktivera administratörs användare för ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="a558a-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="a558a-115">Det här kommandot aktiverar administratörs användaren för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="a558a-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="a558a-116">Exempel 2: Ange det lagrings konto som används av ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="a558a-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="a558a-117">Det här kommandot anger det angivna behållar-registret så att det använder ett befintligt lagrings konto \` mystorageaccount \` i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a558a-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="a558a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a558a-118">PARAMETERS</span></span>

### <span data-ttu-id="a558a-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="a558a-119">-DisableAdminUser</span></span>
<span data-ttu-id="a558a-120">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="a558a-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="a558a-121">-EnableAdminUser</span></span>
<span data-ttu-id="a558a-122">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="a558a-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a558a-123">-Name</span></span>
<span data-ttu-id="a558a-124">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="a558a-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a558a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a558a-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a558a-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a558a-127">-StorageAccountName</span></span>
<span data-ttu-id="a558a-128">Namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a558a-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a558a-129">-Tag</span></span>
<span data-ttu-id="a558a-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a558a-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="a558a-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="a558a-131">For example:</span></span>

<span data-ttu-id="a558a-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a558a-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a558a-133">-Confirm</span></span>
<span data-ttu-id="a558a-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a558a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a558a-135">-WhatIf</span></span>
<span data-ttu-id="a558a-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a558a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a558a-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a558a-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a558a-138">-DefaultProfile</span></span>
<span data-ttu-id="a558a-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a558a-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a558a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a558a-140">-ResourceId</span></span>
<span data-ttu-id="a558a-141">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="a558a-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="a558a-142">-Sku</span></span>
<span data-ttu-id="a558a-143">SKU för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="a558a-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a558a-144">CommonParameters</span></span>
<span data-ttu-id="a558a-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a558a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a558a-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a558a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a558a-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a558a-147">INPUTS</span></span>

### <span data-ttu-id="a558a-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="a558a-148">None</span></span>
<span data-ttu-id="a558a-149">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a558a-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a558a-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a558a-150">OUTPUTS</span></span>

### <span data-ttu-id="a558a-151">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a558a-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="a558a-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a558a-152">NOTES</span></span>

## <span data-ttu-id="a558a-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a558a-153">RELATED LINKS</span></span>

[<span data-ttu-id="a558a-154">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a558a-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="a558a-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a558a-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="a558a-156">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a558a-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

