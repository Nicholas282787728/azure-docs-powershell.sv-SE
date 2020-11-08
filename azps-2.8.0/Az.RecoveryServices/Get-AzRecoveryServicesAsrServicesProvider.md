---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919763"
---
# <span data-ttu-id="159cb-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="159cb-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="159cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="159cb-102">SYNOPSIS</span></span>
<span data-ttu-id="159cb-103">Hämtar information om de ASR Recovery Services-leverantörer som registrerats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="159cb-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="159cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="159cb-104">SYNTAX</span></span>

### <span data-ttu-id="159cb-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="159cb-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="159cb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="159cb-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="159cb-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="159cb-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="159cb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="159cb-108">DESCRIPTION</span></span>
<span data-ttu-id="159cb-109">Cmdleten **Get-AzRecoveryServicesAsrServicesProvider** hämtar information om Azure Site Recovery-leverantörer i valvet.</span><span class="sxs-lookup"><span data-stu-id="159cb-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="159cb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="159cb-110">EXAMPLES</span></span>

### <span data-ttu-id="159cb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="159cb-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="159cb-112">Lista alla ASR-leverantörer registrerade i det Recovery Services-valv som motsvarar den angivna Fabric-resursen.</span><span class="sxs-lookup"><span data-stu-id="159cb-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="159cb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="159cb-113">PARAMETERS</span></span>

### <span data-ttu-id="159cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159cb-114">-DefaultProfile</span></span>
<span data-ttu-id="159cb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="159cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="159cb-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="159cb-116">-Fabric</span></span>
<span data-ttu-id="159cb-117">Anger ASR-Fabric-objekt.</span><span class="sxs-lookup"><span data-stu-id="159cb-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="159cb-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="159cb-118">-FriendlyName</span></span>
<span data-ttu-id="159cb-119">Anger det egna namnet på ASR Recovery Services-leverantören för att få information om.</span><span class="sxs-lookup"><span data-stu-id="159cb-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159cb-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="159cb-120">-Name</span></span>
<span data-ttu-id="159cb-121">Anger namnet på ASR Recovery Services-leverantören för att få information om.</span><span class="sxs-lookup"><span data-stu-id="159cb-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159cb-122">CommonParameters</span></span>
<span data-ttu-id="159cb-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="159cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159cb-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="159cb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159cb-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="159cb-125">INPUTS</span></span>

### <span data-ttu-id="159cb-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="159cb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="159cb-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="159cb-127">OUTPUTS</span></span>

### <span data-ttu-id="159cb-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="159cb-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="159cb-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="159cb-129">NOTES</span></span>

## <span data-ttu-id="159cb-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="159cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="159cb-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="159cb-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="159cb-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="159cb-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)