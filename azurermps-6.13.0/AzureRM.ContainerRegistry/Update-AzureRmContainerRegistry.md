---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 10321e780532cd522e7cc1d4532baa360350c324
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755341"
---
# <span data-ttu-id="82623-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82623-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="82623-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82623-102">SYNOPSIS</span></span>
<span data-ttu-id="82623-103">Uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="82623-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82623-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82623-104">SYNTAX</span></span>

### <span data-ttu-id="82623-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="82623-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82623-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="82623-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82623-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="82623-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82623-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82623-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82623-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82623-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82623-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82623-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82623-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82623-111">DESCRIPTION</span></span>
<span data-ttu-id="82623-112">Update-AzureRmContainerRegistry cmdlet uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="82623-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="82623-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82623-113">EXAMPLES</span></span>

### <span data-ttu-id="82623-114">Exempel 1: Aktivera administratörs användare för ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="82623-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="82623-115">Det här kommandot aktiverar administratörs användaren för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="82623-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="82623-116">Exempel 2: Ange det lagrings konto som används av ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="82623-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="82623-117">Det här kommandot anger det angivna behållar-registret så att det använder ett befintligt lagrings konto \` mystorageaccount \` i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="82623-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="82623-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82623-118">PARAMETERS</span></span>

### <span data-ttu-id="82623-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82623-119">-DefaultProfile</span></span>
<span data-ttu-id="82623-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="82623-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82623-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="82623-121">-DisableAdminUser</span></span>
<span data-ttu-id="82623-122">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="82623-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82623-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="82623-123">-EnableAdminUser</span></span>
<span data-ttu-id="82623-124">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="82623-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82623-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="82623-125">-Name</span></span>
<span data-ttu-id="82623-126">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="82623-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82623-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82623-127">-ResourceGroupName</span></span>
<span data-ttu-id="82623-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="82623-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82623-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82623-129">-ResourceId</span></span>
<span data-ttu-id="82623-130">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="82623-130">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82623-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="82623-131">-Sku</span></span>
<span data-ttu-id="82623-132">SKU för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="82623-132">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82623-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="82623-133">-StorageAccountName</span></span>
<span data-ttu-id="82623-134">Namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="82623-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="82623-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="82623-135">-Tag</span></span>
<span data-ttu-id="82623-136">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="82623-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="82623-137">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="82623-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="82623-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82623-138">-Confirm</span></span>
<span data-ttu-id="82623-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82623-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82623-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82623-140">-WhatIf</span></span>
<span data-ttu-id="82623-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82623-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82623-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82623-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82623-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82623-143">CommonParameters</span></span>
<span data-ttu-id="82623-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82623-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82623-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82623-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82623-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82623-146">INPUTS</span></span>

### <span data-ttu-id="82623-147">System. String</span><span class="sxs-lookup"><span data-stu-id="82623-147">System.String</span></span>

## <span data-ttu-id="82623-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82623-148">OUTPUTS</span></span>

### <span data-ttu-id="82623-149">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82623-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="82623-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82623-150">NOTES</span></span>

## <span data-ttu-id="82623-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82623-151">RELATED LINKS</span></span>

[<span data-ttu-id="82623-152">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82623-152">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="82623-153">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82623-153">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="82623-154">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82623-154">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

