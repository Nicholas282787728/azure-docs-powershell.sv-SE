---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: 0cbcc49f4b37b150b783467f45dcc7d4d7e53f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754702"
---
# <span data-ttu-id="09deb-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="09deb-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="09deb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09deb-102">SYNOPSIS</span></span>
<span data-ttu-id="09deb-103">Hämtar information om ett programpaket i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="09deb-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="09deb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09deb-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09deb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09deb-105">DESCRIPTION</span></span>
<span data-ttu-id="09deb-106">Cmdleten **Get-AzBatchApplicationPackage** hämtar information om ett programpaket i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="09deb-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="09deb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09deb-107">EXAMPLES</span></span>

### <span data-ttu-id="09deb-108">Exempel 1: Hämta information om ett programpaket i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="09deb-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="09deb-109">Det här kommandot får information om version 1,0 av paketet Litware.</span><span class="sxs-lookup"><span data-stu-id="09deb-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="09deb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09deb-110">PARAMETERS</span></span>

### <span data-ttu-id="09deb-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09deb-111">-AccountName</span></span>
<span data-ttu-id="09deb-112">Anger namnet på den Batch-konto från vilken denna cmdlet hämtar information.</span><span class="sxs-lookup"><span data-stu-id="09deb-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="09deb-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="09deb-113">-ApplicationId</span></span>
<span data-ttu-id="09deb-114">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="09deb-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="09deb-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="09deb-115">-ApplicationVersion</span></span>
<span data-ttu-id="09deb-116">Anger versionen för programmet.</span><span class="sxs-lookup"><span data-stu-id="09deb-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="09deb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09deb-117">-DefaultProfile</span></span>
<span data-ttu-id="09deb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09deb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09deb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09deb-119">-ResourceGroupName</span></span>
<span data-ttu-id="09deb-120">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="09deb-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="09deb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09deb-121">CommonParameters</span></span>
<span data-ttu-id="09deb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09deb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09deb-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09deb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09deb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09deb-124">INPUTS</span></span>

### <span data-ttu-id="09deb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="09deb-125">System.String</span></span>

## <span data-ttu-id="09deb-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09deb-126">OUTPUTS</span></span>

### <span data-ttu-id="09deb-127">Microsoft.Azure.Commands.BatCH. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="09deb-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="09deb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09deb-128">NOTES</span></span>

## <span data-ttu-id="09deb-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09deb-129">RELATED LINKS</span></span>

[<span data-ttu-id="09deb-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="09deb-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="09deb-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="09deb-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="09deb-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="09deb-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="09deb-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="09deb-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="09deb-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="09deb-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="09deb-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="09deb-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


