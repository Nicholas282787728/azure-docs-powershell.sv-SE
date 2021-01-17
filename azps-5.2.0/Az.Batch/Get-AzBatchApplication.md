---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399595"
---
# <span data-ttu-id="01d82-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01d82-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="01d82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01d82-102">SYNOPSIS</span></span>
<span data-ttu-id="01d82-103">Hämtar information om det angivna programmet.</span><span class="sxs-lookup"><span data-stu-id="01d82-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="01d82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01d82-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01d82-105">DESCRIPTION</span></span>
<span data-ttu-id="01d82-106">Cmdleten **Get-AzBatchApplication** hämtar information om ett program i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="01d82-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="01d82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01d82-107">EXAMPLES</span></span>

### <span data-ttu-id="01d82-108">Exempel 1: Visa programmen i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="01d82-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="01d82-109">Det här kommandot visar alla program i ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="01d82-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="01d82-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01d82-110">PARAMETERS</span></span>

### <span data-ttu-id="01d82-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01d82-111">-AccountName</span></span>
<span data-ttu-id="01d82-112">Anger namnet på batch-kontot som innehåller programmet.</span><span class="sxs-lookup"><span data-stu-id="01d82-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="01d82-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="01d82-113">-ApplicationName</span></span>
<span data-ttu-id="01d82-114">Anger namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="01d82-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="01d82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d82-115">-DefaultProfile</span></span>
<span data-ttu-id="01d82-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01d82-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01d82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d82-117">-ResourceGroupName</span></span>
<span data-ttu-id="01d82-118">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="01d82-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="01d82-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d82-119">CommonParameters</span></span>
<span data-ttu-id="01d82-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d82-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d82-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01d82-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d82-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01d82-122">INPUTS</span></span>

### <span data-ttu-id="01d82-123">System. String</span><span class="sxs-lookup"><span data-stu-id="01d82-123">System.String</span></span>

## <span data-ttu-id="01d82-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01d82-124">OUTPUTS</span></span>

### <span data-ttu-id="01d82-125">Microsoft.Azure.Commands.BatCH. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="01d82-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="01d82-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01d82-126">NOTES</span></span>

## <span data-ttu-id="01d82-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01d82-127">RELATED LINKS</span></span>

[<span data-ttu-id="01d82-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="01d82-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="01d82-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01d82-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="01d82-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="01d82-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="01d82-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01d82-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="01d82-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="01d82-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="01d82-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01d82-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


