---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411496"
---
# <span data-ttu-id="c1d0a-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c1d0a-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="c1d0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d0a-103">Tar bort en post för programpaket och den binära filen.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="c1d0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1d0a-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1d0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="c1d0a-106">Cmdleten **Remove-AzBatchApplicationPackage** tar bort en post för programpaketet och den binära filen från ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="c1d0a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="c1d0a-108">Exempel 1: ta bort ett programpaket från ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="c1d0a-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="c1d0a-109">Det här kommandot tar bort version 1,0 av Litware-programmet från ContosoBatchGroup-kontot.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="c1d0a-110">Kommandot tar bort både paket posten och blobben som innehåller den binära filen.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="c1d0a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1d0a-111">PARAMETERS</span></span>

### <span data-ttu-id="c1d0a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1d0a-112">-AccountName</span></span>
<span data-ttu-id="c1d0a-113">Anger namnet på det konto som den här cmdleten tar bort ett programpaket från.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="c1d0a-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c1d0a-114">-ApplicationName</span></span>
<span data-ttu-id="c1d0a-115">Anger namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="c1d0a-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="c1d0a-116">-ApplicationVersion</span></span>
<span data-ttu-id="c1d0a-117">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="c1d0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d0a-118">-DefaultProfile</span></span>
<span data-ttu-id="c1d0a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d0a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1d0a-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1d0a-121">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c1d0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d0a-122">CommonParameters</span></span>
<span data-ttu-id="c1d0a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d0a-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1d0a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d0a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1d0a-125">INPUTS</span></span>

### <span data-ttu-id="c1d0a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c1d0a-126">System.String</span></span>

## <span data-ttu-id="c1d0a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1d0a-127">OUTPUTS</span></span>

### <span data-ttu-id="c1d0a-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="c1d0a-128">System.Void</span></span>

## <span data-ttu-id="c1d0a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1d0a-129">NOTES</span></span>

## <span data-ttu-id="c1d0a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1d0a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c1d0a-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c1d0a-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="c1d0a-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c1d0a-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="c1d0a-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c1d0a-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="c1d0a-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c1d0a-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="c1d0a-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c1d0a-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="c1d0a-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c1d0a-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


