---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103299"
---
# <span data-ttu-id="a05ef-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a05ef-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="a05ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a05ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a05ef-103">Lägger till ett program i angivet batch-konto.</span><span class="sxs-lookup"><span data-stu-id="a05ef-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="a05ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a05ef-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a05ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a05ef-105">DESCRIPTION</span></span>
<span data-ttu-id="a05ef-106">Cmdleten **New-AzBatchApplication** lägger till ett program till det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="a05ef-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="a05ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a05ef-107">EXAMPLES</span></span>

### <span data-ttu-id="a05ef-108">Exempel 1: lägga till ett tomt program i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="a05ef-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="a05ef-109">Det här kommandot skapar programmet Litware i ContosoBatch-kontot.</span><span class="sxs-lookup"><span data-stu-id="a05ef-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="a05ef-110">Programmet innehåller inte några paket.</span><span class="sxs-lookup"><span data-stu-id="a05ef-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="a05ef-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a05ef-111">PARAMETERS</span></span>

### <span data-ttu-id="a05ef-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a05ef-112">-AccountName</span></span>
<span data-ttu-id="a05ef-113">Anger namnet på den Batch-konto som den här cmdleten lägger till ett program.</span><span class="sxs-lookup"><span data-stu-id="a05ef-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="a05ef-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="a05ef-114">-AllowUpdates</span></span>
<span data-ttu-id="a05ef-115">Anger om paket i programmet kan skrivas över med samma versions sträng.</span><span class="sxs-lookup"><span data-stu-id="a05ef-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="a05ef-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a05ef-116">-ApplicationName</span></span>
<span data-ttu-id="a05ef-117">Anger namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="a05ef-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="a05ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05ef-118">-DefaultProfile</span></span>
<span data-ttu-id="a05ef-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a05ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a05ef-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a05ef-120">-DisplayName</span></span>
<span data-ttu-id="a05ef-121">Anger programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="a05ef-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="a05ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="a05ef-123">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="a05ef-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a05ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05ef-124">CommonParameters</span></span>
<span data-ttu-id="a05ef-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05ef-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a05ef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05ef-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a05ef-127">INPUTS</span></span>

### <span data-ttu-id="a05ef-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a05ef-128">System.String</span></span>

### <span data-ttu-id="a05ef-129">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a05ef-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a05ef-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a05ef-130">OUTPUTS</span></span>

### <span data-ttu-id="a05ef-131">Microsoft.Azure.Commands.BatCH. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a05ef-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="a05ef-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a05ef-132">NOTES</span></span>

## <span data-ttu-id="a05ef-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a05ef-133">RELATED LINKS</span></span>

[<span data-ttu-id="a05ef-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a05ef-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="a05ef-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a05ef-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="a05ef-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a05ef-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="a05ef-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a05ef-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="a05ef-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a05ef-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="a05ef-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a05ef-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


