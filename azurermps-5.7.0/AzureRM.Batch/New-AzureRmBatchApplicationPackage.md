---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 621aa03b2819815dc538650ea30120c63009235e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583675"
---
# <span data-ttu-id="3da28-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3da28-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="3da28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3da28-102">SYNOPSIS</span></span>
<span data-ttu-id="3da28-103">Skapar ett programpaket i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="3da28-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3da28-104">SYNTAX</span></span>

### <span data-ttu-id="3da28-105">UploadAndActivate (standard)</span><span class="sxs-lookup"><span data-stu-id="3da28-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3da28-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3da28-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3da28-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3da28-107">DESCRIPTION</span></span>
<span data-ttu-id="3da28-108">Cmdleten **New-AzureRmBatchApplicationPackage** skapar ett programpaket i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="3da28-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="3da28-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3da28-109">EXAMPLES</span></span>

### <span data-ttu-id="3da28-110">Exempel 1: installera ett programpaket i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="3da28-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="3da28-111">Det här kommandot skapar och aktiverar version 1,0 av Litware-programmet och laddar upp innehållet i litware.1.0.zip som innehållet i programpaketet.</span><span class="sxs-lookup"><span data-stu-id="3da28-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="3da28-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3da28-112">PARAMETERS</span></span>

### <span data-ttu-id="3da28-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3da28-113">-AccountName</span></span>
<span data-ttu-id="3da28-114">Anger namnet på den Batch-konto där cmdleten lägger till ett programpaket.</span><span class="sxs-lookup"><span data-stu-id="3da28-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="3da28-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3da28-115">-ActivateOnly</span></span>
<span data-ttu-id="3da28-116">Anger att denna cmdlet aktiverar ett programpaket som redan har laddats upp.</span><span class="sxs-lookup"><span data-stu-id="3da28-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ActivateOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da28-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3da28-117">-ApplicationId</span></span>
<span data-ttu-id="3da28-118">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="3da28-118">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da28-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3da28-119">-ApplicationVersion</span></span>
<span data-ttu-id="3da28-120">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="3da28-120">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da28-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da28-121">-DefaultProfile</span></span>
<span data-ttu-id="3da28-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3da28-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da28-123">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="3da28-123">-FilePath</span></span>
<span data-ttu-id="3da28-124">Anger vilken fil som ska laddas upp som den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="3da28-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: UploadAndActivate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da28-125">-Format</span><span class="sxs-lookup"><span data-stu-id="3da28-125">-Format</span></span>
<span data-ttu-id="3da28-126">Anger formatet för den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="3da28-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da28-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da28-127">-ResourceGroupName</span></span>
<span data-ttu-id="3da28-128">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="3da28-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da28-129">CommonParameters</span></span>
<span data-ttu-id="3da28-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da28-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da28-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da28-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3da28-132">INPUTS</span></span>

### <span data-ttu-id="3da28-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="3da28-133">None</span></span>
<span data-ttu-id="3da28-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3da28-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3da28-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3da28-135">OUTPUTS</span></span>

### <span data-ttu-id="3da28-136">Microsoft.Azure.Commands.BatCH. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3da28-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="3da28-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3da28-137">NOTES</span></span>

## <span data-ttu-id="3da28-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3da28-138">RELATED LINKS</span></span>

[<span data-ttu-id="3da28-139">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3da28-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="3da28-140">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3da28-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3da28-141">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3da28-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="3da28-142">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3da28-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="3da28-143">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3da28-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3da28-144">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3da28-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


