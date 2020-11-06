---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: a67113443702d443bfd0b936af05e14c8fbbb96e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575016"
---
# <span data-ttu-id="8bf5f-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8bf5f-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="8bf5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8bf5f-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf5f-103">Skapar ett programpaket i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bf5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8bf5f-104">SYNTAX</span></span>

### <span data-ttu-id="8bf5f-105">UploadAndActivate (standard)</span><span class="sxs-lookup"><span data-stu-id="8bf5f-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bf5f-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="8bf5f-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bf5f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8bf5f-107">DESCRIPTION</span></span>
<span data-ttu-id="8bf5f-108">Cmdleten **New-AzureRmBatchApplicationPackage** skapar ett programpaket i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="8bf5f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8bf5f-109">EXAMPLES</span></span>

### <span data-ttu-id="8bf5f-110">Exempel 1: installera ett programpaket i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="8bf5f-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="8bf5f-111">Det här kommandot skapar och aktiverar version 1,0 av Litware-programmet och laddar upp innehållet i litware.1.0.zip som innehållet i programpaketet.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="8bf5f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8bf5f-112">PARAMETERS</span></span>

### <span data-ttu-id="8bf5f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8bf5f-113">-AccountName</span></span>
<span data-ttu-id="8bf5f-114">Anger namnet på den Batch-konto där cmdleten lägger till ett programpaket.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="8bf5f-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="8bf5f-115">-ActivateOnly</span></span>
<span data-ttu-id="8bf5f-116">Anger att denna cmdlet aktiverar ett programpaket som redan har laddats upp.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf5f-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8bf5f-117">-ApplicationId</span></span>
<span data-ttu-id="8bf5f-118">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="8bf5f-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="8bf5f-119">-ApplicationVersion</span></span>
<span data-ttu-id="8bf5f-120">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf5f-121">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="8bf5f-121">-FilePath</span></span>
<span data-ttu-id="8bf5f-122">Anger vilken fil som ska laddas upp som den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-122">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf5f-123">-Format</span><span class="sxs-lookup"><span data-stu-id="8bf5f-123">-Format</span></span>
<span data-ttu-id="8bf5f-124">Anger formatet för den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-124">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf5f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf5f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8bf5f-126">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-126">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf5f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf5f-127">-DefaultProfile</span></span>
<span data-ttu-id="8bf5f-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bf5f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf5f-129">CommonParameters</span></span>
<span data-ttu-id="8bf5f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf5f-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf5f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf5f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8bf5f-132">INPUTS</span></span>

## <span data-ttu-id="8bf5f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8bf5f-133">OUTPUTS</span></span>

### <span data-ttu-id="8bf5f-134">Microsoft.Azure.Commands.BatCH. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8bf5f-134">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="8bf5f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8bf5f-135">NOTES</span></span>

## <span data-ttu-id="8bf5f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8bf5f-136">RELATED LINKS</span></span>

[<span data-ttu-id="8bf5f-137">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8bf5f-137">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="8bf5f-138">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8bf5f-138">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8bf5f-139">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8bf5f-139">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="8bf5f-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8bf5f-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="8bf5f-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8bf5f-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8bf5f-142">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8bf5f-142">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


