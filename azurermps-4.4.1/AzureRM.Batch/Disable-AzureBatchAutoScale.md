---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579800"
---
# <span data-ttu-id="f97dd-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f97dd-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="f97dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f97dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f97dd-103">Inaktiverar automatisk skalning av en pool.</span><span class="sxs-lookup"><span data-stu-id="f97dd-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f97dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f97dd-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f97dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f97dd-105">DESCRIPTION</span></span>
<span data-ttu-id="f97dd-106">Cmdleten **disable-AzureBatchAutoScale** inaktiverar automatisk skalning för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="f97dd-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="f97dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f97dd-107">EXAMPLES</span></span>

### <span data-ttu-id="f97dd-108">Exempel 1: inaktivera automatisk skalning av en pool</span><span class="sxs-lookup"><span data-stu-id="f97dd-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="f97dd-109">Det här kommandot inaktiverar automatisk skalning för poolen med namnet min pool.</span><span class="sxs-lookup"><span data-stu-id="f97dd-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="f97dd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f97dd-110">PARAMETERS</span></span>

### <span data-ttu-id="f97dd-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f97dd-111">-BatchContext</span></span>
<span data-ttu-id="f97dd-112">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f97dd-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f97dd-113">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f97dd-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f97dd-114">-ID</span><span class="sxs-lookup"><span data-stu-id="f97dd-114">-Id</span></span>
<span data-ttu-id="f97dd-115">Anger poolens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="f97dd-115">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f97dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97dd-116">-DefaultProfile</span></span>
<span data-ttu-id="f97dd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f97dd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f97dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97dd-118">CommonParameters</span></span>
<span data-ttu-id="f97dd-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f97dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97dd-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97dd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97dd-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f97dd-121">INPUTS</span></span>

### <span data-ttu-id="f97dd-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f97dd-122">BatchAccountContext</span></span>
<span data-ttu-id="f97dd-123">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f97dd-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f97dd-124">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="f97dd-124">String</span></span>
<span data-ttu-id="f97dd-125">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f97dd-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f97dd-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f97dd-126">OUTPUTS</span></span>

## <span data-ttu-id="f97dd-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f97dd-127">NOTES</span></span>

## <span data-ttu-id="f97dd-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f97dd-128">RELATED LINKS</span></span>

[<span data-ttu-id="f97dd-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f97dd-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="f97dd-130">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f97dd-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="f97dd-131">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f97dd-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


