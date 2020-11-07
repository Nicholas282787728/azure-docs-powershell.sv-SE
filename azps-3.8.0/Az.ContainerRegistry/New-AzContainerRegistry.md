---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 1c546894cf9b11dcb65fb12b9b0575e2fd3191fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926265"
---
# <span data-ttu-id="ffa47-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ffa47-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="ffa47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ffa47-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa47-103">Skapar ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="ffa47-103">Creates a container registry.</span></span>

## <span data-ttu-id="ffa47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ffa47-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ffa47-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa47-106">New-AzContainerRegistry-cmdleten skapar en container-registrering.</span><span class="sxs-lookup"><span data-stu-id="ffa47-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="ffa47-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ffa47-107">EXAMPLES</span></span>

### <span data-ttu-id="ffa47-108">Exempel 1: skapa ett behållar register med ett nytt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ffa47-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ffa47-109">Det här kommandot skapar ett behållar register med ett nytt lagrings konto i resurs gruppen \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="ffa47-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="ffa47-110">Exempel 2: skapa en behållare med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ffa47-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ffa47-111">Det här kommandot skapar ett behållar register med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ffa47-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="ffa47-112">Exempel 3: skapa ett behållar register med ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ffa47-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ffa47-113">Det här kommandot skapar ett behållar register med ett befintligt lagrings konto \` mystorageaccount \` i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ffa47-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="ffa47-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ffa47-114">PARAMETERS</span></span>

### <span data-ttu-id="ffa47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa47-115">-DefaultProfile</span></span>
<span data-ttu-id="ffa47-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ffa47-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffa47-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ffa47-117">-EnableAdminUser</span></span>
<span data-ttu-id="ffa47-118">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="ffa47-118">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa47-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="ffa47-119">-Location</span></span>
<span data-ttu-id="ffa47-120">Behållarens register plats.</span><span class="sxs-lookup"><span data-stu-id="ffa47-120">Container Registry Location.</span></span>
<span data-ttu-id="ffa47-121">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ffa47-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="ffa47-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ffa47-122">-Name</span></span>
<span data-ttu-id="ffa47-123">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="ffa47-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="ffa47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa47-124">-ResourceGroupName</span></span>
<span data-ttu-id="ffa47-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ffa47-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ffa47-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="ffa47-126">-Sku</span></span>
<span data-ttu-id="ffa47-127">SKU för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="ffa47-127">Container Registry SKU.</span></span>
<span data-ttu-id="ffa47-128">Tillåtna värden: grundläggande.</span><span class="sxs-lookup"><span data-stu-id="ffa47-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa47-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ffa47-129">-StorageAccountName</span></span>
<span data-ttu-id="ffa47-130">Namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ffa47-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="ffa47-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ffa47-131">-Tag</span></span>
<span data-ttu-id="ffa47-132">Register märken för behållare. nyckel värde par i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ffa47-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="ffa47-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ffa47-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ffa47-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ffa47-134">-Confirm</span></span>
<span data-ttu-id="ffa47-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ffa47-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa47-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa47-136">-WhatIf</span></span>
<span data-ttu-id="ffa47-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ffa47-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa47-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ffa47-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa47-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa47-139">CommonParameters</span></span>
<span data-ttu-id="ffa47-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa47-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa47-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffa47-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa47-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ffa47-142">INPUTS</span></span>

### <span data-ttu-id="ffa47-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ffa47-143">System.String</span></span>

## <span data-ttu-id="ffa47-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ffa47-144">OUTPUTS</span></span>

### <span data-ttu-id="ffa47-145">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ffa47-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ffa47-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ffa47-146">NOTES</span></span>

## <span data-ttu-id="ffa47-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ffa47-147">RELATED LINKS</span></span>

[<span data-ttu-id="ffa47-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ffa47-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="ffa47-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ffa47-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="ffa47-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ffa47-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

