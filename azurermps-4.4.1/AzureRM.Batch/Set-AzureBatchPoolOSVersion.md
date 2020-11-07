---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756636"
---
# <span data-ttu-id="99421-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="99421-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="99421-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99421-102">SYNOPSIS</span></span>
<span data-ttu-id="99421-103">Ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="99421-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99421-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99421-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99421-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99421-105">DESCRIPTION</span></span>
<span data-ttu-id="99421-106">Cmdleten **set-AzureBatchPoolOSVersion** ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="99421-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="99421-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99421-107">EXAMPLES</span></span>

### <span data-ttu-id="99421-108">Exempel 1: Ange mål operativ systemets version för en pool</span><span class="sxs-lookup"><span data-stu-id="99421-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="99421-109">Det här kommandot anger mål operativ system versionen för poolen för pool till WA-gäst-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="99421-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="99421-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99421-110">PARAMETERS</span></span>

### <span data-ttu-id="99421-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99421-111">-BatchContext</span></span>
<span data-ttu-id="99421-112">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="99421-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99421-113">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="99421-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="99421-114">-ID</span><span class="sxs-lookup"><span data-stu-id="99421-114">-Id</span></span>
<span data-ttu-id="99421-115">Anger poolens ID.</span><span class="sxs-lookup"><span data-stu-id="99421-115">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="99421-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="99421-116">-TargetOSVersion</span></span>
<span data-ttu-id="99421-117">Anger vilken version av Azure-gäst operativ systemet som ska installeras på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="99421-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="99421-118">Mer information om Azure gäst operativ system versioner finns i avsnittet om hur du använder Azure gäst OS och SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ -kompatibilitet ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="99421-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99421-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99421-119">-DefaultProfile</span></span>
<span data-ttu-id="99421-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99421-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99421-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99421-121">CommonParameters</span></span>
<span data-ttu-id="99421-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99421-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99421-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99421-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99421-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99421-124">INPUTS</span></span>

### <span data-ttu-id="99421-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99421-125">BatchAccountContext</span></span>
<span data-ttu-id="99421-126">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="99421-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="99421-127">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="99421-127">String</span></span>
<span data-ttu-id="99421-128">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="99421-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="99421-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99421-129">OUTPUTS</span></span>

## <span data-ttu-id="99421-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99421-130">NOTES</span></span>

## <span data-ttu-id="99421-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99421-131">RELATED LINKS</span></span>

[<span data-ttu-id="99421-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="99421-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


