---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 6c2ab80f5b9fb38ed2f6399d9f186134f4659edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579792"
---
# <span data-ttu-id="92b68-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92b68-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="92b68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92b68-102">SYNOPSIS</span></span>
<span data-ttu-id="92b68-103">Lägger till ett program i angivet batch-konto.</span><span class="sxs-lookup"><span data-stu-id="92b68-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92b68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92b68-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92b68-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92b68-105">DESCRIPTION</span></span>
<span data-ttu-id="92b68-106">Cmdleten **New-AzureRmBatchApplication** lägger till ett program till det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="92b68-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="92b68-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92b68-107">EXAMPLES</span></span>

### <span data-ttu-id="92b68-108">Exempel 1: lägga till ett tomt program i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="92b68-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="92b68-109">Det här kommandot skapar programmet Litware i ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="92b68-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="92b68-110">Programmet innehåller inte några paket.</span><span class="sxs-lookup"><span data-stu-id="92b68-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="92b68-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92b68-111">PARAMETERS</span></span>

### <span data-ttu-id="92b68-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="92b68-112">-AccountName</span></span>
<span data-ttu-id="92b68-113">Anger namnet på den Batch-konto som den här cmdleten lägger till ett program.</span><span class="sxs-lookup"><span data-stu-id="92b68-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="92b68-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="92b68-114">-AllowUpdates</span></span>
<span data-ttu-id="92b68-115">Anger om paket i programmet kan skrivas över med samma versions sträng.</span><span class="sxs-lookup"><span data-stu-id="92b68-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b68-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="92b68-116">-ApplicationId</span></span>
<span data-ttu-id="92b68-117">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="92b68-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="92b68-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92b68-118">-DisplayName</span></span>
<span data-ttu-id="92b68-119">Anger programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="92b68-119">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b68-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b68-120">-ResourceGroupName</span></span>
<span data-ttu-id="92b68-121">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="92b68-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="92b68-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b68-122">-DefaultProfile</span></span>
<span data-ttu-id="92b68-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92b68-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b68-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b68-124">CommonParameters</span></span>
<span data-ttu-id="92b68-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b68-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b68-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b68-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b68-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92b68-127">INPUTS</span></span>

## <span data-ttu-id="92b68-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92b68-128">OUTPUTS</span></span>

### <span data-ttu-id="92b68-129">Microsoft.Azure.Commands.BatCH. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="92b68-129">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="92b68-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92b68-130">NOTES</span></span>

## <span data-ttu-id="92b68-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92b68-131">RELATED LINKS</span></span>

[<span data-ttu-id="92b68-132">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92b68-132">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="92b68-133">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="92b68-133">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="92b68-134">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="92b68-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="92b68-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92b68-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="92b68-136">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="92b68-136">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="92b68-137">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92b68-137">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


