---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: e22d3c58072fbabd3f927f6b9065f22422492622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573552"
---
# <span data-ttu-id="77b5e-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77b5e-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="77b5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="77b5e-103">Hämtar information om det angivna programmet.</span><span class="sxs-lookup"><span data-stu-id="77b5e-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77b5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77b5e-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77b5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77b5e-105">DESCRIPTION</span></span>
<span data-ttu-id="77b5e-106">Cmdleten **Get-AzureRmBatchApplication** hämtar information om ett program i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="77b5e-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="77b5e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77b5e-107">EXAMPLES</span></span>

### <span data-ttu-id="77b5e-108">Exempel 1: Visa programmen i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="77b5e-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="77b5e-109">Det här kommandot visar alla program i ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="77b5e-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="77b5e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77b5e-110">PARAMETERS</span></span>

### <span data-ttu-id="77b5e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77b5e-111">-AccountName</span></span>
<span data-ttu-id="77b5e-112">Anger namnet på batch-kontot som innehåller programmet.</span><span class="sxs-lookup"><span data-stu-id="77b5e-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="77b5e-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="77b5e-113">-ApplicationId</span></span>
<span data-ttu-id="77b5e-114">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="77b5e-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b5e-115">-DefaultProfile</span></span>
<span data-ttu-id="77b5e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77b5e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77b5e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b5e-117">-ResourceGroupName</span></span>
<span data-ttu-id="77b5e-118">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="77b5e-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="77b5e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b5e-119">CommonParameters</span></span>
<span data-ttu-id="77b5e-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b5e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b5e-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b5e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b5e-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77b5e-122">INPUTS</span></span>

### <span data-ttu-id="77b5e-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="77b5e-123">None</span></span>
<span data-ttu-id="77b5e-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="77b5e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77b5e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77b5e-125">OUTPUTS</span></span>

### <span data-ttu-id="77b5e-126">Microsoft.Azure.Commands.BatCH. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="77b5e-126">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="77b5e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77b5e-127">NOTES</span></span>

## <span data-ttu-id="77b5e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77b5e-128">RELATED LINKS</span></span>

[<span data-ttu-id="77b5e-129">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="77b5e-129">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="77b5e-130">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77b5e-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="77b5e-131">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="77b5e-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="77b5e-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77b5e-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="77b5e-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="77b5e-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="77b5e-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77b5e-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


