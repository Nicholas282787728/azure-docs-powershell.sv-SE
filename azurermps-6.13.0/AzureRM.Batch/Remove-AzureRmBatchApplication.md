---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: 61288340bb2b9acb2bd47388d8f776d5c732b6f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574024"
---
# <span data-ttu-id="936ea-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="936ea-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="936ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="936ea-102">SYNOPSIS</span></span>
<span data-ttu-id="936ea-103">Tar bort ett program från ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="936ea-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="936ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="936ea-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="936ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="936ea-105">DESCRIPTION</span></span>
<span data-ttu-id="936ea-106">Cmdleten **Remove-AzureRmBatchApplication** tar bort ett program från ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="936ea-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="936ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="936ea-107">EXAMPLES</span></span>

### <span data-ttu-id="936ea-108">Exempel 1: ta bort ett program från ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="936ea-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="936ea-109">Det här kommandot tar bort programmet Litware från ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="936ea-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="936ea-110">Kommandot fungerar inte om programmet innehåller paket.</span><span class="sxs-lookup"><span data-stu-id="936ea-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="936ea-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="936ea-111">PARAMETERS</span></span>

### <span data-ttu-id="936ea-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="936ea-112">-AccountName</span></span>
<span data-ttu-id="936ea-113">Anger namnet på det konto som den här cmdleten tar bort ett program från.</span><span class="sxs-lookup"><span data-stu-id="936ea-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="936ea-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="936ea-114">-ApplicationId</span></span>
<span data-ttu-id="936ea-115">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="936ea-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="936ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936ea-116">-DefaultProfile</span></span>
<span data-ttu-id="936ea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="936ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="936ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="936ea-119">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="936ea-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="936ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936ea-120">CommonParameters</span></span>
<span data-ttu-id="936ea-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="936ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936ea-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936ea-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="936ea-123">INPUTS</span></span>

### <span data-ttu-id="936ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="936ea-124">System.String</span></span>

## <span data-ttu-id="936ea-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="936ea-125">OUTPUTS</span></span>

### <span data-ttu-id="936ea-126">System. Void</span><span class="sxs-lookup"><span data-stu-id="936ea-126">System.Void</span></span>

## <span data-ttu-id="936ea-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="936ea-127">NOTES</span></span>

## <span data-ttu-id="936ea-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="936ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="936ea-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="936ea-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="936ea-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="936ea-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="936ea-131">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="936ea-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="936ea-132">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="936ea-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="936ea-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="936ea-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="936ea-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="936ea-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


