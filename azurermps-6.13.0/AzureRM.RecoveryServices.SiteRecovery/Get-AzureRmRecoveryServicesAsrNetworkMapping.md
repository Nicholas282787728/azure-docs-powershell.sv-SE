---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: d85de944742d7ad265c1e7e979dddb15808df95e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580015"
---
# <span data-ttu-id="71fdb-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="71fdb-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="71fdb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="71fdb-103">Hämtar information om nätverks mappningar för webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="71fdb-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71fdb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71fdb-104">SYNTAX</span></span>

### <span data-ttu-id="71fdb-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="71fdb-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71fdb-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="71fdb-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71fdb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71fdb-107">DESCRIPTION</span></span>
<span data-ttu-id="71fdb-108">Cmdleten **Get-AzureRmRecoveryServicesAsrNetworkMapping** hämtar information om nätverks mappningar för Azure Site Recovery för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="71fdb-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="71fdb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71fdb-109">EXAMPLES</span></span>

### <span data-ttu-id="71fdb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="71fdb-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="71fdb-111">Hämtar alla nätverks mappningar för det skickade nätverket.</span><span class="sxs-lookup"><span data-stu-id="71fdb-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="71fdb-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="71fdb-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="71fdb-113">Hämtar nätverks mappning med angivet namn i angivet Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="71fdb-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="71fdb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71fdb-114">PARAMETERS</span></span>

### <span data-ttu-id="71fdb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fdb-115">-DefaultProfile</span></span>
<span data-ttu-id="71fdb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71fdb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71fdb-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="71fdb-117">-Name</span></span>
<span data-ttu-id="71fdb-118">Namnet på det objekt för automatisk nätverks mappning som ska visas.</span><span class="sxs-lookup"><span data-stu-id="71fdb-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fdb-119">-Network</span><span class="sxs-lookup"><span data-stu-id="71fdb-119">-Network</span></span>
<span data-ttu-id="71fdb-120">Skaffa de nätverks mappningar för automatisk återställning som motsvarar det angivna objektet för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="71fdb-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71fdb-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="71fdb-121">-PrimaryFabric</span></span>
<span data-ttu-id="71fdb-122">Hämta de nätverks mappningar för automatisk återställning som motsvarar det angivna primära infrastruktur resursen.</span><span class="sxs-lookup"><span data-stu-id="71fdb-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71fdb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fdb-123">CommonParameters</span></span>
<span data-ttu-id="71fdb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71fdb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fdb-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71fdb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fdb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71fdb-126">INPUTS</span></span>

### <span data-ttu-id="71fdb-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="71fdb-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="71fdb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71fdb-128">OUTPUTS</span></span>

### <span data-ttu-id="71fdb-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="71fdb-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="71fdb-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71fdb-130">NOTES</span></span>

## <span data-ttu-id="71fdb-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71fdb-131">RELATED LINKS</span></span>

[<span data-ttu-id="71fdb-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="71fdb-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="71fdb-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="71fdb-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
