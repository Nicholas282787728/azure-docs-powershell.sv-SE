---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756930"
---
# <span data-ttu-id="4a299-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a299-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="4a299-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a299-102">SYNOPSIS</span></span>
<span data-ttu-id="4a299-103">Skapar en medie tjänst om medie tjänsten redan finns, uppdateras alla dess egenskaper med angivna indata.</span><span class="sxs-lookup"><span data-stu-id="4a299-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a299-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a299-104">SYNTAX</span></span>

### <span data-ttu-id="4a299-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="4a299-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a299-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="4a299-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a299-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a299-107">DESCRIPTION</span></span>
<span data-ttu-id="4a299-108">Cmdleten **New-AzureRmMediaService** skapar en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="4a299-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="4a299-109">Om medie tjänsten redan finns uppdaterar denna cmdlet dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4a299-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="4a299-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a299-110">EXAMPLES</span></span>

### <span data-ttu-id="4a299-111">Example1: skapa en medie tjänst med endast det primära lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="4a299-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="4a299-112">Det här exemplet visar hur du skapar en medie tjänst med endast det primära lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4a299-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="4a299-113">Det här skriptet använder flera andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4a299-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="4a299-114">Exempel 2: skapa en medie tjänst med flera lagrings enheter</span><span class="sxs-lookup"><span data-stu-id="4a299-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="4a299-115">Det här exemplet visar hur du skapar en medie tjänst med flera lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="4a299-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="4a299-116">Det här skriptet använder flera andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4a299-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="4a299-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a299-117">PARAMETERS</span></span>

### <span data-ttu-id="4a299-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a299-118">-AccountName</span></span>
<span data-ttu-id="4a299-119">Anger namnet på den medie tjänst som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="4a299-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a299-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="4a299-120">-Location</span></span>
<span data-ttu-id="4a299-121">Anger den region som den här cmdleten skapar medie tjänsten i.</span><span class="sxs-lookup"><span data-stu-id="4a299-121">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a299-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a299-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a299-123">Anger namnet på resurs gruppen som medie tjänsten är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="4a299-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="4a299-124">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4a299-124">-StorageAccountId</span></span>
<span data-ttu-id="4a299-125">Anger det lagrings konto som är kopplat till medie tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="4a299-125">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a299-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="4a299-126">-StorageAccounts</span></span>
<span data-ttu-id="4a299-127">Anger en matris med lagrings konton som ska kopplas till medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4a299-127">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a299-128">-Taggar</span><span class="sxs-lookup"><span data-stu-id="4a299-128">-Tags</span></span>
<span data-ttu-id="4a299-129">Anger taggar för medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4a299-129">Specifies tags for the media service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a299-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a299-130">-Confirm</span></span>
<span data-ttu-id="4a299-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a299-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a299-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a299-132">-WhatIf</span></span>
<span data-ttu-id="4a299-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a299-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a299-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a299-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a299-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a299-135">-DefaultProfile</span></span>
<span data-ttu-id="4a299-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a299-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a299-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a299-137">CommonParameters</span></span>
<span data-ttu-id="4a299-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a299-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a299-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a299-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a299-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a299-140">INPUTS</span></span>

## <span data-ttu-id="4a299-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a299-141">OUTPUTS</span></span>

### <span data-ttu-id="4a299-142">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="4a299-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="4a299-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a299-143">NOTES</span></span>

## <span data-ttu-id="4a299-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a299-144">RELATED LINKS</span></span>

[<span data-ttu-id="4a299-145">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a299-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="4a299-146">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a299-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="4a299-147">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a299-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


