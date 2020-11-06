---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 157e7a3ee0cc7ea4a80517bf98d17c05df8c7899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574413"
---
# <span data-ttu-id="ec986-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ec986-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="ec986-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec986-102">SYNOPSIS</span></span>
<span data-ttu-id="ec986-103">Uppdaterar inställningarna för det angivna programmet.</span><span class="sxs-lookup"><span data-stu-id="ec986-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec986-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec986-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec986-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec986-105">DESCRIPTION</span></span>
<span data-ttu-id="ec986-106">Cmdleten **set-AzureRmBatchApplication** ändrar inställningar för det angivna Azure Batch-programmet.</span><span class="sxs-lookup"><span data-stu-id="ec986-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="ec986-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec986-107">EXAMPLES</span></span>

### <span data-ttu-id="ec986-108">Exempel 1: uppdatera ett program i ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="ec986-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="ec986-109">Det här kommandot ändrar om Llitware-programmet i ContosoBatch-kontot kan uppdatera.</span><span class="sxs-lookup"><span data-stu-id="ec986-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="ec986-110">Kommandot ändrar inte standard versionen eller visnings namnet för programmet.</span><span class="sxs-lookup"><span data-stu-id="ec986-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="ec986-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec986-111">PARAMETERS</span></span>

### <span data-ttu-id="ec986-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec986-112">-AccountName</span></span>
<span data-ttu-id="ec986-113">Anger namnet på det kommando konto där denna cmdlet ändrar ett program.</span><span class="sxs-lookup"><span data-stu-id="ec986-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="ec986-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="ec986-114">-AllowUpdates</span></span>
<span data-ttu-id="ec986-115">Anger om paket i programmet kan skrivas över med samma versions sträng.</span><span class="sxs-lookup"><span data-stu-id="ec986-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec986-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ec986-116">-ApplicationId</span></span>
<span data-ttu-id="ec986-117">Anger ID för programmet.</span><span class="sxs-lookup"><span data-stu-id="ec986-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="ec986-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec986-118">-DefaultProfile</span></span>
<span data-ttu-id="ec986-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec986-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec986-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="ec986-120">-DefaultVersion</span></span>
<span data-ttu-id="ec986-121">Anger vilket paket som ska användas om en klient begär programmet men inte anger en version.</span><span class="sxs-lookup"><span data-stu-id="ec986-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec986-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ec986-122">-DisplayName</span></span>
<span data-ttu-id="ec986-123">Anger programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="ec986-123">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec986-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec986-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec986-125">Anger namnet på den resurs grupp som innehåller batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="ec986-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ec986-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec986-126">CommonParameters</span></span>
<span data-ttu-id="ec986-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec986-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec986-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec986-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec986-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec986-129">INPUTS</span></span>

### <span data-ttu-id="ec986-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="ec986-130">None</span></span>
<span data-ttu-id="ec986-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ec986-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec986-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec986-132">OUTPUTS</span></span>

## <span data-ttu-id="ec986-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec986-133">NOTES</span></span>

## <span data-ttu-id="ec986-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec986-134">RELATED LINKS</span></span>

[<span data-ttu-id="ec986-135">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ec986-135">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="ec986-136">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ec986-136">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ec986-137">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ec986-137">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="ec986-138">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ec986-138">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ec986-139">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ec986-139">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="ec986-140">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ec986-140">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


