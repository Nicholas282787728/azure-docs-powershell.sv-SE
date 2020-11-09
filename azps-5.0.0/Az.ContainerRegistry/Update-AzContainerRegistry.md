---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321744"
---
# <span data-ttu-id="d8e02-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8e02-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="d8e02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8e02-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e02-103">Uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="d8e02-103">Updates a container registry.</span></span>

## <span data-ttu-id="d8e02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8e02-104">SYNTAX</span></span>

### <span data-ttu-id="d8e02-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d8e02-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e02-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e02-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e02-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e02-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e02-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e02-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e02-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e02-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e02-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e02-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e02-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8e02-111">DESCRIPTION</span></span>
<span data-ttu-id="d8e02-112">Update-AzContainerRegistry cmdlet uppdaterar en behållar register.</span><span class="sxs-lookup"><span data-stu-id="d8e02-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="d8e02-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8e02-113">EXAMPLES</span></span>

### <span data-ttu-id="d8e02-114">Exempel 1: Aktivera administratörs användare för ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="d8e02-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="d8e02-115">Det här kommandot aktiverar administratörs användaren för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d8e02-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="d8e02-116">Exempel 2: Ange det lagrings konto som används av ett angivet behållar-register</span><span class="sxs-lookup"><span data-stu-id="d8e02-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="d8e02-117">Det här kommandot anger det angivna behållar-registret så att det använder ett befintligt lagrings konto \` mystorageaccount \` i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d8e02-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="d8e02-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8e02-118">PARAMETERS</span></span>

### <span data-ttu-id="d8e02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e02-119">-DefaultProfile</span></span>
<span data-ttu-id="d8e02-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8e02-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8e02-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d8e02-121">-DisableAdminUser</span></span>
<span data-ttu-id="d8e02-122">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d8e02-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="d8e02-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d8e02-123">-EnableAdminUser</span></span>
<span data-ttu-id="d8e02-124">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d8e02-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="d8e02-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8e02-125">-Name</span></span>
<span data-ttu-id="d8e02-126">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="d8e02-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="d8e02-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8e02-127">-NetworkRuleSet</span></span>
<span data-ttu-id="d8e02-128">Nätverks regeln för en behållar register.</span><span class="sxs-lookup"><span data-stu-id="d8e02-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e02-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e02-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8e02-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d8e02-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="d8e02-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8e02-131">-ResourceId</span></span>
<span data-ttu-id="d8e02-132">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="d8e02-132">The container registry resource id</span></span>

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

### <span data-ttu-id="d8e02-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="d8e02-133">-Sku</span></span>
<span data-ttu-id="d8e02-134">SKU för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d8e02-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="d8e02-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8e02-135">-StorageAccountName</span></span>
<span data-ttu-id="d8e02-136">Namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d8e02-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="d8e02-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d8e02-137">-Tag</span></span>
<span data-ttu-id="d8e02-138">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d8e02-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="d8e02-139">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d8e02-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d8e02-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8e02-140">-Confirm</span></span>
<span data-ttu-id="d8e02-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8e02-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e02-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e02-142">-WhatIf</span></span>
<span data-ttu-id="d8e02-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8e02-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e02-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8e02-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e02-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e02-145">CommonParameters</span></span>
<span data-ttu-id="d8e02-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e02-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e02-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8e02-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e02-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8e02-148">INPUTS</span></span>

### <span data-ttu-id="d8e02-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e02-149">System.String</span></span>

## <span data-ttu-id="d8e02-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8e02-150">OUTPUTS</span></span>

### <span data-ttu-id="d8e02-151">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8e02-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d8e02-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8e02-152">NOTES</span></span>

## <span data-ttu-id="d8e02-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8e02-153">RELATED LINKS</span></span>

[<span data-ttu-id="d8e02-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8e02-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="d8e02-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8e02-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="d8e02-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8e02-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

