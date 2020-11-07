---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754689"
---
# <span data-ttu-id="722ea-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722ea-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="722ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="722ea-102">SYNOPSIS</span></span>
<span data-ttu-id="722ea-103">Tar bort ett program från ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="722ea-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="722ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="722ea-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="722ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="722ea-105">DESCRIPTION</span></span>
<span data-ttu-id="722ea-106">Cmdleten **Remove-AzBatchApplication** tar bort ett program från ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="722ea-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="722ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="722ea-107">EXAMPLES</span></span>

### <span data-ttu-id="722ea-108">Exempel 1: ta bort ett program från ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="722ea-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="722ea-109">Det här kommandot tar bort programmet Litware från ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="722ea-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="722ea-110">Kommandot fungerar inte om programmet innehåller paket.</span><span class="sxs-lookup"><span data-stu-id="722ea-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="722ea-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="722ea-111">PARAMETERS</span></span>

### <span data-ttu-id="722ea-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="722ea-112">-AccountName</span></span>
<span data-ttu-id="722ea-113">Anger namnet på det konto som den här cmdleten tar bort ett program från.</span><span class="sxs-lookup"><span data-stu-id="722ea-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="722ea-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="722ea-114">-ApplicationId</span></span>
<span data-ttu-id="722ea-115">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="722ea-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="722ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722ea-116">-DefaultProfile</span></span>
<span data-ttu-id="722ea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="722ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="722ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="722ea-119">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="722ea-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="722ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722ea-120">CommonParameters</span></span>
<span data-ttu-id="722ea-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="722ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722ea-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="722ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722ea-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="722ea-123">INPUTS</span></span>

### <span data-ttu-id="722ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="722ea-124">System.String</span></span>

## <span data-ttu-id="722ea-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="722ea-125">OUTPUTS</span></span>

### <span data-ttu-id="722ea-126">System. Void</span><span class="sxs-lookup"><span data-stu-id="722ea-126">System.Void</span></span>

## <span data-ttu-id="722ea-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="722ea-127">NOTES</span></span>

## <span data-ttu-id="722ea-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="722ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="722ea-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722ea-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="722ea-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="722ea-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="722ea-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722ea-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="722ea-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="722ea-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="722ea-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="722ea-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="722ea-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722ea-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


