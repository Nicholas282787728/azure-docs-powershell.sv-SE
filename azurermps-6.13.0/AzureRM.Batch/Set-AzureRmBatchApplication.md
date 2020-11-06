---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 8ede896e6a49cee5305e7f9fd42f6dab130e7986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578987"
---
# <span data-ttu-id="54d46-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54d46-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="54d46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54d46-102">SYNOPSIS</span></span>
<span data-ttu-id="54d46-103">Uppdaterar inställningarna för det angivna programmet.</span><span class="sxs-lookup"><span data-stu-id="54d46-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54d46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54d46-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54d46-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54d46-105">DESCRIPTION</span></span>
<span data-ttu-id="54d46-106">Cmdleten **set-AzureRmBatchApplication** ändrar inställningar för det angivna Azure Batch-programmet.</span><span class="sxs-lookup"><span data-stu-id="54d46-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="54d46-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54d46-107">EXAMPLES</span></span>

### <span data-ttu-id="54d46-108">Exempel 1: uppdatera ett program i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="54d46-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="54d46-109">Det här kommandot ändrar om Llitware-programmet i ContosoBatch-kontot kan uppdatera.</span><span class="sxs-lookup"><span data-stu-id="54d46-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="54d46-110">Kommandot ändrar inte standard versionen eller visnings namnet för programmet.</span><span class="sxs-lookup"><span data-stu-id="54d46-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="54d46-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54d46-111">PARAMETERS</span></span>

### <span data-ttu-id="54d46-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54d46-112">-AccountName</span></span>
<span data-ttu-id="54d46-113">Anger namnet på det kommando konto där denna cmdlet ändrar ett program.</span><span class="sxs-lookup"><span data-stu-id="54d46-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="54d46-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="54d46-114">-AllowUpdates</span></span>
<span data-ttu-id="54d46-115">Anger om paket i programmet kan skrivas över med samma versions sträng.</span><span class="sxs-lookup"><span data-stu-id="54d46-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="54d46-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54d46-116">-ApplicationId</span></span>
<span data-ttu-id="54d46-117">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="54d46-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="54d46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d46-118">-DefaultProfile</span></span>
<span data-ttu-id="54d46-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54d46-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d46-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="54d46-120">-DefaultVersion</span></span>
<span data-ttu-id="54d46-121">Anger vilket paket som ska användas om en klient begär programmet men inte anger en version.</span><span class="sxs-lookup"><span data-stu-id="54d46-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="54d46-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="54d46-122">-DisplayName</span></span>
<span data-ttu-id="54d46-123">Anger programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="54d46-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="54d46-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d46-124">-ResourceGroupName</span></span>
<span data-ttu-id="54d46-125">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="54d46-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="54d46-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d46-126">CommonParameters</span></span>
<span data-ttu-id="54d46-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d46-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d46-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d46-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d46-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54d46-129">INPUTS</span></span>

### <span data-ttu-id="54d46-130">System. String</span><span class="sxs-lookup"><span data-stu-id="54d46-130">System.String</span></span>

### <span data-ttu-id="54d46-131">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="54d46-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="54d46-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54d46-132">OUTPUTS</span></span>

### <span data-ttu-id="54d46-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="54d46-133">System.Void</span></span>

## <span data-ttu-id="54d46-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54d46-134">NOTES</span></span>

## <span data-ttu-id="54d46-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54d46-135">RELATED LINKS</span></span>

[<span data-ttu-id="54d46-136">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54d46-136">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="54d46-137">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54d46-137">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="54d46-138">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54d46-138">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="54d46-139">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54d46-139">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="54d46-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54d46-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="54d46-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54d46-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


