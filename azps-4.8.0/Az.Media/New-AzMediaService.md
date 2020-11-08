---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: a7554468824e85dbd922c0fac874ca9d881c13d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261226"
---
# <span data-ttu-id="9d8da-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9d8da-101">New-AzMediaService</span></span>

## <span data-ttu-id="9d8da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d8da-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8da-103">Skapar en medie tjänst om medie tjänsten redan finns, uppdateras alla dess egenskaper med angivna indata.</span><span class="sxs-lookup"><span data-stu-id="9d8da-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="9d8da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d8da-104">SYNTAX</span></span>

### <span data-ttu-id="9d8da-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="9d8da-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d8da-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="9d8da-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d8da-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d8da-107">DESCRIPTION</span></span>
<span data-ttu-id="9d8da-108">Cmdleten **New-AzMediaService** skapar en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="9d8da-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="9d8da-109">Om medie tjänsten redan finns uppdaterar denna cmdlet dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9d8da-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="9d8da-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d8da-110">EXAMPLES</span></span>

### <span data-ttu-id="9d8da-111">Example1: skapa en medie tjänst med endast det primära lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="9d8da-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="9d8da-112">Det här exemplet visar hur du skapar en medie tjänst med endast det primära lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="9d8da-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="9d8da-113">Det här skriptet använder flera andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="9d8da-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="9d8da-114">Exempel 2: skapa en medie tjänst med flera lagrings enheter</span><span class="sxs-lookup"><span data-stu-id="9d8da-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="9d8da-115">Det här exemplet visar hur du skapar en medie tjänst med flera lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="9d8da-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="9d8da-116">Det här skriptet använder flera andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="9d8da-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="9d8da-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d8da-117">PARAMETERS</span></span>

### <span data-ttu-id="9d8da-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9d8da-118">-AccountName</span></span>
<span data-ttu-id="9d8da-119">Anger namnet på den medie tjänst som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="9d8da-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9d8da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8da-120">-DefaultProfile</span></span>
<span data-ttu-id="9d8da-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9d8da-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d8da-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="9d8da-122">-Location</span></span>
<span data-ttu-id="9d8da-123">Anger den region som den här cmdleten skapar medie tjänsten i.</span><span class="sxs-lookup"><span data-stu-id="9d8da-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="9d8da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d8da-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d8da-125">Anger namnet på resurs gruppen som medie tjänsten är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="9d8da-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="9d8da-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9d8da-126">-StorageAccountId</span></span>
<span data-ttu-id="9d8da-127">Anger det lagrings konto som är kopplat till medie tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="9d8da-127">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="9d8da-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="9d8da-128">-StorageAccounts</span></span>
<span data-ttu-id="9d8da-129">Anger en matris med lagrings konton som ska kopplas till medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9d8da-129">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="9d8da-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9d8da-130">-Tag</span></span>
<span data-ttu-id="9d8da-131">De taggar som är kopplade till medie tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="9d8da-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="9d8da-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d8da-132">-Confirm</span></span>
<span data-ttu-id="9d8da-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d8da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d8da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d8da-134">-WhatIf</span></span>
<span data-ttu-id="9d8da-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d8da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d8da-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d8da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d8da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8da-137">CommonParameters</span></span>
<span data-ttu-id="9d8da-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d8da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8da-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8da-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8da-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d8da-140">INPUTS</span></span>

### <span data-ttu-id="9d8da-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9d8da-141">System.String</span></span>

### <span data-ttu-id="9d8da-142">Microsoft. Azure. commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="9d8da-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="9d8da-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d8da-143">OUTPUTS</span></span>

### <span data-ttu-id="9d8da-144">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="9d8da-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="9d8da-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d8da-145">NOTES</span></span>

## <span data-ttu-id="9d8da-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d8da-146">RELATED LINKS</span></span>

[<span data-ttu-id="9d8da-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9d8da-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="9d8da-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9d8da-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="9d8da-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9d8da-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


