---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 609c7e161b131d80f9b41355f13ced8636a591e8
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93586604"
---
# <span data-ttu-id="d91e3-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d91e3-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="d91e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d91e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d91e3-103">Hämtar information om ett programpaket i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="d91e3-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d91e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d91e3-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d91e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d91e3-105">DESCRIPTION</span></span>
<span data-ttu-id="d91e3-106">Cmdleten **Get-AzureRmBatchApplicationPackage** hämtar information om ett programpaket i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="d91e3-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="d91e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d91e3-107">EXAMPLES</span></span>

### <span data-ttu-id="d91e3-108">Exempel 1: Hämta information om ett programpaket i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="d91e3-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="d91e3-109">Det här kommandot får information om version 1,0 av paketet Litware.</span><span class="sxs-lookup"><span data-stu-id="d91e3-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="d91e3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d91e3-110">PARAMETERS</span></span>

### <span data-ttu-id="d91e3-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d91e3-111">-AccountName</span></span>
<span data-ttu-id="d91e3-112">Anger namnet på den Batch-konto från vilken denna cmdlet hämtar information.</span><span class="sxs-lookup"><span data-stu-id="d91e3-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="d91e3-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d91e3-113">-ApplicationId</span></span>
<span data-ttu-id="d91e3-114">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="d91e3-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d91e3-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="d91e3-115">-ApplicationVersion</span></span>
<span data-ttu-id="d91e3-116">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="d91e3-116">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91e3-117">-DefaultProfile</span></span>
<span data-ttu-id="d91e3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d91e3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d91e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="d91e3-120">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="d91e3-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d91e3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91e3-121">CommonParameters</span></span>
<span data-ttu-id="d91e3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d91e3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91e3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d91e3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91e3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d91e3-124">INPUTS</span></span>

### <span data-ttu-id="d91e3-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="d91e3-125">None</span></span>
<span data-ttu-id="d91e3-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d91e3-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d91e3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d91e3-127">OUTPUTS</span></span>

### <span data-ttu-id="d91e3-128">Microsoft.Azure.Commands.BatCH. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d91e3-128">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="d91e3-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d91e3-129">NOTES</span></span>

## <span data-ttu-id="d91e3-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d91e3-130">RELATED LINKS</span></span>

[<span data-ttu-id="d91e3-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d91e3-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="d91e3-132">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d91e3-132">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="d91e3-133">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d91e3-133">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d91e3-134">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d91e3-134">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="d91e3-135">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d91e3-135">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d91e3-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d91e3-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


