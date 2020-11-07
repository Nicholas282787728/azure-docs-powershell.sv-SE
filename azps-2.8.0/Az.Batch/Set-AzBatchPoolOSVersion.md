---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928542"
---
# <span data-ttu-id="c2084-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="c2084-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="c2084-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2084-102">SYNOPSIS</span></span>
<span data-ttu-id="c2084-103">Ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="c2084-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="c2084-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2084-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2084-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2084-105">DESCRIPTION</span></span>
<span data-ttu-id="c2084-106">Cmdleten **set-AzBatchPoolOSVersion** ändrar operativ system versionen för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="c2084-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="c2084-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2084-107">EXAMPLES</span></span>

### <span data-ttu-id="c2084-108">Exempel 1: Ange mål operativ systemets version för en pool</span><span class="sxs-lookup"><span data-stu-id="c2084-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="c2084-109">Det här kommandot anger mål operativ system versionen för poolen för pool till WA-gäst-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="c2084-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="c2084-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2084-110">PARAMETERS</span></span>

### <span data-ttu-id="c2084-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c2084-111">-BatchContext</span></span>
<span data-ttu-id="c2084-112">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2084-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c2084-113">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2084-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c2084-114">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="c2084-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c2084-115">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="c2084-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c2084-116">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c2084-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c2084-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2084-117">-DefaultProfile</span></span>
<span data-ttu-id="c2084-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2084-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2084-119">-ID</span><span class="sxs-lookup"><span data-stu-id="c2084-119">-Id</span></span>
<span data-ttu-id="c2084-120">Anger poolens ID.</span><span class="sxs-lookup"><span data-stu-id="c2084-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="c2084-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="c2084-121">-TargetOSVersion</span></span>
<span data-ttu-id="c2084-122">Anger vilken version av Azure-gäst operativ systemet som ska installeras på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="c2084-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="c2084-123">Mer information om Azure gäst operativ system versioner finns i avsnittet om hur du använder Azure gäst OS och SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ -kompatibilitet ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="c2084-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="c2084-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2084-124">CommonParameters</span></span>
<span data-ttu-id="c2084-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2084-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2084-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2084-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2084-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2084-127">INPUTS</span></span>

### <span data-ttu-id="c2084-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c2084-128">System.String</span></span>

### <span data-ttu-id="c2084-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c2084-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c2084-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2084-130">OUTPUTS</span></span>

### <span data-ttu-id="c2084-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="c2084-131">System.Void</span></span>

## <span data-ttu-id="c2084-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2084-132">NOTES</span></span>

## <span data-ttu-id="c2084-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2084-133">RELATED LINKS</span></span>

[<span data-ttu-id="c2084-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c2084-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


