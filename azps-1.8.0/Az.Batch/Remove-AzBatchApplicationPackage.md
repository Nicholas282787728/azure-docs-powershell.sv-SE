---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f4b47bb2abab783e4a6995ce57512dbd579e25e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754688"
---
# <span data-ttu-id="cac7f-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cac7f-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="cac7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cac7f-102">SYNOPSIS</span></span>
<span data-ttu-id="cac7f-103">Tar bort en post för programpaket och den binära filen.</span><span class="sxs-lookup"><span data-stu-id="cac7f-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="cac7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cac7f-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cac7f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cac7f-105">DESCRIPTION</span></span>
<span data-ttu-id="cac7f-106">Cmdleten **Remove-AzBatchApplicationPackage** tar bort en post för programpaketet och den binära filen från ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="cac7f-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="cac7f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cac7f-107">EXAMPLES</span></span>

### <span data-ttu-id="cac7f-108">Exempel 1: ta bort ett programpaket från ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="cac7f-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="cac7f-109">Det här kommandot tar bort version 1,0 av Litware-programmet från ContosoBatchGroup-kontot.</span><span class="sxs-lookup"><span data-stu-id="cac7f-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="cac7f-110">Kommandot tar bort både paket posten och blobben som innehåller den binära filen.</span><span class="sxs-lookup"><span data-stu-id="cac7f-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="cac7f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cac7f-111">PARAMETERS</span></span>

### <span data-ttu-id="cac7f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cac7f-112">-AccountName</span></span>
<span data-ttu-id="cac7f-113">Anger namnet på det konto som den här cmdleten tar bort ett programpaket från.</span><span class="sxs-lookup"><span data-stu-id="cac7f-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="cac7f-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cac7f-114">-ApplicationId</span></span>
<span data-ttu-id="cac7f-115">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="cac7f-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="cac7f-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="cac7f-116">-ApplicationVersion</span></span>
<span data-ttu-id="cac7f-117">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="cac7f-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="cac7f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac7f-118">-DefaultProfile</span></span>
<span data-ttu-id="cac7f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cac7f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac7f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac7f-120">-ResourceGroupName</span></span>
<span data-ttu-id="cac7f-121">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="cac7f-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="cac7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac7f-122">CommonParameters</span></span>
<span data-ttu-id="cac7f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac7f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac7f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac7f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cac7f-125">INPUTS</span></span>

### <span data-ttu-id="cac7f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cac7f-126">System.String</span></span>

## <span data-ttu-id="cac7f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cac7f-127">OUTPUTS</span></span>

### <span data-ttu-id="cac7f-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="cac7f-128">System.Void</span></span>

## <span data-ttu-id="cac7f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cac7f-129">NOTES</span></span>

## <span data-ttu-id="cac7f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cac7f-130">RELATED LINKS</span></span>

[<span data-ttu-id="cac7f-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cac7f-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="cac7f-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cac7f-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="cac7f-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cac7f-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="cac7f-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cac7f-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="cac7f-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cac7f-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="cac7f-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cac7f-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


