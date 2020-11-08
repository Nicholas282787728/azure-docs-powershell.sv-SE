---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091866"
---
# <span data-ttu-id="e449f-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e449f-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="e449f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e449f-102">SYNOPSIS</span></span>
<span data-ttu-id="e449f-103">Hämtar information om det angivna programmet.</span><span class="sxs-lookup"><span data-stu-id="e449f-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="e449f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e449f-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e449f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e449f-105">DESCRIPTION</span></span>
<span data-ttu-id="e449f-106">Cmdleten **Get-AzBatchApplication** hämtar information om ett program i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="e449f-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="e449f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e449f-107">EXAMPLES</span></span>

### <span data-ttu-id="e449f-108">Exempel 1: Visa programmen i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="e449f-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="e449f-109">Det här kommandot visar alla program i ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="e449f-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="e449f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e449f-110">PARAMETERS</span></span>

### <span data-ttu-id="e449f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e449f-111">-AccountName</span></span>
<span data-ttu-id="e449f-112">Anger namnet på batch-kontot som innehåller programmet.</span><span class="sxs-lookup"><span data-stu-id="e449f-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="e449f-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e449f-113">-ApplicationName</span></span>
<span data-ttu-id="e449f-114">Anger namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="e449f-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e449f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e449f-115">-DefaultProfile</span></span>
<span data-ttu-id="e449f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e449f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e449f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e449f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e449f-118">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="e449f-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="e449f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e449f-119">CommonParameters</span></span>
<span data-ttu-id="e449f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e449f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e449f-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e449f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e449f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e449f-122">INPUTS</span></span>

### <span data-ttu-id="e449f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e449f-123">System.String</span></span>

## <span data-ttu-id="e449f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e449f-124">OUTPUTS</span></span>

### <span data-ttu-id="e449f-125">Microsoft.Azure.Commands.BatCH. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="e449f-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="e449f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e449f-126">NOTES</span></span>

## <span data-ttu-id="e449f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e449f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e449f-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e449f-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="e449f-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e449f-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="e449f-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e449f-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="e449f-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e449f-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="e449f-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e449f-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="e449f-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e449f-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


