---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574329"
---
# <span data-ttu-id="6f9be-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f9be-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="6f9be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f9be-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9be-103">Skapar ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="6f9be-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f9be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f9be-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f9be-105">DESCRIPTION</span></span>
<span data-ttu-id="6f9be-106">New-AzureRmContainerRegistry-cmdleten skapar en container-registrering.</span><span class="sxs-lookup"><span data-stu-id="6f9be-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="6f9be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f9be-107">EXAMPLES</span></span>

### <span data-ttu-id="6f9be-108">Exempel 1: skapa ett behållar register med ett nytt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6f9be-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="6f9be-109">Det här kommandot skapar ett behållar register med ett nytt lagrings konto i resurs gruppen \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="6f9be-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="6f9be-110">Exempel 2: skapa en behållare med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="6f9be-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="6f9be-111">Det här kommandot skapar ett behållar register med administratörs användare aktive rad.</span><span class="sxs-lookup"><span data-stu-id="6f9be-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="6f9be-112">Exempel 3: skapa ett behållar register med ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6f9be-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="6f9be-113">Det här kommandot skapar ett behållar register med ett befintligt lagrings konto \` mystorageaccount \` i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6f9be-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="6f9be-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f9be-114">PARAMETERS</span></span>

### <span data-ttu-id="6f9be-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="6f9be-115">-EnableAdminUser</span></span>
<span data-ttu-id="6f9be-116">Aktivera administratörs användare för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="6f9be-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9be-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="6f9be-117">-Location</span></span>
<span data-ttu-id="6f9be-118">Behållarens register plats.</span><span class="sxs-lookup"><span data-stu-id="6f9be-118">Container Registry Location.</span></span>
<span data-ttu-id="6f9be-119">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6f9be-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="6f9be-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f9be-120">-Name</span></span>
<span data-ttu-id="6f9be-121">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="6f9be-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9be-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f9be-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6f9be-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9be-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="6f9be-124">-Sku</span></span>
<span data-ttu-id="6f9be-125">SKU för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="6f9be-125">Container Registry SKU.</span></span>
<span data-ttu-id="6f9be-126">Tillåtna värden: grundläggande.</span><span class="sxs-lookup"><span data-stu-id="6f9be-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9be-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f9be-127">-StorageAccountName</span></span>
<span data-ttu-id="6f9be-128">Namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6f9be-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="6f9be-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6f9be-129">-Tag</span></span>
<span data-ttu-id="6f9be-130">Register märken för behållare. nyckel värde par i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6f9be-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="6f9be-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="6f9be-131">For example:</span></span>

<span data-ttu-id="6f9be-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6f9be-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6f9be-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f9be-133">-Confirm</span></span>
<span data-ttu-id="6f9be-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f9be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9be-135">-WhatIf</span></span>
<span data-ttu-id="6f9be-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f9be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9be-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f9be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f9be-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9be-138">-DefaultProfile</span></span>
<span data-ttu-id="6f9be-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6f9be-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f9be-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9be-140">CommonParameters</span></span>
<span data-ttu-id="6f9be-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f9be-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9be-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f9be-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9be-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f9be-143">INPUTS</span></span>

### <span data-ttu-id="6f9be-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="6f9be-144">None</span></span>
<span data-ttu-id="6f9be-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6f9be-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f9be-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f9be-146">OUTPUTS</span></span>

### <span data-ttu-id="6f9be-147">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f9be-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="6f9be-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f9be-148">NOTES</span></span>

## <span data-ttu-id="6f9be-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f9be-149">RELATED LINKS</span></span>

[<span data-ttu-id="6f9be-150">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f9be-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="6f9be-151">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f9be-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="6f9be-152">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f9be-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

