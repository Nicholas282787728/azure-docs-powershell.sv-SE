---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 8ef7ba1c678c09ba10bd87c301a417600f51fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579791"
---
# <span data-ttu-id="2ddd5-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2ddd5-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="2ddd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ddd5-102">SYNOPSIS</span></span>
<span data-ttu-id="2ddd5-103">Tar bort en post för programpaket och den binära filen.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ddd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ddd5-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ddd5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ddd5-105">DESCRIPTION</span></span>
<span data-ttu-id="2ddd5-106">Cmdleten **Remove-AzureRmBatchApplicationPackage** tar bort en post för programpaketet och den binära filen från ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="2ddd5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ddd5-107">EXAMPLES</span></span>

### <span data-ttu-id="2ddd5-108">Exempel 1: ta bort ett programpaket från ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="2ddd5-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="2ddd5-109">Det här kommandot tar bort version 1,0 av Litware-programmet från ContosoBatchGroup-kontot.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="2ddd5-110">Kommandot tar bort både paket posten och blobben som innehåller den binära filen.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="2ddd5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ddd5-111">PARAMETERS</span></span>

### <span data-ttu-id="2ddd5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ddd5-112">-AccountName</span></span>
<span data-ttu-id="2ddd5-113">Anger namnet på det konto som den här cmdleten tar bort ett programpaket från.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="2ddd5-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2ddd5-114">-ApplicationId</span></span>
<span data-ttu-id="2ddd5-115">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="2ddd5-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="2ddd5-116">-ApplicationVersion</span></span>
<span data-ttu-id="2ddd5-117">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="2ddd5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ddd5-118">-ResourceGroupName</span></span>
<span data-ttu-id="2ddd5-119">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="2ddd5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ddd5-120">-DefaultProfile</span></span>
<span data-ttu-id="2ddd5-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ddd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ddd5-122">CommonParameters</span></span>
<span data-ttu-id="2ddd5-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ddd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ddd5-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ddd5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ddd5-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ddd5-125">INPUTS</span></span>

## <span data-ttu-id="2ddd5-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ddd5-126">OUTPUTS</span></span>

## <span data-ttu-id="2ddd5-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ddd5-127">NOTES</span></span>

## <span data-ttu-id="2ddd5-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ddd5-128">RELATED LINKS</span></span>

[<span data-ttu-id="2ddd5-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ddd5-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="2ddd5-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2ddd5-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="2ddd5-131">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ddd5-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="2ddd5-132">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2ddd5-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="2ddd5-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ddd5-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="2ddd5-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ddd5-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


