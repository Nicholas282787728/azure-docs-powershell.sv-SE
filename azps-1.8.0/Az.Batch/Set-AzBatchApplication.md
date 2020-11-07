---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 3dcbd81452ff9c4e5cf029b9c5d6169832d27a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754684"
---
# <span data-ttu-id="61105-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61105-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="61105-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61105-102">SYNOPSIS</span></span>
<span data-ttu-id="61105-103">Uppdaterar inställningarna för det angivna programmet.</span><span class="sxs-lookup"><span data-stu-id="61105-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="61105-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61105-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61105-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61105-105">DESCRIPTION</span></span>
<span data-ttu-id="61105-106">Cmdleten **set-AzBatchApplication** ändrar inställningar för det angivna Azure Batch-programmet.</span><span class="sxs-lookup"><span data-stu-id="61105-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="61105-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61105-107">EXAMPLES</span></span>

### <span data-ttu-id="61105-108">Exempel 1: uppdatera ett program i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="61105-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="61105-109">Det här kommandot ändrar om Llitware-programmet i ContosoBatch-kontot kan uppdatera.</span><span class="sxs-lookup"><span data-stu-id="61105-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="61105-110">Kommandot ändrar inte standard versionen eller visnings namnet för programmet.</span><span class="sxs-lookup"><span data-stu-id="61105-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="61105-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61105-111">PARAMETERS</span></span>

### <span data-ttu-id="61105-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61105-112">-AccountName</span></span>
<span data-ttu-id="61105-113">Anger namnet på det kommando konto där denna cmdlet ändrar ett program.</span><span class="sxs-lookup"><span data-stu-id="61105-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="61105-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="61105-114">-AllowUpdates</span></span>
<span data-ttu-id="61105-115">Anger om paket i programmet kan skrivas över med samma versions sträng.</span><span class="sxs-lookup"><span data-stu-id="61105-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61105-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="61105-116">-ApplicationId</span></span>
<span data-ttu-id="61105-117">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="61105-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="61105-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61105-118">-DefaultProfile</span></span>
<span data-ttu-id="61105-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61105-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61105-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="61105-120">-DefaultVersion</span></span>
<span data-ttu-id="61105-121">Anger vilket paket som ska användas om en klient begär programmet men inte anger en version.</span><span class="sxs-lookup"><span data-stu-id="61105-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="61105-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61105-122">-DisplayName</span></span>
<span data-ttu-id="61105-123">Anger programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="61105-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="61105-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61105-124">-ResourceGroupName</span></span>
<span data-ttu-id="61105-125">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="61105-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="61105-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61105-126">CommonParameters</span></span>
<span data-ttu-id="61105-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61105-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61105-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61105-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61105-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61105-129">INPUTS</span></span>

### <span data-ttu-id="61105-130">System. String</span><span class="sxs-lookup"><span data-stu-id="61105-130">System.String</span></span>

### <span data-ttu-id="61105-131">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="61105-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="61105-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61105-132">OUTPUTS</span></span>

### <span data-ttu-id="61105-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="61105-133">System.Void</span></span>

## <span data-ttu-id="61105-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61105-134">NOTES</span></span>

## <span data-ttu-id="61105-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61105-135">RELATED LINKS</span></span>

[<span data-ttu-id="61105-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61105-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="61105-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="61105-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="61105-138">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61105-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="61105-139">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="61105-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="61105-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61105-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="61105-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="61105-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


