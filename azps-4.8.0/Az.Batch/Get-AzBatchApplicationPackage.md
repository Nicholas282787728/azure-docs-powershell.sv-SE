---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261434"
---
# <span data-ttu-id="418ff-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="418ff-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="418ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="418ff-102">SYNOPSIS</span></span>
<span data-ttu-id="418ff-103">Hämtar information om ett programpaket i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="418ff-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="418ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="418ff-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="418ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="418ff-105">DESCRIPTION</span></span>
<span data-ttu-id="418ff-106">Cmdleten **Get-AzBatchApplicationPackage** hämtar information om ett programpaket i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="418ff-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="418ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="418ff-107">EXAMPLES</span></span>

### <span data-ttu-id="418ff-108">Exempel 1: Hämta information om ett programpaket i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="418ff-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="418ff-109">Det här kommandot får information om version 1,0 av paketet Litware.</span><span class="sxs-lookup"><span data-stu-id="418ff-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="418ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="418ff-110">PARAMETERS</span></span>

### <span data-ttu-id="418ff-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="418ff-111">-AccountName</span></span>
<span data-ttu-id="418ff-112">Anger namnet på den Batch-konto från vilken denna cmdlet hämtar information.</span><span class="sxs-lookup"><span data-stu-id="418ff-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="418ff-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="418ff-113">-ApplicationName</span></span>
<span data-ttu-id="418ff-114">Anger namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="418ff-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="418ff-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="418ff-115">-ApplicationVersion</span></span>
<span data-ttu-id="418ff-116">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="418ff-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418ff-117">-DefaultProfile</span></span>
<span data-ttu-id="418ff-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="418ff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="418ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="418ff-120">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="418ff-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="418ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418ff-121">CommonParameters</span></span>
<span data-ttu-id="418ff-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="418ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418ff-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="418ff-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418ff-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="418ff-124">INPUTS</span></span>

### <span data-ttu-id="418ff-125">System. String</span><span class="sxs-lookup"><span data-stu-id="418ff-125">System.String</span></span>

## <span data-ttu-id="418ff-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="418ff-126">OUTPUTS</span></span>

### <span data-ttu-id="418ff-127">Microsoft.Azure.Commands.BatCH. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="418ff-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="418ff-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="418ff-128">NOTES</span></span>

## <span data-ttu-id="418ff-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="418ff-129">RELATED LINKS</span></span>

[<span data-ttu-id="418ff-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="418ff-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="418ff-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="418ff-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="418ff-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="418ff-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="418ff-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="418ff-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="418ff-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="418ff-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="418ff-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="418ff-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)

