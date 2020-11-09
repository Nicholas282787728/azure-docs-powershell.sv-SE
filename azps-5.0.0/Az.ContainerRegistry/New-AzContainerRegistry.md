---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319592"
---
# <span data-ttu-id="d67f1-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d67f1-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="d67f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d67f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d67f1-103">Skapar ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="d67f1-103">Creates a container registry.</span></span>

## <span data-ttu-id="d67f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d67f1-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d67f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d67f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d67f1-106">New-AzContainerRegistry-cmdleten skapar en container-registrering.</span><span class="sxs-lookup"><span data-stu-id="d67f1-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="d67f1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d67f1-107">EXAMPLES</span></span>

### <span data-ttu-id="d67f1-108">Exempel 1: skapa ett behållar register med ett nytt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d67f1-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d67f1-109">Det här kommandot skapar ett behållar register med ett nytt lagrings konto i resurs gruppen \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="d67f1-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="d67f1-110">Exempel 2: skapa en behållare med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="d67f1-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d67f1-111">Det här kommandot skapar ett behållar register med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="d67f1-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="d67f1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d67f1-112">PARAMETERS</span></span>

### <span data-ttu-id="d67f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67f1-113">-DefaultProfile</span></span>
<span data-ttu-id="d67f1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d67f1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d67f1-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d67f1-115">-EnableAdminUser</span></span>
<span data-ttu-id="d67f1-116">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d67f1-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="d67f1-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="d67f1-117">-Location</span></span>
<span data-ttu-id="d67f1-118">Behållarens register plats.</span><span class="sxs-lookup"><span data-stu-id="d67f1-118">Container Registry Location.</span></span>
<span data-ttu-id="d67f1-119">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d67f1-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="d67f1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d67f1-120">-Name</span></span>
<span data-ttu-id="d67f1-121">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="d67f1-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="d67f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="d67f1-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d67f1-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="d67f1-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="d67f1-124">-Sku</span></span>
<span data-ttu-id="d67f1-125">SKU för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="d67f1-125">Container Registry SKU.</span></span>
<span data-ttu-id="d67f1-126">Tillåtna värden: grundläggande.</span><span class="sxs-lookup"><span data-stu-id="d67f1-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67f1-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d67f1-127">-Tag</span></span>
<span data-ttu-id="d67f1-128">Register märken för behållare. nyckel värde par i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d67f1-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="d67f1-129">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d67f1-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d67f1-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d67f1-130">-Confirm</span></span>
<span data-ttu-id="d67f1-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d67f1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d67f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d67f1-132">-WhatIf</span></span>
<span data-ttu-id="d67f1-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d67f1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d67f1-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d67f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d67f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67f1-135">CommonParameters</span></span>
<span data-ttu-id="d67f1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67f1-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d67f1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67f1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d67f1-138">INPUTS</span></span>

### <span data-ttu-id="d67f1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d67f1-139">System.String</span></span>

## <span data-ttu-id="d67f1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d67f1-140">OUTPUTS</span></span>

### <span data-ttu-id="d67f1-141">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d67f1-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d67f1-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d67f1-142">NOTES</span></span>

## <span data-ttu-id="d67f1-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d67f1-143">RELATED LINKS</span></span>

[<span data-ttu-id="d67f1-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d67f1-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="d67f1-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d67f1-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="d67f1-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d67f1-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

