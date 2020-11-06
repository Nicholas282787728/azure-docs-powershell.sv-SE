---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: d85e0ca61b86e523c6d73ea8d2349d7d692aafb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581779"
---
# <span data-ttu-id="2104d-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="2104d-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="2104d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2104d-102">SYNOPSIS</span></span>
<span data-ttu-id="2104d-103">Ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="2104d-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2104d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2104d-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2104d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2104d-105">DESCRIPTION</span></span>
<span data-ttu-id="2104d-106">Cmdleten **set-AzureBatchPoolOSVersion** ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="2104d-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="2104d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2104d-107">EXAMPLES</span></span>

### <span data-ttu-id="2104d-108">Exempel 1: Ange mål operativ systemets version för en pool</span><span class="sxs-lookup"><span data-stu-id="2104d-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="2104d-109">Det här kommandot anger mål operativ system versionen för poolen för pool till WA-gäst-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="2104d-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="2104d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2104d-110">PARAMETERS</span></span>

### <span data-ttu-id="2104d-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2104d-111">-BatchContext</span></span>
<span data-ttu-id="2104d-112">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2104d-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2104d-113">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2104d-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2104d-114">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="2104d-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2104d-115">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="2104d-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2104d-116">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2104d-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2104d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2104d-117">-DefaultProfile</span></span>
<span data-ttu-id="2104d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2104d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2104d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2104d-119">-Id</span></span>
<span data-ttu-id="2104d-120">Anger poolens ID.</span><span class="sxs-lookup"><span data-stu-id="2104d-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="2104d-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="2104d-121">-TargetOSVersion</span></span>
<span data-ttu-id="2104d-122">Anger vilken version av Azure-gäst operativ systemet som ska installeras på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="2104d-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="2104d-123">Mer information om Azure gäst operativ system versioner finns i avsnittet om hur du använder Azure gäst OS och SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ -kompatibilitet ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="2104d-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="2104d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2104d-124">CommonParameters</span></span>
<span data-ttu-id="2104d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2104d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2104d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2104d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2104d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2104d-127">INPUTS</span></span>

### <span data-ttu-id="2104d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2104d-128">System.String</span></span>

### <span data-ttu-id="2104d-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2104d-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="2104d-130">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2104d-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="2104d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2104d-131">OUTPUTS</span></span>

### <span data-ttu-id="2104d-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="2104d-132">System.Void</span></span>

## <span data-ttu-id="2104d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2104d-133">NOTES</span></span>

## <span data-ttu-id="2104d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2104d-134">RELATED LINKS</span></span>

[<span data-ttu-id="2104d-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2104d-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


