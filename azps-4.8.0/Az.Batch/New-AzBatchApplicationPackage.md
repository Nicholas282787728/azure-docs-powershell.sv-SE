---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103298"
---
# <span data-ttu-id="0326e-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0326e-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="0326e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0326e-102">SYNOPSIS</span></span>
<span data-ttu-id="0326e-103">Skapar ett programpaket i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="0326e-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="0326e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0326e-104">SYNTAX</span></span>

### <span data-ttu-id="0326e-105">UploadAndActivate (standard)</span><span class="sxs-lookup"><span data-stu-id="0326e-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0326e-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="0326e-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0326e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0326e-107">DESCRIPTION</span></span>
<span data-ttu-id="0326e-108">Cmdleten **New-AzBatchApplicationPackage** skapar ett programpaket i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="0326e-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="0326e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0326e-109">EXAMPLES</span></span>

### <span data-ttu-id="0326e-110">Exempel 1: installera ett programpaket i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="0326e-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="0326e-111">Det här kommandot skapar och aktiverar version 1,0 av Litware-programmet och laddar upp innehållet i litware.1.0.zip som innehållet i programpaketet.</span><span class="sxs-lookup"><span data-stu-id="0326e-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="0326e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0326e-112">PARAMETERS</span></span>

### <span data-ttu-id="0326e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0326e-113">-AccountName</span></span>
<span data-ttu-id="0326e-114">Anger namnet på den Batch-konto där cmdleten lägger till ett programpaket.</span><span class="sxs-lookup"><span data-stu-id="0326e-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="0326e-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="0326e-115">-ActivateOnly</span></span>
<span data-ttu-id="0326e-116">Anger att denna cmdlet aktiverar ett programpaket som redan har laddats upp.</span><span class="sxs-lookup"><span data-stu-id="0326e-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="0326e-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0326e-117">-ApplicationName</span></span>
<span data-ttu-id="0326e-118">Anger namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="0326e-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0326e-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="0326e-119">-ApplicationVersion</span></span>
<span data-ttu-id="0326e-120">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="0326e-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="0326e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0326e-121">-DefaultProfile</span></span>
<span data-ttu-id="0326e-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0326e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0326e-123">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="0326e-123">-FilePath</span></span>
<span data-ttu-id="0326e-124">Anger vilken fil som ska laddas upp som den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="0326e-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="0326e-125">-Format</span><span class="sxs-lookup"><span data-stu-id="0326e-125">-Format</span></span>
<span data-ttu-id="0326e-126">Anger formatet för den binära filen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="0326e-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="0326e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0326e-127">-ResourceGroupName</span></span>
<span data-ttu-id="0326e-128">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="0326e-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="0326e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0326e-129">CommonParameters</span></span>
<span data-ttu-id="0326e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0326e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0326e-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0326e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0326e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0326e-132">INPUTS</span></span>

### <span data-ttu-id="0326e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0326e-133">System.String</span></span>

### <span data-ttu-id="0326e-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0326e-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0326e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0326e-135">OUTPUTS</span></span>

### <span data-ttu-id="0326e-136">Microsoft.Azure.Commands.BatCH. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0326e-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="0326e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0326e-137">NOTES</span></span>

## <span data-ttu-id="0326e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0326e-138">RELATED LINKS</span></span>

[<span data-ttu-id="0326e-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0326e-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="0326e-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0326e-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="0326e-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0326e-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="0326e-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0326e-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="0326e-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0326e-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="0326e-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0326e-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)

