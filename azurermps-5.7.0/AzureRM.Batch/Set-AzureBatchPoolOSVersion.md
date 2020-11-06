---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583651"
---
# <span data-ttu-id="13f72-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="13f72-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="13f72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13f72-102">SYNOPSIS</span></span>
<span data-ttu-id="13f72-103">Ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="13f72-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13f72-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13f72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13f72-105">DESCRIPTION</span></span>
<span data-ttu-id="13f72-106">Cmdleten **set-AzureBatchPoolOSVersion** ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="13f72-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="13f72-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13f72-107">EXAMPLES</span></span>

### <span data-ttu-id="13f72-108">Exempel 1: Ange mål operativ systemets version för en pool</span><span class="sxs-lookup"><span data-stu-id="13f72-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="13f72-109">Det här kommandot anger mål operativ system versionen för poolen för pool till WA-gäst-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="13f72-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="13f72-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13f72-110">PARAMETERS</span></span>

### <span data-ttu-id="13f72-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="13f72-111">-BatchContext</span></span>
<span data-ttu-id="13f72-112">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="13f72-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="13f72-113">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="13f72-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="13f72-114">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="13f72-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="13f72-115">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="13f72-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="13f72-116">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="13f72-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13f72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f72-117">-DefaultProfile</span></span>
<span data-ttu-id="13f72-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13f72-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f72-119">-ID</span><span class="sxs-lookup"><span data-stu-id="13f72-119">-Id</span></span>
<span data-ttu-id="13f72-120">Anger poolens ID.</span><span class="sxs-lookup"><span data-stu-id="13f72-120">Specifies the ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13f72-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="13f72-121">-TargetOSVersion</span></span>
<span data-ttu-id="13f72-122">Anger vilken version av Azure-gäst operativ systemet som ska installeras på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="13f72-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="13f72-123">Mer information om Azure gäst operativ system versioner finns i avsnittet om hur du använder Azure gäst OS och SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ -kompatibilitet ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="13f72-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f72-124">CommonParameters</span></span>
<span data-ttu-id="13f72-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f72-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f72-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f72-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13f72-127">INPUTS</span></span>

### <span data-ttu-id="13f72-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="13f72-128">BatchAccountContext</span></span>
<span data-ttu-id="13f72-129">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="13f72-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="13f72-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="13f72-130">String</span></span>
<span data-ttu-id="13f72-131">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="13f72-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="13f72-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13f72-132">OUTPUTS</span></span>

## <span data-ttu-id="13f72-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13f72-133">NOTES</span></span>

## <span data-ttu-id="13f72-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13f72-134">RELATED LINKS</span></span>

[<span data-ttu-id="13f72-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="13f72-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


