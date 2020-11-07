---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 77b3d446c52e72bc31a2802768b00822982d1ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757415"
---
# <span data-ttu-id="12114-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="12114-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="12114-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12114-102">SYNOPSIS</span></span>
<span data-ttu-id="12114-103">Lägger till ett program i angivet batch-konto.</span><span class="sxs-lookup"><span data-stu-id="12114-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12114-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12114-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12114-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12114-105">DESCRIPTION</span></span>
<span data-ttu-id="12114-106">Cmdleten **New-AzureRmBatchApplication** lägger till ett program till det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="12114-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="12114-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12114-107">EXAMPLES</span></span>

### <span data-ttu-id="12114-108">Exempel 1: lägga till ett tomt program i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="12114-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="12114-109">Det här kommandot skapar programmet Litware i ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="12114-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="12114-110">Programmet innehåller inte några paket.</span><span class="sxs-lookup"><span data-stu-id="12114-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="12114-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12114-111">PARAMETERS</span></span>

### <span data-ttu-id="12114-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12114-112">-AccountName</span></span>
<span data-ttu-id="12114-113">Anger namnet på den Batch-konto som den här cmdleten lägger till ett program.</span><span class="sxs-lookup"><span data-stu-id="12114-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="12114-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="12114-114">-AllowUpdates</span></span>
<span data-ttu-id="12114-115">Anger om paket i programmet kan skrivas över med samma versions sträng.</span><span class="sxs-lookup"><span data-stu-id="12114-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12114-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="12114-116">-ApplicationId</span></span>
<span data-ttu-id="12114-117">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="12114-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="12114-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12114-118">-DefaultProfile</span></span>
<span data-ttu-id="12114-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12114-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12114-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="12114-120">-DisplayName</span></span>
<span data-ttu-id="12114-121">Anger programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="12114-121">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12114-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12114-122">-ResourceGroupName</span></span>
<span data-ttu-id="12114-123">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="12114-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="12114-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12114-124">CommonParameters</span></span>
<span data-ttu-id="12114-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12114-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12114-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12114-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12114-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12114-127">INPUTS</span></span>

### <span data-ttu-id="12114-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="12114-128">None</span></span>
<span data-ttu-id="12114-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="12114-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12114-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12114-130">OUTPUTS</span></span>

### <span data-ttu-id="12114-131">Microsoft.Azure.Commands.BatCH. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="12114-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="12114-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12114-132">NOTES</span></span>

## <span data-ttu-id="12114-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12114-133">RELATED LINKS</span></span>

[<span data-ttu-id="12114-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="12114-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="12114-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="12114-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="12114-136">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="12114-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="12114-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="12114-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="12114-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="12114-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="12114-139">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="12114-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)

