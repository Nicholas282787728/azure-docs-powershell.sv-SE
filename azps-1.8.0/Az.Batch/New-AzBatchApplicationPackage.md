---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: 0e5494506873917be7897c547eca900174f5bcab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754692"
---
# <span data-ttu-id="d59a8-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d59a8-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="d59a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d59a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d59a8-103">Skapar ett programpaket i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="d59a8-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="d59a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d59a8-104">SYNTAX</span></span>

### <span data-ttu-id="d59a8-105">UploadAndActivate (standard)</span><span class="sxs-lookup"><span data-stu-id="d59a8-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d59a8-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="d59a8-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d59a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d59a8-107">DESCRIPTION</span></span>
<span data-ttu-id="d59a8-108">Cmdleten **New-AzBatchApplicationPackage** skapar ett programpaket i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="d59a8-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="d59a8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d59a8-109">EXAMPLES</span></span>

### <span data-ttu-id="d59a8-110">Exempel 1: installera ett programpaket i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="d59a8-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="d59a8-111">Det här kommandot skapar och aktiverar version 1,0 av Litware-programmet och laddar upp innehållet i litware.1.0.zip som innehållet i programpaketet.</span><span class="sxs-lookup"><span data-stu-id="d59a8-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="d59a8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d59a8-112">PARAMETERS</span></span>

### <span data-ttu-id="d59a8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d59a8-113">-AccountName</span></span>
<span data-ttu-id="d59a8-114">Anger namnet på den Batch-konto där cmdleten lägger till ett programpaket.</span><span class="sxs-lookup"><span data-stu-id="d59a8-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="d59a8-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="d59a8-115">-ActivateOnly</span></span>
<span data-ttu-id="d59a8-116">Anger att denna cmdlet aktiverar ett programpaket som redan har laddats upp.</span><span class="sxs-lookup"><span data-stu-id="d59a8-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="d59a8-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d59a8-117">-ApplicationId</span></span>
<span data-ttu-id="d59a8-118">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="d59a8-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d59a8-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="d59a8-119">-ApplicationVersion</span></span>
<span data-ttu-id="d59a8-120">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="d59a8-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="d59a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59a8-121">-DefaultProfile</span></span>
<span data-ttu-id="d59a8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d59a8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d59a8-123">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="d59a8-123">-FilePath</span></span>
<span data-ttu-id="d59a8-124">Anger vilken fil som ska laddas upp som den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="d59a8-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="d59a8-125">-Format</span><span class="sxs-lookup"><span data-stu-id="d59a8-125">-Format</span></span>
<span data-ttu-id="d59a8-126">Anger formatet för den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="d59a8-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="d59a8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d59a8-127">-ResourceGroupName</span></span>
<span data-ttu-id="d59a8-128">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="d59a8-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d59a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59a8-129">CommonParameters</span></span>
<span data-ttu-id="d59a8-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59a8-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59a8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59a8-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d59a8-132">INPUTS</span></span>

### <span data-ttu-id="d59a8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d59a8-133">System.String</span></span>

### <span data-ttu-id="d59a8-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d59a8-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d59a8-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d59a8-135">OUTPUTS</span></span>

### <span data-ttu-id="d59a8-136">Microsoft.Azure.Commands.BatCH. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d59a8-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="d59a8-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d59a8-137">NOTES</span></span>

## <span data-ttu-id="d59a8-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d59a8-138">RELATED LINKS</span></span>

[<span data-ttu-id="d59a8-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d59a8-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="d59a8-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d59a8-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="d59a8-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d59a8-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="d59a8-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d59a8-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="d59a8-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d59a8-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="d59a8-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d59a8-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)

